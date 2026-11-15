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
| Código Civil Federal | [`ccf/`](ccf/) | 3103 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CCF.pdf) |
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
| Ley de Comercio Exterior | [`lce/`](lce/) | 109 | 2026-05-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCE.pdf) |
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
| Ley de Educación Naval | [`len/`](len/) | 24 | 2023-03-24 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LEN.pdf) |
| Ley de Energía para el Campo | [`lec/`](lec/) | 14 | 2012-12-28 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/246.pdf) |
| Ley de Expropiación ⚠️ | [`lexp/`](lexp/) | 25 | 2012-01-27 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/35.pdf) |
| Ley de Extradición Internacional | [`lei/`](lei/) | 38 | 2021-05-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/36_200521.pdf) |
| Ley de Firma Electrónica Avanzada | [`lfea/`](lfea/) | 31 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFEA.pdf) |
| Ley de Fiscalización y Rendición de Cuentas de la Federación | [`lfrcf/`](lfrcf/) | 115 | 2026-05-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFRCF.pdf) |
| Ley de Fomento a la Confianza Ciudadana | [`lfcc/`](lfcc/) | 17 | 2020-01-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFCC_200120.pdf) |
| Ley de Fomento a la Industria Vitivinícola | [`lfiv/`](lfiv/) | 35 | 2018-05-23 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFIV_230518.pdf) |
| Ley de Fomento para la Lectura y el Libro | [`lfll/`](lfll/) | 28 | 2023-11-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFLL.pdf) |
| Ley de Fondos de Aseguramiento Agropecuario y Rural | [`lfaar/`](lfaar/) | 96 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFAAR.pdf) |
| Ley de Fondos de Inversión | [`lfi/`](lfi/) | 195 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFI.pdf) |
| Ley de Geotermia | [`lgeo/`](lgeo/) | 66 | 2025-03-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGeo.pdf) |
| Ley de Infraestructura de la Calidad | [`lical/`](lical/) | 165 | 2020-07-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LICal_010720.pdf) |
| Ley de Ingresos de la Federación 2026 | [`lif-2026/`](lif-2026/) | 34 | 2025-11-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIF_2026.pdf) |
| Ley de Ingresos de la Federación para el Ejercicio Fiscal de 2027 | [`lif-2027/`](lif-2027/) | 34 | 2026-11-13 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIF_2027.pdf) |
| Ley de Ingresos sobre Hidrocarburos | [`lish/`](lish/) | 64 | 2025-03-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIH.pdf) |
| Ley de Instituciones de Crédito | [`lic/`](lic/) | 490 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIC.pdf) |
| Ley de Instituciones de Seguros y de Fianzas | [`lisf/`](lisf/) | 510 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LISF.pdf) |
| Ley de Inversión Extranjera | [`lie/`](lie/) | 42 | 2024-05-27 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIE.pdf) |
| Ley de Migración | [`lmigra/`](lmigra/) | 162 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LMigra.pdf) |
| Ley de Minería | [`lmin/`](lmin/) | 79 | 2023-05-08 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LMin.pdf) |
| Ley de Nacionalidad | [`lnac/`](lnac/) | 37 | 2012-04-23 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/53.pdf) |
| Ley de Navegación y Comercio Marítimos | [`lncm/`](lncm/) | 334 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LNCM.pdf) |
| Ley de Obras Públicas y Servicios Relacionados con las Mismas | [`lopsrm/`](lopsrm/) | 133 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOPSRM.pdf) |
| Ley de Organizaciones Ganaderas | [`log/`](log/) | 26 | 2012-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/57.pdf) |
| Ley de Planeación | [`lplan/`](lplan/) | 48 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LPlan.pdf) |
| Ley de Planeación y Transición Energética | [`lpte/`](lpte/) | 100 | 2025-03-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LPTE.pdf) |
| Ley de Premios, Estímulos y Recompensas Civiles | [`lperc/`](lperc/) | 145 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LPERC.pdf) |
| Ley de Productos Orgánicos | [`lpo/`](lpo/) | 50 | 2006-02-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LPO.pdf) |
| Ley de Protección al Ahorro Bancario | [`lpab/`](lpab/) | 95 | 2022-05-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LPAB.pdf) |
| Ley de Protección al Comercio y la Inversión de Normas Extranjeras que Contravengan el Derecho Internacional | [`lpcinecdi/`](lpcinecdi/) | 9 | 2012-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/63.pdf) |
| Ley de Protección del Espacio Aéreo Mexicano | [`lpeam/`](lpeam/) | 26 | 2023-03-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LPEAM.pdf) |
| Ley de Protección y Defensa al Usuario de Servicios Financieros | [`lpdusf/`](lpdusf/) | 129 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LPDUSF.pdf) |
| Ley de Puertos | [`lpue/`](lpue/) | 73 | 2020-12-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/65_071220.pdf) |
| Ley de Recompensas de la Armada de México | [`lram/`](lram/) | 71 | 2021-11-22 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRAM.pdf) |
| Ley de Responsabilidad Civil por Daños Nucleares | [`lrcdn/`](lrcdn/) | 31 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRCDN.pdf) |
| Ley de Seguridad Interior | [`lsint/`](lsint/) | 34 | 2017-12-21 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSInt_300519.pdf) |
| Ley de Seguridad Nacional | [`lsn/`](lsn/) | 76 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSN.pdf) |
| Ley de Sistemas de Pagos | [`lsp/`](lsp/) | 44 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSP.pdf) |
| Ley de Sociedades de Solidaridad Social | [`lsss/`](lsss/) | 43 | 2018-04-24 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/71_240418.pdf) |
| Ley de Tesorería de la Federación | [`ltf/`](ltf/) | 60 | 2015-12-30 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LTF.pdf) |
| Ley de Transparencia y de Fomento a la Competencia en el Crédito Garantizado | [`ltfccg/`](ltfccg/) | 23 | 2014-01-10 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/256.pdf) |
| Ley de Uniones de Crédito | [`luc/`](luc/) | 151 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LUC.pdf) |
| Ley de Vertimientos en las Zonas Marinas Mexicanas | [`lvzmm/`](lvzmm/) | 68 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LVZMM.pdf) |
| Ley de Vivienda | [`lviv/`](lviv/) | 97 | 2026-04-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LViv.pdf) |
| Ley de Vías Generales de Comunicación | [`lvgc/`](lvgc/) | 593 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LVGC.pdf) |
| Ley de la Agencia Nacional de Seguridad Industrial y de Protección al Medio Ambiente del Sector Hidrocarburos | [`lansi/`](lansi/) | 38 | 2022-05-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LANSI.pdf) |
| Ley de la Casa de Moneda de México | [`lcmm/`](lcmm/) | 17 | 2022-05-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCMM.pdf) |
| Ley de la Comisión Nacional Bancaria y de Valores | [`lcnbv/`](lcnbv/) | 31 | 2022-05-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCNBV.pdf) |
| Ley de la Comisión Nacional de Energía | [`lcne/`](lcne/) | 28 | 2025-03-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCNE.pdf) |
| Ley de la Comisión Nacional de los Derechos Humanos | [`lcndh/`](lcndh/) | 86 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCNDH.pdf) |
| Ley de la Economía Social y Solidaria | [`less/`](less/) | 58 | 2025-04-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LESS.pdf) |
| Ley de la Empresa Pública del Estado, Comisión Federal de Electricidad | [`lepecfe/`](lepecfe/) | 131 | 2025-03-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LEPECFE.pdf) |
| Ley de la Empresa Pública del Estado, Petróleos Mexicanos | [`lepepm/`](lepepm/) | 126 | 2025-03-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LEPEPM.pdf) |
| Ley de la Fiscalía General de la República | [`lfgr/`](lfgr/) | 101 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFGR.pdf) |
| Ley de la Guardia Nacional | [`lgn/`](lgn/) | 96 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGN.pdf) |
| Ley de la Policía Federal | [`lpf/`](lpf/) | 55 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LPF.pdf) |
| Ley de los Derechos de las Personas Adultas Mayores | [`ldpam/`](ldpam/) | 52 | 2024-06-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LDPAM.pdf) |
| Ley de los Husos Horarios en los Estados Unidos Mexicanos | [`lhheum/`](lhheum/) | 7 | 2022-11-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LHHEUM.pdf) |
| Ley de los Institutos Nacionales de Salud | [`lins/`](lins/) | 60 | 2022-05-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LINS.pdf) |
| Ley de los Sistemas de Ahorro para el Retiro | [`lsar/`](lsar/) | 148 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSAR.pdf) |
| Ley del Banco de México | [`lbm/`](lbm/) | 73 | 2014-01-10 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/74.pdf) |
| Ley del Diario Oficial de la Federación y Gacetas Gubernamentales | [`ldofgg/`](ldofgg/) | 20 | 2019-05-31 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/75_100619.pdf) |
| Ley del Fondo Mexicano del Petróleo para la Estabilización y el Desarrollo | [`lfmped/`](lfmped/) | 25 | 2025-03-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFMPED.pdf) |
| Ley del Impuesto Especial sobre Producción y Servicios | [`lieps/`](lieps/) | 68 | 2025-11-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIEPS.pdf) |
| Ley del Impuesto al Valor Agregado | [`liva/`](liva/) | 80 | 2021-11-12 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIVA.pdf) |
| Ley del Impuesto sobre la Renta | [`lisr/`](lisr/) | 236 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LISR.pdf) |
| Ley del Instituto Mexicano de la Juventud | [`limj/`](limj/) | 20 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIMJ.pdf) |
| Ley del Instituto Nacional de los Pueblos Indígenas | [`linpi/`](linpi/) | 29 | 2023-12-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LINPI.pdf) |
| Ley del Instituto de Seguridad y Servicios Sociales de los Trabajadores del Estado | [`lissste/`](lissste/) | 259 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LISSSTE.pdf) |
| Ley del Instituto del Fondo Nacional de la Vivienda para los Trabajadores | [`lifnvt/`](lifnvt/) | 95 | 2025-02-21 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIFNVT.pdf) |
| Ley del Instituto del Fondo Nacional para el Consumo de los Trabajadores | [`lifnct/`](lifnct/) | 33 | 2024-01-03 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIFNCT.pdf) |
| Ley del Mercado de Valores | [`lmv/`](lmv/) | 463 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LMV.pdf) |
| Ley del Registro Público Vehicular | [`lrpv/`](lrpv/) | 27 | 2021-05-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/269_200521.pdf) |
| Ley del Sector Eléctrico | [`lse/`](lse/) | 188 | 2025-03-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSE.pdf) |
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
| Ley de Aguas Nacionales | invariantes rotos: [lan] índice == archivos == unidades: 215 md / 216 idx / 216 items (¿colisión de claves?) | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAN.pdf) |
| Ley de Ahorro y Crédito Popular | invariantes rotos: [lacp] índice == archivos == unidades: 232 md / 234 idx / 234 items (¿colisión de claves?) | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LACP.pdf) |
| Ley de Sociedades de Responsabilidad Limitada de Interés Público | 1 unidades no reproducen el PDF (lsrlip/013) | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/70.pdf) |
| Ley de los Impuestos Generales de Importación y de Exportación | 1 unidades no reproducen el PDF (ligie-2022/001) | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIGIE_2022.pdf) |
| Ley del Instituto de Seguridad Social para las Fuerzas Armadas Mexicanas | 3 unidades no reproducen el PDF (lissfam/027, lissfam/034, lissfam/037) | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LISSFAM.pdf) |
| Ley del Sector Hidrocarburos | 1 unidades no reproducen el PDF (lsh/077) | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSH.pdf) |

<!-- EXCLUIDAS:FIN -->
