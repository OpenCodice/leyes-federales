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
| Código Federal de Procedimientos Civiles | [`cfpc/`](cfpc/) | 630 | 2021-06-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CFPC.pdf) |
| Código Fiscal de la Federación | [`cff/`](cff/) | 421 | 2026-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CFF.pdf) |
| Código Militar de Procedimientos Penales | [`cmpp/`](cmpp/) | 452 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CMPP.pdf) |
| Código Nacional de Procedimientos Civiles y Familiares | [`cnpcf/`](cnpcf/) | 1191 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CNPCF.pdf) |
| Código Nacional de Procedimientos Penales | [`cnpp/`](cnpp/) | 490 | 2025-11-28 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CNPP.pdf) |
| Código Penal Federal | [`cpf/`](cpf/) | 555 | 2026-03-13 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CPF.pdf) |
| Código de Comercio | [`ccom/`](ccom/) | 1641 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CCom.pdf) |
| Código de Justicia Militar | [`cjm/`](cjm/) | 952 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/CJM.pdf) |
| Estatuto de Gobierno del Distrito Federal | [`egdf/`](egdf/) | 145 | 2014-06-27 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/10_270614.pdf) |
| Impuesto sobre Servicios Expresamente Declarados de Interés Público por Ley, en los que Intervengan Empresas Concesionarias de Bienes del Dominio Directo de la Nación (LEY que establece, reforma y adiciona las disposiciones relativas a diversos impuestos) | [`lisipl/`](lisipl/) | 7 | 1968-12-31 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/79.pdf) |
| Ley Aduanera | [`ladua/`](ladua/) | 277 | 2025-11-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAdua.pdf) |
| Ley Agraria | [`lagra/`](lagra/) | 201 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAgra.pdf) |
| Ley Federal contra la Delincuencia Organizada | [`lfcdo/`](lfcdo/) | 57 | 2025-11-28 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFCDO.pdf) |
| Ley Federal de Armas de Fuego y Explosivos | [`lfafe/`](lfafe/) | 125 | 2025-05-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFAFE.pdf) |
| Ley Federal de Austeridad Republicana | [`lfar/`](lfar/) | 30 | 2025-04-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFAR.pdf) |
| Ley Federal de Cine y el Audiovisual | [`lfca/`](lfca/) | 68 | 2026-05-22 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFCA.pdf) |
| Ley Federal de Cinematografía | [`lfc/`](lfc/) | 58 | 2021-03-22 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFC.pdf) |
| Ley Federal de Competencia Económica | [`lfce/`](lfce/) | 153 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFCE.pdf) |
| Ley Federal de Consulta Popular | [`lfcpo/`](lfcpo/) | 65 | 2021-05-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFCPo_190521.pdf) |
| Ley Federal de Correduría Pública | [`lfcp/`](lfcp/) | 23 | 2012-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/105.pdf) |
| Ley Federal de Declaración Especial de Ausencia para Personas Desaparecidas | [`lfdeapd/`](lfdeapd/) | 33 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFDEAPD.pdf) |
| Ley Federal de Defensoría Pública | [`lfdefp/`](lfdefp/) | 42 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFDefP.pdf) |
| Ley Federal de Derechos | [`lfd/`](lfd/) | 694 | 2025-11-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFD.pdf) |
| Ley Federal de Deuda Pública | [`lgdp/`](lgdp/) | 32 | 2018-01-30 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/136_300118.pdf) |
| Ley Federal de Fomento a las Actividades Realizadas por Organizaciones de la Sociedad Civil | [`lffaosc/`](lffaosc/) | 32 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFFAOSC.pdf) |
| Ley Federal de Juegos y Sorteos | [`lfjs/`](lfjs/) | 17 | 1947-12-31 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/109.pdf) |
| Ley Federal de Presupuesto y Responsabilidad Hacendaria | [`lfprh/`](lfprh/) | 124 | 2026-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPRH.pdf) |
| Ley Federal de Procedimiento Administrativo | [`lfpa/`](lfpa/) | 118 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPA.pdf) |
| Ley Federal de Procedimiento Contencioso Administrativo | [`lfpca/`](lfpca/) | 106 | 2026-06-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPCA.pdf) |
| Ley Federal de Protección a la Propiedad Industrial | [`lfppi/`](lfppi/) | 421 | 2026-04-03 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPPI.pdf) |
| Ley Federal de Protección al Consumidor | [`lfpc/`](lfpc/) | 190 | 2025-12-12 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPC.pdf) |
| Ley Federal de Protección de Datos Personales en Posesión de los Particulares | [`lfpdppp/`](lfpdppp/) | 64 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPDPPP.pdf) |
| Ley Federal de Protección del Patrimonio Cultural de los Pueblos y Comunidades Indígenas y Afromexicanas | [`lfppcpcia/`](lfppcpcia/) | 75 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPPCPCIA.pdf) |
| Ley Federal de Remuneraciones de los Servidores Públicos | [`lfremsp/`](lfremsp/) | 34 | 2021-05-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFRemSP_190521.pdf) |
| Ley Federal de Responsabilidad Ambiental | [`lfra/`](lfra/) | 56 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFRA.pdf) |
| Ley Federal de Responsabilidad Patrimonial del Estado | [`lfrpe/`](lfrpe/) | 35 | 2023-12-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFRPE.pdf) |
| Ley Federal de Responsabilidades de los Servidores Públicos | [`lfrsp/`](lfrsp/) | 94 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFRSP.pdf) |
| Ley Federal de Revocación de Mandato | [`lfrm/`](lfrm/) | 61 | 2021-09-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFRM.pdf) |
| Ley Federal de Sanidad Animal | [`lfsa/`](lfsa/) | 177 | 2024-05-21 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFSA.pdf) |
| Ley Federal de Sanidad Vegetal | [`lfsv/`](lfsv/) | 97 | 2022-05-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFSV.pdf) |
| Ley Federal de Seguridad Privada | [`lfsp/`](lfsp/) | 50 | 2011-10-17 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFSP.pdf) |
| Ley Federal de Variedades Vegetales | [`lfvv/`](lfvv/) | 48 | 2022-05-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFVV.pdf) |
| Ley Federal de Zonas Económicas Especiales | [`lfzee/`](lfzee/) | 50 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFZEE.pdf) |
| Ley Federal de las Entidades Paraestatales | [`lfep/`](lfep/) | 69 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFEP.pdf) |
| Ley Federal de los Derechos del Contribuyente | [`lfdc/`](lfdc/) | 24 | 2005-06-23 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFDC.pdf) |
| Ley Federal de los Trabajadores al Servicio del Estado, Reglamentaria del Apartado B) del Artículo 123 Constitucional | [`lftse/`](lftse/) | 177 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFTSE.pdf) |
| Ley Federal del Derecho de Autor | [`lfda/`](lfda/) | 259 | 2026-05-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFDA.pdf) |
| Ley Federal del Impuesto sobre Automóviles Nuevos | [`lfisan/`](lfisan/) | 14 | 2021-11-12 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFISAN.pdf) |
| Ley Federal del Mar | [`lfm/`](lfm/) | 65 | 1986-01-08 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/124.pdf) |
| Ley Federal del Trabajo | [`lft/`](lft/) | 1265 | 2026-05-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFT.pdf) |
| Ley Federal para Prevenir y Eliminar la Discriminación | [`lfped/`](lfped/) | 105 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPED.pdf) |
| Ley Federal para Prevenir y Sancionar los Delitos Cometidos en Materia de Hidrocarburos | [`lfpsdmh/`](lfpsdmh/) | 24 | 2021-11-12 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPSDMH.pdf) |
| Ley Federal para el Control de Precursores Químicos, Productos Químicos Esenciales y Máquinas para Elaborar Cápsulas, Tabletas y/o Comprimidos | [`lfcpq/`](lfcpq/) | 31 | 2023-05-03 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFCPQ.pdf) |
| Ley Federal para el Control de Sustancias Químicas Susceptibles de Desvío para la Fabricación de Armas Químicas | [`lfcsq/`](lfcsq/) | 75 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFCSQ.pdf) |
| Ley Federal para el Fomento de la Microindustria y la Actividad Artesanal | [`lffmaa/`](lffmaa/) | 45 | 2023-03-27 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFFMAA.pdf) |
| Ley Federal para el Fomento y Protección del Maíz Nativo | [`lffpmn/`](lffpmn/) | 13 | 2020-04-13 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFFPMN_130420.pdf) |
| Ley Federal para la Administración y Enajenación de Bienes del Sector Público | [`lfaebsp/`](lfaebsp/) | 100 | 2024-04-30 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFAEBSP.pdf) |
| Ley Federal para la Prevención e Identificación de Operaciones con Recursos de Procedencia Ilícita | [`lfpiorpi/`](lfpiorpi/) | 73 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPIORPI.pdf) |
| Ley Federal para la Protección a Personas que Intervienen en el Procedimiento Penal | [`lfppipp/`](lfppipp/) | 52 | 2021-05-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPPIPP_200521.pdf) |
| Ley Federal sobre Monumentos y Zonas Arqueológicos, Artísticos e Históricos | [`lfmzaah/`](lfmzaah/) | 62 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFMZAAH.pdf) |
| Ley General de Acceso de las Mujeres a una Vida Libre de Violencias | [`lgamvlv/`](lgamvlv/) | 103 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGAMVLV.pdf) |
| Ley General de Aguas | [`lgag/`](lgag/) | 45 | 2025-12-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGAg.pdf) |
| Ley General de Archivos | [`lga/`](lga/) | 123 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGA.pdf) |
| Ley General de Asentamientos Humanos, Ordenamiento Territorial y Desarrollo Urbano | [`lgahotdu/`](lgahotdu/) | 119 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGAHOTDU.pdf) |
| Ley General de Bibliotecas | [`lgb/`](lgb/) | 45 | 2023-11-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGB.pdf) |
| Ley General de Bienes Nacionales | [`lgbn/`](lgbn/) | 158 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGBN.pdf) |
| Ley General de Cambio Climático | [`lgcc/`](lgcc/) | 116 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGCC.pdf) |
| Ley General de Comunicación Social | [`lgcs/`](lgcs/) | 45 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGCS.pdf) |
| Ley General de Contabilidad Gubernamental | [`lgcg/`](lgcg/) | 87 | 2026-05-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGCG.pdf) |
| Ley General de Cultura Física y Deporte | [`lgcfd/`](lgcfd/) | 157 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGCFD.pdf) |
| Ley General de Cultura y Derechos Culturales | [`lgcdc/`](lgcdc/) | 42 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGCDC.pdf) |
| Ley General de Derechos Lingüísticos de los Pueblos Indígenas | [`lgdlpi/`](lgdlpi/) | 25 | 2023-10-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGDLPI.pdf) |
| Ley General de Desarrollo Forestal Sustentable | [`lgdfs/`](lgdfs/) | 173 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGDFS.pdf) |
| Ley General de Desarrollo Social | [`lgds/`](lgds/) | 87 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGDS.pdf) |
| Ley General de Economía Circular | [`lgec/`](lgec/) | 49 | 2026-01-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGEC.pdf) |
| Ley General de Educación | [`lge/`](lge/) | 183 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGE.pdf) |
| Ley General de Educación Superior | [`lges/`](lges/) | 77 | 2021-04-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGES_200421.pdf) |
| Ley General de Instituciones y Procedimientos Electorales | [`lgipe/`](lgipe/) | 542 | 2026-06-02 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGIPE.pdf) |
| Ley General de Mecanismos Alternativos de Solución de Controversias | [`lgmasc/`](lgmasc/) | 144 | 2024-01-26 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGMASC.pdf) |
| Ley General de Movilidad y Seguridad Vial | [`lgmsv/`](lgmsv/) | 82 | 2023-12-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGMSV.pdf) |
| Ley General de Organizaciones y Actividades Auxiliares del Crédito | [`lgoaac/`](lgoaac/) | 263 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGOAAC.pdf) |
| Ley General de Partidos Políticos | [`lgpp/`](lgpp/) | 97 | 2023-03-02 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPP.pdf) |
| Ley General de Pesca y Acuacultura Sustentables | [`lgpas/`](lgpas/) | 167 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPAS.pdf) |
| Ley General de Población | [`lgp/`](lgp/) | 165 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGP.pdf) |
| Ley General de Prestación de Servicios para la Atención, Cuidado y Desarrollo Integral Infantil | [`lgpsacdii/`](lgpsacdii/) | 76 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPSACDII.pdf) |
| Ley General de Protección Civil | [`lgpc/`](lgpc/) | 94 | 2023-12-21 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPC.pdf) |
| Ley General de Protección de Datos Personales en Posesión de Sujetos Obligados | [`lgpdppso/`](lgpdppso/) | 137 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPDPPSO.pdf) |
| Ley General de Responsabilidades Administrativas | [`lgra/`](lgra/) | 235 | 2025-12-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGRA.pdf) |
| Ley General de Salud | [`lgs/`](lgs/) | 732 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGS.pdf) |
| Ley General de Sociedades Cooperativas | [`lgsc/`](lgsc/) | 123 | 2025-04-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGSC.pdf) |
| Ley General de Sociedades Mercantiles | [`lgsm/`](lgsm/) | 277 | 2023-10-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGSM.pdf) |
| Ley General de Transparencia y Acceso a la Información Pública | [`lgtaip/`](lgtaip/) | 216 | 2025-03-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGTAIP.pdf) |
| Ley General de Turismo | [`lgt/`](lgt/) | 73 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGT.pdf) |
| Ley General de Títulos y Operaciones de Crédito | [`lgtoc/`](lgtoc/) | 440 | 2024-03-26 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGTOC.pdf) |
| Ley General de Vida Silvestre | [`lgvs/`](lgvs/) | 143 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGVS.pdf) |
| Ley General de Víctimas | [`lgv/`](lgv/) | 202 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGV.pdf) |
| Ley General de la Alimentación Adecuada y Sostenible | [`lgaas/`](lgaas/) | 111 | 2024-04-17 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGAAS.pdf) |
| Ley General de los Derechos de Niñas, Niños y Adolescentes | [`lgdnna/`](lgdnna/) | 181 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGDNNA.pdf) |
| Ley General de los Medios de Impugnación en Materia Electoral | [`lgmime/`](lgmime/) | 70 | 2023-03-02 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGMIME.pdf) |
| Ley General del Equilibrio Ecológico y la Protección al Ambiente | [`lgeepa/`](lgeepa/) | 270 | 2026-01-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGEEPA.pdf) |
| Ley General del Sistema Nacional Anticorrupción | [`lgsna/`](lgsna/) | 60 | 2021-05-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGSNA_200521.pdf) |
| Ley General del Sistema Nacional de Seguridad Pública | [`lgsnsp/`](lgsnsp/) | 147 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGSNSP.pdf) |
| Ley General del Sistema de Medios de Impugnación en Materia Electoral | [`lgsmime/`](lgsmime/) | 118 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGSMIME.pdf) |
| Ley General del Sistema para la Carrera de las Maestras y los Maestros | [`lgscmm/`](lgscmm/) | 107 | 2019-09-30 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGSCMM_300919.pdf) |
| Ley General en Materia de Delitos Electorales | [`lgmde/`](lgmde/) | 29 | 2021-05-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGMDE_200521.pdf) |
| Ley General en Materia de Desaparición Forzada de Personas, Desaparición Cometida por Particulares y del Sistema Nacional de Búsqueda de Personas | [`lgmdfp/`](lgmdfp/) | 189 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGMDFP.pdf) |
| Ley General en materia de Humanidades, Ciencias, Tecnologías e Innovación | [`lgmhcti/`](lgmhcti/) | 100 | 2023-05-08 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGMHCTI.pdf) |
| Ley General para Prevenir y Sancionar los Delitos en Materia de Secuestro, Reglamentaria de la fracción XXI del artículo 73 de la Constitución Política de los Estados Unidos Mexicanos | [`lgpsdms/`](lgpsdms/) | 48 | 2021-05-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPSDMS_200521.pdf) |
| Ley General para Prevenir, Investigar y Sancionar la Tortura y Otros Tratos o Penas Crueles, Inhumanos o Degradantes | [`lgpist/`](lgpist/) | 96 | 2022-04-28 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPIST.pdf) |
| Ley General para Prevenir, Investigar y Sancionar los Delitos en Materia de Extorsión, Reglamentaria de la fracción XXI del artículo 73 de la Constitución Política de los Estados Unidos Mexicanos | [`lgpisdme/`](lgpisdme/) | 43 | 2025-11-28 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPISDME.pdf) |
| Ley General para Prevenir, Sancionar y Erradicar los Delitos en Materia de Trata de Personas y para la Protección y Asistencia a las Víctimas de estos Delitos | [`lgpsedmtp/`](lgpsedmtp/) | 126 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPSEDMTP.pdf) |
| Ley General para el Control del Tabaco | [`lgct/`](lgct/) | 57 | 2022-02-17 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGCT.pdf) |
| Ley General para el Fortalecimiento y Armonización Catastral y Registral | [`lgfacr/`](lgfacr/) | 45 | 2026-10-23 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGFACR.pdf) |
| Ley General para la Atención y Protección a Personas con la Condición del Espectro Autista | [`lgappcea/`](lgappcea/) | 18 | 2015-04-30 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGAPPCEA_270516.pdf) |
| Ley General para la Detección Oportuna del Cáncer en la Infancia y la Adolescencia | [`lgdocia/`](lgdocia/) | 32 | 2021-01-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGDOCIA_070121.pdf) |
| Ley General para la Igualdad Sustantiva entre Mujeres y Hombres | [`lgimh/`](lgimh/) | 52 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGISMH.pdf) |
| Ley General para la Inclusión de las Personas con Discapacidad | [`lgipd/`](lgipd/) | 60 | 2024-06-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGIPD.pdf) |
| Ley General para la Prevención Social de la Violencia y la Delincuencia | [`lgpsvd/`](lgpsvd/) | 30 | 2021-05-04 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPSVD_040521.pdf) |
| Ley General para la Prevención y Gestión Integral de los Residuos | [`lgpgir/`](lgpgir/) | 126 | 2026-01-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPGIR.pdf) |
| Ley Monetaria de los Estados Unidos Mexicanos | [`lmeum/`](lmeum/) | 24 | 2026-01-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LMEUM.pdf) |
| Ley Nacional de Ejecución Penal | [`lnep/`](lnep/) | 207 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LNEP.pdf) |
| Ley Nacional de Extinción de Dominio | [`lned/`](lned/) | 251 | 2025-11-28 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LNED.pdf) |
| Ley Nacional de Mecanismos Alternativos de Solución de Controversias en Materia Penal | [`lnmascmp/`](lnmascmp/) | 52 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LNMASCMP.pdf) |
| Ley Nacional del Registro de Detenciones | [`lnrd/`](lnrd/) | 36 | 2019-05-27 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LNRD_270519.pdf) |
| Ley Nacional del Sistema Integral de Justicia Penal para Adolescentes | [`lnsijpa/`](lnsijpa/) | 266 | 2022-12-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LNSIJPA.pdf) |
| Ley Nacional para Eliminar Trámites Burocráticos | [`lnetb/`](lnetb/) | 114 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LNETB.pdf) |
| Ley Nacional sobre el Uso de la Fuerza | [`lnuf/`](lnuf/) | 44 | 2024-01-24 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LNUF.pdf) |
| Ley Orgánica de Nacional Financiera | [`lonf/`](lonf/) | 38 | 2014-01-10 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/162.pdf) |
| Ley Orgánica de Sociedad Hipotecaria Federal | [`loshf/`](loshf/) | 38 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOSHF.pdf) |
| Ley Orgánica de la Administración Pública Federal | [`loapf/`](loapf/) | 72 | 2026-05-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOAPF.pdf) |
| Ley Orgánica de la Armada de México | [`loam/`](loam/) | 101 | 2025-11-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOAM.pdf) |
| Ley Orgánica de la Procuraduría General de Justicia del Distrito Federal | [`lopgjdf/`](lopgjdf/) | 84 | 2011-06-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOPGJDF.pdf) |
| Ley Orgánica de la Procuraduría de la Defensa del Contribuyente | [`lopdc/`](lopdc/) | 28 | 2022-05-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOPDC.pdf) |
| Ley Orgánica de la Universidad Autónoma Agraria Antonio Narro | [`louaaan/`](louaaan/) | 26 | 2006-04-26 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOUAAAN.pdf) |
| Ley Orgánica de la Universidad Autónoma Metropolitana | [`louam/`](louam/) | 37 | 1973-12-17 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/157.pdf) |
| Ley Orgánica de la Universidad Nacional Autónoma de México | [`lounam/`](lounam/) | 18 | 1945-01-06 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/158.pdf) |
| Ley Orgánica de los Tribunales Agrarios | [`lota/`](lota/) | 30 | 1998-01-23 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/159.pdf) |
| Ley Orgánica del Banco Nacional de Comercio Exterior | [`lobnce/`](lobnce/) | 37 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOBNCE.pdf) |
| Ley Orgánica del Banco Nacional de Obras y Servicios Públicos | [`lobnosp/`](lobnosp/) | 36 | 2024-04-01 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOBNOSP.pdf) |
| Ley Orgánica del Banco Nacional del Ejército, Fuerza Aérea y Armada | [`lobnefaa/`](lobnefaa/) | 59 | 2014-01-10 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/167.pdf) |
| Ley Orgánica del Banco del Bienestar | [`lobb/`](lobb/) | 41 | 2019-07-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/164_190719.pdf) |
| Ley Orgánica del Centro Federal de Conciliación y Registro Laboral | [`locfcrl/`](locfcrl/) | 25 | 2020-01-06 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOCFCRL_060120.pdf) |
| Ley Orgánica del Congreso General de los Estados Unidos Mexicanos | [`locg/`](locg/) | 151 | 2025-07-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOCGEUM.pdf) |
| Ley Orgánica del Ejército y Fuerza Aérea Mexicanos | [`loefam/`](loefam/) | 233 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOEFAM.pdf) |
| Ley Orgánica del Instituto Nacional de Antropología e Historia | [`loinah/`](loinah/) | 20 | 2015-12-17 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/170_171215.pdf) |
| Ley Orgánica del Instituto Politécnico Nacional | [`loipn/`](loipn/) | 34 | 1981-12-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/171.pdf) |
| Ley Orgánica del Poder Judicial de la Federación | [`lopjf/`](lopjf/) | 307 | 2025-11-28 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOPJF.pdf) |
| Ley Orgánica del Seminario de Cultura Mexicana | [`loscm/`](loscm/) | 16 | 2022-05-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOSCM.pdf) |
| Ley Orgánica del Tribunal Federal de Justicia Administrativa | [`lotfja/`](lotfja/) | 70 | 2025-10-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LOTFJA.pdf) |
| Ley Reglamentaria de la Fracción V del Artículo 76 de la Constitución General de la República | [`lrfv-art76/`](lrfv-art76/) | 15 | 1978-12-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/202.pdf) |
| Ley Reglamentaria de la Fracción XIII Bis del Apartado B, del Artículo 123 de la Constitución Política de los Estados Unidos Mexicanos | [`lrfxiiib-art123/`](lrfxiiib-art123/) | 25 | 2021-07-31 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRFXIIIB_Art123.pdf) |
| Ley Reglamentaria de la Fracción XVIII del Artículo 73 Constitucional, en lo que se Refiere a la Facultad del Congreso para Dictar Reglas para Determinar el Valor Relativo de la Moneda Extranjera | [`lrfxviii-art73/`](lrfxviii-art73/) | 2 | 1982-12-27 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/204.pdf) |
| Ley Reglamentaria de la fracción VI del artículo 76 de la Constitución Política de los Estados Unidos Mexicanos | [`lrart76-fracvi/`](lrart76-fracvi/) | 25 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRArt76_fracVI.pdf) |
| Ley Reglamentaria de las Fracciones I y II del Artículo 105 de la Constitución Política de los Estados Unidos Mexicanos | [`lrfiyii-art105/`](lrfiyii-art105/) | 74 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRFIyII_Art105.pdf) |
| Ley Reglamentaria del Artículo 27 Constitucional en Materia Nuclear | [`lrart27-mn/`](lrart27-mn/) | 52 | 2012-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/207.pdf) |
| Ley Reglamentaria del Artículo 3o. de la Constitución Política de los Estados Unidos Mexicanos, en materia de Mejora Continua de la Educación | [`lrart3-mmce/`](lrart3-mmce/) | 68 | 2019-09-30 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRArt3_MMCE_300919.pdf) |
| Ley Reglamentaria del Artículo 5o. Constitucional, relativo al ejercicio de las profesiones en la Ciudad de México | [`lrart5-prof/`](lrart5-prof/) | 73 | 2018-01-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/208_190118.pdf) |
| Ley Reglamentaria del Servicio Ferroviario | [`lrsf/`](lrsf/) | 69 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRSF.pdf) |
| Ley Reglamentaria del artículo 6o., párrafo primero, de la Constitución Política de los Estados Unidos Mexicanos, en materia del Derecho de Réplica | [`lrart6-mdr/`](lrart6-mdr/) | 42 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRArt6_MDR.pdf) |
| Ley Sobre el Contrato de Seguro | [`lcs/`](lcs/) | 210 | 2013-04-04 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/211.pdf) |
| Ley Sobre la Aprobación de Tratados Internacionales en Materia Económica | [`latime/`](latime/) | 14 | 2004-09-02 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/271.pdf) |
| Ley de Adquisiciones, Arrendamientos y Servicios del Sector Público | [`laassp/`](laassp/) | 120 | 2025-04-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAASSP.pdf) |
| Ley de Aeropuertos | [`laero/`](laero/) | 101 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAero.pdf) |
| Ley de Aguas Nacionales | [`lan/`](lan/) | 215 | 2025-12-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAN.pdf) |
| Ley de Ahorro y Crédito Popular | [`lacp/`](lacp/) | 232 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LACP.pdf) |
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
| Ley de Concursos Mercantiles | [`lcm/`](lcm/) | 355 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCM.pdf) |
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
| Ley de Expropiación | [`lexp/`](lexp/) | 25 | 2012-01-27 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/35.pdf) |
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
| Ley de Sociedades de Responsabilidad Limitada de Interés Público | [`lsrlip/`](lsrlip/) | 13 | 2012-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/70.pdf) |
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
| Ley del Instituto de Seguridad Social para las Fuerzas Armadas Mexicanas | [`lissfam/`](lissfam/) | 231 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LISSFAM.pdf) |
| Ley del Instituto de Seguridad y Servicios Sociales de los Trabajadores del Estado | [`lissste/`](lissste/) | 259 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LISSSTE.pdf) |
| Ley del Instituto del Fondo Nacional de la Vivienda para los Trabajadores | [`lifnvt/`](lifnvt/) | 95 | 2025-02-21 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIFNVT.pdf) |
| Ley del Instituto del Fondo Nacional para el Consumo de los Trabajadores | [`lifnct/`](lifnct/) | 33 | 2024-01-03 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIFNCT.pdf) |
| Ley del Mercado de Valores | [`lmv/`](lmv/) | 463 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LMV.pdf) |
| Ley del Registro Público Vehicular | [`lrpv/`](lrpv/) | 27 | 2021-05-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/269_200521.pdf) |
| Ley del Sector Eléctrico | [`lse/`](lse/) | 188 | 2025-03-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSE.pdf) |
| Ley del Sector Hidrocarburos | [`lsh/`](lsh/) | 166 | 2025-03-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSH.pdf) |
| Ley del Seguro Social | [`lss/`](lss/) | 385 | 2026-01-15 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSS.pdf) |
| Ley del Servicio Exterior Mexicano | [`lsem/`](lsem/) | 86 | 2018-04-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/96_190418.pdf) |
| Ley del Servicio Militar | [`lsm/`](lsm/) | 65 | 2022-05-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSM.pdf) |
| Ley del Servicio Postal Mexicano | [`lspm/`](lspm/) | 72 | 2023-01-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSPM.pdf) |
| Ley del Servicio Profesional de Carrera en la Administración Pública Federal | [`lspcapf/`](lspcapf/) | 80 | 2006-01-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/260.pdf) |
| Ley del Servicio de Administración Tributaria | [`lsat/`](lsat/) | 41 | 2018-12-04 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/93_041218.pdf) |
| Ley del Sistema Nacional de Información Estadística y Geográfica | [`lsnieg/`](lsnieg/) | 134 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSNIEG.pdf) |
| Ley del Sistema Nacional de Investigación e Inteligencia en Materia de Seguridad Pública | [`lsniimsp/`](lsniimsp/) | 51 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSNIIMSP.pdf) |
| Ley del Sistema Público de Radiodifusión del Estado Mexicano | [`lsprem/`](lsprem/) | 32 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSPREM.pdf) |
| Ley en Materia de Telecomunicaciones y Radiodifusión | [`lmtr/`](lmtr/) | 299 | 2025-07-16 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LMTR.pdf) |
| Ley para Conservar la Neutralidad del País | [`lcnp/`](lcnp/) | 4 | 2018-06-21 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/176_210618.pdf) |
| Ley para Determinar el Valor de la Unidad de Medida y Actualización | [`ldvuma/`](ldvuma/) | 5 | 2016-12-30 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LDVUMA_301216.pdf) |
| Ley para Impulsar el Incremento Sostenido de la Productividad y la Competitividad de la Economía Nacional | [`liispcen/`](liispcen/) | 21 | 2024-04-17 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIISPCEN.pdf) |
| Ley para Regular las Actividades de las Sociedades Cooperativas de Ahorro y Préstamo | [`lrascap/`](lrascap/) | 144 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRASCAP.pdf) |
| Ley para Regular las Agrupaciones Financieras | [`lraf/`](lraf/) | 193 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRAF.pdf) |
| Ley para Regular las Instituciones de Tecnología Financiera | [`lritf/`](lritf/) | 145 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRITF.pdf) |
| Ley para Regular las Sociedades de Información Crediticia | [`lrsic/`](lrsic/) | 85 | 2024-01-24 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRSIC.pdf) |
| Ley para el Desarrollo de la Competitividad de la Micro, Pequeña y Mediana Empresa | [`ldcmpme/`](ldcmpme/) | 26 | 2023-10-20 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LDCMPME.pdf) |
| Ley para el Diálogo, la Conciliación y la Paz Digna en Chiapas | [`ldcpdch/`](ldcpdch/) | 13 | 1995-03-11 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/177.pdf) |
| Ley para el Fomento de la Inversión en Infraestructura Estratégica para el Desarrollo con Bienestar | [`lfiiedb/`](lfiiedb/) | 141 | 2026-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFIIEDB.pdf) |
| Ley para el uso y protección de la denominación y del emblema de la Cruz Roja | [`lupdecr/`](lupdecr/) | 20 | 2007-03-23 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LUPDECR.pdf) |
| Ley para la Comprobación, Ajuste y Cómputo de Servicios de la Armada de México | [`lcacsam/`](lcacsam/) | 25 | 2009-06-12 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/268.pdf) |
| Ley para la Comprobación, Ajuste y Cómputo de Servicios en el Ejército y Fuerza Aérea Mexicanos | [`lcacsefam/`](lcacsefam/) | 37 | 2024-05-03 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCACSEFAM.pdf) |
| Ley para la Protección de Personas Defensoras de Derechos Humanos y Periodistas | [`lppddhp/`](lppddhp/) | 67 | 2022-04-28 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LPPDDHP.pdf) |
| Ley para la Transparencia y Ordenamiento de los Servicios Financieros | [`ltosf/`](ltosf/) | 88 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LTOSF.pdf) |
| Ley para la Transparencia, Prevención y Combate de Prácticas Indebidas en Materia de Contratación de Publicidad | [`ltpcpimcp/`](ltpcpimcp/) | 13 | 2021-06-03 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LTPCPIMCP.pdf) |
| Ley que Aprueba la Adhesión de México al Convenio Constitutivo del Banco de Desarrollo del Caribe y su Ejecución | [`lmccbdc/`](lmccbdc/) | 10 | 2014-12-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/187_291214.pdf) |
| Ley que Crea el Fondo de Garantía y Fomento para la Agricultura, Ganadería y Avicultura | [`lfgfaga/`](lfgfaga/) | 14 | 2012-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/192.pdf) |
| Ley que Crea la Universidad del Ejército y Fuerza Aérea | [`luefa/`](luefa/) | 7 | 1975-12-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/196.pdf) |
| Ley que Declara Reservas Mineras Nacionales los Yacimientos de Uranio, Torio y las demás Substancias de las cuales se Obtengan Isótopos Hendibles que puedan Producir Energía Nuclear | [`lrmnyut/`](lrmnyut/) | 16 | 1972-01-12 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/197.pdf) |
| Ley que Establece Bases para la Ejecución en México, por el Poder Ejecutivo Federal, del Convenio Constitutivo de la Asociación Internacional de Fomento | [`lccaif/`](lccaif/) | 11 | 2025-06-06 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LCCAIF.pdf) |
| Ley que Establece Bases para la Ejecución en México, por el Poder Ejecutivo Federal, del Convenio Constitutivo del Banco Interamericano de Desarrollo | [`lccbid/`](lccbid/) | 12 | 2014-12-29 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/200_291214.pdf) |
| Ley que crea el Instituto Nacional de Bellas Artes y Literatura | [`linbal/`](linbal/) | 16 | 2015-12-17 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/193_171215.pdf) |
| Ley que crea la Agencia Espacial Mexicana | [`laem/`](laem/) | 17 | 2010-07-30 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LAEM.pdf) |
| Ley que crea la Universidad Autónoma Chapingo | [`luach/`](luach/) | 16 | 1977-12-30 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/195.pdf) |
| Ley sobre Cámaras Agrícolas, que en lo sucesivo se denominarán Asociaciones Agrícolas | [`lcaaa/`](lcaaa/) | 19 | 2012-04-09 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/23.pdf) |
| Ley sobre Refugiados, Protección Complementaria y Asilo Político | [`lrpcap/`](lrpcap/) | 79 | 2022-02-18 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LRPCAP.pdf) |
| Ley sobre el Escudo, la Bandera y el Himno Nacionales | [`lebhn/`](lebhn/) | 70 | 2025-07-21 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LEBHN.pdf) |
| Ley sobre la Celebración de Tratados | [`lsct/`](lsct/) | 11 | 2025-11-14 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LSCT.pdf) |
| Ordenanza General de la Armada | [`oga/`](oga/) | 1868 | 2000-10-19 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/218.pdf) |
| Presupuesto de Egresos de la Federación para el Ejercicio Fiscal 2026 | [`pef-2026/`](pef-2026/) | 39 | — | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/PEF_2026.pdf) |
| Reglamento Interior del Servicio de Administración Tributaria | [`risat/`](risat/) | 56 | 2021-12-21 | [PDF](https://wwwmat.sat.gob.mx/cs/Satellite?blobcol=urldata&blobkey=id&blobtable=MungoBlobs&blobwhere=1461176458878&ssbinary=true) |
| Reglamento de la Cámara de Diputados | [`reg-diputados/`](reg-diputados/) | 323 | 2025-05-07 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/Reg_Diputados.pdf) |
| Reglamento de la LFPIORPI | [`rlfpiorpi/`](rlfpiorpi/) | 70 | 2026-03-27 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/regley/Reg_LFPIORPI.pdf) |
| Reglamento de la Ley Aduanera | [`rladua/`](rladua/) | 282 | 2026-02-23 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/regley/Reg_LAdua.pdf) |
| Reglamento de la Ley del IEPS | [`rlieps/`](rlieps/) | 19 | 2006-12-04 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/regley/Reg_LIEPS.pdf) |
| Reglamento de la Ley del Impuesto al Valor Agregado | [`rliva/`](rliva/) | 84 | 2014-09-25 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/regley/Reg_LIVA_250914.pdf) |
| Reglamento de la Ley del Impuesto sobre la Renta | [`rlisr/`](rlisr/) | 313 | 2016-05-06 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/regley/Reg_LISR_060516.pdf) |
| Reglamento del Código Fiscal de la Federación | [`rcff/`](rcff/) | 113 | 2014-04-02 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/regley/Reg_CFF.pdf) |
| Reglamento del Senado de la República | [`reg-senado/`](reg-senado/) | 317 | 2024-12-06 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/Reg_Senado.pdf) |
| Reglamento para el Gobierno Interior del Congreso General de los Estados Unidos Mexicanos | [`rgic/`](rgic/) | 214 | 2010-12-24 | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/219.pdf) |

<!-- DOCUMENTOS:FIN -->

## Fuera del corpus

Leyes del índice cuya extracción no quedó fiel al PDF. Se reintentan solas
cuando cambia su PDF o el extractor.

<!-- EXCLUIDAS:INICIO -->

| Ley | Motivo | PDF oficial |
|---|---|---|
| Ley Federal de Producción, Certificación y Comercio de Semillas | La marca de agua girada del PDF deja letras sueltas dentro del texto de varios artículos. | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPCCS_110518.pdf) |
| Ley de los Impuestos Generales de Importación y de Exportación | La tarifa del artículo 1o. es una tabla de varias columnas; en texto plano las columnas se mezclan a media descripción. | [PDF](https://www.diputados.gob.mx/LeyesBiblio/pdf/LIGIE_2022.pdf) |

<!-- EXCLUIDAS:FIN -->

## Licencia

[CC0 1.0](LICENSE): dominio público. Los textos legislativos no son objeto de
derechos de autor (Ley Federal del Derecho de Autor, artículo 14, fracción
VIII); con CC0, la compilación, la metadata y el historial también se pueden
usar, copiar y redistribuir sin restricciones ni atribución.
