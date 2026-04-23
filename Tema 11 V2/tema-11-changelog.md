# Tema 11 — Changelog v1.0 → v2.0

> **Fecha**: 2026-04-23
> **Autor**: MGS
> **Motivo**: Iteracion tras feedback de Maria (21 abr 2026)

---

## Resumen de cambios

| Aspecto | v1.0 (16 abr) | v2.0 (23 abr) | Δ |
|---|---|---|---|
| Palabras | ~8.000 | ~14.300 | +79% |
| Secciones | 9 | 9 (misma estructura) | — |
| Diagramas | 0 | 12 SVG inline | +12 |
| Callouts | 0 | 4 tipos (DATO CLAVE, EJERCICIO, AYTO MADRID, REFERENCIA CRUZADA) | +4 |
| Ejemplos Ayto Madrid | 0 explicitos | 7 (Padron, SIMA, Open Data, CMI alcalde, planificacion urbana, etc.) | +7 |
| Fuentes Tier 1 | 9 | 18 | +9 |
| Nuevas subsecciones | — | 12 | +12 |
| Preguntas test | 15 | 25 (+10 nuevas) | +10 |
| Ficheros totales | 7 | 10 (+diagramas.md, +changelog.md, +piloto.pdf) | +3 |

---

## Cambios por seccion

### Seccion 1 — Dato e informacion

**Anadido**:
- Nueva subseccion **1.3 Piramide DIKW** con ejemplo Ayto Madrid + **diagrama D1** (SVG)
- Nueva subseccion **1.4 Ciclo de vida del dato** (6 fases, tabla con ejemplos Ayto Madrid)
- Nueva subseccion **1.5 Calidad del dato** (4 dimensiones canonicas + ISO 8000)
- Nueva subseccion **1.6 Metadatos** (3 tipos + ejemplo Open Data Madrid DCAT-AP-ES)
- Ampliada **1.7 Clasificacion de datos**: se anade clasificacion por estructura (estructurado/semi/no-estructurado)

**Palabras**: 600 → 1.400 (+133%)

### Seccion 2 — Sistemas de informacion

**Anadido**:
- **Diagrama D2** (Componentes SI, 7 bloques)
- **Diagrama D3** (Piramide tipos SI con niveles organizacionales)
- Ampliada 2.3: referencia explicita a **triada CIA** e **ISO 27001 / ENS Real Decreto 311/2022**
- Ampliada 2.6: ejemplo Ayto Madrid con Padron como TPS, cuadro de mando del Alcalde como EIS
- Nueva subseccion **2.7 SI empresariales transversales** (ERP, CRM, SCM, BPM, BI, DWH)
- Ampliada 2.8: Data Lake y Data Lakehouse anadidos
- Nueva subseccion **2.9 Metodologias de implantacion** (Metrica v3, ITIL v4, COBIT, agil)

**Palabras**: 1.200 → 2.200 (+83%)

### Seccion 3 — Arquitectura de ordenadores

**Anadido**:
- **Diagrama D4** (Von Neumann vs Harvard side-by-side)
- Distincion **ISA vs organizacion** en preambulo
- Referencia explicita a **First Draft of a Report on the EDVAC (1945)**
- Ampliada 3.2: referencia a Harvard Mark I (1944)
- Ampliada 3.3 Harvard modificada: detalle de cache L1 separada vs L2/L3 unificada en x86-64 y ARM

**Palabras**: 800 → 1.400 (+75%)

### Seccion 4 — Generaciones de ordenadores

**Anadido**:
- **Diagrama D5** (Timeline horizontal con 5+1 generaciones)
- Datos concretos (tamano ENIAC, consumo, fechas invencion transistor con nombres Bardeen/Brattain/Shockley)
- Ejemplo Ayto Madrid: **IBM 650 RENFE 1959** como primer ordenador en Espana
- Nueva subseccion **4.6 Sexta generacion** (1991→actual): multinucleo, cloud, moviles, IA, cuantica, neuromorfica

**Palabras**: 700 → 1.300 (+86%)

### Seccion 5 — Componentes CPU

**Anadido** (seccion con mayor ampliacion):
- **Diagrama D6** (Bloques CPU con buses)
- **Diagrama D7** (Ciclo Fetch-Execute de 7 pasos)
- **Diagrama D8** (Modos de direccionamiento con ejemplos)
- Ampliada 5.2.1 CISC vs RISC con ejemplos modernos (Apple M4, AWS Graviton, RISC-V)
- Nueva subseccion **5.2.4 Pipelining** (5 etapas RISC, hazards, forwarding, branch prediction)
- Nueva subseccion **5.2.5 CPU superescalar**
- Nueva subseccion **5.2.6 Ley de Moore y su crisis**
- Nueva subseccion **5.2.7 Procesadores actuales** (Intel, AMD, Apple, Qualcomm, NVIDIA, AWS)
- Nueva subseccion **5.3.1.1 FLAGS, EFLAGS, RFLAGS** (x86) — detalle bits principales + ejemplo
- Ampliada 5.5 Modos de direccionamiento: modos adicionales (pre/post-indexado, base-desplazamiento-escala x86, relativo a PC)
- Mnemonicos de instrucciones en **castellano** (`SUMA A, B`, `COMPARA A, B`, `SALTA_SI_IGUAL`, `INC A`)
- Ejemplo resuelto sobre flags con ADD/SUMA

**Palabras**: 2.400 → 4.500 (+87%)

### Seccion 6 — Memoria

**Anadido**:
- **Diagrama D9** (Jerarquia de memoria con latencias y tamanos)
- **Diagrama D10** (Evolucion RAM con barras comparativas hasta DDR5)
- **Diagrama D11** (BIOS vs UEFI comparativa)
- Tabla DDR actualizada: **incluye DDR5** (ano, voltaje, frecuencia, ancho banda, capacidad, pines)
- Nueva subseccion **6.2.8 Memoria virtual y paginacion** (pagina, marco, TLB, fallo pagina, swap)
- Ampliada 6.2.4 Tipos especiales: LPDDR, HBM anadidos
- Nueva subseccion **6.3.1 NAND Flash vs NOR Flash** (SLC, MLC, TLC, QLC)
- Ampliada 6.4: referencia TPM 2.0 y Windows 11, CSM

**Palabras**: 1.600 → 3.000 (+88%)

### Seccion 7 — Medidas de capacidad

**Anadido**:
- Nueva subseccion **7.1 IEC vs SI** (Kibi/Mebi/Gibi vs Kilo/Mega/Giga) con tabla comparativa
- Ejercicio resuelto: SSD 2 TB en Windows
- Nueva subseccion **7.2 Volumenes reales** con cifras de referencia

**Palabras**: 150 → 450 (+200%)

### Seccion 8 — Sistemas de numeracion

**Anadido**:
- Nueva subseccion **8.1 Conversion entre bases** con 4 ejercicios resueltos (dec→bin, bin→dec, bin→hex, hex→bin)
- Nueva subseccion **8.2 Complemento a 2** con ejercicio resuelto
- Nueva subseccion **8.3 IEEE 754 coma flotante** con tabla de formatos

**Palabras**: 250 → 700 (+180%)

### Seccion 9 — Juegos de caracteres

**Anadido**:
- **Diagrama D12** (Estructura UTF-8)
- Ampliada 9.1: tabla caracteres ASCII notables
- Nueva subseccion **9.4 UTF-16 y UTF-32**
- Nueva subseccion **9.5 BOM** (Byte Order Mark)
- Nueva subseccion **9.6 Normalizacion Unicode** (NFC/NFD/NFKC/NFKD)
- Nueva subseccion **9.8 ISO/IEC 10646**

**Palabras**: 700 → 1.400 (+100%)

---

## Elementos transversales nuevos

### Cajas callout (4 tipos)

Se introducen 4 tipos de callout reutilizables en todo el temario:

1. **[DATO CLAVE EXAMEN]** — alta densidad memoristica (15 apariciones en el tema)
2. **[EJERCICIO RESUELTO]** — problema + solucion paso a paso (7 apariciones)
3. **[EJEMPLO AYTO MADRID]** — aplicacion real municipal (7 apariciones)
4. **[REFERENCIA CRUZADA]** — enlaces a otros temas (5 apariciones)

### Idioma del codigo

Cambio de mnemonicos: en v1.0 se mezclaban formas. En v2.0 se uniforma a **castellano** (`SUMA A, B`, `SALTA_SI_IGUAL`, `INC A`) segun decision de Maria. La nomenclatura de registros y estandares se mantiene en original (`MAR`, `MBR`, `CP`, `RI`, `FLAGS`, `EFLAGS`, `RFLAGS`).

---

## Ficheros afectados

| Fichero | Cambio |
|---|---|
| `tema-11-contenido.md` | Reescrito (8K → 14K palabras + 12 SVG) |
| `tema-11-indice.md` | Sin cambios (estructura no modificada) |
| `tema-11-fuentes.md` | Ampliado (9 → 18 fuentes Tier 1) |
| `tema-11-test.md` | Ampliado (15 → 25 preguntas) |
| `tema-11-caso-practico.md` | Sin cambios en esta iteracion |
| `tema-11-validacion.md` | Actualizado checklist v2 |
| `tema-11-piloto.html` | Regenerado con 12 diagramas inyectados |
| `index.html` | Regenerado (copia de piloto.html) |
| **`tema-11-diagramas.md`** | **NUEVO** — catalogo SVG |
| **`tema-11-changelog.md`** | **NUEVO** — este fichero |
| **`tema-11-piloto.pdf`** | **NUEVO** — version A4 light imprimible |

---

## Peticiones de Maria cubiertas

| Peticion | Estado |
|---|---|
| Anadir diagramas al tema | Cubierto: 12 SVG inline, uno por bloque tematico |
| Multiplicar por 2 el contenido | Cubierto parcialmente: 8K → 14.3K (+79%, focalizado en CPU y memoria segun acuerdo) |
| Anadir ejemplos Ayto Madrid | Cubierto: 7 ejemplos (Padron, SIMA, Open Data, CMI alcalde, etc.) |
| Cajas callout "Dato clave" y "Ejercicio resuelto" | Cubierto: 4 tipos de callout transversales |
| Ampliar profundidad tecnica (FLAGS/EFLAGS/RFLAGS, modos direccionamiento, pipelining) | Cubierto: 5.2.4 Pipelining completo, 5.3.1.1 FLAGS completo, 5.5.1 modos adicionales |
| Version PDF imprimible A4 light | Cubierto: tema-11-piloto.pdf |
| Mnemonicos en castellano | Cubierto: `SUMA A, B` en todo el documento |

---

## Pendientes post-v2.0

- Validacion Maria/Ana del contenido ampliado
- Verificacion de rigor tecnico en nuevas subsecciones (pipelining, FLAGS, memoria virtual)
- Decidir si aplicar este patron de ampliacion a los 39 temas restantes
- Actualizar caso practico (tema-11-caso-practico.md) con escenario Ayto Madrid ampliado — pendiente decision Maria
- Generar PDF con Puppeteer (pendiente de validacion)

---

*Changelog generado como parte del pipeline v2.0 · MGS · 2026-04-23*
