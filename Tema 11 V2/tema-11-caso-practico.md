# Tema 11 — Caso Practico

> **Titulo**: Informatica basica. Representacion y comunicacion de la informacion.
> **Nivel**: C1 — Tecnico Auxiliar TIC, Ayuntamiento de Madrid
> **Estado**: PILOTO v1.0 — Pendiente validacion
> **Tiempo estimado**: 30 minutos

---

## Enunciado

El Ayuntamiento de Madrid esta renovando los equipos informaticos del area de Atencion al Ciudadano. Como tecnico auxiliar TIC, se le asigna la tarea de evaluar las especificaciones tecnicas de los nuevos equipos propuestos y asesorar sobre su adecuacion.

El proveedor ha presentado la siguiente propuesta para 50 puestos de trabajo:

| Componente | Especificacion |
|---|---|
| Procesador | Intel Core i5-13400 (arquitectura x86, 10 nucleos, 16 hilos) |
| Memoria RAM | 16 GB DDR4-3200 (2 x 8 GB) |
| Almacenamiento | SSD NVMe 512 GB |
| Firmware | UEFI con Secure Boot habilitado |
| Sistema Operativo | Windows 11 Pro |

---

## Cuestiones

### Cuestion 1 — Arquitectura del procesador (2 puntos)

a) Indique a que tipo de arquitectura de conjunto de instrucciones pertenece el procesador Intel Core i5-13400 (CISC o RISC). Justifique su respuesta.

b) Explique brevemente como es posible que un procesador de este tipo consiga un rendimiento elevado a pesar de utilizar instrucciones complejas.

<details>
<summary>Respuesta orientativa</summary>

a) El Intel Core i5-13400 pertenece a la arquitectura **CISC** (Complex Instruction Set Computer), ya que forma parte de la familia x86 de Intel. Los procesadores CISC se caracterizan por disponer de un conjunto amplio de instrucciones complejas que permiten operaciones entre operandos en memoria y registros.

b) A pesar de ser CISC, los procesadores x86 modernos alcanzan alto rendimiento porque internamente **traducen las instrucciones complejas CISC a microinstrucciones simples tipo RISC** antes de ejecutarlas. De esta forma combinan la compatibilidad del set de instrucciones x86 con la eficiencia de ejecucion de las arquitecturas RISC.

*Referencia: tema-11-contenido.md, seccion 5.2.1*
</details>

---

### Cuestion 2 — MultiThreading (2 puntos)

El procesador especificado tiene 10 nucleos y 16 hilos.

a) Explique que tecnologia permite que un procesador tenga mas hilos que nucleos fisicos y como la denomina Intel.

b) Si 6 de los 10 nucleos soportan esta tecnologia y los 4 restantes no, justifique matematicamente los 16 hilos totales.

<details>
<summary>Respuesta orientativa</summary>

a) La tecnologia se denomina **HyperThreading** (nombre comercial de Intel) o **MultiThreading**. Permite duplicar las unidades logicas de cada nucleo, de modo que un unico nucleo fisico puede ejecutar dos tareas (hilos) de forma simultanea. AMD denomina a su implementacion equivalente **SMT (Simultaneous Multi-Threading)**.

b) Calculo:
- 6 nucleos con HyperThreading: 6 x 2 = 12 hilos
- 4 nucleos sin HyperThreading: 4 x 1 = 4 hilos
- **Total: 12 + 4 = 16 hilos**

Esto corresponde a la arquitectura hibrida de Intel (P-cores con HT + E-cores sin HT).

*Referencia: tema-11-contenido.md, seccion 5.2.3*
</details>

---

### Cuestion 3 — Memoria RAM (3 puntos)

La propuesta incluye 16 GB DDR4-3200 en configuracion 2 x 8 GB.

a) Indique cuantos pines tienen los modulos DDR4 y en que rango de frecuencias operan segun la especificacion estandar.

b) Explique que es la tecnologia Dual Channel y que requisitos deben cumplir los modulos para activarla. Indique si la configuracion propuesta (2 x 8 GB) cumple estos requisitos.

c) Si el area de Atencion al Ciudadano trabaja con aplicaciones criticas que no admiten errores en memoria, recomendaria RAM ECC o No-ECC? Justifique su respuesta indicando las implicaciones.

<details>
<summary>Respuesta orientativa</summary>

a) Los modulos DDR4 tienen **288 pines** y operan en un rango de frecuencia estandar de **2133 a 4000 MHz**. DDR4-3200 indica una frecuencia de 3200 MHz, dentro del rango estandar.

b) **Dual Channel** permite a la CPU trabajar con dos canales independientes y simultaneos para acceder a datos, **duplicando el ancho de banda**. Requisitos: los 2 modulos deben tener la **misma frecuencia, misma capacidad y misma latencia**. La configuracion 2 x 8 GB cumple los requisitos si ambos modulos son identicos en frecuencia (3200 MHz), capacidad (8 GB) y latencia (CL).

c) Para aplicaciones criticas de Atencion al Ciudadano, la eleccion depende del contexto:
- **RAM ECC** detecta y corrige errores de 1 bit mediante un sistema de paridad. Se usa en servidores y entornos criticos. Requiere que placa base y procesador soporten ECC.
- **RAM No-ECC** no tiene correccion de errores. Es la habitual en PCs de escritorio.

Para puestos de atencion al ciudadano (no servidores), la recomendacion seria **No-ECC**, ya que el Intel i5-13400 no soporta ECC y los errores de memoria en puestos de trabajo individuales no suponen un riesgo critico. La fiabilidad critica debe garantizarse a nivel de **servidor** (donde si deberia usarse ECC).

*Referencia: tema-11-contenido.md, secciones 6.2.2, 6.2.4, 6.2.6*
</details>

---

### Cuestion 4 — BIOS vs UEFI (2 puntos)

a) Indique tres diferencias entre BIOS y UEFI que sean relevantes para la seguridad y el rendimiento de los equipos del Ayuntamiento.

b) Explique que es Secure Boot y por que es relevante en un entorno de administracion publica.

<details>
<summary>Respuesta orientativa</summary>

a) Tres diferencias relevantes:

| Aspecto | BIOS | UEFI |
|---|---|---|
| **Arranque** | Mas lento | Mas rapido (mejor productividad) |
| **Seguridad** | Sin arranque seguro | Secure Boot protege contra bootkits |
| **Particiones** | 4 particiones MBR, max 2,2 TB | 128 particiones GPT, max 8 ZB (permite discos grandes) |

b) **Secure Boot** es una funcionalidad de UEFI que verifica que el sistema operativo que se va a cargar esta **autenticado digitalmente** antes de permitir su ejecucion. Evita el inicio de software no autorizado (bootkits, rootkits) que podria ejecutarse antes del sistema operativo.

En un entorno de administracion publica es relevante porque:
- Protege contra malware que se ejecuta antes de que el antivirus este activo.
- Cumple con los requisitos del **Esquema Nacional de Seguridad** en cuanto a integridad del arranque.
- Impide la manipulacion del sistema de arranque por usuarios no autorizados.

*Referencia: tema-11-contenido.md, seccion 6.4 [UEFI-SPEC]*
</details>

---

### Cuestion 5 — Codificacion de caracteres (1 punto)

Los formularios de Atencion al Ciudadano deben admitir nombres con caracteres especiales (acentos, ene, cedilla) y eventualmente caracteres de otros alfabetos (cirilico, arabe).

Que codificacion de caracteres recomendaria para la base de datos que almacene estos datos? Justifique su respuesta.

<details>
<summary>Respuesta orientativa</summary>

Se recomienda **UTF-8** por las siguientes razones:

1. **Universalidad**: permite representar cualquier caracter del estandar Unicode, incluyendo latin con diacriticos (acentos, ene, cedilla), cirilico, arabe y cualquier otro alfabeto.
2. **Compatibilidad**: es compatible con US-ASCII, por lo que los caracteres basicos ocupan solo 1 byte (eficiencia en textos predominantemente latinos).
3. **Estandar web**: es la codificacion dominante en la web y recomendada por el W3C, facilitando la interoperabilidad con otros sistemas.
4. **Autosincronizacion**: evita ambiguedades en la decodificacion de caracteres multibyte.

Alternativas descartadas:
- ISO-8859-1/Latin-1: solo cubre Europa occidental, no soporta cirilico ni arabe.
- EBCDIC: propietario de IBM, no estandar.
- UTF-16: menos eficiente para textos predominantemente latinos (2 bytes minimo vs 1 en UTF-8).

*Referencia: tema-11-contenido.md, seccion 9.3 [UNICODE-STD]*
</details>

---

## Criterios de evaluacion

| Cuestion | Puntos | Evaluacion |
|---|---|---|
| 1. Arquitectura CISC/RISC | 2 | Identificacion correcta + justificacion microinstrucciones |
| 2. MultiThreading | 2 | Concepto HT/SMT + calculo correcto 16 hilos |
| 3. Memoria RAM | 3 | Pines DDR4 + Dual Channel + ECC justificado |
| 4. BIOS/UEFI | 2 | 3 diferencias + Secure Boot + contexto AAPP |
| 5. Codificacion | 1 | UTF-8 + justificacion completa |
| **Total** | **10** | |

---

*Caso practico generado con asistencia de IA — Pendiente validacion humana*
*Contexto: supuesto practico de nivel C1 TIC para Ayuntamiento de Madrid*
*Fecha: 2026-04-16*
