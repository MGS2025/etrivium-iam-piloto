# Tema 11 — Test de Autoevaluacion

> **Titulo**: Informatica basica. Representacion y comunicacion de la informacion.
> **Formato**: 15 preguntas tipo test A/B/C (formato oficial oposicion)
> **Nivel**: C1 — Tecnico Auxiliar TIC, Ayuntamiento de Madrid
> **Estado**: PILOTO v1.0 — Pendiente validacion
> **Fuentes**: ver tema-11-fuentes.md

---

## Instrucciones

- Cada pregunta tiene **3 opciones** (A, B, C). Solo una es correcta.
- Penalizacion en examen real: respuesta incorrecta descuenta 1/3 del valor de una correcta.
- Tiempo orientativo: 1 minuto por pregunta.

---

### Pregunta 1

**Cual es la unidad minima de informacion en un sistema informatico?**

A) Byte
B) Bit
C) Nibble

<details>
<summary>Respuesta</summary>

**Correcta: B) Bit**

El bit (binary digit) es la unidad minima de informacion, representando un valor binario (0 o 1). Un byte esta compuesto por 8 bits, y un nibble por 4 bits.

*Referencia: tema-11-contenido.md, seccion 7 — Medidas de capacidad [ISO-2382]*
</details>

---

### Pregunta 2

**En la arquitectura Von Neumann, cual es la causa principal de su cuello de botella?**

A) La ALU no puede realizar operaciones aritmeticas y logicas simultaneamente
B) Los datos y las instrucciones comparten el mismo bus de memoria
C) La Unidad de Control no puede decodificar mas de una instruccion a la vez

<details>
<summary>Respuesta</summary>

**Correcta: B) Los datos y las instrucciones comparten el mismo bus de memoria**

El cuello de botella de Von Neumann se produce porque datos e instrucciones comparten un unico bus, impidiendo la busqueda simultanea de instrucciones y datos. La arquitectura Harvard resuelve esto con buses separados.

*Referencia: tema-11-contenido.md, seccion 3.1 [STALLINGS-COA, Cap. 2]*
</details>

---

### Pregunta 3

**Que caracteristica diferencia fundamentalmente la arquitectura Harvard de la Von Neumann?**

A) Harvard utiliza microprocesadores RISC exclusivamente
B) Harvard separa la memoria de instrucciones de la memoria de datos
C) Harvard no utiliza buses de control

<details>
<summary>Respuesta</summary>

**Correcta: B) Harvard separa la memoria de instrucciones de la memoria de datos**

La arquitectura Harvard divide la memoria principal en memoria de instrucciones y memoria de datos, cada una con su propio bus, permitiendo acceso simultaneo y eliminando el cuello de botella de Von Neumann.

*Referencia: tema-11-contenido.md, seccion 3.2 [STALLINGS-COA, Cap. 2]*
</details>

---

### Pregunta 4

**Cual de las siguientes afirmaciones sobre los procesadores RISC es correcta?**

A) Utilizan instrucciones complejas que requieren entre 4 y 10 ciclos de reloj
B) Solo las instrucciones de carga y almacenamiento acceden a la memoria de datos
C) Son la arquitectura predominante en los ordenadores de escritorio x86

<details>
<summary>Respuesta</summary>

**Correcta: B) Solo las instrucciones de carga y almacenamiento acceden a la memoria de datos**

Esta es una caracteristica fundamental de RISC. La opcion A describe CISC (4-10 ciclos). La opcion C es incorrecta: x86 es CISC (aunque internamente traduce a microinstrucciones RISC). Ejemplos RISC: ARM, MIPS, SPARC.

*Referencia: tema-11-contenido.md, seccion 5.2.1 [STALLINGS-COA, Cap. 15]*
</details>

---

### Pregunta 5

**Que componente de la CPU contiene la direccion de la siguiente instruccion a ejecutar?**

A) Registro de Instruccion (RI)
B) Contador de Programa (CP)
C) Registro de Estado (FLAGS)

<details>
<summary>Respuesta</summary>

**Correcta: B) Contador de Programa (CP)**

El Contador de Programa (tambien llamado Registro de Control de Secuencia) contiene en todo momento la direccion de memoria de la siguiente instruccion a ejecutar. El RI contiene la instruccion en ejecucion. FLAGS almacena condiciones de la ultima operacion.

*Referencia: tema-11-contenido.md, seccion 5.3.2 [STALLINGS-COA, Cap. 20]*
</details>

---

### Pregunta 6

**Cuantos bytes componen un Kilobyte (KB) segun el sistema binario?**

A) 1.000 bytes
B) 1.024 bytes
C) 512 bytes

<details>
<summary>Respuesta</summary>

**Correcta: B) 1.024 bytes**

En el sistema binario, 1 KB = 2^10 = 1.024 bytes. La opcion A (1.000) corresponde al sistema decimal utilizado por fabricantes de discos duros para expresar capacidades comerciales.

*Referencia: tema-11-contenido.md, seccion 7 [ISO-2382]*
</details>

---

### Pregunta 7

**En la primera generacion de ordenadores (1940-1952), cual era el componente electronico principal?**

A) Transistores
B) Circuitos integrados
C) Valvulas de vacio

<details>
<summary>Respuesta</summary>

**Correcta: C) Valvulas de vacio**

La primera generacion utilizaba valvulas y tubos de vacio. Los transistores corresponden a la segunda generacion (1952-1964) y los circuitos integrados a la tercera (1964-1970).

*Referencia: tema-11-contenido.md, seccion 4.1 [TANENBAUM-SO, Cap. 1]*
</details>

---

### Pregunta 8

**Que tipo de bus transporta las direcciones de memoria sobre las que se va a actuar en operaciones de lectura y escritura?**

A) Bus de datos
B) Bus de control
C) Bus de direcciones

<details>
<summary>Respuesta</summary>

**Correcta: C) Bus de direcciones**

El bus de direcciones transporta las direcciones de memoria. El bus de datos traslada los datos en si. El bus de control transmite senales de la Unidad de Control interpretadas como ordenes.

*Referencia: tema-11-contenido.md, seccion 5.1 [STALLINGS-COA, Cap. 3]*
</details>

---

### Pregunta 9

**Que tipo de memoria ROM puede borrarse mediante exposicion a luz ultravioleta y reprogramarse electricamente?**

A) PROM
B) EPROM
C) EEPROM

<details>
<summary>Respuesta</summary>

**Correcta: B) EPROM**

La EPROM (Erasable Programmable ROM) se borra mediante luz ultravioleta y se programa electricamente. La PROM solo puede programarse una vez. La EEPROM se borra y reprograma electricamente, sin necesidad de luz ultravioleta.

*Referencia: tema-11-contenido.md, seccion 6.3*
</details>

---

### Pregunta 10

**Cual de las siguientes NO es una funcion basica de un sistema de informacion?**

A) Procesamiento de informacion
B) Compilacion de codigo fuente
C) Almacenamiento de informacion

<details>
<summary>Respuesta</summary>

**Correcta: B) Compilacion de codigo fuente**

Las 4 funciones basicas de un SI son: entrada, almacenamiento, procesamiento y salida de informacion. La compilacion de codigo fuente es una funcion especifica de herramientas de desarrollo de software, no una funcion generica de un SI.

*Referencia: tema-11-contenido.md, seccion 2.5*
</details>

---

### Pregunta 11

**Cuantos pines tienen los modulos de memoria DDR4?**

A) 240 pines
B) 184 pines
C) 288 pines

<details>
<summary>Respuesta</summary>

**Correcta: C) 288 pines**

DDR4 tiene 288 pines. DDR tiene 184 pines. DDR2 y DDR3 comparten 240 pines pero con la muesca en diferente posicion (incompatibles entre si).

*Referencia: tema-11-contenido.md, seccion 6.2.2 [JEDEC-DDR]*
</details>

---

### Pregunta 12

**Que codificacion de caracteres utiliza entre 1 y 4 bytes por caracter y es compatible con ASCII de 7 bits?**

A) EBCDIC
B) UTF-8
C) ISO-8859-1

<details>
<summary>Respuesta</summary>

**Correcta: B) UTF-8**

UTF-8 utiliza longitud variable (1-4 bytes) y es plenamente compatible con US-ASCII de 7 bits. EBCDIC es un codigo de 8 bits de IBM no compatible con ASCII. ISO-8859-1 usa 8 bits fijos.

*Referencia: tema-11-contenido.md, seccion 9.3 [UNICODE-STD]*
</details>

---

### Pregunta 13

**Que tecnologia permite a un nucleo de procesador realizar dos tareas simultaneas?**

A) Multiprocesamiento
B) MultiThreading (HyperThreading / SMT)
C) Multinucleo

<details>
<summary>Respuesta</summary>

**Correcta: B) MultiThreading (HyperThreading / SMT)**

El MultiThreading duplica las unidades logicas de cada nucleo, permitiendo dos tareas simultaneas por nucleo. Intel lo denomina HyperThreading y AMD lo denomina SMT. El multiprocesamiento implica multiples CPUs. Multinucleo significa multiples nucleos fisicos en un chip.

*Referencia: tema-11-contenido.md, seccion 5.2.3*
</details>

---

### Pregunta 14

**Cual de las siguientes diferencias entre UEFI y BIOS es correcta?**

A) BIOS soporta hasta 128 particiones GPT por disco, UEFI solo 4 particiones MBR
B) UEFI se ejecuta en 16 bits, igual que BIOS
C) UEFI soporta hasta 128 particiones GPT por disco, mientras que BIOS se limita a 4 particiones MBR

<details>
<summary>Respuesta</summary>

**Correcta: C) UEFI soporta hasta 128 particiones GPT por disco, mientras que BIOS se limita a 4 particiones MBR**

UEFI permite 128 particiones GPT (hasta 8 ZB) frente a las 4 particiones MBR de BIOS (hasta 2,2 TB). UEFI se ejecuta en 32 o 64 bits, no en 16. La opcion A invierte los datos.

*Referencia: tema-11-contenido.md, seccion 6.4 [UEFI-SPEC]*
</details>

---

### Pregunta 15

**En el ciclo de ejecucion de instrucciones, que ocurre durante la fase de busqueda (FETCH)?**

A) La ALU ejecuta la operacion aritmetica correspondiente
B) La instruccion es localizada en memoria y transferida al Registro de Instruccion
C) El Contador de Programa se decrementa para apuntar a la instruccion anterior

<details>
<summary>Respuesta</summary>

**Correcta: B) La instruccion es localizada en memoria y transferida al Registro de Instruccion**

En la fase FETCH: (1) el CP transfiere la direccion al MAR, (2) la memoria entrega la instruccion al MBR, (3) se transfiere al RI. La ejecucion de operaciones por la ALU corresponde a la fase de ejecucion. El CP normalmente se incrementa, no se decrementa.

*Referencia: tema-11-contenido.md, seccion 5.4 [STALLINGS-COA, Cap. 12]*
</details>

---

## Resumen de resultados

| Pregunta | Correcta | Seccion del temario |
|---|---|---|
| 1 | B | 7. Medidas de capacidad |
| 2 | B | 3.1. Von Neumann |
| 3 | B | 3.2. Harvard |
| 4 | B | 5.2.1. CISC vs RISC |
| 5 | B | 5.3.2. Unidad de Control |
| 6 | B | 7. Medidas de capacidad |
| 7 | C | 4.1. Primera generacion |
| 8 | C | 5.1. Buses |
| 9 | B | 6.3. Memoria ROM |
| 10 | B | 2.5. Funciones SI |
| 11 | C | 6.2.2. Tabla DDR |
| 12 | B | 9.3. Unicode/UTF-8 |
| 13 | B | 5.2.3. MultiThreading |
| 14 | C | 6.4. BIOS/UEFI |
| 15 | B | 5.4. Ciclo instruccion |

**Distribucion tematica**: Cubre las 9 secciones del tema de forma equilibrada.

---

*Test generado con asistencia de IA — Pendiente validacion humana*
*Cada pregunta vinculada a seccion del temario y fuente documental*
*Fecha: 2026-04-16*
