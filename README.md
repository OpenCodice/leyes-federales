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

| Ley | Carpeta | Artículos | Última reforma incorporada | PDF oficial |
|---|---|---|---|---|
| Código Civil Federal | [`ccf/`](ccf/) | 3085 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CCF.pdf) |
| Código Fiscal de la Federación | [`cff/`](cff/) | 421 | 2026-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CFF.pdf) |
| Código Nacional de Procedimientos Penales | [`cnpp/`](cnpp/) | 490 | 2025-11-28 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CNPP.pdf) |
| Código Penal Federal | [`cpf/`](cpf/) | 555 | 2026-03-13 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CPF.pdf) |
| Código de Comercio | [`ccom/`](ccom/) | 1641 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CCom.pdf) |
| Ley Federal del Trabajo | [`lft/`](lft/) | 1265 | 2026-05-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFT.pdf) |
| Ley General de Salud | [`lgs/`](lgs/) | 728 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGS.pdf) |
| Ley General del Equilibrio Ecológico y la Protección al Ambiente | [`lgeepa/`](lgeepa/) | 270 | 2026-01-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGEEPA.pdf) |
| Ley de Amparo, Reglamentaria de los artículos 103 y 107 de la Constitución Política de los Estados Unidos Mexicanos | [`lamp/`](lamp/) | 272 | 2025-10-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAmp.pdf) |
| Ley del Mercado de Valores | [`lmv/`](lmv/) | 463 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LMV.pdf) |

<!-- DOCUMENTOS:FIN -->

## Fuera del corpus

Leyes del índice cuya extracción no quedó fiel al PDF. Se reintentan solas
cuando cambia su PDF o el extractor.

<!-- EXCLUIDAS:INICIO -->

_Ninguna._

<!-- EXCLUIDAS:FIN -->
