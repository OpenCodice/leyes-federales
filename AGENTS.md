# leyes-federales — guía para agentes

Texto vigente de las leyes federales de la Cámara de Diputados (LeyesBiblio), un
archivo por artículo, versionado para que el historial de git sea el registro de
sus reformas. Es un repo de datos: el único código es la validación de los PR
(`revisar-pr.yml`); las tablas del README las regenera la vigilancia
(`scripts/readme_federal.py` del extractor).

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

La vigilancia no vive aquí: es `vigilar-federal.yml` de
[`fiscal-extractor`](https://github.com/OpenCodice/fiscal-extractor), y la lanza
cada lunes a las 13:00 UTC (después de la fiscal, que publica arreglos en el
mismo extractor) el Worker `scheduler` de Cloudflare. A mano:
`gh workflow run vigilar-federal.yml -R OpenCodice/fiscal-extractor -f lote=40`,
o `-f docs="lgs lft"`. Así el historial de este repo solo tiene cambios de texto
legal.

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
   anterior, queda `revision_pendiente` en `fuentes.json` y se reintenta en la
   siguiente vigilancia. Nada se asigna a una persona.
4. Abre aquí un PR `verificado` con **un commit por ley** (y uno aparte para
   `fuentes.json` y el README); `revisar-pr` corre `validar` y lo fusiona con
   rebase, conservándolos. Si quedan altas pendientes, o el agente reparó el
   extractor, la vigilancia espera esa fusión y lanza la siguiente corrida.

El título de cada commit dice qué le pasó a esa ley: `Reforma LGS (DOF
2026-01-15): arts. 4o, 22`, `Alta de LGS`, `Corrección de extracción LGS: 3
artículos` o `Retiro de LGS: …`. `git log -- lgs/` es la historia de la LGS.

## Lo único que se edita aquí

`revisar-pr.yml` y la documentación (el README fuera
de sus bloques generados). Trabaja en `main`, con `git pull --ff-only` antes;
`main` exige el check `validar`.
