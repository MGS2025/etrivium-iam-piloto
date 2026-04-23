# Tema 11 — Registro de Fuentes

> **Tema**: 11 — Informatica basica. Representacion y comunicacion de la informacion: elementos constitutivos de un sistema de informacion. Caracteristicas y funciones. Arquitectura de ordenadores. Componentes internos de los equipos microinformaticos.
>
> **Bloque**: Parte II — Tecnico
> **Estado**: V2.0 — Pendiente validacion
> **Fecha actualizacion**: 2026-04-23 (v2.0)

---

## Fuentes Tier 1 (primarias)

| ID | Titulo | Origen | Fecha/Vigencia | Secciones usadas | URL/Referencia |
|---|---|---|---|---|---|
| IEEE-610 | IEEE Standard Glossary of Software Engineering Terminology | IEEE | 1990 (referencia estandar) | Definiciones dato, informacion, sistema de informacion | IEEE Std 610.12-1990 |
| ISO-2382 | ISO/IEC 2382 — Information technology — Vocabulary | ISO/IEC | 2015 (vigente) | Definiciones formales: dato, informacion, sistema de informacion, hardware, software | iso.org/standard/63598.html |
| ISO-11179 | ISO/IEC 11179 — Metadata Registries | ISO/IEC | 2015-2024 (multi-parte) | Metadatos (seccion 1.6) | iso.org/standard/35342.html |
| ISO-8000 | ISO 8000 — Data Quality | ISO | 2009-2022 (multi-parte) | Calidad del dato (seccion 1.5) | iso.org/standard/50798.html |
| STALLINGS-COA | Computer Organization and Architecture (11th ed.) — William Stallings | Pearson | 2018 | Cap. 1-4: Arquitectura Von Neumann, Harvard, CPU, buses, registros, ALU, ciclo instruccion. Cap. 12-15: pipelining, RISC, cache. Cap. 13: modos direccionamiento | ISBN 978-0134997193 |
| TANENBAUM-SO | Structured Computer Organization (6th ed.) — Andrew Tanenbaum | Pearson | 2012 | Cap. 1-2: Generaciones de ordenadores, niveles de organizacion. Cap. 3: memoria virtual | ISBN 978-0132916523 |
| PATTERSON-HENNESSY | Computer Organization and Design: The Hardware/Software Interface (6th ed.) — Patterson & Hennessy | Morgan Kaufmann | 2020 | Pipelining, RISC-V, arquitectura moderna | ISBN 978-0128200643 |
| INTEL-SDM | Intel 64 and IA-32 Architectures Software Developer's Manual | Intel Corp. | 2024 (actualizado periodicamente) | Vol. 1 Cap. 3: Registros FLAGS/EFLAGS/RFLAGS, modos direccionamiento, CISC x86 | intel.com/sdm |
| ARM-ARM | ARM Architecture Reference Manual (ARMv9-A) | ARM Holdings | 2024 | Arquitectura RISC moderna, registros APSR, modos direccionamiento ARM | developer.arm.com/documentation |
| JEDEC-DDR | JEDEC Standards for DDR Memory (DDR4 JESD79-4, DDR5 JESD79-5) | JEDEC | DDR4: 2012 / DDR5: 2020, rev 2024 | Especificaciones DDR1-DDR5, pines, frecuencias, voltajes, ancho de banda | jedec.org |
| IEEE-754 | IEEE Standard for Floating-Point Arithmetic | IEEE | 1985 (original) / 2019 (actual) | Representacion de numeros reales en coma flotante (seccion 8.3) | IEEE Std 754-2019 |
| UNICODE-STD | The Unicode Standard, Version 15.1 | Unicode Consortium | 2023 | Cap. 2-3: UTF-8, UTF-16, UTF-32, BOM, normalizacion NFC/NFD, code points | unicode.org/versions/Unicode15.1.0 |
| ISO-10646 | ISO/IEC 10646 — Universal Coded Character Set | ISO/IEC | 2020 | Repertorio de caracteres equivalente a Unicode | iso.org/standard/76835.html |
| RFC-20 | ASCII format for Network Interchange | IETF | 1969 (vigente, estandar historico) | Tabla ASCII 7 bits, caracteres control | tools.ietf.org/html/rfc20 |
| UEFI-SPEC | UEFI Specification 2.10 | UEFI Forum | 2022 | Sec. 1-2: Diferencias BIOS/UEFI, Secure Boot, GPT, TPM 2.0 | uefi.org/specifications |
| ENS-RD311 | Esquema Nacional de Seguridad (Real Decreto 311/2022) | BOE | 2022 | Triada CIA, categorias de sistemas | boe.es/buscar/doc.php?id=BOE-A-2022-7191 |
| RGPD | Reglamento (UE) 2016/679 — Proteccion de datos | DOUE | 2016 (aplicacion 2018) | Proteccion de datos personales, ciclo de vida | eur-lex.europa.eu/eli/reg/2016/679 |
| METRICA-V3 | Metodologia MAP Metrica Version 3 | Ministerio AP | 2001 (vigente en pliegos) | Metodologia oficial desarrollo SI administracion publica | administracionelectronica.gob.es |

## Fuentes Tier 2 (secundarias — contraste)

| ID | Titulo | Origen | Uso |
|---|---|---|---|
| FORO-OPOS-T11 | Tema 11 existente (Test_Prompting/Tema 11.docx) | Foro Opositores / Material previo | Patron de profundidad y enfoque C1. Base de contenido a reestructurar y verificar |
| MDN-CHARSET | MDN Web Docs — Character encodings | Mozilla | Referencia rapida UTF-8 vs ASCII extendido |
| KINGSTON-RAM | Kingston Technology — Understanding RAM | Kingston | Tablas DDR comparativas, formato divulgativo verificable |
| LAUDON-MIS | Management Information Systems (17th ed.) — Kenneth Laudon | Pearson | 2021 | Clasificacion TPS/MIS/DSS/EIS, ERP, CRM |
| ACKOFF-DIKW | From Data to Wisdom — Russell Ackoff | Journal of Applied Systems Analysis | 1989 | Origen del modelo DIKW (seccion 1.3) |
| KAPLAN-BSC | The Balanced Scorecard — Kaplan & Norton | Harvard Business Review | 1992 | Cuadro de Mando Integral (seccion 2.8) |
| DATOS-MADRID | Portal Open Data Ayuntamiento de Madrid | Ayto. Madrid | Ejemplo real metadatos DCAT-AP-ES (seccion 1.6) | datos.madrid.es |
| IDC-DATA-SPHERE | IDC Global DataSphere Forecast | IDC | 2024 | Volumenes globales de datos (seccion 7.2) |

## Fuentes Tier 3 — NO utilizadas

- Wikipedia (consultada para orientacion, NO citada)
- Blogs tecnicos, Medium, Dev.to
- Contenido generado por IA sin fuente verificable
- Documentacion de consumo masivo no tecnica (Xataka, etc.)

---

## Nuevas fuentes anadidas en v2.0 (respecto a v1.0)

| Fuente | Motivo |
|---|---|
| ISO-11179 | Nueva seccion 1.6 sobre metadatos |
| ISO-8000 | Nueva seccion 1.5 sobre calidad del dato |
| PATTERSON-HENNESSY | Nueva seccion 5.2.4 sobre pipelining |
| ARM-ARM | Referencia RISC moderna (seccion 5.2) |
| IEEE-754 | Nueva seccion 8.3 sobre coma flotante |
| ISO-10646 | Nueva seccion 9.8 |
| ENS-RD311 | Referencia explicita triada CIA (seccion 2.3) |
| RGPD | Ciclo de vida del dato (seccion 1.4) |
| METRICA-V3 | Seccion 2.9 metodologias |
| LAUDON-MIS | Ampliacion clasificacion SI |
| ACKOFF-DIKW | Origen piramide DIKW |
| KAPLAN-BSC | Origen Cuadro de Mando Integral |
| DATOS-MADRID | Ejemplo real Ayto Madrid |
| IDC-DATA-SPHERE | Cifras contextuales (seccion 7.2) |

---

## Notas de validacion

- [ ] Maria/Ana revisa correspondencia contenido <> fuentes Tier 1
- [ ] Verificar que tablas DDR coinciden con specs JEDEC JESD79-5 actuales (DDR5)
- [ ] Confirmar que el nivel de profundidad es adecuado para C1 tras ampliacion pipelining/FLAGS
- [ ] Contrastar generaciones de ordenadores con Tanenbaum cap. 1 (6ª generacion tratada como extension moderna)
- [ ] Verificar vigencia del Real Decreto 311/2022 (ENS) y del RGPD/LOPDGDD
- [ ] Validar referencia Metrica v3 aplicada al pliego del Ayto Madrid
