# leyes-federales — guía para agentes

Texto vigente de las leyes federales de la Cámara de Diputados (LeyesBiblio), un
archivo por artículo, versionado para que el historial de git sea el registro de
sus reformas. Es un repo de datos: el único código es `scripts/gen_readme.py`.

**No edites a mano nada de las carpetas de leyes, `metadata/` ni `fuentes.json`.**
Todo lo genera [`fiscal-extractor`](https://github.com/OpenCodice/fiscal-extractor)
(módulo `extractor/federal.py`) a partir de los PDF oficiales. Si un artículo
está mal, el arreglo va en el extractor.

## Estructura

- `{ley}/NNN.md` — el texto. La clave de la ley es el nombre de su página en
  LeyesBiblio (`ref/lgs.htm` → `lgs`), estable aunque cambie el nombre del PDF;
  las leyes que también están en `fiscal-mexicano` usan la misma clave allá y
  aquí (están duplicadas a propósito, por ahora).
- `metadata/{ley}/` — índice y fechas de reforma. No hay `pasajes.jsonl`: aquí
  no hay buscador que lo use y pesaría cientos de MB.
- `fuentes.json` — el registro generado del índice: por ley, su URL, la huella
  del PDF (sha256, ETag, Last-Modified), la huella del extractor que la produjo,
  su estado (`incluida` o `excluida` con `motivo`) y cómo entró (`alta.via`:
  `limpia` o `reparada` por el agente). Los PDF no se guardan.

## Cómo cambia este repo

`vigilar.yml` corre cada lunes 09:00 UTC (y a mano con `gh workflow run
vigilar.yml -f lote=40`, o `-f docs="lgs lft"`):

1. **planear** — lee el índice y hace HEAD a cada PDF. Reprocesa solo lo que
   cambió: leyes nuevas (hasta `lote` por corrida), PDF con otras cabeceras, o
   todo si cambió el parser del extractor. Las excluidas se reintentan cuando
   cambia su PDF o el extractor.
2. **extraer** — reparte el plan entre varios jobs: descarga, extrae y audita.
3. **cerrar** — junta los resultados. Si la auditoría determinista falló en
   algún documento, y solo entonces, lanza al agente (Claude Code) para
   reparar el extractor; sus compuertas (pruebas, sin regresiones en los
   documentos ni en una muestra de leyes publicadas) deciden si el arreglo se
   publica. Después: lo nuevo que quedó fiel entra; lo nuevo que no, se deja
   fuera y se anota; lo ya publicado que no quedó fiel conserva su versión
   anterior y abre un issue.
4. Abre un PR `verificado`; `revisar-pr` corre `validar` y lo fusiona. Con la
   etiqueta `continuar` (quedan altas pendientes, o el agente reparó el
   extractor y hay que reconstruir con él) lanza la siguiente corrida.

El título del commit distingue reforma (`Reforma LGS (DOF 2026-01-15): arts. 4o,
22`), alta (`Alta de 40 leyes federales: …`) y corrección de extracción.

## Lo único que se edita aquí

Los workflows, `scripts/gen_readme.py` y la documentación (el README fuera de
sus bloques generados). Trabaja en `main`, con `git pull --ff-only` antes;
`main` exige el check `validar`.
