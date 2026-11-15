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
| Código Civil Federal ⚠️ | [`ccf/`](ccf/) | 3085 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CCF.pdf) |
| Código Fiscal de la Federación | [`cff/`](cff/) | 421 | 2026-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CFF.pdf) |
| Código Militar de Procedimientos Penales | [`cmpp/`](cmpp/) | 452 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CMPP.pdf) |
| Código Nacional de Procedimientos Civiles y Familiares | [`cnpcf/`](cnpcf/) | 1191 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CNPCF.pdf) |
| Código Nacional de Procedimientos Penales | [`cnpp/`](cnpp/) | 490 | 2025-11-28 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CNPP.pdf) |
| Código Penal Federal | [`cpf/`](cpf/) | 555 | 2026-03-13 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CPF.pdf) |
| Código de Comercio | [`ccom/`](ccom/) | 1641 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CCom.pdf) |
| Código de Justicia Militar | [`cjm/`](cjm/) | 952 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CJM.pdf) |
| Estatuto de Gobierno del Distrito Federal | [`egdf/`](egdf/) | 145 | 2014-06-27 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/10_270614.pdf) |
| Ley Aduanera | [`ladua/`](ladua/) | 277 | 2025-11-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAdua.pdf) |
| Ley Agraria | [`lagra/`](lagra/) | 201 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAgra.pdf) |
| Ley Federal del Trabajo | [`lft/`](lft/) | 1265 | 2026-05-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFT.pdf) |
| Ley General de Salud | [`lgs/`](lgs/) | 728 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGS.pdf) |
| Ley General del Equilibrio Ecológico y la Protección al Ambiente | [`lgeepa/`](lgeepa/) | 270 | 2026-01-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGEEPA.pdf) |
| Ley de Adquisiciones, Arrendamientos y Servicios del Sector Público | [`laassp/`](laassp/) | 120 | 2025-04-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAASSP.pdf) |
| Ley de Aeropuertos | [`laero/`](laero/) | 101 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAero.pdf) |
| Ley de Amnistía | [`lamn/`](lamn/) | 9 | 2024-06-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAmn.pdf) |
| Ley de Amnistía | [`lamni/`](lamni/) | 4 | 1994-01-22 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/19.pdf) |
| Ley de Amparo, Reglamentaria de los artículos 103 y 107 de la Constitución Política de los Estados Unidos Mexicanos | [`lamp/`](lamp/) | 272 | 2025-10-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAmp.pdf) |
| Ley de Ascensos de la Armada de México | [`laam/`](laam/) | 57 | 2025-12-17 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAAM.pdf) |
| Ley de Ascensos y Recompensas del Ejército, Fuerza Aérea y Guardia Nacional | [`larefam/`](larefam/) | 78 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAREFAGN.pdf) |
| Ley de Asistencia Social | [`lasoc/`](lasoc/) | 68 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LASoc.pdf) |
| Ley de Asociaciones Público Privadas | [`lapp/`](lapp/) | 143 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAPP.pdf) |
| Ley de Asociaciones Religiosas y Culto Público | [`larcp/`](larcp/) | 37 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LARCP.pdf) |
| Ley de Aviación Civil | [`lac/`](lac/) | 145 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAC.pdf) |
| Ley de Ayuda Alimentaria para los Trabajadores | [`laat/`](laat/) | 22 | 2011-01-17 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAAT.pdf) |
| Ley de Biocombustibles | [`lbio/`](lbio/) | 46 | 2025-03-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LBio.pdf) |
| Ley de Bioseguridad de Organismos Genéticamente Modificados | [`lbogm/`](lbogm/) | 124 | 2022-05-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LBOGM.pdf) |
| Ley de Caminos, Puentes y Autotransporte Federal | [`lcpaf/`](lcpaf/) | 93 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCPAF.pdf) |
| Ley de Capitalización del Procampo | [`lcpro/`](lcpro/) | 22 | 2001-12-31 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/238.pdf) |
| Ley de Carrera Judicial del Poder Judicial de la Federación | [`lcjpjf/`](lcjpjf/) | 74 | 2025-01-02 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCJPJF.pdf) |
| Ley de Comercio Exterior | [`lce/`](lce/) | 98 | 2026-05-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCE.pdf) |
| Ley de Concursos Mercantiles | [`lcm/`](lcm/) | 353 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCM.pdf) |
| Ley de Contribución de Mejoras por Obras Públicas Federales de Infraestructura Hidráulica | [`lcmopfih/`](lcmopfih/) | 15 | 1990-12-26 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/30.pdf) |
| Ley de Cooperación Internacional para el Desarrollo | [`lcid/`](lcid/) | 42 | 2020-11-06 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCID_061120.pdf) |
| Ley de Coordinación Fiscal | [`lcf/`](lcf/) | 67 | 2024-01-03 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCF.pdf) |
| Ley de Cámaras Empresariales y sus Confederaciones | [`lcec/`](lcec/) | 45 | 2019-04-12 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCEC_120419.pdf) |
| Ley de Desarrollo Rural Sustentable | [`ldrs/`](ldrs/) | 193 | 2024-06-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LDRS.pdf) |
| Ley de Desarrollo Sustentable de la Cafeticultura | [`ldsc/`](ldsc/) | 85 | 2025-12-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LDSC.pdf) |
| Ley de Desarrollo Sustentable de la Caña de Azúcar | [`ldsca/`](ldsca/) | 150 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LDSCA.pdf) |
| Ley de Disciplina Financiera de las Entidades Federativas y los Municipios | [`ldfefm/`](ldfefm/) | 65 | 2022-05-10 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LDFEFM.pdf) |
| Ley de Disciplina del Ejército, Fuerza Aérea y Guardia Nacional | [`ldefam/`](ldefam/) | 57 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LDEFAGN.pdf) |
| Ley de Disciplina para el Personal de la Armada de México | [`ldparm/`](ldparm/) | 80 | 2002-12-13 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/252.pdf) |
| Ley de Economía Digital para Pagos Digitales y Electrónicos | [`ledpde/`](ledpde/) | 22 | 2026-11-04 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LEDPDE.pdf) |
| Ley de Educación Militar del Ejército, Fuerza Aérea y Guardia Nacional | [`lemefam/`](lemefam/) | 52 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LEMEFAGN.pdf) |
| Ley del Mercado de Valores | [`lmv/`](lmv/) | 463 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LMV.pdf) |
| Reglamento Interior del Servicio de Administración Tributaria | [`risat/`](risat/) | 56 | 2021-12-21 | [PDF](https://wwwmat.sat.gob.mx/cs/Satellite?blobcol=urldata&blobkey=id&blobtable=MungoBlobs&blobwhere=1461176458878&ssbinary=true) |

<!-- DOCUMENTOS:FIN -->

## Fuera del corpus

Leyes del índice cuya extracción no quedó fiel al PDF. Se reintentan solas
cuando cambia su PDF o el extractor.

<!-- EXCLUIDAS:INICIO -->

| Ley | Motivo | PDF oficial |
|---|---|---|
| Código Federal de Procedimientos Civiles | 1 unidades no reproducen el PDF (cfpc/068) | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CFPC.pdf) |
| Impuesto sobre Servicios Expresamente Declarados de Interés Público por Ley, en los que Intervengan Empresas Concesionarias de Bienes del Dominio Directo de la Nación (LEY que establece, reforma y adiciona las disposiciones relativas a diversos impuestos) | invariantes rotos: [lisipl] al menos una unidad: 0 unidades | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/79.pdf) |
| Ley de Aguas Nacionales | invariantes rotos: [lan] índice == archivos == unidades: 215 md / 216 idx / 216 items (¿colisión de claves?). 1 unidades no reproducen el PDF (lan/029-bis-1) | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAN.pdf) |
| Ley de Ahorro y Crédito Popular | invariantes rotos: [lacp] índice == archivos == unidades: 232 md / 234 idx / 234 items (¿colisión de claves?) | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LACP.pdf) |

<!-- EXCLUIDAS:FIN -->
