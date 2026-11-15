# Leyes federales de México

Texto vigente de las leyes federales que publica la H. Cámara de Diputados en
[LeyesBiblio](https://www.diputados.gob.mx/LeyesBiblio/index.htm), un archivo
por artículo, versionado en git: cada reforma es un commit, y el historial de
un archivo es el historial de ese artículo.

Incluye también los reglamentos fiscales que publica la Cámara y el Reglamento
Interior del SAT. La Constitución vive en
[constitucion-mexicana](https://github.com/OpenCodice/constitucion-mexicana) y
el resto del corpus fiscal (RMF, anexos, criterios) en
[fiscal-mexicano](https://github.com/OpenCodice/fiscal-mexicano).

## Cómo está organizado

- `{ley}/NNN.md` — un artículo (`lgs/004.md`, `lft/353-u.md`,
  `lgs/077-bis-35-a.md`). Cada archivo trae el encabezado del artículo y su
  texto, con las notas de reforma tal como vienen en el PDF.
- `metadata/{ley}/articulos.json` — índice de la ley: Título, Capítulo y
  Sección de cada artículo, y sus fechas de reforma.
- `metadata/{ley}/reformas.json` — fecha de reforma (DOF) → artículos.
- `fuentes.json` — el registro: de qué PDF salió cada ley (URL y huella
  sha256), con qué versión del extractor, y si está publicada o se dejó fuera
  y por qué. Los PDF no se guardan aquí.

## De dónde sale el texto

Nada se edita a mano. Todo lo genera
[fiscal-extractor](https://github.com/OpenCodice/fiscal-extractor) a partir de
los PDF oficiales. Cada lunes se revisa el índice de la Cámara y las cabeceras
de cada PDF; solo se reprocesa lo que cambió. Una auditoría determinista
comprueba que cada párrafo extraído esté literal en el PDF y que no quede
texto sin extraer; si falla, un agente intenta corregir el extractor. Una ley
que no queda fiel al PDF no se publica: aparece abajo con el motivo.

## Leyes publicadas

<!-- DOCUMENTOS:INICIO -->

_Ninguna._

<!-- DOCUMENTOS:FIN -->

## Fuera del corpus

Leyes del índice cuya extracción no quedó fiel al PDF. Se reintentan solas
cuando cambia su PDF o el extractor.

<!-- EXCLUIDAS:INICIO -->

_Ninguna._

<!-- EXCLUIDAS:FIN -->
