# Tema 11 — Contenido Teorico

> **Titulo oficial**: Informatica basica. Representacion y comunicacion de la informacion: elementos constitutivos de un sistema de informacion. Caracteristicas y funciones. Arquitectura de ordenadores. Componentes internos de los equipos microinformaticos.
>
> **Bloque**: Parte II — Tecnico
> **Nivel**: C1 — Tecnico Auxiliar TIC, Ayuntamiento de Madrid
> **Estado**: PILOTO v1.0 — Pendiente validacion
> **Fecha generacion**: 2026-04-16
> **Fuentes**: Ver tema-11-fuentes.md

---

## 1. Concepto de dato e informacion

### 1.1. Definicion de dato

Un **dato** es una representacion simbolica (numerica, alfabetica, alfanumerica) de un atributo o variable cuantitativa o cualitativa. Los datos describen hechos empiricos, sucesos y entidades. [ISO-2382]

Los datos constituyen la **minima unidad semantica** y se corresponden con elementos primarios de informacion que, por si solos, son irrelevantes — no contienen significado contextual ni orientan la toma de decisiones.

> **Ejemplo**: El valor "42" es un dato. Por si solo no aporta informacion util.

### 1.2. Definicion de informacion

La **informacion** es el resultado de procesar, contextualizar y organizar datos, de modo que adquieren significado util para el receptor y permiten la toma de decisiones. [ISO-2382]

> **Ejemplo**: "42 aprobados de 90 presentados" es informacion — aporta contexto y utilidad.

La informacion debe cumplir dos requisitos fundamentales:

- **Integridad**: todos los datos necesarios estan disponibles.
- **Inequivocidad**: no se generan dudas sobre su significado.

Adicionalmente, para que la informacion sea util debe ser: **relevante, precisa, completa y adecuada**.

**Formula conceptual**:

```
Informacion = Datos + Contexto (anadir valor) + Utilidad (disminuir la incertidumbre)
```

### 1.3. Clasificacion de datos

La clasificacion de los datos en informatica no responde a un unico criterio. Las clasificaciones son complementarias, no excluyentes.

**Segun su funcion en el sistema de informacion** (clasificacion mas relevante):

| Tipo | Descripcion |
|---|---|
| **Datos de entrada** | Se introducen en el sistema para su tratamiento. Proceden de usuarios o dispositivos de entrada (teclado, escaner, etc.) |
| **Datos intermedios** | Se generan durante el procesamiento. No son visibles para el usuario final, pero son necesarios para la ejecucion interna |
| **Datos de salida** | Resultado final del procesamiento. Se presentan al usuario como informacion util a traves de dispositivos de salida |

**Segun su naturaleza**:

- **Datos numericos**: representan cantidades, permiten operaciones matematicas.
- **Datos alfabeticos**: formados exclusivamente por letras.
- **Datos alfanumericos**: combinan letras, numeros y otros caracteres.

**Segun su variabilidad**:

- **Datos fijos o constantes**: su valor no cambia durante la ejecucion.
- **Datos variables**: pueden modificarse durante el proceso.

---

## 2. Sistemas de informacion

### 2.1. Definicion y concepto

Un **sistema de informacion** es un conjunto de elementos (aplicaciones, maquinaria, usuarios, procedimientos) disenado para el tratamiento de informacion, de manera que esta quede disponible de forma eficiente para su uso posterior. [ISO-2382]

Los sistemas de informacion ayudan a administrar, recolectar, recuperar, procesar, almacenar y distribuir informacion relevante para los procesos de una organizacion.

> **Nota importante**: El termino "sistema de informacion" no es sinonimo de "sistema informatico". Un sistema de informacion no requiere necesariamente componentes informaticos, aunque en la practica la mayoria los incorporan. Los sistemas de informacion informaticos son un subconjunto de los sistemas de informacion en general.

### 2.2. Componentes basicos

Los sistemas de informacion se componen de tres partes principales: **personas, procesos de negocio y tecnologias de la informacion**. Desglosados:

| Componente | Descripcion |
|---|---|
| **Hardware** | Tecnologia de almacenamiento, comunicaciones, entradas y salidas de datos |
| **Software** | Aplicaciones destinadas a recoger, almacenar, procesar y analizar datos |
| **Datos** | Porciones de informacion donde reside el valor del sistema |
| **Procedimientos** | Politicas y reglas de negocio aplicables a los procesos de la organizacion |
| **Usuarios** | Personas que interactuan con la informacion extraida — componente decisivo para el exito |
| **Red** | Infraestructura que permite compartir recursos entre dispositivos |
| **Retroalimentacion** | Base para la mejora continua del sistema |

### 2.3. Caracteristicas de un sistema de informacion

Para que un sistema de informacion sea considerado como tal, debe cumplir las siguientes caracteristicas:

1. **Disponibilidad** de la informacion cuando se precise y a traves del medio requerido.
2. **Seleccion adecuada**, evitando sobrecarga o informacion irrelevante.
3. **Adaptacion y personalizacion** en la presentacion, segun el usuario o contexto.
4. **Capacidad de relacion** entre datos o contenidos, facilitando su interpretacion.
5. **Tiempos de respuesta adecuados**, garantizando eficiencia.
6. **Exactitud y calidad** de los datos, asegurando informacion veraz y actualizada.
7. **Flexibilidad**, permitiendo adaptacion a nuevas necesidades.
8. **Fiabilidad**, garantizando funcionamiento correcto y continuo.
9. **Seguridad**, protegiendo la informacion (confidencialidad, integridad y disponibilidad).
10. **Copias de seguridad** periodicas para recuperacion ante fallos.

### 2.4. Elementos funcionales

Un sistema de informacion estandar se estructura en los siguientes elementos:

- **Base de datos**: almacena toda la informacion requerida para la toma de decisiones. La informacion se organiza en registros especificos e identificables.
- **Transacciones**: elementos de interfaz que permiten al usuario consultar, agregar, modificar o eliminar registros.
- **Informes**: elementos mediante los cuales el usuario obtiene registros o informacion estadistica (contar, sumar) segun criterios de busqueda definidos.
- **Procesos**: elementos que, segun una logica predefinida, obtienen informacion de la base de datos y generan nuevos registros. Solo son controlados por el usuario.
- **Usuario**: todas las personas que interactuan con el sistema, desde el nivel ejecutivo hasta el operativo.
- **Procedimientos administrativos**: reglas y politicas que rigen el comportamiento de los usuarios frente al sistema. Deben asegurar que nunca un usuario tenga acceso directo a la base de datos.

**Modulos funcionales**:

| Modulo | Funcion |
|---|---|
| Definicion del SI | Define la estructura de las bases de datos y formatos de documentos |
| Entrada | Dota al SI de elementos de entrada adecuados a la informacion |
| Analisis | Aplica algoritmos para procesar datos y obtener informacion |
| Busqueda | Gestiona las fuentes para busquedas coordinadas y sencillas |
| Difusion | Notificaciones de informacion relevante a los usuarios |
| Evaluacion | Recopila estadisticas y opiniones para mejora del SI |

### 2.5. Funciones principales

La funcion principal de un SI es **ofrecer informacion relevante, eliminando datos superfluos**, filtrada y ordenada para busquedas eficientes.

Se distinguen 4 funciones basicas:

1. **Entrada de informacion**: proceso mediante el cual el SI toma los datos a procesar. Las entradas pueden ser **manuales** (proporcionadas por el usuario) o **automaticas** (procedentes de otros sistemas — interfaces automaticas).

2. **Almacenamiento de informacion**: capacidad del sistema para recordar la informacion guardada. Es una de las funciones mas importantes.

3. **Procesamiento de informacion**: capacidad para efectuar calculos segun una secuencia de operaciones preestablecida. Permite la transformacion de datos fuente en informacion util para la toma de decisiones.

4. **Salida de informacion**: capacidad para sacar la informacion procesada al exterior. La salida de un SI puede constituir la entrada a otro SI.

### 2.6. Tipos de sistemas de informacion

**Clasificacion generica**:

- Sistemas competitivos
- Sistemas cooperativos
- Sistemas que modifican el estilo de operacion del negocio

**Clasificacion por funcion**:

| Tipo | Sigla | Descripcion |
|---|---|---|
| Sistema de Soporte a la Decision | **DSS** | Herramienta de analisis de datos para apoyo en toma de decisiones |
| Sistema de Procesamiento de Transacciones | **TPS** | Gestiona transacciones producidas en la organizacion. Tambien llamado SI operativo |
| Sistema de Informacion Ejecutiva | **EIS** | Orientado a nivel gerencial. Monitoriza variables del area. Maneja informacion estrategica |
| Sistema de Informacion Gerencial | **MIS** | Orientado a resolver problemas empresariales en general |

### 2.7. Herramientas complementarias

- **Cuadro de Mando Integral (CMI / Balanced Scorecard / BSC)**: herramienta de control empresarial que permite establecer y monitorizar los objetivos de una empresa y sus areas. Muestra de forma continuada el cumplimiento del plan estrategico.

- **Datawarehouse**: base de datos corporativa que integra y depura informacion de una o mas fuentes distintas, para luego procesarla permitiendo su analisis desde multiples perspectivas y con grandes velocidades de respuesta.

---

## 3. Arquitectura de ordenadores

La arquitectura de ordenadores se define como el **conjunto de reglas, normas y procedimientos que especifican las interrelaciones entre los componentes logicos y fisicos** que forman parte de un sistema informatico, asi como las caracteristicas que debe cumplir cada componente. [STALLINGS-COA, Cap. 1]

### 3.1. Arquitectura Von Neumann

Tambien conocida como **modelo de Von Neumann** o **arquitectura Princeton**. Propuesta por John von Neumann en 1945. [STALLINGS-COA, Cap. 2]

**Componentes**:

- **Unidad de proceso (CPU)**: contiene una Unidad Aritmetico-Logica (ALU), registros del procesador y una Unidad de Control (UC) con un registro de instrucciones y un contador de programa (CP).
- **Memoria**: almacena **tanto datos como instrucciones** en un unico espacio de memoria.
- **Mecanismos de entrada/salida (E/S)**.

Estos elementos estan conectados mediante **buses de datos**.

**Caracteristica fundamental**: datos e instrucciones comparten la misma memoria y el mismo bus.

> **Cuello de botella de Von Neumann**: No pueden darse simultaneamente una busqueda de instrucciones y una operacion de datos, ya que comparten un bus comun. La velocidad de comunicacion entre CPU y memoria es inferior a la velocidad de procesamiento de la CPU, lo que limita el rendimiento del sistema. Este problema se agrava con cada nueva generacion de procesadores, ya que la velocidad de proceso y la capacidad de memoria han aumentado mas rapidamente que la tasa de transferencia entre ambos.

### 3.2. Arquitectura Harvard

Contiene los mismos elementos que Von Neumann, pero con una **diferencia fundamental**: la memoria principal se divide en **memoria de instrucciones** y **memoria de datos**, cada una con su propio bus exclusivo. [STALLINGS-COA, Cap. 2]

**Ventaja clave**: al tener buses separados, se pueden simultanear operaciones sobre datos e instrucciones, eliminando el cuello de botella de Von Neumann y aumentando el rendimiento.

| Caracteristica | Von Neumann | Harvard |
|---|---|---|
| Memoria | Unica (datos + instrucciones) | Separada (datos / instrucciones) |
| Buses | Bus compartido | Buses independientes |
| Acceso simultaneo | No | Si |
| Cuello de botella | Si | No (o reducido) |
| Complejidad | Menor | Mayor |

### 3.3. Arquitectura Harvard modificada

En la actualidad, la mayoria de los procesadores implementan una **arquitectura Harvard modificada**, que permite que los contenidos de la memoria de instrucciones sean accedidos como si fuesen datos. Esto posibilita tareas como la carga de un programa desde disco para su posterior ejecucion.

Caracteristicas:

- La memoria de instrucciones y datos ocupan **diferente espacio de direcciones**.
- Acceden a la CPU por **buses distintos**.
- Pueden ser accedidas de **diferente manera**.

---

## 4. Generaciones de ordenadores

Las generaciones se definen por tres aspectos principales: la **tecnologia vigente**, las **tecnicas de programacion** y el **impacto en la sociedad**. [TANENBAUM-SO, Cap. 1]

### 4.1. Primera generacion (1940-1952) — Valvulas de vacio

| Aspecto | Detalle |
|---|---|
| Tecnologia | Reles electromagneticos, valvulas y tubos de vacio |
| Memoria | Tarjetas y cintas perforadas, lineas de demora de mercurio |
| Velocidad | Milisegundos |
| Uso | Aplicaciones cientificas y militares |
| Programacion | Lenguaje maquina (interruptores manuales) |
| Ejemplo | **ENIAC** |

### 4.2. Segunda generacion (1952-1964) — Transistores

| Aspecto | Detalle |
|---|---|
| Tecnologia | **Transistor** sustituye a la valvula de vacio |
| Memoria | Nucleos de ferrita, soportes magneticos |
| Mejoras | Reduccion de tamano, consumo y coste; aumento de fiabilidad |
| Uso | Se extienden a empresas y universidades (administracion, gestion) |
| Programacion | Lenguajes evolucionados: **Ensamblador, Fortran, Cobol, Algol** |
| Otros avances | Circuitos impresos sustituyen al cableado; primeros perifericos |
| Ejemplo | **TRADIC** (primer ordenador con transistores) |

### 4.3. Tercera generacion (1964-1970) — Circuitos integrados

| Aspecto | Detalle |
|---|---|
| Tecnologia | **Circuitos integrados** — SSI (10 transistores/chip), luego MSI (hasta 1.000) |
| Memoria | Semiconductores y discos magneticos |
| Mejoras | Miniaturizacion, primeras minicomputadoras |
| Software | Sistemas operativos con multiprogramacion, tiempo real, modo interactivo |
| Programacion | Aparece **BASIC** |
| Ejemplo | **PDP-11** (DEC), superordenador **CDC-7600** |

### 4.4. Cuarta generacion (1970-1981) — Microprocesador

| Aspecto | Detalle |
|---|---|
| Tecnologia | **LSI** y **VLSI** (mas de 10.000 puertas logicas/chip) |
| Hito | En **1971** aparece el **microprocesador**: toda la CPU en un unico chip |
| Conmutacion | 10 nanosegundos |
| Almacenamiento | Disquete (Floppy Disk) |
| Uso | Primeros **ordenadores personales** (IBM PC), clonicos compatibles |
| Otros | Redes de ordenadores, teleinformatica |

### 4.5. Quinta generacion (1981-1991)

| Aspecto | Detalle |
|---|---|
| Tecnologia | Componentes **VLSI** masivos |
| Conmutacion | 1 nanosegundo |
| Avances | Inteligencia Artificial, Sistemas Expertos |
| Programacion | Lenguajes cercanos al lenguaje natural |
| Interfaces | Sistemas operativos con **interfaces graficas**, raton |
| Redes | Interconexion global: **Internet** |
| Impacto | Expansion masiva de la microinformatica a todos los sectores |

---

## 5. Componentes internos de los equipos microinformaticos

El hardware de un ordenador se estructura en tres subsistemas: [STALLINGS-COA, Cap. 3]

1. **Unidad Central de Proceso (UCP/CPU)**
2. **Memoria central**
3. **Unidades de entrada/salida (perifericos)**

### 5.1. Buses

Un **bus** es un conjunto de circuitos que se encargan de la conexion y comunicacion entre los diversos componentes del ordenador. La comunicacion se realiza mediante lineas electricas paralelas. [STALLINGS-COA, Cap. 3]

| Tipo de bus | Funcion |
|---|---|
| **Bus de control** | Transmite senales de la Unidad de Control interpretadas como ordenes por el resto de dispositivos |
| **Bus de direcciones** | Transporta las direcciones de memoria sobre las que se va a actuar (lectura/escritura) |
| **Bus de datos** | Traslada datos hacia/desde la memoria y otros dispositivos |

### 5.2. El procesador (CPU)

El procesador, tambien denominado **CPU (Central Processing Unit)**, es el subsistema mas importante del ordenador. Actua como su cerebro, coordinando y supervisando el funcionamiento del sistema y procesando las instrucciones de los programas. [STALLINGS-COA, Cap. 3]

**Secuencia invariable de operacion**:
1. Extraer de memoria una instruccion del programa en ejecucion.
2. Analizar dicha instruccion.
3. Realizar las operaciones necesarias para su ejecucion.

Actualmente, la CPU esta integrada en un **microprocesador** (chip), montado sobre la **placa base** y acompanado de un disipador de calor.

> **Nota**: Los terminos UCP, CPU, microprocesador y procesador son equivalentes.

#### 5.2.1. Tecnologias: CISC vs RISC

**CISC (Complex Instruction Set Computer)** [INTEL-SDM]

- Conjunto de instrucciones **amplio y complejo**.
- Permite operaciones complejas entre operandos en memoria o registros.
- Dificulta el paralelismo entre instrucciones.
- Los sistemas CISC modernos convierten instrucciones complejas en **microinstrucciones tipo RISC** internamente.
- Requiere **4 a 10 ciclos de reloj** por instruccion.
- Ejemplos: **Intel x86, AMD, Motorola**.

Ventajas CISC:
- Reduce la dificultad de crear compiladores.
- Permite reducir el coste total del sistema.
- Mejora la compactacion de codigo.
- Facilita la depuracion de errores.

**RISC (Reduced Instruction Set Computer)** [STALLINGS-COA, Cap. 15]

- Conjunto de instrucciones **reducido y simple**.
- Instrucciones de **tamano fijo** en pocos formatos.
- Solo las instrucciones de carga/almacenamiento acceden a memoria de datos.
- Cada instruccion se ejecuta en **un solo ciclo de CPU**.
- Ejemplos: **ARM, MIPS, SPARC, PowerPC**.

Ventajas RISC:
- CPU mas rapida (menos ciclos por instruccion).
- Direcciones no destructivas en RAM (conserva operandos + resultado).
- Favorece segmentacion y paralelismo.

**Tabla comparativa**:

| Aspecto | CISC | RISC |
|---|---|---|
| Instrucciones | Complejas, tamano variable | Simples, tamano fijo |
| Ciclos por instruccion | 4-10 | 1 |
| Acceso a memoria | Cualquier instruccion | Solo carga/almacenamiento |
| Paralelismo | Dificil | Favorable |
| Uso tipico | PCs de escritorio (x86) | Moviles, consolas, servidores ARM |
| Ejemplos | Intel, AMD, Motorola | ARM, MIPS, SPARC, PowerPC |

> **Dato clave para examen**: El procesador x86 (el mas comun en PCs de escritorio) es CISC, pero internamente traduce instrucciones CISC a microinstrucciones RISC antes de ejecutarlas.

#### 5.2.2. Medidas de potencia

- **FLOPS**: numero de operaciones de coma flotante por segundo.
- **MIPS**: millones de instrucciones por segundo. Solo comparable entre CPUs con el mismo conjunto de instrucciones.

#### 5.2.3. Multiprocesamiento y MultiThreading

- **Multiprocesamiento**: un equipo con mas de una CPU ejecutando procesos. Un circuito integrado con mas de una CPU es un **procesador multinucleo**. No confundir con multitarea.

- **MultiThreading**: tecnologia que permite duplicar las unidades logicas de cada nucleo, permitiendo a un nucleo realizar **dos tareas simultaneas**. Patente de Sun Microsystems (1994).
  - Intel lo denomina **HyperThreading**.
  - AMD lo denomina **SMT (Simultaneous Multi-Threading)**.
  - Ambas tecnologias son virtualmente identicas en concepto y resultado.

### 5.3. Unidad Central de Proceso — Componentes internos

La CPU esta formada por tres subsistemas: [STALLINGS-COA, Cap. 12]

1. **Registros de acceso rapido**
2. **Unidad de Control (UC)**
3. **Unidad Aritmetico-Logica (ALU/UAL)**

#### 5.3.1. Registros

Un **registro** es una pequena zona de memoria de acceso muy rapido y directo por parte del procesador, que almacena un dato, instruccion o direccion de memoria. Caracteristica: **poca capacidad, alta velocidad**.

**Tipos de registros**:

| Tipo | Funcion |
|---|---|
| **Registros de datos** | Almacenan valores numericos y caracteres |
| **Acumulador** | Almacena temporalmente resultados aritmeticos/logicos intermedios para la ALU |
| **Registro de pila** | Mantiene la posicion actual de la pila de llamadas |
| **Registro indice** | Direcciona datos hacia/desde la RAM |
| **MBR (Memory Buffer Register)** | Conectado al bus de datos. Lee/escribe datos del bus dirigidos a memoria o E/S |
| **MAR (Memory Address Register)** | Contiene la direccion del dato a leer/escribir. Conectado al bus de direcciones |
| **GPRs (Proposito general)** | Almacenan direcciones o datos generales — sin funcion especifica |
| **SPRs (Proposito especifico)** | Guardan datos del estado del sistema (registro de estado, Instruction Pointer) |
| **Registro de estado (CCR)** | Determina si una instruccion debe ejecutarse. Incluye el registro FLAGS |
| **Registros de coma flotante** | Almacenan representaciones de numeros reales para operaciones rapidas |
| **Registros constantes** | Valores de solo lectura: cero, uno, PI |

> **Capacidad de direccionamiento**: Si el MAR tiene **n bits**, se pueden direccionar un maximo de **2^n palabras**.

> **Registro FLAGS** (Intel x86): 16 bits de ancho. Sucesores: **EFLAGS** (32 bits), **RFLAGS** (64 bits).

#### 5.3.2. Unidad de Control

La Unidad de Control es la **parte mas importante del microprocesador**. Controla el funcionamiento de todo el conjunto excepto las operaciones aritmeticas (gestionadas por la ALU). [STALLINGS-COA, Cap. 20]

**Componentes**:

| Componente | Funcion |
|---|---|
| **Reloj** | Proporciona impulsos con frecuencia constante que marcan los ciclos basicos. Ej: Pentium IV a 2 GHz = 2.000 millones de pulsos/segundo (no equivale a instrucciones/segundo, ya que muchas requieren multiples pulsos) |
| **Contador de Programa (CP)** | Registro que contiene la direccion de memoria de la **siguiente instruccion** a ejecutar. Al encender el ordenador toma un valor por defecto donde se encuentra la primera instruccion |
| **Registro de Instruccion (RI)** | Contiene la instruccion en ejecucion. Tiene dos partes: **codigo de operacion** (que hacer) y **operandos** (donde hacerlo) |
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
| **Registro de Estado** | Almacena informacion sobre condiciones de la ultima operacion (positivo/negativo, mayor/menor, etc.) |

**Tipos de operaciones**:

1. **Aritmeticas sobre enteros**: suma, resta, multiplicacion, division.
2. **Logicas a nivel de bit**: AND, OR, NOT, XOR, NAND, NOR, XNOR.
3. **Desplazamiento y rotacion de bits**: desplazan bits a izquierda/derecha. Equivalencia aritmetica: multiplicacion/division por potencias de 2.

**Tablas de verdad de operaciones logicas**:

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

**Clasificacion de instrucciones por numero de operandos**:

| Tipo | Descripcion | Ejemplo |
|---|---|---|
| Sin operandos | Acciones de control sin datos explicitos | `FIN` |
| Un operando | Actuan sobre un dato o direccion | `SALTO 12345` |
| Dos operandos | Dos elementos; uno suele ser destino | `SUMA A, B` (resultado en B) |
| Tres operandos | Dos fuentes + un destino | `SUMA A, B, C` (A+B se guarda en C) |

El **ciclo de instruccion** es el conjunto de acciones que realiza el ordenador para ejecutar cada instruccion. Se divide en dos fases: [STALLINGS-COA, Cap. 12]

#### Fase 1: Busqueda (FETCH)

La instruccion es localizada en memoria y transferida a la Unidad de Control:

1. La UC transfiere el contenido del **Contador de Programa (CP)** al **Registro de Direccion de Memoria (RDM/MAR)** a traves del bus de direcciones.
2. El sistema de memoria accede a la posicion indicada y transfiere la instruccion al **Registro de Intercambio de Memoria (RIM/MBR)**.
3. La instruccion se transfiere del RIM al **Registro de Instruccion (RI)** a traves del bus de datos.

#### Fase 2: Ejecucion

1. El **decodificador** interpreta la instruccion del RI. El **secuenciador** activa los circuitos necesarios (ej: la ALU en operaciones aritmeticas).
2. El **Contador de Programa** se actualiza: normalmente se incrementa para apuntar a la siguiente instruccion. En instrucciones de salto, se carga con una nueva direccion.

### 5.5. Modos de direccionamiento

Los modos de direccionamiento son las diferentes formas de transformar el campo de operando de la instruccion en la **direccion efectiva** del operando. [STALLINGS-COA, Cap. 13]

Se clasifican en **propios** (operando en memoria) e **impropios** (operando en registros u otros lugares).

| Modo | Tipo | Descripcion |
|---|---|---|
| **Implicito** (inherente) | Impropio | El operando esta en la definicion de la instruccion. Usado en acumuladores y pilas |
| **Inmediato** (literal) | Impropio | El operando esta incluido en la propia instruccion. Util para inicializar registros |
| **Directo/Absoluto** | Propio | El campo de operando contiene la direccion donde esta el dato. A registro o a memoria |
| **Indirecto** | Propio | El campo contiene una direccion donde se encuentra la direccion efectiva del operando. Necesita un acceso extra a memoria |
| **Relativo a registro base** | Propio | Direccion efectiva = contenido registro base + desplazamiento (siempre positivo). Permite codigos reentrantes |
| **Relativo a registro indice** | Propio | Direccion efectiva = contenido registro indice + direccion de memoria pasada como argumento |

---

## 6. Memoria

### 6.1. Clasificaciones

**Por tipo**:
- **Memoria interna**: RAM, ROM, registros, cache.
- **Memoria externa**: disco duro, CD-ROM, USB, SSD.

**Por volatilidad**:
- **Volatil**: se borra al perder alimentacion electrica (RAM).
- **No volatil**: persiste tras apagar el equipo (ROM, Flash, SSD).

**Por jerarquia de velocidad/capacidad** (piramide de memoria):

```
        /  Registros  \        ← Maxima velocidad, minima capacidad
       /    Cache L1    \
      /    Cache L2/L3   \
     /    Memoria RAM     \
    /   Almac. secundario  \   (SSD, HDD)
   /  Almac. terciario      \  (cinta, nube)  ← Minima velocidad, maxima capacidad
```

> **Regla fundamental**: a mayor velocidad, menor capacidad y viceversa.

### 6.2. Memoria RAM

La **memoria RAM (Random Access Memory)** es memoria principal de tipo **volatil**: su contenido se pierde al apagar el sistema. [JEDEC-DDR]

**Funcion**: almacenar temporalmente los datos e instrucciones que utiliza el procesador durante la ejecucion de programas. Actua como espacio de trabajo intermedio.

**Caracteristica principal**: **acceso aleatorio** — se puede leer/escribir en cualquier posicion en el mismo tiempo, independientemente de su ubicacion.

#### 6.2.1. Evolucion de la memoria RAM

| Tecnologia | Epoca | Descripcion |
|---|---|---|
| Nucleos de Ferrita | Anos 40-50 | Malla con nucleos de ferrita en las intersecciones |
| DIP | Anos 60-70 | Basadas en transistores |
| SIPP | Anos 80 | Modulos de 30 pines. Procesador 80286 |
| SIMM | Anos 80 | Contactos en lugar de pines, muesca de orientacion. Procesador 80486. 32 bits. 30 o 72 contactos |
| DIMM | Anos 90 | Chips en ambas caras. 168 contactos, 2 muescas. 64 bits |
| DIMM DDR | Actualidad | Evolucion de DIMM. 184 contactos |

#### 6.2.2. Tabla comparativa DDR

| Especificacion | DDR | DDR2 | DDR3 | DDR4 |
|---|---|---|---|---|
| **Frecuencia (MHz)** | 266-400 | 667-800 | 1066-2400 | 2133-4000 |
| **Capacidad maxima** | 1 GB | 2 GB | 16 GB | 64 GB |
| **Pines** | 184 | 240 | 240 | 288 |

> **Nota**: DDR2 y DDR3 tienen el mismo numero de pines (240) pero son **fisica y electricamente incompatibles** — la muesca esta en distinta posicion. [JEDEC-DDR]

#### 6.2.3. Tipos especiales de RAM

| Tipo | Descripcion | Uso |
|---|---|---|
| **RIMM** | Modulos Rambus, disipador de calor, 232 contactos | Memorias RDRAM (alto rendimiento) |
| **FB-DIMM** | Datos en serie, menos lineas, mayor velocidad | Servidores |
| **GDDR** | RAM DDR para graficas, integrada en la GPU | Tarjetas graficas |
| **SO-DIMM** | Version compacta de DIMM | Portatiles |
| **Micro-DIMM** | Mas pequeno que SO-DIMM | Dispositivos ultracompactos |
| **Buffered/Registered** | Registros intermedios CPU-memoria, mayor fiabilidad, menor velocidad, incluye ECC | Servidores |
| **Unbuffered** | Comunicacion directa con Northbridge, mas rapida, menos segura | PCs domesticos |

#### 6.2.4. RAM ECC vs No-ECC

- **No-ECC**: sin correccion de errores. Uso en PCs, tablets, portatiles.
- **ECC (Error Checking and Correction)**: sistema de paridad para detectar errores de 1 bit. No resuelve errores multibit. Uso en servidores. Requiere soporte de placa base y procesador.

#### 6.2.5. RAM volatil y no volatil

- **Volatil**:
  - **SRAM** (Static RAM): basada en biestables.
  - **DRAM** (Dynamic RAM): basada en condensadores.
- **No volatil**:
  - **NVRAM**: dispone de fuente de energia de respaldo.

#### 6.2.6. Parametros de la memoria RAM

| Parametro | Descripcion |
|---|---|
| **Velocidad (MHz)** | Millones de operaciones (lectura/escritura) por segundo |
| **Ancho de banda (MB/s o GB/s)** | Maxima cantidad de datos transferida por segundo |
| **Dual Channel** | Permite a la CPU usar dos canales simultaneos, duplicando el ancho de banda. Requiere 2 modulos identicos (misma frecuencia, capacidad y latencia) |
| **Tiempo de acceso (ns)** | Tiempo que tarda la CPU en acceder a la memoria |
| **Latencia** | Retardo al acceder a componentes de la RAM |
| **Latencia CAS (CL)** | Ciclos de reloj desde la peticion de lectura hasta la entrega de datos. **Cuanto menor, mas rapida** |

#### 6.2.7. RAM-CMOS

Memoria de entre **64 y 256 bytes** vinculada al reloj de tiempo real del sistema. Alimentada por la **pila de la placa base** (tecnologia CMOS de bajo consumo).

Almacena la **configuracion del sistema**: velocidad de buses, discos instalados, secuencia de arranque, contrasena, overclock, activacion de dispositivos.

La informacion es usada por el BIOS durante el arranque. Si los datos son incorrectos, se genera un error. Para restaurar valores de fabrica, se corta la alimentacion de la pila.

> **No confundir RAM-CMOS con BIOS**: son entidades de memoria diferentes, aunque la RAM-CMOS se configura desde la utilidad del BIOS.

### 6.3. Memoria ROM

La **memoria ROM (Read Only Memory)** es memoria principal de tipo **no volatil**: conserva la informacion almacenada al apagar el sistema.

**Funcion**: almacenar de forma permanente programas e instrucciones esenciales, como el **firmware**. Destaca la **BIOS**, ubicada en la placa base, con las rutinas basicas de arranque e inicializacion.

#### Tipos de memoria ROM

| Tipo | Descripcion | Reprogramable |
|---|---|---|
| **ROM** | Programada de fabrica, contenido inalterable. Obsoleta actualmente | No |
| **PROM** | Programable una unica vez por el usuario mediante un programador PROM. Depende de fusibles que se queman una sola vez | Una vez |
| **EPROM** | Borrable mediante exposicion a **luz ultravioleta**. Reprogramable electricamente | Si (UV + electrica) |
| **EEPROM** | Borrable y reprogramable **electricamente**. Permite sobreescritura sin extraer el chip. Lectura exhaustiva que puede ralentizar operaciones | Si (electrica) |
| **Flash** | Variante de EEPROM. Borrado y escritura **en bloques**. Ampliamente utilizada en dispositivos actuales (pendrives, SSD, tarjetas SD) | Si (por bloques) |

### 6.4. BIOS y UEFI

Ambos son **firmware**: codigo almacenado en memoria aparte de la placa base que contiene las instrucciones de control de los circuitos del equipo. [UEFI-SPEC]

**BIOS (Basic Input Output System)** — Creado en 1975:
- Al encender, inicializa, configura y comprueba el hardware (RAM, discos, placa base, GPU).
- Selecciona el dispositivo de arranque y lanza el sistema operativo.
- Gestiona energia y temperatura.

**UEFI (Unified Extensible Firmware Interface)** — Sucesor del BIOS, escrito en C:
- Realiza todo lo del BIOS + funciones adicionales.

**Diferencias UEFI vs BIOS**:

| Aspecto | BIOS | UEFI |
|---|---|---|
| Interfaz | Consola MS-DOS, solo teclado | Interfaz grafica moderna, raton, animaciones |
| Conectividad | Sin internet | Puede conectarse a internet para actualizarse |
| Codigo | 16 bits | 32 o 64 bits |
| Arranque | Mas lento | Mas rapido |
| Seguridad | Sin arranque seguro | **Secure Boot** (evita bootkits) |
| Almacenamiento | Solo recursos especificos | Cualquier memoria no volatil, extensible |
| Particiones | **4 particiones MBR** (max 2,2 TB) | **128 particiones GPT** (max 8 ZB) |

---

## 7. Medidas de capacidad de memoria

| Unidad | Descripcion | Equivalencia |
|---|---|---|
| **Bit** | Digito binario (0 o 1). Unidad minima de informacion | — |
| **Nibble** | Grupo de 4 bits | 4 bits |
| **Byte** | Grupo de 8 bits. Unidad mas pequena que representa un caracter | 8 bits |
| **Palabra** | Grupo fijo de bits procesados como unidad (varia por arquitectura: 8, 16, 32, 64, 96 bits) | Variable |
| **Kilobyte (KB)** | | 1.024 Bytes |
| **Megabyte (MB)** | | 1.024 KB |
| **Gigabyte (GB)** | | 1.024 MB |
| **Terabyte (TB)** | | 1.024 GB |
| **Petabyte (PB)** | | 1.024 TB |
| **Exabyte (EB)** | | 1.024 PB |
| **Zettabyte (ZB)** | | 1.024 EB |
| **Yottabyte (YB)** | | 1.024 ZB |

---

## 8. Sistemas de numeracion

Un sistema de numeracion es un conjunto de simbolos y reglas que permiten construir numeros validos. [STALLINGS-COA, Cap. 9]

| Sistema | Base | Simbolos | Uso principal |
|---|---|---|---|
| **Decimal** | 10 | 0-9 | Uso humano cotidiano |
| **Binario** | 2 | 0, 1 | Uso interno de ordenadores y sistemas digitales |
| **Octal** | 8 | 0-7 | Representacion compacta de binario (permisos Unix) |
| **Hexadecimal** | 16 | 0-9, A-F | Direcciones de memoria, colores, MAC addresses |

> **Dato clave**: El sistema **binario** es el utilizado por los ordenadores de forma interna para realizar absolutamente todos los procesos.

---

## 9. Juegos de caracteres

### 9.1. ASCII

**ASCII (American Standard Code for Information Interchange)**: codigo de caracteres basado en el alfabeto latino. Creado en **1963** por el Comite Estadounidense de Estandares (ASA/ANSI). [RFC-20]

- Utiliza **7 bits** para representar caracteres.
- Define **33 caracteres no imprimibles** (control) + **95 caracteres imprimibles** (desde el espacio).
- En total: **128 caracteres**.
- Inicialmente usaba un bit adicional de paridad para deteccion de errores en transmision.

### 9.2. ASCII extendido

Cualquier juego de caracteres de **8 bits** donde los codigos 32-126 coinciden con los caracteres imprimibles de ASCII.

Utiliza los codigos superiores a 128 para caracteres adicionales (acentos, n, etc.).

Codificaciones mas comunes:
- **Pagina 437**: IBM PC / MS-DOS en ingles.
- **Pagina 850**: IBM PC / MS-DOS Europa occidental.
- **Latin-1 (ISO-8859-1)**: Unix. Con modificaciones en Windows (Windows-1252) y Mac.

### 9.3. Unicode y UTF-8

**Unicode**: estandar de codificacion disenado para texto de multiples lenguajes. Nombre proviene de tres objetivos: **universalidad, uniformidad, unicidad**. [UNICODE-STD]

Especifica un nombre e identificador numerico unico (**code point**) para cada caracter. Trata caracteres alfabeticos, ideograficos y simbolos de forma equivalente.

**UTF-8 (8-bit Unicode Transformation Format)**: formato de codificacion de longitud variable. Es la codificacion dominante en la web.

| Bytes | Caracteres cubiertos | Rango |
|---|---|---|
| 1 byte | US-ASCII (128 caracteres) | Compatibilidad total con ASCII |
| 2 bytes | ~1.920 caracteres (latin con diacriticos, griego, cirilico, hebreo, arabe) | Alfabetos extendidos |
| 3 bytes | Plano basico multilingue (BMP), incluido CJK | Mayoria de caracteres de uso comun |
| 4 bytes | Planos suplementarios (matematicos, historicos, emojis) | Caracteres especiales |

**Ventajas de UTF-8**:
- Compatible con US-ASCII.
- Eficiente en textos latinos (1 byte por caracter ASCII).
- Autosincronizacion (puede identificarse el inicio de cada caracter).
- Sin solapamiento entre bytes de diferentes caracteres.

**Desventajas de UTF-8**:
- Caracteres CJK ocupan 3 bytes (vs 2 en UTF-16).
- Acceso directo a posiciones dificil (requiere recorrido secuencial).
- Mayor coste computacional en ordenacion/indexacion vs UTF-16/UTF-32.

### 9.4. EBCDIC

**EBCDIC (Extended Binary Coded Decimal Interchange Code)**: codigo de caracteres de **8 bits** desarrollado por **IBM**. Usado en sistemas **mainframe**.

- 1 byte por caracter = 256 combinaciones posibles.
- Existen multiples variantes (paginas de codigos) segun idioma/entorno.
- No es compatible con ASCII.

---

*Documento generado con asistencia de IA — Pendiente validacion humana (Maria/Ana)*
*Fuentes: ver tema-11-fuentes.md*
*Fecha: 2026-04-16*
