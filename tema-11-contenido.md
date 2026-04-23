# Tema 11 — Contenido Teorico

> **Titulo oficial**: Informatica basica. Representacion y comunicacion de la informacion: elementos constitutivos de un sistema de informacion. Caracteristicas y funciones. Arquitectura de ordenadores. Componentes internos de los equipos microinformaticos.
>
> **Bloque**: Parte II — Tecnico
> **Nivel**: C1 — Tecnico Auxiliar TIC, Ayuntamiento de Madrid
> **Version**: 2.0 — Pendiente validacion
> **Fecha generacion**: 2026-04-23
> **Fuentes**: Ver tema-11-fuentes.md · **Diagramas**: Ver tema-11-diagramas.md · **Cambios**: Ver tema-11-changelog.md
>
> *Extension: ~16.000 palabras · 12 diagramas SVG embebidos · 4 tipos de callout transversales*

---

## Convenciones del documento

Este tema incluye cuatro tipos de **cajas callout** para facilitar el estudio:

> **[DATO CLAVE EXAMEN]** Informacion de alta densidad memoristica, con alta probabilidad de aparecer en el test oficial.

> **[EJERCICIO RESUELTO]** Problema + solucion paso a paso. Util para secciones con calculos.

> **[EJEMPLO AYTO MADRID]** Aplicacion real de la teoria al entorno municipal (SIMA, Padron, sede electronica, Portal del ciudadano).

> **[REFERENCIA CRUZADA]** Enlace conceptual a otros temas del temario oficial.

Los mnemonicos de instrucciones maquina se muestran en **castellano** (`SUMA A, B`). Los registros, estandares y productos se mantienen en su nomenclatura original (CP, MAR, FLAGS, DDR5...). Las fuentes se referencian con etiquetas breves tipo `[STALLINGS-COA, Cap. 2]` — el registro completo esta en `tema-11-fuentes.md`.

---

## 1. Concepto de dato e informacion

### 1.1. Definicion de dato

Un **dato** es una representacion simbolica (numerica, alfabetica, alfanumerica) de un atributo o variable cuantitativa o cualitativa. Los datos describen hechos empiricos, sucesos y entidades. [ISO-2382]

Los datos constituyen la **minima unidad semantica** y se corresponden con elementos primarios de informacion que, por si solos, son **irrelevantes**: no contienen significado contextual ni orientan la toma de decisiones. Un dato aislado es un simbolo sin significado atribuido.

> **Ejemplo**: El valor "42" es un dato. Por si solo no aporta informacion util: podria ser una edad, un peso, un numero de aula, la respuesta a la vida.

### 1.2. Definicion de informacion

La **informacion** es el resultado de procesar, contextualizar y organizar datos, de modo que adquieren significado util para el receptor y permiten la toma de decisiones. [ISO-2382]

> **Ejemplo**: "42 aprobados de 90 presentados" es informacion — aporta contexto (cuantificador "aprobados", poblacion "de 90 presentados") y utilidad (permite calcular el 46,7% de aprobados).

La informacion debe cumplir dos requisitos fundamentales:

- **Integridad**: todos los datos necesarios estan disponibles para que la informacion sea completa.
- **Inequivocidad**: no se generan dudas sobre su significado; una sola interpretacion es posible.

Adicionalmente, para que la informacion sea util debe ser: **relevante** (aporta valor para la decision), **precisa** (coincide con la realidad), **completa** (no omite elementos necesarios) y **adecuada** (llega al usuario correcto en el momento correcto).

**Formula conceptual**:

```
Informacion = Datos + Contexto (anadir valor) + Utilidad (disminuir la incertidumbre)
```

### 1.3. Piramide DIKW: dato, informacion, conocimiento, sabiduria

La clasificacion tradicional en informatica opera sobre dato e informacion, pero la literatura sobre gestion del conocimiento anade dos niveles superiores: **conocimiento** y **sabiduria**. El modelo resultante se conoce como **piramide DIKW** (Data-Information-Knowledge-Wisdom), atribuida a Russell Ackoff (1989) y ampliamente adoptada por organismos como la ONU y la OCDE para documentar sus sistemas de gestion del conocimiento.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 600 340" role="img" aria-label="Piramide DIKW con ejemplo Ayto Madrid">
  <style>
    .dikw-label{font:600 14px system-ui,sans-serif;fill:#fff}
    .dikw-example{font:12px system-ui,sans-serif;fill:#1a1a1a}
    .dikw-title{font:700 13px system-ui,sans-serif;fill:#0055a0;text-transform:uppercase;letter-spacing:1px}
  </style>
  <polygon points="280,30 330,30 345,70 265,70" fill="#003d73"/>
  <polygon points="265,70 345,70 365,120 245,120" fill="#0055a0"/>
  <polygon points="245,120 365,120 390,180 220,180" fill="#3378b9"/>
  <polygon points="220,180 390,180 420,250 190,250" fill="#6ea3d2"/>
  <text x="305" y="56" text-anchor="middle" class="dikw-label">Sabiduria</text>
  <text x="305" y="99" text-anchor="middle" class="dikw-label">Conocimiento</text>
  <text x="305" y="155" text-anchor="middle" class="dikw-label">Informacion</text>
  <text x="305" y="220" text-anchor="middle" class="dikw-label">Dato</text>
  <line x1="420" y1="50" x2="470" y2="50" stroke="#0055a0" stroke-width="1"/>
  <line x1="420" y1="99" x2="470" y2="99" stroke="#0055a0" stroke-width="1"/>
  <line x1="420" y1="155" x2="470" y2="155" stroke="#0055a0" stroke-width="1"/>
  <line x1="420" y1="220" x2="470" y2="220" stroke="#0055a0" stroke-width="1"/>
  <text x="480" y="40" class="dikw-title">Decision</text>
  <text x="480" y="55" class="dikw-example">"subir el IBI?"</text>
  <text x="480" y="94" class="dikw-title">Tendencia</text>
  <text x="480" y="109" class="dikw-example">"crece la poblacion"</text>
  <text x="480" y="150" class="dikw-title">Contexto</text>
  <text x="480" y="165" class="dikw-example">"3,45 M habitantes"</text>
  <text x="480" y="215" class="dikw-title">Bruto</text>
  <text x="480" y="230" class="dikw-example">"3.450.000"</text>
  <text x="305" y="285" text-anchor="middle" font="italic 11px system-ui,sans-serif" fill="#666">+ contexto, + analisis, + experiencia</text>
</svg>

Los cuatro niveles responden a preguntas distintas:

1. **Dato** — responde a *¿que hay?*: hechos brutos, sin procesar, sin juicio.
2. **Informacion** — responde a *¿que es?*: datos contextualizados, con quien/cuando/donde.
3. **Conocimiento** — responde a *¿como funciona?*: patrones, relaciones, correlaciones.
4. **Sabiduria** — responde a *¿que hacemos?*: decisiones fundamentadas, principios de accion.

> **[EJEMPLO AYTO MADRID]** Aplicado al **Padron Municipal**: el valor "3.450.000" es dato; "3.450.000 habitantes empadronados a 31-12-2025" es informacion; "la poblacion crece al 0,8% anual y envejece" es conocimiento; "hay que reforzar los servicios sociales en distritos envejecidos" es sabiduria (decision).

### 1.4. Ciclo de vida del dato

Un dato no es un objeto estatico: nace, se transforma, se almacena, se usa y en algun momento se archiva o elimina. El **ciclo de vida del dato** (Data Lifecycle Management, DLM) estructura estas etapas para garantizar gobernanza, trazabilidad y cumplimiento normativo.

Las **seis fases canonicas** del ciclo de vida son:

| Fase | Accion | Ejemplo Ayto Madrid |
|---|---|---|
| **1. Captura** | Adquisicion desde la fuente | Alta en Padron (formulario presencial o online) |
| **2. Almacenamiento** | Persistencia en sistema controlado | Base de datos corporativa (Oracle, PostgreSQL) |
| **3. Procesamiento** | Transformacion, limpieza, calculos | Calculo del porcentaje de empadronados por distrito |
| **4. Uso** | Explotacion por usuarios/aplicaciones | Portal del ciudadano, Informes estadisticos |
| **5. Publicacion/Comunicacion** | Distribucion controlada | Open Data Madrid, boletines, web municipal |
| **6. Archivo o eliminacion** | Retencion legal o destruccion segura | Archivo historico (5 años) o borrado RGPD |

El ciclo incluye puntos de control transversales: **seguridad** (cifrado, control acceso), **calidad** (validacion, depuracion), **metadatos** (descripcion del dato) y **cumplimiento** (RGPD, LOPDGDD, ENS).

### 1.5. Calidad del dato

Un dato tecnicamente correcto pero de baja calidad puede generar informacion enganosa y decisiones incorrectas. Las **cuatro dimensiones canonicas de calidad del dato** son:

- **Exactitud** (*accuracy*): el dato refleja fielmente la realidad. Un NIF erroneo en Padron tiene exactitud cero.
- **Completitud** (*completeness*): no faltan atributos obligatorios. Un registro de ciudadano sin fecha de nacimiento esta incompleto.
- **Consistencia** (*consistency*): el mismo dato tiene el mismo valor en todos los sistemas. Si en Padron figura "Juan Perez" y en Tributos "J. Perez", hay inconsistencia.
- **Oportunidad** (*timeliness*): el dato esta actualizado en el momento en que se usa. Una direccion desactualizada provoca notificaciones no entregadas.

Normas adicionales como **ISO 8000** (Data Quality) amplian estas a 10-14 dimensiones (unicidad, validez, precision, plausibilidad, etc.), usadas en auditorias de calidad masivas.

> **[DATO CLAVE EXAMEN]** Las 4 dimensiones minimas de calidad del dato son: **exactitud, completitud, consistencia y oportunidad**. ISO 8000 amplia a 10+ dimensiones.

### 1.6. Metadatos

Los **metadatos** son "datos sobre los datos": describen el contexto, contenido y estructura de un dato. Sin metadatos, un conjunto de datos es una secuencia de numeros sin significado documentado. [ISO-11179]

Tres tipos principales:

- **Metadatos descriptivos**: identifican y describen el dato (titulo, autor, palabras clave). Ej: autor del dataset del Padron, fecha de ultima actualizacion.
- **Metadatos estructurales**: describen como se organiza el dato (relaciones, campos, tipos). Ej: esquema de tabla SQL, definicion XML/JSON Schema.
- **Metadatos administrativos**: gobiernan el uso, retencion y acceso (permisos, copyright, fechas). Ej: nivel ENS, clasificacion RGPD, retencion legal.

> **[EJEMPLO AYTO MADRID]** En el portal **Open Data Madrid** (datos.madrid.es) cada dataset incluye metadatos estandarizados segun **DCAT-AP-ES**: titulo, descripcion, fecha publicacion, frecuencia actualizacion, licencia (CC-BY 4.0), responsable del dato, formato (CSV, JSON, XML).

### 1.7. Clasificacion de datos

La clasificacion de los datos en informatica no responde a un unico criterio. Las clasificaciones son complementarias, no excluyentes.

**Segun su funcion en el sistema de informacion** (la mas relevante para el examen):

| Tipo | Descripcion | Origen/Destino |
|---|---|---|
| **Datos de entrada** | Se introducen en el sistema para su tratamiento | Usuarios o dispositivos de entrada (teclado, escaner, sensores) |
| **Datos intermedios** | Se generan durante el procesamiento | Memoria de trabajo, no visibles al usuario final |
| **Datos de salida** | Resultado final del procesamiento | Dispositivos de salida (pantalla, impresora, fichero) |

**Segun su naturaleza**:

- **Datos numericos**: representan cantidades, permiten operaciones matematicas. Subtipos: enteros, reales, complejos.
- **Datos alfabeticos**: formados exclusivamente por letras.
- **Datos alfanumericos**: combinan letras, numeros y otros caracteres (el caso mas comun en la practica).
- **Datos logicos/booleanos**: dos valores posibles (verdadero/falso, 1/0).
- **Datos multimedia**: imagenes, audio, video.

**Segun su variabilidad**:

- **Datos fijos o constantes**: su valor no cambia durante la ejecucion (π, velocidad de la luz).
- **Datos variables**: pueden modificarse durante el proceso.

**Segun su estructura**:

- **Datos estructurados**: tablas con esquema fijo (BBDD relacionales).
- **Datos semi-estructurados**: estructura parcial, autodescriptivos (XML, JSON).
- **Datos no estructurados**: sin esquema predefinido (documentos, emails, imagenes).

> **[REFERENCIA CRUZADA]** La clasificacion de datos conecta con el Tema 15 (Bases de datos) — modelo relacional frente a NoSQL — y con el Tema 20 (Sistemas operativos) — gestion de ficheros y dispositivos de E/S.

---

## 2. Sistemas de informacion

### 2.1. Definicion y concepto

Un **sistema de informacion** (SI) es un conjunto de elementos (aplicaciones, maquinaria, usuarios, procedimientos) disenado para el tratamiento de informacion, de manera que esta quede disponible de forma eficiente para su uso posterior. [ISO-2382]

Los sistemas de informacion ayudan a administrar, recolectar, recuperar, procesar, almacenar y distribuir informacion relevante para los procesos de una organizacion, ya sea una empresa privada, una administracion publica o una entidad del tercer sector.

> **Nota importante**: El termino "sistema de informacion" **no es sinonimo** de "sistema informatico". Un sistema de informacion no requiere necesariamente componentes informaticos, aunque en la practica la mayoria los incorporan. Un archivador fisico con fichas de papel es un sistema de informacion perfectamente valido. Los sistemas de informacion informatizados son un subconjunto del conjunto general.

### 2.2. Componentes basicos de un SI

Los sistemas de informacion se componen de tres partes principales: **personas, procesos de negocio y tecnologias de la informacion**. Desglosados en siete componentes estructurales:

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 360" role="img" aria-label="Componentes del sistema de informacion">
  <style>
    .si-tech{fill:#d6e4f0;stroke:#0055a0;stroke-width:1.5}
    .si-human{fill:#f0e4d6;stroke:#e89822;stroke-width:1.5}
    .si-flow{fill:#d8f0dc;stroke:#2d8659;stroke-width:1.5}
    .si-label{font:600 13px system-ui,sans-serif;fill:#1a1a1a;text-anchor:middle}
    .si-sub{font:11px system-ui,sans-serif;fill:#555;text-anchor:middle}
  </style>
  <text x="320" y="28" class="si-label" font-size="16" fill="#0055a0">Sistema de Informacion</text>
  <text x="320" y="45" class="si-sub">7 componentes estructurales [ISO-2382]</text>
  <rect x="40" y="70" width="150" height="60" rx="6" class="si-tech"/>
  <text x="115" y="94" class="si-label">Hardware</text>
  <text x="115" y="112" class="si-sub">CPU, memoria, E/S</text>
  <rect x="245" y="70" width="150" height="60" rx="6" class="si-tech"/>
  <text x="320" y="94" class="si-label">Software</text>
  <text x="320" y="112" class="si-sub">SO, aplicaciones</text>
  <rect x="450" y="70" width="150" height="60" rx="6" class="si-tech"/>
  <text x="525" y="94" class="si-label">Datos</text>
  <text x="525" y="112" class="si-sub">BBDD, ficheros</text>
  <rect x="90" y="160" width="200" height="60" rx="6" class="si-flow"/>
  <text x="190" y="184" class="si-label">Red</text>
  <text x="190" y="202" class="si-sub">LAN, WAN, Internet</text>
  <rect x="350" y="160" width="200" height="60" rx="6" class="si-flow"/>
  <text x="450" y="184" class="si-label">Retroalimentacion</text>
  <text x="450" y="202" class="si-sub">mejora continua</text>
  <rect x="140" y="250" width="160" height="60" rx="6" class="si-human"/>
  <text x="220" y="274" class="si-label">Procedimientos</text>
  <text x="220" y="292" class="si-sub">reglas, politicas</text>
  <rect x="340" y="250" width="160" height="60" rx="6" class="si-human"/>
  <text x="420" y="274" class="si-label">Usuarios</text>
  <text x="420" y="292" class="si-sub">operadores, decisores</text>
</svg>

| Componente | Descripcion |
|---|---|
| **Hardware** | Tecnologia de almacenamiento, comunicaciones, entradas y salidas de datos. |
| **Software** | Aplicaciones destinadas a recoger, almacenar, procesar y analizar datos. |
| **Datos** | Porciones de informacion donde reside el valor del sistema. |
| **Procedimientos** | Politicas y reglas de negocio aplicables a los procesos de la organizacion. |
| **Usuarios** | Personas que interactuan con la informacion — componente decisivo para el exito. |
| **Red** | Infraestructura que permite compartir recursos entre dispositivos. |
| **Retroalimentacion** | Base para la mejora continua del sistema. |

### 2.3. Caracteristicas de un sistema de informacion

Para que un sistema de informacion sea considerado como tal, debe cumplir las siguientes **diez caracteristicas**:

1. **Disponibilidad** de la informacion cuando se precise y a traves del medio requerido.
2. **Seleccion adecuada**, evitando sobrecarga o informacion irrelevante.
3. **Adaptacion y personalizacion** en la presentacion, segun el usuario o contexto.
4. **Capacidad de relacion** entre datos o contenidos, facilitando su interpretacion.
5. **Tiempos de respuesta adecuados**, garantizando eficiencia.
6. **Exactitud y calidad** de los datos, asegurando informacion veraz y actualizada.
7. **Flexibilidad**, permitiendo adaptacion a nuevas necesidades.
8. **Fiabilidad**, garantizando funcionamiento correcto y continuo.
9. **Seguridad**, protegiendo la informacion (**confidencialidad, integridad y disponibilidad** — CIA).
10. **Copias de seguridad** periodicas para recuperacion ante fallos.

> **[DATO CLAVE EXAMEN]** La **triada CIA** (Confidencialidad, Integridad, Disponibilidad) es el principio fundamental de seguridad de la informacion, recogido en **ISO 27001** y en el **Esquema Nacional de Seguridad** (Real Decreto 311/2022, ENS).

### 2.4. Elementos funcionales

Un sistema de informacion estandar se estructura en los siguientes elementos:

- **Base de datos**: almacena toda la informacion requerida para la toma de decisiones. La informacion se organiza en registros especificos e identificables.
- **Transacciones**: elementos de interfaz que permiten al usuario consultar, agregar, modificar o eliminar registros.
- **Informes**: elementos mediante los cuales el usuario obtiene registros o informacion estadistica (contar, sumar) segun criterios de busqueda definidos.
- **Procesos**: elementos que, segun una logica predefinida, obtienen informacion de la base de datos y generan nuevos registros.
- **Usuario**: todas las personas que interactuan con el sistema, desde el nivel ejecutivo hasta el operativo.
- **Procedimientos administrativos**: reglas y politicas que rigen el comportamiento de los usuarios frente al sistema. Nunca un usuario tiene acceso directo a la base de datos; siempre a traves de transacciones autorizadas.

**Modulos funcionales internos**:

| Modulo | Funcion |
|---|---|
| Definicion del SI | Define la estructura de las bases de datos y formatos de documentos |
| Entrada | Dota al SI de elementos de entrada adecuados a la informacion |
| Analisis | Aplica algoritmos para procesar datos y obtener informacion |
| Busqueda | Gestiona las fuentes para busquedas coordinadas y sencillas |
| Difusion | Notificaciones de informacion relevante a los usuarios |
| Evaluacion | Recopila estadisticas y opiniones para mejora del SI |

### 2.5. Funciones principales del SI

La funcion principal de un SI es **ofrecer informacion relevante, eliminando datos superfluos**, filtrada y ordenada para busquedas eficientes.

Se distinguen **cuatro funciones basicas** (regla nemotecnica: **EAPS** — Entrada, Almacenamiento, Procesamiento, Salida):

1. **Entrada de informacion**: proceso mediante el cual el SI toma los datos a procesar. Las entradas pueden ser **manuales** (proporcionadas por el usuario) o **automaticas** (procedentes de otros sistemas mediante interfaces automaticas, APIs, EDI).

2. **Almacenamiento de informacion**: capacidad del sistema para recordar la informacion guardada, tanto en memoria principal como en memoria secundaria. Es una de las funciones mas importantes.

3. **Procesamiento de informacion**: capacidad para efectuar calculos segun una secuencia de operaciones preestablecida. Permite la transformacion de datos fuente en informacion util para la toma de decisiones.

4. **Salida de informacion**: capacidad para sacar la informacion procesada al exterior. La salida de un SI puede constituir la entrada a otro SI (integracion).

### 2.6. Tipos de sistemas de informacion

**Clasificacion generica** (Laudon, 2017):

- **Sistemas competitivos**: orientados a ventaja competitiva (ej. sistemas de precios dinamicos).
- **Sistemas cooperativos**: soportan trabajo colaborativo (ej. Microsoft Teams, Google Workspace).
- **Sistemas que modifican el estilo de operacion del negocio**: transformacion digital.

**Clasificacion por nivel organizacional** (la **mas relevante** para examen):

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 600 340" role="img" aria-label="Piramide de tipos de sistemas de informacion">
  <style>
    .tps-eis{font:700 14px system-ui,sans-serif;fill:#fff;text-anchor:middle}
    .tps-user{font:11px system-ui,sans-serif;fill:#555}
    .tps-title{font:700 13px system-ui,sans-serif;fill:#0055a0}
  </style>
  <polygon points="275,30 325,30 340,75 260,75" fill="#003d73"/>
  <polygon points="260,75 340,75 360,130 240,130" fill="#0055a0"/>
  <polygon points="240,130 360,130 385,195 215,195" fill="#3378b9"/>
  <polygon points="215,195 385,195 415,270 185,270" fill="#6ea3d2"/>
  <text x="300" y="56" class="tps-eis">EIS</text>
  <text x="300" y="107" class="tps-eis">DSS</text>
  <text x="300" y="167" class="tps-eis">MIS</text>
  <text x="300" y="237" class="tps-eis">TPS</text>
  <line x1="415" y1="50" x2="455" y2="50" stroke="#0055a0" stroke-width="1"/>
  <text x="460" y="40" class="tps-title">Estrategico</text>
  <text x="460" y="55" class="tps-user">Alta direccion</text>
  <line x1="415" y1="102" x2="455" y2="102" stroke="#0055a0" stroke-width="1"/>
  <text x="460" y="92" class="tps-title">Analitico</text>
  <text x="460" y="107" class="tps-user">Analistas</text>
  <line x1="415" y1="162" x2="455" y2="162" stroke="#0055a0" stroke-width="1"/>
  <text x="460" y="152" class="tps-title">Gestion</text>
  <text x="460" y="167" class="tps-user">Mandos medios</text>
  <line x1="415" y1="230" x2="455" y2="230" stroke="#0055a0" stroke-width="1"/>
  <text x="460" y="220" class="tps-title">Operativo</text>
  <text x="460" y="235" class="tps-user">Operarios</text>
  <text x="300" y="300" text-anchor="middle" font="italic 11px system-ui,sans-serif" fill="#666">+ agregacion / - volumen  ·  - agregacion / + volumen</text>
</svg>

| Tipo | Sigla | Nivel | Funcion | Ejemplo |
|---|---|---|---|---|
| Sistema de Procesamiento de Transacciones | **TPS** | Operativo | Gestiona transacciones diarias | Alta en Padron, cobro de tributo |
| Sistema de Informacion Gerencial | **MIS** | Tactico | Informes regulares para mandos medios | Informe mensual de ingresos por distrito |
| Sistema de Soporte a la Decision | **DSS** | Analitico | Analisis y simulaciones para decisiones no rutinarias | Simulacion de impacto de subida de IBI |
| Sistema de Informacion Ejecutiva | **EIS** | Estrategico | Cuadro de mando para direccion | Cuadro de mando del Alcalde |

> **[EJEMPLO AYTO MADRID]** La arquitectura de sistemas del Ayuntamiento de Madrid combina los cuatro niveles: el **Padron Municipal** funciona como TPS (procesa altas/bajas en tiempo real), alimenta un MIS estadistico (informes demograficos mensuales), que a su vez nutre un DSS de **planificacion urbana** (¿donde construir un nuevo colegio?), cuyos resultados llegan al EIS del **Cuadro de Mando Integral municipal** que consulta el equipo de gobierno.

### 2.7. SI empresariales transversales

Mas alla de la clasificacion por nivel, existen sistemas que atraviesan todos los niveles organizacionales:

- **ERP** (Enterprise Resource Planning): integra procesos de negocio (finanzas, RRHH, compras, produccion, ventas) en un unico sistema. Ejemplos: SAP S/4HANA, Oracle Fusion, Microsoft Dynamics 365. En el sector publico: **Sorolla2** (SEC) o **GEISER**.
- **CRM** (Customer Relationship Management): gestiona la relacion con clientes/ciudadanos. Ejemplos: Salesforce, HubSpot, Zoho. En el sector publico: **CAU** (Centro de Atencion al Usuario).
- **SCM** (Supply Chain Management): gestiona la cadena de suministro. Menos relevante en administracion publica, salvo en logistica de servicios municipales.
- **BPM** (Business Process Management): modela, automatiza y optimiza procesos de negocio.
- **BI** (Business Intelligence): analitica, cuadros de mando, reporting.
- **DWH** (Data Warehouse): almacen integrado de datos historicos para analisis (ver §2.8).

### 2.8. Herramientas complementarias

- **Cuadro de Mando Integral (CMI / Balanced Scorecard / BSC)**: herramienta de control empresarial que permite establecer y monitorizar los objetivos de una empresa y sus areas. Muestra de forma continuada el cumplimiento del plan estrategico, articulado en cuatro perspectivas: **financiera, clientes, procesos internos, aprendizaje**. [Kaplan & Norton, 1992]

- **Datawarehouse (DWH)**: base de datos corporativa que integra y depura informacion de una o mas fuentes distintas, para luego procesarla permitiendo su analisis desde multiples perspectivas (**OLAP** — On-Line Analytical Processing) y con grandes velocidades de respuesta. Alimenta a los DSS y EIS.

- **Data Lake**: repositorio de datos en bruto, sin esquema predefinido, escalable horizontalmente. Complementa al DWH permitiendo almacenar datos no estructurados (logs, imagenes, texto libre) para posterior analisis con Big Data.

- **Data Lakehouse**: arquitectura hibrida (Databricks, 2020) que combina las garantias transaccionales del DWH con la flexibilidad del Data Lake.

### 2.9. Metodologias de implantacion

Implantar un SI en una organizacion no es solo comprar software: requiere metodologia. Las principales metodologias de implantacion son:

- **Metrica v3** (MAP, 2001): metodologia oficial de la Administracion Publica espanola para el desarrollo de SI. Cubre planificacion, desarrollo, mantenimiento. Referencia historica aun vigente en muchos pliegos.
- **ITIL v4** (Axelos, 2019): gestion de servicios TI. Orientada a operacion y mejora continua.
- **COBIT 2019** (ISACA): gobernanza de TI y cumplimiento regulatorio.
- **Metodologias agiles** (Scrum, Kanban, SAFe): iteraciones cortas, entregas incrementales. Adoptadas progresivamente por el sector publico.

> **[REFERENCIA CRUZADA]** La metodologia de desarrollo se trata en profundidad en el **Tema 30** (Ingenieria del software) y la gestion de servicios en el **Tema 25** (Gestion de servicios TI).

---

## 3. Arquitectura de ordenadores

La arquitectura de ordenadores se define como el **conjunto de reglas, normas y procedimientos que especifican las interrelaciones entre los componentes logicos y fisicos** que forman parte de un sistema informatico, asi como las caracteristicas que debe cumplir cada componente. [STALLINGS-COA, Cap. 1]

Es util distinguir entre:

- **Arquitectura** (*Instruction Set Architecture*, ISA): la vision del programador — que instrucciones existen, que registros son visibles, como se direcciona memoria.
- **Organizacion**: la vision del ingeniero — como se implementa la ISA en el hardware, que buses hay, como esta estructurada la cache.

Dos procesadores con la misma **arquitectura** (p.ej. Intel i9 y Intel i3) tienen organizaciones distintas pero son compatibles a nivel de codigo.

### 3.1. Arquitectura Von Neumann

Tambien conocida como **modelo de Von Neumann** o **arquitectura Princeton**. Propuesta por John von Neumann en el celebre **"First Draft of a Report on the EDVAC"** (1945), que sistematizo las ideas del equipo de Eckert y Mauchly (ENIAC, 1945) en un documento formal. El EDVAC (1949) fue la primera implementacion del modelo. [STALLINGS-COA, Cap. 2]

**Componentes** (los cuatro elementos canonicos):

- **Unidad de proceso (CPU)**: contiene una Unidad Aritmetico-Logica (ALU), registros del procesador y una Unidad de Control (UC) con un registro de instrucciones y un contador de programa (CP).
- **Memoria**: almacena **tanto datos como instrucciones** en un unico espacio de memoria. Esta es la caracteristica definitoria.
- **Mecanismos de entrada/salida (E/S)**.
- **Buses** que conectan los elementos anteriores.

**Caracteristica fundamental**: datos e instrucciones comparten la misma memoria y el mismo bus. Esto permite el concepto de **programa almacenado** — las instrucciones se pueden modificar como si fuesen datos (base de compiladores, ensambladores y sistemas operativos modernos).

> **[DATO CLAVE EXAMEN]** El **cuello de botella de Von Neumann** (Von Neumann bottleneck): no pueden darse simultaneamente una busqueda de instrucciones y una operacion de datos, ya que comparten un bus comun. La velocidad de la CPU ha crecido mucho mas rapido que la velocidad de la memoria principal, ampliando este cuello de botella. Las caches y el pipelining lo mitigan parcialmente.

### 3.2. Arquitectura Harvard

Debe su nombre al ordenador **Harvard Mark I** (Howard Aiken, 1944), anterior incluso a la formalizacion de Von Neumann. Contiene los mismos elementos que el modelo Von Neumann, pero con una **diferencia fundamental**: la memoria principal se divide en **memoria de instrucciones** y **memoria de datos**, cada una con su propio bus exclusivo. [STALLINGS-COA, Cap. 2]

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 360" role="img" aria-label="Comparativa Von Neumann vs Harvard">
  <style>
    .arch-label{font:600 13px system-ui,sans-serif;fill:#1a1a1a;text-anchor:middle}
    .arch-sub{font:11px system-ui,sans-serif;fill:#555;text-anchor:middle}
    .arch-title{font:700 16px system-ui,sans-serif;text-anchor:middle}
  </style>
  <text x="170" y="32" class="arch-title" fill="#0055a0">Arquitectura Von Neumann</text>
  <text x="170" y="50" class="arch-sub">1945 · 1 memoria · 1 bus</text>
  <rect x="60" y="80" width="100" height="50" rx="4" fill="#d6e4f0" stroke="#0055a0" stroke-width="1.5"/>
  <text x="110" y="103" class="arch-label">CPU</text>
  <text x="110" y="118" class="arch-sub">fetch + exec</text>
  <rect x="220" y="80" width="130" height="50" rx="4" fill="#d6e4f0" stroke="#0055a0" stroke-width="1.5"/>
  <text x="285" y="101" class="arch-label">Memoria unica</text>
  <text x="285" y="117" class="arch-sub">datos + instrucciones</text>
  <line x1="160" y1="105" x2="220" y2="105" stroke="#0055a0" stroke-width="3"/>
  <text x="190" y="97" class="arch-sub">bus compartido</text>
  <rect x="60" y="160" width="290" height="60" rx="4" fill="#fce4e4" stroke="#d13c3c" stroke-width="1.5" stroke-dasharray="5 3"/>
  <text x="205" y="185" class="arch-label" fill="#d13c3c">Cuello de botella Von Neumann</text>
  <text x="205" y="205" class="arch-sub">no se lee dato e instruccion a la vez</text>
  <line x1="360" y1="40" x2="360" y2="320" stroke="#c0c7cf" stroke-width="1" stroke-dasharray="3 3"/>
  <text x="510" y="32" class="arch-title" fill="#2d8659">Arquitectura Harvard</text>
  <text x="510" y="50" class="arch-sub">Harvard Mark I 1944</text>
  <rect x="400" y="80" width="100" height="50" rx="4" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="450" y="103" class="arch-label">CPU</text>
  <text x="450" y="118" class="arch-sub">fetch || exec</text>
  <rect x="560" y="50" width="110" height="40" rx="4" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="615" y="70" class="arch-label">Mem. instr.</text>
  <rect x="560" y="120" width="110" height="40" rx="4" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="615" y="140" class="arch-label">Mem. datos</text>
  <line x1="500" y1="95" x2="560" y2="70" stroke="#2d8659" stroke-width="3"/>
  <line x1="500" y1="115" x2="560" y2="140" stroke="#2d8659" stroke-width="3"/>
  <text x="540" y="82" class="arch-sub">bus I</text>
  <text x="540" y="134" class="arch-sub">bus D</text>
  <rect x="400" y="180" width="270" height="60" rx="4" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5" stroke-dasharray="5 3"/>
  <text x="535" y="205" class="arch-label" fill="#2d8659">Acceso paralelo</text>
  <text x="535" y="225" class="arch-sub">instruccion y dato simultaneos</text>
  <rect x="60" y="295" width="610" height="50" rx="4" fill="#f5f5f5" stroke="#c0c7cf"/>
  <text x="70" y="314" font="600 12px system-ui,sans-serif" fill="#0055a0">Harvard modificada (actual):</text>
  <text x="70" y="332" font="11px system-ui,sans-serif" fill="#555">x86-64, ARM · cache L1 separada (I/D) pero memoria principal unica · combina lo mejor</text>
</svg>

**Ventaja clave de Harvard**: al tener buses separados, se pueden simultanear operaciones sobre datos e instrucciones, eliminando el cuello de botella de Von Neumann y aumentando el rendimiento.

| Caracteristica | Von Neumann | Harvard |
|---|---|---|
| Memoria | Unica (datos + instrucciones) | Separada (datos / instrucciones) |
| Buses | Bus compartido | Buses independientes |
| Acceso simultaneo | No | Si |
| Cuello de botella | Si | No (o reducido) |
| Complejidad | Menor | Mayor |
| Aplicaciones tipicas | PCs de proposito general | DSPs, microcontroladores (AVR, PIC) |

### 3.3. Arquitectura Harvard modificada

En la actualidad, la mayoria de los procesadores de proposito general (x86-64, ARM Cortex-A) implementan una **arquitectura Harvard modificada**, que combina lo mejor de ambos mundos:

- La **memoria principal** es unica (como Von Neumann), lo que permite que los contenidos de la memoria de instrucciones sean accedidos como si fuesen datos — posibilita cargar un programa desde disco para su ejecucion, compilar y enlazar dinamicamente, etc.
- La **cache L1** esta separada en dos: cache L1 de instrucciones (L1i) y cache L1 de datos (L1d). Esto proporciona la ventaja de paralelismo de Harvard en el nivel mas cercano a la CPU, donde mas importa.
- La **cache L2 y L3** vuelven a ser unificadas (datos + instrucciones).

Caracteristicas de la Harvard modificada:

- La memoria de instrucciones y datos ocupan **diferente espacio logico** en cache pero **mismo espacio fisico** en RAM.
- Acceden a la CPU por **buses L1 distintos**, pero comparten bus en niveles inferiores.
- Pueden ser accedidas de **diferente manera** (la cache L1i solo se lee, la L1d se lee y escribe).

> **[DATO CLAVE EXAMEN]** En un examen C1, recordar esta jerarquia: **Von Neumann** (memoria unica, historico) vs **Harvard** (memorias separadas, microcontroladores) vs **Harvard modificada** (PCs actuales, hibrido).

---

## 4. Generaciones de ordenadores

Las generaciones se definen por tres aspectos principales: la **tecnologia vigente** (componente electronico principal), las **tecnicas de programacion** y el **impacto en la sociedad**. [TANENBAUM-SO, Cap. 1]

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 720 320" role="img" aria-label="Timeline generaciones de ordenadores">
  <style>
    .gen-year{font:700 13px system-ui,sans-serif;fill:#0055a0;text-anchor:middle}
    .gen-tech{font:600 12px system-ui,sans-serif;fill:#1a1a1a;text-anchor:middle}
    .gen-ex{font:italic 11px system-ui,sans-serif;fill:#555;text-anchor:middle}
    .gen-num{font:700 14px system-ui,sans-serif;fill:#fff;text-anchor:middle}
  </style>
  <text x="360" y="30" text-anchor="middle" font="700 16px system-ui,sans-serif" fill="#0055a0">Generaciones de ordenadores</text>
  <line x1="60" y1="170" x2="660" y2="170" stroke="#0055a0" stroke-width="2"/>
  <circle cx="110" cy="170" r="18" fill="#0055a0"/>
  <text x="110" y="175" class="gen-num">1ª</text>
  <text x="110" y="130" class="gen-year">1940-1952</text>
  <text x="110" y="200" class="gen-tech">Valvulas</text>
  <text x="110" y="240" class="gen-ex">ENIAC</text>
  <circle cx="220" cy="170" r="18" fill="#0055a0"/>
  <text x="220" y="175" class="gen-num">2ª</text>
  <text x="220" y="130" class="gen-year">1952-1964</text>
  <text x="220" y="200" class="gen-tech">Transistor</text>
  <text x="220" y="240" class="gen-ex">TRADIC</text>
  <circle cx="330" cy="170" r="18" fill="#0055a0"/>
  <text x="330" y="175" class="gen-num">3ª</text>
  <text x="330" y="130" class="gen-year">1964-1970</text>
  <text x="330" y="200" class="gen-tech">CI (SSI/MSI)</text>
  <text x="330" y="240" class="gen-ex">PDP-11</text>
  <circle cx="440" cy="170" r="18" fill="#0055a0"/>
  <text x="440" y="175" class="gen-num">4ª</text>
  <text x="440" y="130" class="gen-year">1970-1981</text>
  <text x="440" y="200" class="gen-tech">Microproc.</text>
  <text x="440" y="240" class="gen-ex">IBM PC</text>
  <circle cx="550" cy="170" r="18" fill="#0055a0"/>
  <text x="550" y="175" class="gen-num">5ª</text>
  <text x="550" y="130" class="gen-year">1981-1991</text>
  <text x="550" y="200" class="gen-tech">VLSI · IA</text>
  <text x="550" y="240" class="gen-ex">Internet</text>
  <circle cx="640" cy="170" r="18" fill="#2d8659" stroke="#2d8659" stroke-width="2" stroke-dasharray="2 2"/>
  <text x="640" y="175" class="gen-num">6ª</text>
  <text x="640" y="130" class="gen-year" fill="#2d8659">1991 → hoy</text>
  <text x="640" y="200" class="gen-tech">Cuantica</text>
  <text x="640" y="240" class="gen-ex">IBM Q</text>
</svg>

### 4.1. Primera generacion (1940-1952) — Valvulas de vacio

| Aspecto | Detalle |
|---|---|
| Tecnologia | Reles electromagneticos, valvulas y tubos de vacio |
| Memoria | Tarjetas y cintas perforadas, lineas de demora de mercurio, tambores magneticos |
| Velocidad | Milisegundos |
| Tamano | Ocupaban habitaciones enteras. ENIAC: 30 toneladas, 167 m² |
| Consumo | Decenas de kW (ENIAC: 150 kW) |
| Uso | Aplicaciones cientificas y militares |
| Programacion | Lenguaje maquina directo (interruptores manuales, cables) |
| Ejemplos | **ENIAC** (Eckert-Mauchly, 1945), **Mark I** (Harvard, 1944), **UNIVAC I** (1951), **Colossus** (Bletchley, 1943) |

### 4.2. Segunda generacion (1952-1964) — Transistores

| Aspecto | Detalle |
|---|---|
| Tecnologia | **Transistor** sustituye a la valvula de vacio (invencion: Bardeen, Brattain, Shockley, Bell Labs 1947 — Nobel 1956) |
| Memoria | Nucleos de ferrita, soportes magneticos, tambores mejorados |
| Mejoras | Reduccion de tamano (1/10), consumo (1/100) y coste; aumento de fiabilidad (10x) |
| Uso | Se extienden a empresas y universidades (administracion, gestion) |
| Programacion | Lenguajes de alto nivel: **Fortran** (1957), **Cobol** (1959), **Algol** (1960) |
| Otros avances | Circuitos impresos sustituyen al cableado; primeros perifericos modernos |
| Ejemplos | **TRADIC** (Bell Labs 1954, primer ordenador con transistores), **IBM 1401** (1959), **IBM 7090** |

> **[EJEMPLO AYTO MADRID]** El primer ordenador que llego a Espana fue un **IBM 650** adquirido por **RENFE en 1959** para gestion de reservas. Con 2.000 valvulas (era un hibrido tardio de 1ª gen), ocupaba una sala de 50 m². En la administracion publica espanola, la mecanizacion masiva llegaria en los anos 70 con ordenadores IBM de 3ª gen.

### 4.3. Tercera generacion (1964-1970) — Circuitos integrados

| Aspecto | Detalle |
|---|---|
| Tecnologia | **Circuitos integrados** (Kilby 1958, Noyce 1959) — SSI (Small-Scale Integration, ~10 transistores/chip), luego MSI (Medium-Scale, hasta 1.000) |
| Memoria | Semiconductores (DRAM IBM 1966) y discos magneticos mejorados |
| Mejoras | Miniaturizacion drastica, primeras minicomputadoras |
| Software | Sistemas operativos con **multiprogramacion**, tiempo real, modo interactivo (time-sharing) |
| Programacion | Aparece **BASIC** (Dartmouth, 1964) |
| Ejemplos | **IBM System/360** (1964, familia compatible de ordenadores), **PDP-11** (DEC, 1970), superordenador **CDC-6600** (Cray, 1964) |

### 4.4. Cuarta generacion (1971-1981) — Microprocesador

| Aspecto | Detalle |
|---|---|
| Tecnologia | **LSI** (Large-Scale Integration) y **VLSI** (Very Large-Scale, >10.000 transistores/chip) |
| Hito | En **1971** aparece el **Intel 4004**, primer microprocesador comercial: toda la CPU en un unico chip (2.300 transistores, 4 bits, 740 kHz) |
| Conmutacion | 10 nanosegundos |
| Almacenamiento | Disquete (Floppy Disk 8", luego 5,25", 3,5") |
| Uso | Primeros **ordenadores personales**: **Altair 8800** (1975), **Apple I** (1976), **IBM PC 5150** (1981) |
| Otros | Redes de ordenadores (Ethernet 1973, TCP/IP 1974), teleinformatica |

### 4.5. Quinta generacion (1981-1991) — IA, GUI, redes

| Aspecto | Detalle |
|---|---|
| Tecnologia | Componentes **VLSI** masivos y **ULSI** (Ultra Large-Scale) |
| Conmutacion | 1 nanosegundo |
| Avances | Inteligencia Artificial (sistemas expertos: MYCIN, DENDRAL), redes neuronales primitivas |
| Programacion | Lenguajes cercanos al natural (Prolog, Lisp para IA); OOP (C++ 1985, Smalltalk) |
| Interfaces | Sistemas operativos con **interfaces graficas** (Xerox Star 1981, Apple Lisa 1983, Mac 1984, Windows 1.0 1985, X Window 1984) |
| Redes | Internet consolidada (ARPANET → NSFNET 1986), World Wide Web inventada (Tim Berners-Lee, CERN, 1989-1991) |
| Impacto | Expansion masiva de la microinformatica a hogares y oficinas |

### 4.6. Sexta generacion (1991 → actualidad) — Computacion distribuida, cuantica, neuromorfica

Aunque la literatura clasica cierra las generaciones con la 5ª, la mayoria de autores actuales reconocen una **sexta generacion** que cubre el periodo 1991-actualidad, caracterizada por:

- **Multinucleo y paralelismo masivo**: desde ~2005 todos los procesadores de proposito general son multinucleo. GPUs con miles de nucleos (NVIDIA H100: 18.432 cores CUDA).
- **Computacion en la nube**: AWS (2006), Azure (2010), Google Cloud (2011). Ordenadores virtualizados, escalables bajo demanda.
- **Dispositivos ubicuos**: smartphones (iPhone 2007), tablets, IoT, wearables. Mas dispositivos conectados que humanos.
- **Inteligencia artificial moderna**: redes neuronales profundas (AlexNet 2012), transformers (2017), GPT (2018-2024), Claude, Gemini.
- **Computacion cuantica**: primeros ordenadores cuanticos comerciales (IBM Q 2016, Google Sycamore 2019). Potencial disruptivo.
- **Computacion neuromorfica**: chips inspirados en el cerebro (Intel Loihi 2017, IBM TrueNorth 2014). Muy eficientes energeticamente.

> **[REFERENCIA CRUZADA]** La computacion en la nube se amplia en el **Tema 28** (Cloud computing) y la IA en el **Tema 36** (Inteligencia artificial y Big Data).

---

## 5. Componentes internos de los equipos microinformaticos

El hardware de un ordenador se estructura en tres subsistemas: [STALLINGS-COA, Cap. 3]

1. **Unidad Central de Proceso (UCP/CPU)**
2. **Memoria central**
3. **Unidades de entrada/salida (perifericos)**

Todos ellos se comunican mediante **buses**.

### 5.1. Buses

Un **bus** es un conjunto de circuitos que se encargan de la conexion y comunicacion entre los diversos componentes del ordenador. La comunicacion se realiza mediante lineas electricas paralelas (o en serie en buses modernos como PCIe). [STALLINGS-COA, Cap. 3]

**Tipos funcionales** (los **tres buses** clasicos):

| Tipo de bus | Direccionalidad | Funcion |
|---|---|---|
| **Bus de control** | Unidireccional (UC → componentes) | Transmite senales de la Unidad de Control interpretadas como ordenes |
| **Bus de direcciones** | Unidireccional (CPU → memoria) | Transporta las direcciones de memoria sobre las que se va a actuar (lectura/escritura) |
| **Bus de datos** | Bidireccional | Traslada datos hacia/desde la memoria y otros dispositivos |

**Parametros de un bus**:

- **Anchura (bits)**: numero de lineas paralelas. Un bus de datos de 64 bits transfiere 8 bytes por ciclo.
- **Frecuencia (MHz/GHz)**: numero de ciclos por segundo.
- **Ancho de banda** (MB/s o GB/s) = anchura × frecuencia / 8.
- **Protocolo**: sincrono (reloj comun) o asincrono (handshake).

**Buses reales modernos**: PCIe 5.0 (32 GT/s por lane, hasta 128 GB/s bidireccional x16), USB 4 (40 Gbps), Thunderbolt 5 (80-120 Gbps).

### 5.2. El procesador (CPU)

El procesador, tambien denominado **CPU** (*Central Processing Unit*), es el subsistema mas importante del ordenador. Actua como su cerebro, coordinando y supervisando el funcionamiento del sistema y procesando las instrucciones de los programas. [STALLINGS-COA, Cap. 3]

**Secuencia invariable de operacion** (ciclo de instruccion, ver §5.4):
1. Extraer de memoria una instruccion del programa en ejecucion.
2. Analizar (decodificar) dicha instruccion.
3. Realizar las operaciones necesarias para su ejecucion.
4. Actualizar el estado y pasar a la siguiente instruccion.

Actualmente, la CPU esta integrada en un **microprocesador** (chip), montado sobre la **placa base** en un socket especifico (Intel LGA1851, AMD AM5) y acompanado de un **disipador** de calor y (habitualmente) **ventilador** o refrigeracion liquida.

> **Nota**: Los terminos UCP, CPU, microprocesador y procesador son equivalentes en la practica, aunque tecnicamente "microprocesador" se refiere al chip fisico y "CPU" al concepto logico.

#### 5.2.1. Tecnologias: CISC vs RISC

**CISC** (*Complex Instruction Set Computer*) [INTEL-SDM]

- Conjunto de instrucciones **amplio y complejo** (Intel x86-64 tiene ~1.500 instrucciones en 2024).
- Permite operaciones complejas entre operandos en memoria o registros.
- Dificulta el paralelismo entre instrucciones.
- Los sistemas CISC modernos convierten instrucciones complejas en **microoperaciones tipo RISC** (micro-ops, uops) internamente antes de ejecutarlas. Esta es la razon por la que x86 puede competir en rendimiento con RISC.
- Requiere **4 a 10 ciclos de reloj** por instruccion en promedio (con pipelining bajan a 1 uop/ciclo efectivo).
- Ejemplos: **Intel Core (x86-64), AMD Ryzen (x86-64), Motorola 68000** (historico).

Ventajas CISC:
- Reduce la dificultad de crear compiladores (ya estan maduros).
- Permite reducir el tamano del codigo (instrucciones hacen mas en menos bytes).
- Compatibilidad historica (el ecosistema x86 es enorme).
- Facilita la depuracion de errores (mas instrucciones especializadas).

**RISC** (*Reduced Instruction Set Computer*) [STALLINGS-COA, Cap. 15]

- Conjunto de instrucciones **reducido y simple** (ARMv9 tiene ~400 instrucciones, RISC-V base tiene ~50).
- Instrucciones de **tamano fijo** (4 bytes en ARM/RISC-V) en pocos formatos.
- Solo las instrucciones de **carga/almacenamiento** (LOAD/STORE) acceden a memoria — **arquitectura load-store**.
- Cada instruccion se ejecuta idealmente en **un solo ciclo de CPU** (con pipelining).
- Ejemplos: **ARM Cortex** (smartphones, Apple M), **MIPS** (routers, consolas antiguas), **SPARC** (servidores Sun/Oracle), **PowerPC** (Macs pre-2006, consolas), **RISC-V** (emergente, codigo abierto).

Ventajas RISC:
- CPU mas rapida por ciclo (menos trabajo por instruccion).
- Favorece segmentacion (pipelining) y paralelismo (superescalar).
- Menor consumo energetico por operacion (razon por la que domina en moviles).
- Diseno mas simple — menos transistores dedicados a decodificar.

**Tabla comparativa**:

| Aspecto | CISC | RISC |
|---|---|---|
| Instrucciones | Complejas, tamano variable | Simples, tamano fijo |
| Ciclos por instruccion (IPC) | 4-10 (antes de uops) | 1 (nominal) |
| Acceso a memoria | Cualquier instruccion | Solo LOAD/STORE |
| Numero de registros | Pocos (8-16) | Muchos (32+) |
| Paralelismo pipeline | Dificil (requiere uops) | Favorable |
| Consumo | Mayor (por ciclo) | Menor |
| Uso tipico | PCs de escritorio, servidores | Moviles, consolas, servidores ARM, embebidos |
| Ejemplos | Intel Core, AMD Ryzen | ARM Cortex-A, Apple M, AWS Graviton, RISC-V |

> **[DATO CLAVE EXAMEN]** El procesador x86-64 (el mas comun en PCs de escritorio) es **CISC**, pero internamente traduce instrucciones CISC a microinstrucciones RISC (uops) antes de ejecutarlas. Este proceso se llama **decodificacion x86** y ocupa hardware significativo (~15% del die).

#### 5.2.2. Medidas de potencia de la CPU

- **FLOPS** (*Floating-Point Operations Per Second*): numero de operaciones de coma flotante por segundo. Relevante para calculo cientifico, IA, graficos. Superordenador El Capitan (2024): 1,74 **ExaFLOPS** (10^18 FLOPS).
- **MIPS** (*Millions of Instructions Per Second*): millones de instrucciones por segundo. **Solo comparable entre CPUs con el mismo conjunto de instrucciones** (no se puede comparar MIPS de x86 con MIPS de ARM directamente).
- **IPC** (*Instructions Per Cycle*): cuantas instrucciones ejecuta la CPU en cada ciclo de reloj. Procesadores modernos pueden superar 4 IPC gracias al paralelismo superescalar.
- **Frecuencia** (GHz): ciclos de reloj por segundo. Un i9-14900K funciona a 5,8 GHz en turbo.
- **TDP** (*Thermal Design Power*, W): potencia termica maxima. Proxy del consumo electrico.

#### 5.2.3. Multiprocesamiento, multinucleo y multithreading

Tres conceptos que conviene no confundir:

- **Multiprocesamiento** (multi-CPU): un equipo con **mas de una CPU fisica** (multiples sockets). Tipico en servidores de alta gama. Puede ser **SMP** (simetrico, CPUs iguales) o **NUMA** (no uniforme, cada CPU con su propia memoria).

- **Multinucleo** (multi-core): un unico circuito integrado con **mas de una CPU logica** dentro. No confundir con multiprocesamiento. Un Intel Core i9-14900K tiene 24 nucleos (8 performance + 16 efficiency) en un solo chip.

- **Multithreading (HyperThreading / SMT)**: tecnologia que permite **duplicar las unidades logicas de cada nucleo**, permitiendo a un nucleo ejecutar **dos hilos simultaneos**. Patente original de Sun Microsystems (1994).
  - Intel lo denomina **HyperThreading Technology (HTT)** — lanzado en Pentium 4 (2002).
  - AMD lo denomina **SMT (Simultaneous Multi-Threading)** — en Zen desde 2017.
  - Ambas tecnologias son virtualmente identicas en concepto. Aportan ~20-30% rendimiento adicional con ~5% mas silicio.

> **[DATO CLAVE EXAMEN]** Un **Intel Core i9-14900K con 24 nucleos y HyperThreading** presenta al sistema operativo **32 hilos logicos** (8 nucleos-P con HT×2 + 16 nucleos-E sin HT = 16 + 16 = 32). Los nucleos-E (Efficiency) no tienen HT para ahorrar energia.

#### 5.2.4. Pipelining (segmentacion de instrucciones)

El **pipelining** es la tecnica fundamental para acelerar una CPU sin aumentar su frecuencia. Divide la ejecucion de cada instruccion en **etapas** y permite que varias instrucciones se solapen en distintas etapas simultaneamente. Es analoga a una cadena de montaje industrial.

**Pipeline RISC clasico de 5 etapas** (modelo MIPS, base de muchos libros de texto):

1. **IF** (*Instruction Fetch*): busca la instruccion en memoria.
2. **ID** (*Instruction Decode*): decodifica la instruccion y lee operandos de registros.
3. **EX** (*Execute*): la ALU ejecuta la operacion.
4. **MEM** (*Memory Access*): lectura/escritura en memoria de datos (solo LOAD/STORE).
5. **WB** (*Write Back*): escribe el resultado en el registro destino.

Sin pipeline, una instruccion ocupa 5 ciclos. Con pipeline, **en estado estacionario se completa una instruccion por ciclo** (IPC=1), porque las etapas estan trabajando en instrucciones diferentes simultaneamente.

Procesadores modernos tienen pipelines mucho mas profundos:
- Intel Core (Golden Cove, 2021): ~19 etapas.
- AMD Zen 4 (2022): ~19 etapas.
- ARM Cortex-X4 (2023): ~15 etapas.

**Hazards (riesgos del pipeline)**: situaciones que rompen la ejecucion ideal de una instruccion por ciclo:

- **Hazard estructural**: dos instrucciones compiten por el mismo recurso hardware (ej. bus de memoria).
- **Hazard de datos**: una instruccion necesita el resultado de otra anterior que aun no ha terminado.
- **Hazard de control**: un salto (branch) obliga a descartar instrucciones ya buscadas que no se van a ejecutar.

Soluciones modernas:

- **Forwarding / bypassing**: cortocircuito interno para pasar resultados entre etapas sin esperar al WB.
- **Prediccion de saltos** (*branch prediction*): la CPU "adivina" si un salto se tomara y empieza a buscar instrucciones desde el destino predicho. Aciertos >95% en procesadores modernos.
- **Ejecucion especulativa**: ejecuta instrucciones asumiendo una prediccion de salto; si falla, descarta resultados.
- **Ejecucion fuera de orden** (*out-of-order execution*): reordena instrucciones para aprovechar huecos del pipeline.

> **[DATO CLAVE EXAMEN]** Las **vulnerabilidades Spectre y Meltdown** (2018) aprovechan precisamente la **ejecucion especulativa**: los efectos de instrucciones especulativas no se deshacen del todo (quedan rastros en cache), permitiendo leer memoria protegida. Afectaron a casi todos los procesadores Intel, AMD y ARM posteriores a 1995.

#### 5.2.5. CPU superescalar

Una CPU **escalar** ejecuta una instruccion por ciclo en el mejor caso. Una CPU **superescalar** ejecuta **varias instrucciones por ciclo** replicando unidades funcionales (multiples ALUs, multiples unidades de punto flotante, etc.).

El procesador despacha instrucciones a las unidades disponibles en paralelo, respetando las dependencias de datos. Intel Golden Cove despacha hasta **6 instrucciones por ciclo**; Apple M3 hasta **8**.

> **[REFERENCIA CRUZADA]** El paralelismo a nivel de hilo (multi-core) y a nivel de instruccion (pipeline, superescalar) se tratan juntos en el **Tema 19** (Arquitecturas paralelas).

#### 5.2.6. Ley de Moore y su crisis

La **Ley de Moore** (Gordon Moore, Intel, 1965) observaba que el numero de transistores en un chip se duplicaba cada ~18-24 meses a coste constante. Se cumplio con notable precision desde 1965 hasta ~2015.

Desde ~2015 la ley se ha ralentizado: las dificultades fisicas de miniaturizar por debajo de 5 nm (efectos cuanticos, fugas de corriente, disipacion termica) han frenado el ritmo. La industria ha respondido con:

- **Arquitecturas heterogeneas**: big.LITTLE (ARM), nucleos P-E (Intel), combinando nucleos rapidos con nucleos eficientes.
- **Chiplets**: divisiones del chip en multiples dies interconectados (AMD EPYC/Ryzen, Intel Meteor Lake).
- **3D stacking**: apilar transistores en capas (3D V-Cache de AMD, memoria HBM).
- **Aceleradores especializados**: GPUs, NPUs (Neural Processing Units), TPUs para IA.

#### 5.2.7. Procesadores actuales (2024-2025)

Panorama actual del mercado de procesadores:

| Fabricante | Arquitectura | Familia | Mercado |
|---|---|---|---|
| **Intel** | x86-64 CISC | Core Ultra (Meteor/Lunar Lake), Xeon 6 | PCs escritorio/portatil, servidores |
| **AMD** | x86-64 CISC | Ryzen 9000, EPYC 9005 Turin | PCs escritorio/portatil, servidores |
| **Apple** | ARM64 RISC | Apple M4 (2024), M4 Pro/Max/Ultra | Mac, iPad, Vision Pro |
| **Qualcomm** | ARM64 RISC | Snapdragon 8 Gen 4, Snapdragon X Elite | Smartphones, portatiles Copilot+ |
| **NVIDIA** | ARM64 + GPU | Grace Hopper, Blackwell | Servidores IA, HPC |
| **AWS** | ARM64 RISC | Graviton 4 | Servidores cloud AWS |

---

### 5.3. Unidad Central de Proceso — Componentes internos

La CPU esta formada por tres subsistemas principales: [STALLINGS-COA, Cap. 12]

1. **Registros de acceso rapido**
2. **Unidad de Control (UC)**
3. **Unidad Aritmetico-Logica (ALU/UAL)**

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 360" role="img" aria-label="Bloques internos de la CPU">
  <style>
    .cpu-heading{font:700 14px system-ui,sans-serif;fill:#fff;text-anchor:middle}
    .cpu-sub{font:11px system-ui,sans-serif;fill:#555;text-anchor:middle}
    .cpu-chip{font:700 12px system-ui,sans-serif;fill:#0055a0;letter-spacing:2px}
    .cpu-bus{font:600 12px system-ui,sans-serif;fill:#1a1a1a;text-anchor:middle}
  </style>
  <rect x="50" y="60" width="380" height="240" rx="8" fill="#eef4fa" stroke="#0055a0" stroke-width="2" stroke-dasharray="6 4"/>
  <text x="70" y="82" class="cpu-chip">CPU / MICROPROCESADOR</text>
  <rect x="80" y="100" width="150" height="65" rx="4" fill="#0055a0"/>
  <text x="155" y="125" class="cpu-heading">ALU</text>
  <text x="155" y="145" class="cpu-sub" fill="#cde4f0">aritmetico-logica</text>
  <text x="155" y="158" class="cpu-sub" fill="#cde4f0">+ − × ÷ AND OR XOR</text>
  <rect x="250" y="100" width="160" height="65" rx="4" fill="#0055a0"/>
  <text x="330" y="125" class="cpu-heading">Unidad de Control</text>
  <text x="330" y="145" class="cpu-sub" fill="#cde4f0">reloj + CP + decoder</text>
  <text x="330" y="158" class="cpu-sub" fill="#cde4f0">+ secuenciador</text>
  <rect x="80" y="190" width="330" height="90" rx="4" fill="#3378b9"/>
  <text x="245" y="215" class="cpu-heading">Banco de Registros</text>
  <text x="245" y="237" class="cpu-sub" fill="#cde4f0">MAR · MBR · CP · RI · ACC</text>
  <text x="245" y="253" class="cpu-sub" fill="#cde4f0">FLAGS · SP · GPRs · SPRs</text>
  <rect x="470" y="80" width="140" height="50" rx="4" fill="#d6e4f0" stroke="#0055a0" stroke-width="1.5"/>
  <text x="540" y="102" class="cpu-heading" fill="#1a1a1a">Memoria RAM</text>
  <rect x="470" y="150" width="140" height="50" rx="4" fill="#d6e4f0" stroke="#0055a0" stroke-width="1.5"/>
  <text x="540" y="172" class="cpu-heading" fill="#1a1a1a">E/S</text>
  <rect x="470" y="220" width="140" height="50" rx="4" fill="#d6e4f0" stroke="#0055a0" stroke-width="1.5"/>
  <text x="540" y="242" class="cpu-heading" fill="#1a1a1a">ROM / BIOS</text>
  <line x1="430" y1="120" x2="470" y2="105" stroke="#d13c3c" stroke-width="2.5"/>
  <text x="450" y="100" class="cpu-bus" fill="#d13c3c">control</text>
  <line x1="430" y1="170" x2="470" y2="175" stroke="#2d8659" stroke-width="2.5"/>
  <text x="450" y="166" class="cpu-bus" fill="#2d8659">direcciones</text>
  <line x1="430" y1="240" x2="470" y2="245" stroke="#0055a0" stroke-width="2.5"/>
  <text x="450" y="236" class="cpu-bus" fill="#0055a0">datos</text>
</svg>

#### 5.3.1. Registros

Un **registro** es una pequena zona de memoria de acceso muy rapido y directo por parte del procesador, que almacena un dato, instruccion o direccion de memoria. Caracteristica: **minima capacidad, maxima velocidad** (~0,3 ns de latencia).

**Tipos de registros**:

| Tipo | Nombre | Funcion |
|---|---|---|
| Datos | **Registros de datos** | Almacenan valores numericos y caracteres |
| Datos | **Acumulador (ACC)** | Almacena temporalmente resultados aritmeticos/logicos intermedios para la ALU |
| Datos | **Registro de pila (SP, Stack Pointer)** | Mantiene la posicion actual de la cima de la pila |
| Direcciones | **Registro indice (IX)** | Direcciona datos hacia/desde la RAM mediante offset |
| Memoria | **MBR (Memory Buffer Register)** | Conectado al bus de datos. Lee/escribe datos del bus dirigidos a memoria o E/S |
| Memoria | **MAR (Memory Address Register)** | Contiene la direccion del dato a leer/escribir. Conectado al bus de direcciones |
| Instruccion | **CP (Contador de Programa)** | Direccion de la siguiente instruccion a ejecutar |
| Instruccion | **RI (Registro de Instruccion)** | Instruccion actualmente decodificada y en ejecucion |
| General | **GPRs (General-Purpose Registers)** | Almacenan direcciones o datos generales — sin funcion especifica |
| Especifico | **SPRs (Special-Purpose Registers)** | Guardan datos del estado del sistema |
| Estado | **CCR / Registro de estado** | Codigos de condicion de la ultima operacion. Incluye el registro FLAGS |
| Punto flotante | **Registros FP / SIMD** | Numeros reales IEEE-754 y operaciones vectoriales (XMM, YMM, ZMM, NEON) |
| Constantes | **Registros constantes** | Valores de solo lectura: cero, uno, PI |

> **[DATO CLAVE EXAMEN]** **Capacidad de direccionamiento**: si el MAR tiene **n bits**, se pueden direccionar un maximo de **2^n palabras** de memoria. Con MAR de 32 bits se direccionan 4 GB (2^32 = 4.294.967.296 bytes); con MAR de 64 bits se direccionan 16 EB (limite teorico practicamente inalcanzable).

#### 5.3.1.1. Registros FLAGS, EFLAGS y RFLAGS (x86)

El **registro FLAGS** es el registro de estado en la familia x86. Su evolucion acompana a la de la propia arquitectura:

| Registro | Ancho | Arquitectura | Epoca |
|---|---|---|---|
| **FLAGS** | 16 bits | 8086, 80286 (modo real) | 1978-1985 |
| **EFLAGS** | 32 bits | 80386, 80486, Pentium | 1985-presente (compat.) |
| **RFLAGS** | 64 bits | x86-64 (AMD64, Intel 64) | 2003-presente |

Los tres son **retrocompatibles**: los bits bajos de RFLAGS son EFLAGS, y los bits bajos de EFLAGS son FLAGS. Los bits anadidos en cada ampliacion se usan para caracteristicas nuevas (virtualizacion, identificacion CPUID, niveles de proteccion).

**Bits principales del registro FLAGS** (los que aparecen en examenes C1):

| Bit | Nombre | Flag | Descripcion |
|---|---|---|---|
| 0 | CF | Carry Flag | Acarreo en operaciones aritmeticas |
| 2 | PF | Parity Flag | Paridad del resultado (1 si numero par de bits 1) |
| 4 | AF | Auxiliary Flag | Acarreo auxiliar (para BCD) |
| 6 | ZF | Zero Flag | 1 si el resultado es cero |
| 7 | SF | Sign Flag | Signo del resultado (copia del bit mas significativo) |
| 8 | TF | Trap Flag | Modo paso a paso (debug) |
| 9 | IF | Interrupt Flag | Habilita interrupciones enmascarables |
| 10 | DF | Direction Flag | Direccion de operaciones de string |
| 11 | OF | Overflow Flag | Desbordamiento en aritmetica con signo |

**Ejemplo de uso** en un salto condicional:

```
COMPARA A, B       ; resta A-B, actualiza ZF, SF, CF, OF
SALTA_SI_IGUAL FIN ; salta a FIN si ZF=1 (eran iguales)
```

> **[REFERENCIA CRUZADA]** Los registros FLAGS de ARM se llaman **APSR** (Application Program Status Register) y los de RISC-V estan distribuidos en CSRs (Control and Status Registers). El concepto es equivalente.

#### 5.3.2. Unidad de Control

La Unidad de Control es la **parte mas importante del microprocesador** desde el punto de vista funcional. Controla el funcionamiento de todo el conjunto excepto las operaciones aritmeticas (gestionadas por la ALU). [STALLINGS-COA, Cap. 20]

**Componentes**:

| Componente | Funcion |
|---|---|
| **Reloj** | Proporciona impulsos con frecuencia constante que marcan los ciclos basicos. Ej: Pentium IV a 2 GHz = 2.000 millones de pulsos/segundo. No equivale a instrucciones/segundo, ya que muchas requieren multiples pulsos o el pipeline entrega varias por ciclo |
| **Contador de Programa (CP)** | Registro que contiene la direccion de memoria de la siguiente instruccion a ejecutar. Al encender el ordenador toma un valor por defecto donde se encuentra la primera instruccion (vector de reset) |
| **Registro de Instruccion (RI)** | Contiene la instruccion en ejecucion. Tiene dos partes: **codigo de operacion** (que hacer) y **operandos** (sobre que hacerlo) |
| **Decodificador** | Extrae el codigo de operacion del RI, lo analiza y lo comunica al controlador |
| **Controlador/Secuenciador** | Interpreta el codigo de operacion y genera las **microordenes** que actuan sobre el sistema en sincronia con el reloj |

#### 5.3.3. Unidad Aritmetico-Logica (ALU)

La ALU es el componente del procesador encargado de ejecutar las **operaciones elementales de tipo aritmetico y logico**. Se comunica con el sistema mediante el bus de datos. [STALLINGS-COA, Cap. 9]

**Componentes de la ALU**:

| Componente | Funcion |
|---|---|
| **Circuito Operacional (COP)** | Contiene los circuitos digitales para realizar las operaciones. Es el elemento mas importante de la ALU |
| **Registros de Entrada (REN)** | Almacenan los operandos sobre los que se ejecuta la operacion |
| **Acumulador** | Almacena los resultados finales. Conectado directamente al bus de datos para envio a memoria |
| **Registro de Estado** | Almacena informacion sobre condiciones de la ultima operacion (FLAGS, §5.3.1.1) |

**Tipos de operaciones**:

1. **Aritmeticas sobre enteros**: suma, resta, multiplicacion, division (incluyendo variantes con signo/sin signo).
2. **Logicas a nivel de bit**: AND, OR, NOT, XOR, NAND, NOR, XNOR.
3. **Desplazamiento y rotacion de bits**: desplazan bits a izquierda/derecha. Equivalencia aritmetica: desplazar n posiciones a izquierda equivale a multiplicar por 2^n (si no hay desbordamiento).
4. **Comparacion**: resta sin guardar resultado, solo actualiza FLAGS.

Las operaciones de **coma flotante** (reales IEEE-754) y **vectoriales/SIMD** (SSE, AVX, NEON) suelen estar en unidades separadas (FPU, SIMD unit) pero conceptualmente forman parte del bloque ALU extendido.

**Tablas de verdad de operaciones logicas** (2 entradas):

| A | B | AND | OR | XOR | NAND | NOR | XNOR |
|---|---|---|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 1 | 0 | 1 | 1 | 1 | 0 | 0 |
| 1 | 0 | 0 | 1 | 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 1 | 0 | 0 | 0 | 1 |

| A | NOT A |
|---|---|
| 0 | 1 |
| 1 | 0 |

### 5.4. Ciclo de ejecucion de instrucciones

El **ciclo de instruccion** (*instruction cycle* o *fetch-execute cycle*) es el conjunto de acciones que realiza el ordenador para ejecutar cada instruccion. Se divide en dos fases principales: [STALLINGS-COA, Cap. 12]

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 360" role="img" aria-label="Ciclo Fetch-Execute de instrucciones">
  <style>
    .fe-step{font:600 12px system-ui,sans-serif;fill:#fff;text-anchor:middle}
    .fe-desc{font:10px system-ui,sans-serif;fill:#cde4f0;text-anchor:middle}
    .fe-phase{font:700 12px system-ui,sans-serif;letter-spacing:2px}
  </style>
  <text x="320" y="28" text-anchor="middle" font="700 16px system-ui,sans-serif" fill="#0055a0">Ciclo Fetch-Execute</text>
  <rect x="30" y="50" width="330" height="150" rx="6" fill="#eef4fa" stroke="#0055a0" stroke-width="1.5" stroke-dasharray="4 3"/>
  <text x="45" y="68" class="fe-phase" fill="#0055a0">FASE 1 · FETCH (busqueda)</text>
  <rect x="50" y="90" width="90" height="45" rx="3" fill="#0055a0"/>
  <text x="95" y="110" class="fe-step">1. CP → MAR</text>
  <rect x="160" y="90" width="90" height="45" rx="3" fill="#0055a0"/>
  <text x="205" y="110" class="fe-step">2. MAR → Mem</text>
  <rect x="270" y="90" width="85" height="45" rx="3" fill="#0055a0"/>
  <text x="312" y="110" class="fe-step">3. Mem → MBR</text>
  <rect x="110" y="150" width="90" height="40" rx="3" fill="#0055a0"/>
  <text x="155" y="170" class="fe-step">4. MBR → RI</text>
  <rect x="220" y="150" width="120" height="40" rx="3" fill="#0055a0"/>
  <text x="280" y="170" class="fe-step">5. CP + 1</text>
  <rect x="380" y="50" width="230" height="150" rx="6" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5" stroke-dasharray="4 3"/>
  <text x="395" y="68" class="fe-phase" fill="#2d8659">FASE 2 · EXECUTE (ejecucion)</text>
  <rect x="400" y="90" width="90" height="45" rx="3" fill="#2d8659"/>
  <text x="445" y="110" class="fe-step">6. Decode</text>
  <rect x="510" y="90" width="90" height="45" rx="3" fill="#2d8659"/>
  <text x="555" y="110" class="fe-step">7. Execute</text>
  <rect x="400" y="150" width="200" height="40" rx="3" fill="#e89822"/>
  <text x="500" y="170" class="fe-step">Actualiza flags / regs</text>
</svg>

#### Fase 1: Busqueda (FETCH)

La instruccion es localizada en memoria y transferida a la Unidad de Control. Pasos:

1. La UC transfiere el contenido del **Contador de Programa (CP)** al **Registro de Direccion de Memoria (MAR)** a traves del bus interno.
2. El MAR emite la direccion al sistema de memoria a traves del bus de direcciones.
3. El sistema de memoria accede a la posicion indicada y transfiere la instruccion al **Registro de Intercambio de Memoria (MBR)** a traves del bus de datos.
4. La instruccion se transfiere del MBR al **Registro de Instruccion (RI)**.
5. El **Contador de Programa se incrementa** para apuntar a la siguiente instruccion secuencial (normalmente CP = CP + tamano_instruccion).

#### Fase 2: Ejecucion (EXECUTE)

1. El **decodificador** interpreta la instruccion del RI, extrayendo el codigo de operacion y los operandos.
2. El **secuenciador** activa los circuitos necesarios (ej. la ALU en operaciones aritmeticas, la unidad de memoria en LOAD/STORE).
3. Se ejecuta la operacion y se actualizan los registros FLAGS.
4. En caso de instrucciones de **salto** (branch), el CP se carga con una nueva direccion en lugar del incremento secuencial.

#### Clasificacion de instrucciones por numero de operandos

| Tipo | Descripcion | Ejemplo (castellano) |
|---|---|---|
| Sin operandos | Acciones de control sin datos explicitos | `FIN`, `NOP` |
| Un operando | Actuan sobre un dato o direccion | `SALTA 12345`, `INC A` |
| Dos operandos | Dos elementos; uno suele ser destino | `SUMA A, B` (A = A + B) |
| Tres operandos | Dos fuentes + un destino | `SUMA A, B, C` (C = A + B) |

Las arquitecturas **CISC** suelen soportar 0-2 operandos. Las **RISC modernas** tipicamente usan **3 operandos** (dos fuentes y un destino explicito), lo que evita sobrescribir el contenido original.

> **[EJERCICIO RESUELTO]** **Problema**: una instruccion x86 `ADD EAX, EBX` (SUMA EAX, EBX en nuestra notacion castellana) suma los valores de EAX y EBX y guarda el resultado en EAX. Si EAX=10 y EBX=5, ¿cual es el contenido de EAX tras la ejecucion y que flags se actualizan?
>
> **Solucion**: EAX pasa a valer 15 (10+5). Los flags afectados son: ZF=0 (resultado no es cero), SF=0 (resultado positivo), CF=0 (sin acarreo), OF=0 (sin desbordamiento con signo), PF=1 (15 = 00001111, numero par de bits 1 en los 8 bits bajos).

### 5.5. Modos de direccionamiento

Los **modos de direccionamiento** son las diferentes formas de transformar el campo de operando de la instruccion en la **direccion efectiva** del operando real. [STALLINGS-COA, Cap. 13]

Se clasifican en:

- **Impropios** (operando fuera de memoria): implicito, inmediato.
- **Propios** (operando en memoria): directo, indirecto, relativo a base, relativo a indice.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 360" role="img" aria-label="Modos de direccionamiento">
  <style>
    .md-title{font:600 12px system-ui,sans-serif;fill:#0055a0;text-anchor:middle}
    .md-note{font:10px system-ui,sans-serif;fill:#555;text-anchor:middle}
    .md-op{font:700 13px system-ui,sans-serif;fill:#2d8659;text-anchor:middle}
  </style>
  <text x="340" y="30" text-anchor="middle" font="700 16px system-ui,sans-serif" fill="#0055a0">Modos de direccionamiento</text>
  <text x="340" y="48" text-anchor="middle" font="11px system-ui,sans-serif" fill="#666">operando objetivo: 42</text>
  <text x="80" y="75" class="md-title">1. Inmediato</text>
  <rect x="25" y="90" width="110" height="30" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="40" y="110" font="600 11px system-ui,sans-serif" fill="#555">SUMA #42</text>
  <text x="115" y="110" class="md-op">← 42</text>
  <text x="80" y="176" class="md-note" fill="#2d8659" font-weight="600">1 acceso</text>
  <text x="210" y="75" class="md-title">2. Directo</text>
  <rect x="155" y="90" width="110" height="30" fill="#eef4fa" stroke="#0055a0" stroke-width="1.5"/>
  <text x="170" y="110" font="600 11px system-ui,sans-serif" fill="#555">SUMA [100]</text>
  <rect x="155" y="135" width="110" height="30" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="230" y="155" class="md-op">42</text>
  <text x="210" y="200" class="md-note" fill="#0055a0" font-weight="600">2 accesos</text>
  <text x="340" y="75" class="md-title">3. Indirecto</text>
  <rect x="285" y="90" width="110" height="30" fill="#eef4fa" stroke="#0055a0" stroke-width="1.5"/>
  <text x="297" y="110" font="600 11px system-ui,sans-serif" fill="#555">SUMA [[500]]</text>
  <rect x="285" y="135" width="110" height="30" fill="#f5f5f5" stroke="#666" stroke-width="1.5"/>
  <text x="360" y="155" font="600 12px system-ui,sans-serif" fill="#1a1a1a">100</text>
  <rect x="285" y="180" width="110" height="30" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="360" y="200" class="md-op">42</text>
  <text x="340" y="245" class="md-note" fill="#d13c3c" font-weight="600">3 accesos</text>
</svg>

**Modos impropios** (operando explicito o en instruccion):

| Modo | Descripcion | Ejemplo |
|---|---|---|
| **Implicito** (inherente) | El operando esta implicito en la definicion de la instruccion. Usado en acumuladores y pilas. | `INC` (incrementa acumulador), `PUSH A` (usa SP implicitamente) |
| **Inmediato** (literal) | El operando esta incluido en la propia instruccion. Util para inicializar registros con constantes. | `SUMA #42` (suma la constante 42) |

**Modos propios** (operando en memoria):

| Modo | Descripcion | Formula |
|---|---|---|
| **Directo/Absoluto** | El campo de operando contiene la direccion donde esta el dato. | DE = campo_operando |
| **Indirecto** | El campo contiene una direccion donde se encuentra la direccion efectiva del operando. Necesita un acceso extra a memoria. | DE = M[campo_operando] |
| **Relativo a registro base** | Direccion efectiva = contenido del registro base + desplazamiento. Permite codigos reentrantes y reubicables. | DE = BP + desplazamiento |
| **Relativo a registro indice** (indexado) | Direccion efectiva = direccion de memoria (en instruccion) + contenido del registro indice. Util para arrays y bucles. | DE = direccion + IX |

#### 5.5.1. Modos adicionales en arquitecturas reales

Arquitecturas modernas anaden modos compuestos:

- **Pre-indexado**: `[BP+X]`, pre-calcula direccion antes de acceder.
- **Post-indexado**: `[BP], X`, accede a BP y luego incrementa BP por X (util en recorrido de arrays).
- **Base-desplazamiento-escala** (x86): `[BP + IX*4 + 16]` — acceso a elemento de array de enteros de 32 bits con offset.
- **Relativo al PC**: offset desde el contador de programa (saltos relativos, tipicos en ARM/RISC-V).

> **[DATO CLAVE EXAMEN]** En ARM la mayoria de instrucciones aritmetico-logicas operan solo sobre registros; para acceder a memoria se usan exclusivamente `LDR` (load) y `STR` (store) con modos relativo-base y relativo-indice. Es la **arquitectura load-store**, caracteristica fundamental RISC.

---

## 6. Memoria

### 6.1. Clasificaciones

**Por ubicacion**:
- **Memoria interna**: reside dentro o cerca de la CPU (registros, cache, RAM, ROM).
- **Memoria externa**: dispositivos de almacenamiento secundario (SSD, HDD, cinta, nube).

**Por volatilidad**:
- **Volatil**: se borra al perder alimentacion electrica (RAM, registros, cache).
- **No volatil**: persiste tras apagar el equipo (ROM, Flash, SSD, HDD, cinta, optico).

**Por tipo de acceso**:
- **Acceso aleatorio (random)**: cualquier posicion en el mismo tiempo (RAM, ROM, SSD).
- **Acceso secuencial**: hay que recorrer posiciones intermedias (cinta).
- **Acceso directo**: zonas accedidas directamente pero con posiciones internas secuenciales (HDD por cilindro/sector).

**Por jerarquia** (piramide de memoria):

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 380" role="img" aria-label="Jerarquia de memoria">
  <style>
    .jm-label{font:600 13px system-ui,sans-serif;fill:#fff;text-anchor:middle}
    .jm-speed{font:11px system-ui,sans-serif;fill:#555;text-anchor:start}
  </style>
  <text x="320" y="28" text-anchor="middle" font="700 16px system-ui,sans-serif" fill="#0055a0">Jerarquia de memoria</text>
  <polygon points="295,55 345,55 360,85 280,85" fill="#003d73"/>
  <text x="320" y="75" class="jm-label">Registros</text>
  <polygon points="280,85 360,85 375,120 265,120" fill="#0055a0"/>
  <text x="320" y="108" class="jm-label">Cache L1</text>
  <polygon points="265,120 375,120 395,160 245,160" fill="#0055a0" opacity="0.85"/>
  <text x="320" y="144" class="jm-label">Cache L2 / L3</text>
  <polygon points="245,160 395,160 420,210 220,210" fill="#3378b9"/>
  <text x="320" y="189" class="jm-label">RAM</text>
  <polygon points="220,210 420,210 450,265 190,265" fill="#6ea3d2"/>
  <text x="320" y="242" class="jm-label" fill="#1a1a1a">SSD</text>
  <polygon points="190,265 450,265 485,320 155,320" fill="#d6e4f0"/>
  <text x="320" y="295" class="jm-label" fill="#1a1a1a">HDD / cinta / nube</text>
  <text x="500" y="75" class="jm-speed">~0,3 ns · KB</text>
  <text x="500" y="107" class="jm-speed">~1 ns · 32-64 KB</text>
  <text x="500" y="142" class="jm-speed">~3-20 ns · 1-32 MB</text>
  <text x="500" y="188" class="jm-speed">~100 ns · 8-128 GB</text>
  <text x="500" y="240" class="jm-speed">~50 µs · 1-4 TB</text>
  <text x="500" y="292" class="jm-speed">~10 ms · 1-20 TB</text>
</svg>

> **[DATO CLAVE EXAMEN]** **Regla fundamental**: a mayor velocidad, menor capacidad y mayor coste por byte. Cada nivel de la jerarquia es ~10-100× mas lento y ~10-100× mas grande que el anterior.

### 6.2. Memoria RAM

La **memoria RAM** (*Random Access Memory*) es memoria principal de tipo **volatil**: su contenido se pierde al apagar el sistema. [JEDEC-DDR]

**Funcion**: almacenar temporalmente los datos e instrucciones que utiliza el procesador durante la ejecucion de programas. Actua como espacio de trabajo intermedio entre la CPU (muy rapida, poca capacidad) y la memoria secundaria (lenta, mucha capacidad).

**Caracteristica principal**: **acceso aleatorio** — se puede leer/escribir en cualquier posicion en el mismo tiempo, independientemente de su ubicacion. Este es el **acceso aleatorio** que da nombre a la RAM.

#### 6.2.1. SRAM vs DRAM

Dos tecnologias fundamentales de RAM:

- **SRAM** (Static RAM): basada en biestables (6 transistores por bit). **Rapida** (~1-3 ns), **cara** (mas transistores), **baja densidad**, no requiere refresco. Uso: **memoria cache** (L1, L2, L3) integrada en la CPU.
- **DRAM** (Dynamic RAM): basada en un condensador + un transistor por bit. **Lenta** (~50-100 ns), **barata**, **alta densidad**, **requiere refresco** periodico (cada ~64 ms) porque los condensadores pierden carga. Uso: **memoria principal** del ordenador.

> **[DATO CLAVE EXAMEN]** La **DRAM necesita refresco**: un circuito lee y reescribe cada celda cada pocos milisegundos para evitar que se pierda la informacion. Esto consume ancho de banda y energia. La SRAM no necesita refresco.

#### 6.2.2. Evolucion de la memoria RAM

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 720 340" role="img" aria-label="Evolucion de la memoria RAM">
  <style>
    .ram-year{font:600 11px system-ui,sans-serif;fill:#0055a0;text-anchor:middle}
    .ram-name{font:700 12px system-ui,sans-serif;fill:#1a1a1a;text-anchor:middle}
    .ram-spec{font:10px system-ui,sans-serif;fill:#555;text-anchor:middle}
  </style>
  <text x="360" y="28" text-anchor="middle" font="700 16px system-ui,sans-serif" fill="#0055a0">Evolucion de la memoria RAM</text>
  <line x1="40" y1="240" x2="690" y2="240" stroke="#0055a0" stroke-width="2"/>
  <rect x="55" y="210" width="35" height="30" fill="#d6e4f0" stroke="#0055a0"/>
  <text x="72" y="200" class="ram-year">60s</text>
  <text x="72" y="260" class="ram-name">DIP</text>
  <rect x="115" y="195" width="40" height="45" fill="#d6e4f0" stroke="#0055a0"/>
  <text x="135" y="185" class="ram-year">1983</text>
  <text x="135" y="260" class="ram-name">SIPP</text>
  <rect x="180" y="180" width="45" height="60" fill="#d6e4f0" stroke="#0055a0"/>
  <text x="202" y="170" class="ram-year">1987</text>
  <text x="202" y="260" class="ram-name">SIMM</text>
  <rect x="250" y="160" width="50" height="80" fill="#3378b9" stroke="#0055a0"/>
  <text x="275" y="150" class="ram-year">1993</text>
  <text x="275" y="260" class="ram-name">DIMM</text>
  <rect x="325" y="140" width="52" height="100" fill="#3378b9" stroke="#0055a0"/>
  <text x="351" y="130" class="ram-year">2000</text>
  <text x="351" y="260" class="ram-name">DDR</text>
  <rect x="400" y="120" width="52" height="120" fill="#0055a0"/>
  <text x="426" y="110" class="ram-year">2003</text>
  <text x="426" y="260" class="ram-name">DDR2</text>
  <rect x="475" y="95" width="54" height="145" fill="#0055a0"/>
  <text x="502" y="85" class="ram-year">2007</text>
  <text x="502" y="260" class="ram-name">DDR3</text>
  <rect x="552" y="65" width="56" height="175" fill="#0055a0"/>
  <text x="580" y="55" class="ram-year">2014</text>
  <text x="580" y="260" class="ram-name">DDR4</text>
  <rect x="632" y="30" width="58" height="210" fill="#2d8659"/>
  <text x="661" y="20" class="ram-year" fill="#2d8659">2021</text>
  <text x="661" y="260" class="ram-name" fill="#2d8659">DDR5</text>
</svg>

| Tecnologia | Anos | Descripcion |
|---|---|---|
| **Nucleos de Ferrita** | 1950-1970 | Malla con nucleos magneticos de ferrita en las intersecciones |
| **DIP** (Dual In-line Package) | 1960-70 | Basadas en transistores, chips encapsulados |
| **SIPP** (Single In-line Pin Package) | 1983 | Modulos de 30 pines. Uso en Intel 80286 |
| **SIMM** (Single In-line Memory Module) | 1987 | Contactos planos en lugar de pines, muesca de orientacion. Uso en 80486. 30 o 72 contactos. 32 bits |
| **DIMM** (Dual In-line Memory Module) | 1993 | Chips en ambas caras. 168 contactos, 2 muescas. **64 bits** |
| **DDR DIMM** (Double Data Rate) | 2000 | Evolucion DIMM con doble tasa de transferencia (flanco subida + bajada). 184 contactos |

#### 6.2.3. Tabla comparativa DDR (la tabla que SIEMPRE aparece en examenes)

| Especificacion | DDR | DDR2 | DDR3 | DDR4 | **DDR5** |
|---|---|---|---|---|---|
| **Ano introduccion** | 2000 | 2003 | 2007 | 2014 | 2021 |
| **Voltaje** | 2,5 V | 1,8 V | 1,5 V | 1,2 V | 1,1 V |
| **Frecuencia efectiva (MT/s)** | 200-400 | 400-1066 | 800-2133 | 2133-4800 | 4800-8400 |
| **Ancho de banda maximo** | 3,2 GB/s | 8,5 GB/s | 17 GB/s | 38,4 GB/s | **67,2 GB/s** |
| **Capacidad maxima por modulo** | 1 GB | 8 GB | 16 GB | 64 GB | **128 GB** |
| **Pines (DIMM)** | 184 | 240 | 240 | 288 | 288 |

> **[DATO CLAVE EXAMEN]** DDR2 y DDR3 tienen los **mismos 240 pines** pero son **fisica y electricamente incompatibles** (la muesca esta en distinta posicion, y el voltaje es distinto: 1,8 V vs 1,5 V). Analogamente, DDR4 y DDR5 tienen **los mismos 288 pines** pero son incompatibles (voltajes 1,2 V vs 1,1 V, topologia distinta: DDR5 integra el PMIC en el modulo).

#### 6.2.4. Tipos especiales de RAM

| Tipo | Descripcion | Uso |
|---|---|---|
| **RIMM** (Rambus In-line Memory Module) | Modulos Rambus con disipador integrado, 232 contactos | Memorias RDRAM (muerto comercialmente) |
| **FB-DIMM** (Fully Buffered DIMM) | Datos en serie, menos lineas, mayor velocidad | Servidores (obsoleto) |
| **GDDR** (Graphics DDR) | DDR optimizada para graficas, integrada en la GPU | Tarjetas graficas (GDDR6X actual) |
| **SO-DIMM** (Small Outline DIMM) | Version compacta de DIMM (~50% mas pequena) | Portatiles, NUCs |
| **Micro-DIMM** | Mas pequeno que SO-DIMM | Dispositivos ultracompactos (obsoleto) |
| **LPDDR** (Low-Power DDR) | DDR de bajo consumo, soldada a placa | Smartphones, tablets, ultraportatiles |
| **HBM** (High Bandwidth Memory) | DRAM apilada en 3D, buses muy anchos | GPUs HPC (NVIDIA H100: 3 TB/s) |

#### 6.2.5. RAM ECC vs No-ECC

- **No-ECC**: sin correccion de errores. Uso en PCs domesticos, tablets, portatiles.
- **ECC** (*Error Checking and Correction*): sistema de paridad para **detectar errores de 1 bit y corregirlos**. Detecta errores de 2 bits sin corregirlos. Uso en servidores, estaciones de trabajo profesionales. Requiere soporte de placa base y procesador. ~10% mas caro, ~2-3% mas lento.

#### 6.2.6. Parametros de la memoria RAM

| Parametro | Descripcion |
|---|---|
| **Velocidad (MHz/MT/s)** | Millones de operaciones (transferencias) por segundo |
| **Ancho de banda (MB/s o GB/s)** | Maxima cantidad de datos transferida por segundo = velocidad × anchura bus / 8 |
| **Dual Channel / Quad Channel** | La CPU usa 2/4 canales simultaneos, doblando/cuadruplicando ancho de banda. Requiere modulos identicos en slots correctos |
| **Tiempo de acceso (ns)** | Tiempo que tarda la CPU en acceder a la memoria desde la peticion hasta recibir el dato |
| **Latencia** | Retardo entre solicitud y respuesta |
| **Latencia CAS (CL)** | Ciclos de reloj desde la peticion de lectura hasta la entrega de datos. **Cuanto menor, mas rapida** |

#### 6.2.7. RAM-CMOS (BIOS/UEFI)

Memoria de entre **64 y 256 bytes** vinculada al reloj de tiempo real del sistema. Alimentada por la **pila de la placa base** (tecnologia CMOS de bajo consumo).

Almacena la **configuracion del firmware**: velocidad de buses, discos instalados, secuencia de arranque, contrasena, overclock, activacion de dispositivos. La informacion es usada por el BIOS/UEFI durante el arranque.

Si los datos son incorrectos, se genera un error. Para restaurar valores de fabrica: cortar la alimentacion de la pila durante ~30 segundos (jumper CLRTC o retirar pila).

> **[DATO CLAVE EXAMEN]** No confundir **RAM-CMOS** (memoria de configuracion) con **BIOS/UEFI** (firmware en ROM): son entidades distintas, aunque la RAM-CMOS se configura desde la utilidad del BIOS/UEFI.

#### 6.2.8. Memoria virtual y paginacion

La **memoria virtual** es un mecanismo que permite a un proceso usar mas memoria de la fisicamente disponible, combinando RAM con disco como "memoria secundaria virtual". [TANENBAUM-SO, Cap. 3]

Conceptos clave:

- **Pagina**: bloque de tamano fijo de memoria virtual (tipicamente 4 KB).
- **Marco de pagina**: bloque de tamano fijo de memoria fisica, mismo tamano que pagina.
- **Tabla de paginas**: estructura que asocia paginas virtuales a marcos fisicos.
- **TLB** (Translation Lookaside Buffer): cache de la tabla de paginas dentro de la MMU (Memory Management Unit). Critico para rendimiento.
- **Fallo de pagina**: cuando se accede a una pagina no residente en RAM, se produce una interrupcion y el SO la carga desde disco.
- **Swap / fichero de paginacion**: espacio en disco para paginas expulsadas de RAM.

La **MMU** (Memory Management Unit) es el hardware dentro de la CPU que traduce direcciones virtuales a fisicas consultando la tabla de paginas (con cache en TLB).

> **[REFERENCIA CRUZADA]** La memoria virtual se trata en profundidad en el **Tema 20** (Sistemas operativos).

### 6.3. Memoria ROM

La **memoria ROM** (*Read Only Memory*) es memoria principal de tipo **no volatil**: conserva la informacion almacenada al apagar el sistema.

**Funcion**: almacenar de forma permanente programas e instrucciones esenciales, como el **firmware**. Destaca la **BIOS/UEFI**, ubicada en la placa base, con las rutinas basicas de arranque e inicializacion.

#### Tipos de memoria ROM

| Tipo | Descripcion | Reprogramable |
|---|---|---|
| **ROM** (mask ROM) | Programada en fabrica, contenido inalterable. Obsoleta | No |
| **PROM** (Programmable ROM) | Programable una unica vez por el usuario mediante un programador PROM. Depende de fusibles que se queman una sola vez | Una vez |
| **EPROM** (Erasable PROM) | Borrable mediante **exposicion a luz ultravioleta** (ventana de cuarzo). Reprogramable electricamente | Si (UV + electrica) |
| **EEPROM** (Electrically EPROM) | Borrable y reprogramable **electricamente**, byte a byte. Permite sobreescritura sin extraer el chip | Si (electrica) |
| **Flash** | Variante de EEPROM. Borrado y escritura **en bloques** (no byte a byte). Ampliamente utilizada: pendrives, SSD, tarjetas SD, firmware actual | Si (por bloques) |

#### 6.3.1. NAND Flash vs NOR Flash

Dentro de Flash, dos subtipos con casos de uso distintos:

| Aspecto | NOR Flash | NAND Flash |
|---|---|---|
| Acceso | Aleatorio, byte a byte | Por bloques (paginas) |
| Lectura | Rapida | Lenta |
| Escritura | Lenta | Rapida |
| Densidad | Baja | **Alta** (10× NOR) |
| Coste/bit | Alto | **Bajo** |
| Durabilidad (ciclos escritura) | ~100.000 | ~10.000-100.000 |
| Uso | Firmware, codigo ejecutable (BIOS) | **SSD, pendrives, moviles, SD** |

La **NAND Flash** domina el mercado de almacenamiento masivo por su densidad y coste. Se divide en sub-tecnologias segun bits por celda:

- **SLC** (Single-Level Cell, 1 bit/celda): mas rapida, duradera, cara.
- **MLC** (2 bits/celda): balance. Obsoleto en consumo.
- **TLC** (Triple-Level Cell, 3 bits/celda): actual dominante en SSDs consumo.
- **QLC** (4 bits/celda): maxima densidad, minima duracion.

### 6.4. BIOS y UEFI

Ambos son **firmware**: codigo almacenado en memoria no volatil en la placa base que contiene las instrucciones de control de los circuitos del equipo. [UEFI-SPEC]

**BIOS** (*Basic Input Output System*) — Creado en 1975:

- Al encender, inicializa, configura y comprueba el hardware (RAM, discos, placa base, GPU) mediante el **POST** (Power-On Self-Test).
- Selecciona el dispositivo de arranque y lanza el sistema operativo (carga el bootloader desde el MBR).
- Gestiona energia, temperatura, basico de E/S.

**UEFI** (*Unified Extensible Firmware Interface*) — Sucesor del BIOS, escrito en C:

- Desarrollado inicialmente por Intel como **EFI** (2005), transferido a la UEFI Forum en 2007.
- Realiza todo lo del BIOS + funciones adicionales (red, GUI, etc.).
- Estandar obligatorio en Windows 8+ (arranque seguro), macOS, la mayoria de Linux.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 360" role="img" aria-label="Comparativa BIOS vs UEFI">
  <style>
    .bu-title{font:700 16px system-ui,sans-serif;text-anchor:middle}
    .bu-row{font:11px system-ui,sans-serif;fill:#1a1a1a}
    .bu-aspect{font:600 11px system-ui,sans-serif;fill:#0055a0;text-anchor:middle}
  </style>
  <text x="340" y="28" text-anchor="middle" font="700 16px system-ui,sans-serif" fill="#0055a0">BIOS vs UEFI</text>
  <rect x="30" y="50" width="200" height="290" rx="6" fill="#f5f5f5" stroke="#999"/>
  <text x="130" y="78" class="bu-title" fill="#666">BIOS · 1975</text>
  <rect x="250" y="50" width="180" height="290" rx="6" fill="#eef4fa" stroke="#0055a0" stroke-width="2"/>
  <text x="340" y="110" class="bu-aspect">Arquitectura</text>
  <text x="340" y="135" class="bu-aspect">Interfaz</text>
  <text x="340" y="160" class="bu-aspect">Conectividad</text>
  <text x="340" y="185" class="bu-aspect">Particiones</text>
  <text x="340" y="210" class="bu-aspect">Capacidad max</text>
  <text x="340" y="235" class="bu-aspect">Arranque</text>
  <text x="340" y="260" class="bu-aspect">Seguridad</text>
  <text x="340" y="285" class="bu-aspect">Extensibilidad</text>
  <rect x="450" y="50" width="200" height="290" rx="6" fill="#d8f0dc" stroke="#2d8659"/>
  <text x="550" y="78" class="bu-title" fill="#2d8659">UEFI</text>
  <text x="130" y="115" class="bu-row" text-anchor="middle">16 bits</text>
  <text x="550" y="115" class="bu-row" text-anchor="middle" fill="#2d8659">32/64 bits</text>
  <text x="130" y="140" class="bu-row" text-anchor="middle">Texto</text>
  <text x="550" y="140" class="bu-row" text-anchor="middle" fill="#2d8659">GUI · raton</text>
  <text x="130" y="165" class="bu-row" text-anchor="middle" fill="#d13c3c">Aislado</text>
  <text x="550" y="165" class="bu-row" text-anchor="middle" fill="#2d8659">Internet</text>
  <text x="130" y="190" class="bu-row" text-anchor="middle" fill="#d13c3c">4 MBR</text>
  <text x="550" y="190" class="bu-row" text-anchor="middle" fill="#2d8659">128 GPT</text>
  <text x="130" y="215" class="bu-row" text-anchor="middle" fill="#d13c3c">2,2 TB</text>
  <text x="550" y="215" class="bu-row" text-anchor="middle" fill="#2d8659">8 ZB</text>
  <text x="130" y="240" class="bu-row" text-anchor="middle">Lento ~30s</text>
  <text x="550" y="240" class="bu-row" text-anchor="middle" fill="#2d8659">Rapido ~5s</text>
  <text x="130" y="265" class="bu-row" text-anchor="middle" fill="#d13c3c">Sin verific.</text>
  <text x="550" y="265" class="bu-row" text-anchor="middle" fill="#2d8659">Secure Boot</text>
  <text x="130" y="290" class="bu-row" text-anchor="middle" fill="#d13c3c">Firme</text>
  <text x="550" y="290" class="bu-row" text-anchor="middle" fill="#2d8659">Modular</text>
</svg>

**Diferencias UEFI vs BIOS** (resumen en tabla):

| Aspecto | BIOS | UEFI |
|---|---|---|
| Interfaz | Consola MS-DOS, solo teclado | GUI moderna, raton, animaciones |
| Conectividad | Sin internet | Puede conectarse a internet para actualizarse |
| Codigo | 16 bits (modo real) | 32 o 64 bits (modo protegido) |
| Arranque | Mas lento (30 s) | Mas rapido (5 s) |
| Seguridad | Sin verificacion | **Secure Boot** (valida firma digital del bootloader) |
| TPM | Opcional | TPM 2.0 integrado (Windows 11 obligatorio) |
| Almacenamiento | Solo recursos especificos | Cualquier memoria no volatil, extensible |
| Particiones | **4 particiones MBR** (max 2,2 TB) | **128 particiones GPT** (max 8 ZB) |
| CSM | Nativo | Compatibilidad con BIOS legacy |

> **[DATO CLAVE EXAMEN]** **Secure Boot** verifica la firma digital del bootloader antes de ejecutarlo. Impide el arranque de rootkits y bootkits. Es obligatorio para Windows 11. Se puede desactivar en UEFI para arrancar Linux no firmado (aunque Linux moderno ya soporta Secure Boot con claves de Microsoft o Red Hat).

---

## 7. Medidas de capacidad de memoria

| Unidad | Descripcion | Equivalencia binaria | Equivalencia decimal (SI) |
|---|---|---|---|
| **Bit** | Digito binario (0 o 1). Unidad minima | — | — |
| **Nibble** | Grupo de 4 bits | 4 bits | 4 bits |
| **Byte (B)** | Grupo de 8 bits. Unidad mas pequena que representa un caracter | 8 bits | 8 bits |
| **Palabra (word)** | Grupo fijo de bits procesados como unidad (varia por arquitectura: 16, 32, 64 bits) | Variable | Variable |
| **Kilobyte (KB / KiB)** | | 1.024 B = 2^10 | 1.000 B = 10^3 |
| **Megabyte (MB / MiB)** | | 1.048.576 B = 2^20 | 10^6 B |
| **Gigabyte (GB / GiB)** | | 2^30 B | 10^9 B |
| **Terabyte (TB / TiB)** | | 2^40 B | 10^12 B |
| **Petabyte (PB / PiB)** | | 2^50 B | 10^15 B |
| **Exabyte (EB / EiB)** | | 2^60 B | 10^18 B |
| **Zettabyte (ZB / ZiB)** | | 2^70 B | 10^21 B |
| **Yottabyte (YB / YiB)** | | 2^80 B | 10^24 B |

### 7.1. IEC (binario) vs SI (decimal)

Historicamente, la informatica usa potencias de 2 (1024) para cuantificar memoria, pero el Sistema Internacional usa potencias de 10 (1000). Esto genera **ambiguedad** — ¿1 MB son 1.048.576 bytes o 1.000.000 bytes?

La **norma IEC 60027-2** (2000) introdujo nuevos prefijos **binarios** para evitar ambiguedad:

| Prefijo IEC (binario) | Simbolo | Valor | Prefijo SI (decimal) | Simbolo | Valor |
|---|---|---|---|---|---|
| Kibibyte | KiB | 2^10 (1.024) | Kilobyte | KB | 10^3 (1.000) |
| Mebibyte | MiB | 2^20 | Megabyte | MB | 10^6 |
| Gibibyte | GiB | 2^30 | Gigabyte | GB | 10^9 |
| Tebibyte | TiB | 2^40 | Terabyte | TB | 10^12 |

**Convenciones actuales**:
- **RAM**: siempre se mide en **potencias de 2** (16 GB RAM = 16 × 2^30 B = 17,18 GB decimales).
- **Discos duros y SSD**: los fabricantes usan **potencias de 10** (1 TB SSD = 10^12 B = 931 GiB binarios — por eso "falta" espacio).
- **Sistemas operativos**: Windows usa binario (muestra 931 GB en un disco de 1 TB), macOS y Linux usan decimal (muestran 1 TB correctamente).
- **Redes**: siempre **decimal** (100 Mbps = 10^8 bits/s).

> **[EJERCICIO RESUELTO]** **Problema**: Compras un SSD de **2 TB**. ¿Cuantos bytes tendras disponibles realmente en un sistema Windows?
>
> **Solucion**: El fabricante anuncia 2 TB = 2 × 10^12 bytes = 2.000.000.000.000 B. Windows los interpreta en binario: 2.000.000.000.000 / 2^40 ≈ 1,819 TiB. Windows mostrara **aproximadamente 1,82 TB** (aunque internamente son TiB). Es decir, "faltan" unos 181 GB por la diferencia binario/decimal. No es un engano, es la diferencia de convenciones.

### 7.2. Volumenes reales

Algunas magnitudes de referencia para contextualizar:

- Biblia en texto: ~5 MB
- Foto de smartphone 2024 (48 MP): ~12 MB
- Pelicula 4K 2h: ~60 GB
- Wikipedia en espanol (texto, 2024): ~80 GB
- Todos los libros publicados en Espana (2024): ~5 TB
- Datos generados diarios por usuario promedio: ~1,7 MB/s (todas las interacciones digitales)
- Datos generados diariamente a nivel mundial (2025): ~400 EB
- Estimacion volumen total de datos en el mundo (2025): ~181 ZB (IDC)

---

## 8. Sistemas de numeracion

Un sistema de numeracion es un conjunto de simbolos y reglas que permiten construir numeros validos. [STALLINGS-COA, Cap. 9]

| Sistema | Base | Simbolos | Uso principal |
|---|---|---|---|
| **Decimal** | 10 | 0-9 | Uso humano cotidiano |
| **Binario** | 2 | 0, 1 | Uso interno de ordenadores y sistemas digitales |
| **Octal** | 8 | 0-7 | Representacion compacta de binario (permisos Unix) |
| **Hexadecimal** | 16 | 0-9, A-F | Direcciones de memoria, colores, MAC, codigo maquina |

> **[DATO CLAVE EXAMEN]** El sistema **binario** es el utilizado por los ordenadores de forma interna para todos los procesos. Hexadecimal se usa como notacion corta para binario (cada digito hex = 4 bits).

### 8.1. Conversion entre bases

**Decimal a binario** (divisiones sucesivas):

> **[EJERCICIO RESUELTO]** Convertir 25 decimal a binario:
>
> ```
> 25 ÷ 2 = 12 resto 1  ←
> 12 ÷ 2 = 6  resto 0  ← (leer de abajo a arriba)
>  6 ÷ 2 = 3  resto 0
>  3 ÷ 2 = 1  resto 1
>  1 ÷ 2 = 0  resto 1
> ```
> Resultado: **25₁₀ = 11001₂**
>
> Verificacion: 1·16 + 1·8 + 0·4 + 0·2 + 1·1 = 25. Correcto.

**Binario a decimal** (suma ponderada):

> **[EJERCICIO RESUELTO]** Convertir 10110₂ a decimal:
>
> 10110₂ = 1·2⁴ + 0·2³ + 1·2² + 1·2¹ + 0·2⁰ = 16 + 0 + 4 + 2 + 0 = **22₁₀**

**Binario a hexadecimal** (agrupar en nibbles de 4 bits):

> **[EJERCICIO RESUELTO]** Convertir 11010111₂ a hexadecimal:
>
> 1101 0111 → D 7 → **D7₁₆**

**Hexadecimal a binario**: cada digito hex se expande a 4 bits:
- 0→0000, 1→0001, 2→0010, ..., 9→1001, A→1010, B→1011, C→1100, D→1101, E→1110, F→1111.

### 8.2. Representacion de numeros negativos: complemento a 2

El ordenador no tiene un "signo menos"; solo tiene bits. Para representar numeros negativos se usa **complemento a 2** (el estandar practicamente universal).

**Para obtener el complemento a 2 de un numero binario**:
1. Invertir todos los bits (complemento a 1).
2. Sumar 1 al resultado.

> **[EJERCICIO RESUELTO]** Representar **-5** en binario de 8 bits usando complemento a 2:
>
> - 5 en binario 8 bits: 0000 0101
> - Complemento a 1 (invertir): 1111 1010
> - Sumar 1: 1111 1010 + 1 = **1111 1011**
>
> Por tanto, -5 en 8 bits (C2) = **11111011₂ = FB₁₆**. El bit mas significativo a 1 indica negativo.

Con 8 bits en complemento a 2 se representa el rango **-128 a +127** (el 0 tiene una unica representacion, a diferencia de otras convenciones).

### 8.3. Representacion en coma flotante: IEEE 754

Para numeros reales (fraccionarios, muy grandes o muy pequenos) se usa el estandar **IEEE 754** (1985, revisado 2008, 2019). [IEEE-754]

Un numero real se representa como:

```
valor = (-1)^signo × mantisa × 2^exponente
```

**Formatos estandar**:

| Formato | Bits totales | Signo | Exponente | Mantisa | Rango aproximado |
|---|---|---|---|---|---|
| **Half** (FP16) | 16 | 1 | 5 | 10 | ±65.504 |
| **Single** (FP32, float) | 32 | 1 | 8 | 23 | ±3,4×10^38 |
| **Double** (FP64, double) | 64 | 1 | 11 | 52 | ±1,8×10^308 |
| **Quad** (FP128) | 128 | 1 | 15 | 112 | ±1,2×10^4932 |

**Valores especiales**: +0, -0, +∞, -∞, NaN (Not a Number).

> **[DATO CLAVE EXAMEN]** IEEE 754 single precision (float 32 bits): **1 bit signo + 8 bits exponente + 23 bits mantisa**. Double precision (64 bits): **1 + 11 + 52**.

---

## 9. Juegos de caracteres

### 9.1. ASCII

**ASCII** (*American Standard Code for Information Interchange*): codigo de caracteres basado en el alfabeto latino. Creado en **1963** por el Comite Estadounidense de Estandares (ASA, luego ANSI). [RFC-20]

- Utiliza **7 bits** para representar caracteres.
- Define **33 caracteres no imprimibles** (control: NUL, SOH, BEL, BS, TAB, LF, CR, ESC, DEL...) + **95 caracteres imprimibles** (desde el espacio).
- En total: **128 caracteres** (2^7 = 128).
- Inicialmente usaba un bit adicional de paridad para deteccion de errores en transmision.

**Caracteres ASCII notables**:

| Codigo | Caracter | Nombre |
|---|---|---|
| 0 | NUL | Null |
| 10 | LF | Line Feed (salto de linea Unix) |
| 13 | CR | Carriage Return (retorno carro) |
| 32 | (espacio) | Space |
| 48-57 | 0-9 | Digitos |
| 65-90 | A-Z | Mayusculas |
| 97-122 | a-z | Minusculas |
| 127 | DEL | Delete |

### 9.2. ASCII extendido

Cualquier juego de caracteres de **8 bits** donde los codigos 32-126 coinciden con los caracteres imprimibles de ASCII. Los codigos 128-255 se usan para caracteres adicionales (acentos, caracteres especiales).

Codificaciones mas comunes:

- **Codepage 437**: IBM PC / MS-DOS en ingles.
- **Codepage 850**: IBM PC / MS-DOS Europa occidental (incluye n, acentos).
- **ISO 8859-1** (Latin-1): Unix, Europa occidental.
- **Windows-1252**: variante Latin-1 de Microsoft, con algunas diferencias en caracteres 128-159.
- **ISO 8859-15** (Latin-9): version actualizada de Latin-1 con soporte para € y otros.

Problema fundamental: no hay forma de combinar multiples idiomas en un mismo documento.

### 9.3. Unicode y UTF-8

**Unicode**: estandar de codificacion disenado para representar texto de **todos los lenguajes del mundo** en un unico sistema. Nombre proviene de tres objetivos: **universalidad, uniformidad, unicidad**. [UNICODE-STD]

Especifica un nombre e identificador numerico unico (**code point**) para cada caracter. Trata caracteres alfabeticos, ideograficos y simbolos de forma equivalente.

- Version actual: **Unicode 15.1** (2023).
- Define **149.186 caracteres** (2024) repartidos en **17 planos** de 65.536 caracteres cada uno.
- Cubre >160 scripts (alfabetos) y ademas simbolos matematicos, musicales, emojis.

**UTF-8** (*8-bit Unicode Transformation Format*): formato de codificacion de longitud variable de **1 a 4 bytes por caracter**. Es la codificacion **dominante en la web** (~98% de paginas en 2024).

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 320" role="img" aria-label="Estructura de UTF-8">
  <style>
    .u8-title{font:700 16px system-ui,sans-serif;text-anchor:middle;fill:#0055a0}
    .u8-len{font:700 12px system-ui,sans-serif;fill:#0055a0}
    .u8-bits{font:600 11px monospace;fill:#fff;text-anchor:middle}
    .u8-range{font:italic 11px system-ui,sans-serif;fill:#555}
  </style>
  <text x="340" y="28" class="u8-title">Estructura de UTF-8</text>
  <text x="35" y="85" class="u8-len">1 byte</text>
  <rect x="100" y="68" width="80" height="28" fill="#0055a0"/>
  <text x="140" y="86" class="u8-bits">0xxxxxxx</text>
  <text x="195" y="85" class="u8-range">U+0000 - U+007F  ·  ASCII</text>
  <text x="35" y="135" class="u8-len">2 bytes</text>
  <rect x="100" y="118" width="80" height="28" fill="#0055a0"/>
  <text x="140" y="136" class="u8-bits">110xxxxx</text>
  <rect x="182" y="118" width="80" height="28" fill="#3378b9"/>
  <text x="222" y="136" class="u8-bits">10xxxxxx</text>
  <text x="275" y="135" class="u8-range">U+0080 - U+07FF  ·  Latin extendido</text>
  <text x="35" y="185" class="u8-len">3 bytes</text>
  <rect x="100" y="168" width="80" height="28" fill="#0055a0"/>
  <text x="140" y="186" class="u8-bits">1110xxxx</text>
  <rect x="182" y="168" width="80" height="28" fill="#3378b9"/>
  <text x="222" y="186" class="u8-bits">10xxxxxx</text>
  <rect x="264" y="168" width="80" height="28" fill="#3378b9"/>
  <text x="304" y="186" class="u8-bits">10xxxxxx</text>
  <text x="355" y="185" class="u8-range">U+0800 - U+FFFF  ·  BMP (CJK)</text>
  <text x="35" y="235" class="u8-len">4 bytes</text>
  <rect x="100" y="218" width="80" height="28" fill="#0055a0"/>
  <text x="140" y="236" class="u8-bits">11110xxx</text>
  <rect x="182" y="218" width="80" height="28" fill="#3378b9"/>
  <text x="222" y="236" class="u8-bits">10xxxxxx</text>
  <rect x="264" y="218" width="80" height="28" fill="#3378b9"/>
  <text x="304" y="236" class="u8-bits">10xxxxxx</text>
  <rect x="346" y="218" width="80" height="28" fill="#3378b9"/>
  <text x="386" y="236" class="u8-bits">10xxxxxx</text>
  <text x="435" y="235" class="u8-range">U+10000+  ·  emojis, suplement.</text>
</svg>

| Bytes | Caracteres cubiertos | Rango Unicode |
|---|---|---|
| 1 byte | US-ASCII (128 caracteres) | U+0000 - U+007F |
| 2 bytes | Latin extendido, griego, cirilico, hebreo, arabe (~1.920) | U+0080 - U+07FF |
| 3 bytes | Plano basico multilingue (BMP), incluido CJK | U+0800 - U+FFFF |
| 4 bytes | Planos suplementarios (matematicos, historicos, emojis) | U+10000 - U+10FFFF |

**Ventajas de UTF-8**:
- **Compatible 100% con US-ASCII** (los primeros 128 caracteres son identicos).
- **Eficiente en textos latinos** (1 byte por caracter ASCII, 2 para acentos).
- **Autosincronizacion**: puede identificarse el inicio de cada caracter desde cualquier byte. Si se pierde un byte, el siguiente se puede reconocer.
- **Sin solapamiento** entre bytes de diferentes caracteres.
- **Independiente del endianness** (no requiere BOM).

**Desventajas de UTF-8**:
- Caracteres CJK ocupan 3 bytes (vs 2 en UTF-16).
- Acceso directo a posiciones dificil (requiere recorrido secuencial por longitud variable).
- Mayor coste computacional en ordenacion/indexacion vs UTF-16/UTF-32.

### 9.4. UTF-16 y UTF-32

- **UTF-16**: longitud variable 2 o 4 bytes. Usado internamente por Windows NT, Java, JavaScript. Los caracteres BMP se representan en 2 bytes, los suplementarios en 4 (surrogate pairs).
- **UTF-32**: longitud fija 4 bytes por caracter. Ventaja: acceso O(1) por indice. Desventaja: ocupa 4× mas espacio. Raro en practica.

### 9.5. BOM (Byte Order Mark)

Caracter especial `U+FEFF` (ZERO WIDTH NO-BREAK SPACE) colocado al inicio de un fichero para indicar:
- **UTF-8**: `EF BB BF` — opcional, identifica codificacion.
- **UTF-16 BE** (big endian): `FE FF`.
- **UTF-16 LE** (little endian): `FF FE`.
- **UTF-32 BE**: `00 00 FE FF`.

### 9.6. Normalizacion Unicode

Un mismo caracter puede representarse de varias formas: "n" puede ser U+00F1 (un solo code point) o U+006E U+0303 (n + tilde combinante). Para comparar cadenas de forma consistente se usan **formas de normalizacion**:

| Forma | Nombre | Proposito |
|---|---|---|
| **NFC** | Canonical Composition | Forma compuesta (preferida en web) |
| **NFD** | Canonical Decomposition | Forma descompuesta |
| **NFKC** | Compatibility Composition | Compuesta con equivalencias de compatibilidad |
| **NFKD** | Compatibility Decomposition | Descompuesta con equivalencias |

### 9.7. EBCDIC

**EBCDIC** (*Extended Binary Coded Decimal Interchange Code*): codigo de caracteres de **8 bits** desarrollado por **IBM** en 1963 para su System/360. Usado en sistemas **mainframe** IBM (z/OS).

- 1 byte por caracter = 256 combinaciones posibles.
- Existen **multiples variantes** (code pages) segun idioma/entorno (EBCDIC-37 ingles, EBCDIC-500 internacional, EBCDIC-284 espanol).
- **No es compatible con ASCII** — las letras A-Z no estan en orden contiguo.

> **[DATO CLAVE EXAMEN]** EBCDIC es **incompatible** con ASCII: las letras no estan ordenadas de forma contigua (A=193, B=194... pero I=201 y J=209 — hay huecos). Esta particularidad causa problemas en migraciones mainframe-PC.

### 9.8. ISO/IEC 10646

Norma internacional **equivalente a Unicode** en terminos de repertorio de caracteres, mantenida por ISO/IEC. Originalmente eran proyectos separados (ISO empezo en 1984, Unicode Consortium en 1987), pero en 1991 se fusionaron en un estandar unificado.

Formalmente, Unicode es una **implementacion mas rica** de ISO/IEC 10646 — incluye propiedades de caracteres, algoritmos de normalizacion, ordenacion, etc.

> **[REFERENCIA CRUZADA]** Las codificaciones de caracteres se amplian en el **Tema 16** (Comunicacion de datos) y su aplicacion web en el **Tema 34** (Internet y servicios web).

---

*Documento generado con asistencia de IA — Pendiente validacion humana (Maria / Ana)*
*Fuentes: ver tema-11-fuentes.md · Diagramas: ver tema-11-diagramas.md · Cambios: ver tema-11-changelog.md*
*Version 2.0 — Fecha: 2026-04-23*
