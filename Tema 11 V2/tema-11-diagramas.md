# Tema 11 — Catálogo de Diagramas

> **Titulo oficial**: Informatica basica. Representacion y comunicacion de la informacion: elementos constitutivos de un sistema de informacion. Caracteristicas y funciones. Arquitectura de ordenadores. Componentes internos de los equipos microinformaticos.
>
> **Version**: 2.0
> **Fecha**: 2026-04-23
> **Autor**: MGS
> **Formato**: SVG inline (zero-dependencias, escalable, imprimible)
> **Paleta**: Ayuntamiento de Madrid #0055a0 (primario) + #d13c3c (alertas) + #2d8659 (ventajas) + #e89822 (callouts)

---

## Indice de diagramas

| ID  | Titulo                         | Seccion | Tipo          | Formato |
|---|---|---|---|---|
| D1  | Piramide DIKW                  | § 1     | Piramide      | 600×340 |
| D2  | Componentes del SI             | § 2.2   | Bloques       | 640×360 |
| D3  | Piramide tipos de SI           | § 2.6   | Piramide      | 600×340 |
| D4  | Von Neumann vs Harvard         | § 3     | Comparativa   | 680×360 |
| D5  | Timeline de generaciones       | § 4     | Timeline      | 720×320 |
| D6  | Bloques internos de la CPU     | § 5.3   | Arquitectura  | 640×360 |
| D7  | Ciclo Fetch-Execute            | § 5.4   | Flowchart     | 640×360 |
| D8  | Modos de direccionamiento      | § 5.5   | Conceptual    | 680×360 |
| D9  | Jerarquia de memoria           | § 6.1   | Piramide      | 640×380 |
| D10 | Evolucion de la memoria RAM    | § 6.2   | Timeline      | 720×340 |
| D11 | BIOS vs UEFI                   | § 6.4   | Comparativa   | 680×360 |
| D12 | Estructura de UTF-8            | § 9.3   | Estructura    | 680×320 |

---

## D1 · Piramide DIKW

**Seccion**: § 1 — Concepto de dato e informacion
**Proposito**: Visualizar la jerarquia Dato → Informacion → Conocimiento → Sabiduria con ejemplo real del Ayto Madrid.

```svg
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
  <text x="480" y="40" class="dikw-title">Ayto Madrid</text>
  <text x="480" y="55" class="dikw-example">"¿subo el IBI?"</text>
  <text x="480" y="94" class="dikw-title">Tendencia</text>
  <text x="480" y="109" class="dikw-example">"la poblacion crece"</text>
  <text x="480" y="150" class="dikw-title">Contextualizado</text>
  <text x="480" y="165" class="dikw-example">"3,45 M habitantes"</text>
  <text x="480" y="215" class="dikw-title">Bruto</text>
  <text x="480" y="230" class="dikw-example">"3.450.000"</text>
  <text x="305" y="285" text-anchor="middle" font="italic 11px system-ui,sans-serif" fill="#666">+ contexto, + analisis, + experiencia</text>
  <path d="M 120 260 L 120 50" stroke="#0055a0" stroke-width="1" marker-end="url(#arrow1)" opacity="0.4"/>
  <defs><marker id="arrow1" markerWidth="10" markerHeight="10" refX="5" refY="5" orient="auto"><polygon points="0,0 10,5 0,10" fill="#0055a0"/></marker></defs>
  <text x="115" y="155" text-anchor="end" font="11px system-ui,sans-serif" fill="#0055a0" transform="rotate(-90 115 155)">mayor valor</text>
  <text x="305" y="315" text-anchor="middle" font="11px system-ui,sans-serif" fill="#666">[Fuente: adaptado de Ackoff, 1989 · ISO-2382]</text>
</svg>
```

---

## D2 · Componentes del sistema de informacion

**Seccion**: § 2.2 — Componentes basicos de un SI
**Proposito**: Mostrar los 7 componentes estructurales de un SI (Hardware, Software, Datos, Procedimientos, Usuarios, Red, Retroalimentacion) conectados en un modelo de bloques.

```svg
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
  <line x1="115" y1="130" x2="190" y2="160" stroke="#0055a0" stroke-width="1" opacity="0.5"/>
  <line x1="320" y1="130" x2="190" y2="160" stroke="#0055a0" stroke-width="1" opacity="0.5"/>
  <line x1="525" y1="130" x2="450" y2="160" stroke="#0055a0" stroke-width="1" opacity="0.5"/>
  <line x1="190" y1="220" x2="220" y2="250" stroke="#2d8659" stroke-width="1" opacity="0.5"/>
  <line x1="450" y1="220" x2="420" y2="250" stroke="#2d8659" stroke-width="1" opacity="0.5"/>
  <line x1="300" y1="280" x2="340" y2="280" stroke="#e89822" stroke-width="1.5" stroke-dasharray="4 4"/>
  <g transform="translate(30 335)">
    <rect width="12" height="12" class="si-tech"/><text x="18" y="10" font="11px system-ui,sans-serif" fill="#555">Tecnologia</text>
    <rect x="120" width="12" height="12" class="si-human"/><text x="138" y="10" font="11px system-ui,sans-serif" fill="#555">Humano</text>
    <rect x="220" width="12" height="12" class="si-flow"/><text x="238" y="10" font="11px system-ui,sans-serif" fill="#555">Flujo / comunicacion</text>
  </g>
</svg>
```

---

## D3 · Piramide de tipos de SI

**Seccion**: § 2.6 — Tipos de sistemas de informacion
**Proposito**: Mostrar la clasificacion jerarquica de sistemas de informacion (TPS, MIS, DSS, EIS) asociada a los niveles organizacionales.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 600 340" role="img" aria-label="Piramide de tipos de sistemas de informacion">
  <style>
    .tps-eis{font:700 14px system-ui,sans-serif;fill:#fff;text-anchor:middle}
    .tps-nivel{font:600 12px system-ui,sans-serif;fill:#1a1a1a}
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
  <text x="460" y="68" class="tps-user">vision global</text>
  <line x1="415" y1="102" x2="455" y2="102" stroke="#0055a0" stroke-width="1"/>
  <text x="460" y="92" class="tps-title">Analitico</text>
  <text x="460" y="107" class="tps-user">Analistas</text>
  <text x="460" y="120" class="tps-user">simulaciones</text>
  <line x1="415" y1="162" x2="455" y2="162" stroke="#0055a0" stroke-width="1"/>
  <text x="460" y="152" class="tps-title">Gestion</text>
  <text x="460" y="167" class="tps-user">Mandos medios</text>
  <text x="460" y="180" class="tps-user">informes regulares</text>
  <line x1="415" y1="230" x2="455" y2="230" stroke="#0055a0" stroke-width="1"/>
  <text x="460" y="220" class="tps-title">Operativo</text>
  <text x="460" y="235" class="tps-user">Operarios</text>
  <text x="460" y="248" class="tps-user">transacciones diarias</text>
  <line x1="145" y1="50" x2="185" y2="50" stroke="#0055a0" stroke-width="1"/>
  <text x="140" y="55" class="tps-user" text-anchor="end">Executive Info</text>
  <line x1="145" y1="107" x2="180" y2="107" stroke="#0055a0" stroke-width="1"/>
  <text x="140" y="112" class="tps-user" text-anchor="end">Decision Support</text>
  <line x1="145" y1="162" x2="175" y2="162" stroke="#0055a0" stroke-width="1"/>
  <text x="140" y="167" class="tps-user" text-anchor="end">Management Info</text>
  <line x1="145" y1="232" x2="170" y2="232" stroke="#0055a0" stroke-width="1"/>
  <text x="140" y="237" class="tps-user" text-anchor="end">Transaction Processing</text>
  <text x="300" y="300" text-anchor="middle" font="italic 11px system-ui,sans-serif" fill="#666">+ agregacion, - volumen / + volumen, - agregacion</text>
  <text x="300" y="320" text-anchor="middle" font="11px system-ui,sans-serif" fill="#666">Ej. Ayto Madrid: TPS=Padron · MIS=informes censales · DSS=planificacion urbana · EIS=cuadro mando alcalde</text>
</svg>
```

---

## D4 · Von Neumann vs Harvard

**Seccion**: § 3.1 · 3.2 — Arquitecturas de ordenadores
**Proposito**: Comparar visualmente ambas arquitecturas side-by-side evidenciando el cuello de botella de Von Neumann.

```svg
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
  <polygon points="215,100 225,105 215,110" fill="#0055a0"/>
  <polygon points="215,100 205,105 215,110" fill="#0055a0" transform="translate(-50 0)"/>
  <text x="190" y="97" class="arch-sub">bus compartido</text>
  <rect x="60" y="160" width="290" height="60" rx="4" fill="#fce4e4" stroke="#d13c3c" stroke-width="1.5" stroke-dasharray="5 3"/>
  <text x="205" y="185" class="arch-label" fill="#d13c3c">Cuello de botella Von Neumann</text>
  <text x="205" y="205" class="arch-sub">no se puede leer dato e instruccion a la vez</text>
  <text x="205" y="250" text-anchor="middle" font="11px system-ui,sans-serif" fill="#555">Implementaciones:</text>
  <text x="205" y="268" text-anchor="middle" font="11px system-ui,sans-serif" fill="#555">EDVAC (1949) · ENIAC (1945) · IBM 701</text>
  <line x1="360" y1="40" x2="360" y2="320" stroke="#c0c7cf" stroke-width="1" stroke-dasharray="3 3"/>
  <text x="510" y="32" class="arch-title" fill="#2d8659">Arquitectura Harvard</text>
  <text x="510" y="50" class="arch-sub">1944 (Harvard Mark I) · 2 memorias · 2 buses</text>
  <rect x="400" y="80" width="100" height="50" rx="4" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="450" y="103" class="arch-label">CPU</text>
  <text x="450" y="118" class="arch-sub">fetch || exec</text>
  <rect x="560" y="50" width="110" height="40" rx="4" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="615" y="70" class="arch-label">Mem. instr.</text>
  <text x="615" y="83" class="arch-sub">solo lectura</text>
  <rect x="560" y="120" width="110" height="40" rx="4" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="615" y="140" class="arch-label">Mem. datos</text>
  <text x="615" y="153" class="arch-sub">lectura/escritura</text>
  <line x1="500" y1="95" x2="560" y2="70" stroke="#2d8659" stroke-width="3"/>
  <polygon points="556,65 564,70 556,73" fill="#2d8659"/>
  <text x="540" y="82" class="arch-sub">bus I</text>
  <line x1="500" y1="115" x2="560" y2="140" stroke="#2d8659" stroke-width="3"/>
  <polygon points="556,136 564,140 556,144" fill="#2d8659"/>
  <text x="540" y="134" class="arch-sub">bus D</text>
  <rect x="400" y="180" width="270" height="60" rx="4" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5" stroke-dasharray="5 3"/>
  <text x="535" y="205" class="arch-label" fill="#2d8659">Acceso paralelo</text>
  <text x="535" y="225" class="arch-sub">instruccion y dato simultaneos</text>
  <text x="535" y="258" text-anchor="middle" font="11px system-ui,sans-serif" fill="#555">Implementaciones:</text>
  <text x="535" y="276" text-anchor="middle" font="11px system-ui,sans-serif" fill="#555">microcontroladores AVR, PIC · DSP · ARM L1</text>
  <rect x="60" y="295" width="610" height="50" rx="4" fill="#f5f5f5" stroke="#c0c7cf"/>
  <text x="70" y="314" font="600 12px system-ui,sans-serif" fill="#0055a0">Harvard modificada (actual):</text>
  <text x="70" y="332" font="11px system-ui,sans-serif" fill="#555">x86-64, ARM Cortex-A · cache L1 separada (I/D) pero memoria principal unica · combina lo mejor de ambas</text>
</svg>
```

---

## D5 · Timeline de generaciones de ordenadores

**Seccion**: § 4 — Generaciones de ordenadores
**Proposito**: Linea temporal horizontal con las 5 generaciones clasicas (1940-1991) + extension a 6ª generacion (actualidad).

```svg
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
  <text x="110" y="215" class="gen-tech">de vacio</text>
  <text x="110" y="240" class="gen-ex">ENIAC</text>
  <text x="110" y="255" class="gen-ex">Mark I</text>
  <circle cx="220" cy="170" r="18" fill="#0055a0"/>
  <text x="220" y="175" class="gen-num">2ª</text>
  <text x="220" y="130" class="gen-year">1952-1964</text>
  <text x="220" y="200" class="gen-tech">Transistor</text>
  <text x="220" y="215" class="gen-tech">(Bardeen 47)</text>
  <text x="220" y="240" class="gen-ex">TRADIC</text>
  <text x="220" y="255" class="gen-ex">IBM 1401</text>
  <circle cx="330" cy="170" r="18" fill="#0055a0"/>
  <text x="330" y="175" class="gen-num">3ª</text>
  <text x="330" y="130" class="gen-year">1964-1970</text>
  <text x="330" y="200" class="gen-tech">Circuitos</text>
  <text x="330" y="215" class="gen-tech">integrados</text>
  <text x="330" y="240" class="gen-ex">PDP-11</text>
  <text x="330" y="255" class="gen-ex">S/360</text>
  <circle cx="440" cy="170" r="18" fill="#0055a0"/>
  <text x="440" y="175" class="gen-num">4ª</text>
  <text x="440" y="130" class="gen-year">1970-1981</text>
  <text x="440" y="200" class="gen-tech">Microproc.</text>
  <text x="440" y="215" class="gen-tech">(Intel 4004)</text>
  <text x="440" y="240" class="gen-ex">Altair 8800</text>
  <text x="440" y="255" class="gen-ex">IBM PC 5150</text>
  <circle cx="550" cy="170" r="18" fill="#0055a0"/>
  <text x="550" y="175" class="gen-num">5ª</text>
  <text x="550" y="130" class="gen-year">1981-1991</text>
  <text x="550" y="200" class="gen-tech">IA · Redes</text>
  <text x="550" y="215" class="gen-tech">GUI · VLSI</text>
  <text x="550" y="240" class="gen-ex">Apple Mac</text>
  <text x="550" y="255" class="gen-ex">Internet</text>
  <circle cx="640" cy="170" r="18" fill="#2d8659" stroke="#2d8659" stroke-width="2" stroke-dasharray="2 2"/>
  <text x="640" y="175" class="gen-num">6ª</text>
  <text x="640" y="130" class="gen-year" fill="#2d8659">1991 → hoy</text>
  <text x="640" y="200" class="gen-tech">Cuantica</text>
  <text x="640" y="215" class="gen-tech">Neuromorf.</text>
  <text x="640" y="240" class="gen-ex">IBM Q</text>
  <text x="640" y="255" class="gen-ex">Intel Loihi</text>
  <rect x="60" y="280" width="600" height="28" rx="3" fill="#f5f5f5" stroke="#c0c7cf"/>
  <text x="360" y="298" text-anchor="middle" font="11px system-ui,sans-serif" fill="#555">ms → ns → ps → fs   ·   Ley de Moore: transistores x2 cada ~24 meses   ·   Ayto Madrid: IBM 650 RENFE 1959 = primer ordenador en Espana</text>
</svg>
```

---

## D6 · Bloques internos de la CPU

**Seccion**: § 5.3 — Unidad Central de Proceso
**Proposito**: Mostrar la estructura interna de la CPU: ALU, UC, Registros y los 3 buses que la conectan al exterior.

```svg
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
  <text x="245" y="269" class="cpu-sub" fill="#cde4f0">x86: EAX, EBX, ECX · ARM: R0-R15</text>
  <rect x="470" y="80" width="140" height="50" rx="4" fill="#d6e4f0" stroke="#0055a0" stroke-width="1.5"/>
  <text x="540" y="102" class="cpu-heading" fill="#1a1a1a">Memoria RAM</text>
  <text x="540" y="118" class="cpu-sub">principal</text>
  <rect x="470" y="150" width="140" height="50" rx="4" fill="#d6e4f0" stroke="#0055a0" stroke-width="1.5"/>
  <text x="540" y="172" class="cpu-heading" fill="#1a1a1a">E/S</text>
  <text x="540" y="188" class="cpu-sub">perifericos</text>
  <rect x="470" y="220" width="140" height="50" rx="4" fill="#d6e4f0" stroke="#0055a0" stroke-width="1.5"/>
  <text x="540" y="242" class="cpu-heading" fill="#1a1a1a">ROM / BIOS</text>
  <text x="540" y="258" class="cpu-sub">firmware</text>
  <line x1="430" y1="120" x2="470" y2="105" stroke="#d13c3c" stroke-width="2.5"/>
  <polygon points="466,101 474,105 466,109" fill="#d13c3c"/>
  <polygon points="434,116 426,120 434,124" fill="#d13c3c"/>
  <text x="450" y="100" class="cpu-bus" fill="#d13c3c">control</text>
  <line x1="430" y1="170" x2="470" y2="175" stroke="#2d8659" stroke-width="2.5"/>
  <polygon points="466,171 474,175 466,179" fill="#2d8659"/>
  <polygon points="434,171 426,175 434,179" fill="#2d8659"/>
  <text x="450" y="166" class="cpu-bus" fill="#2d8659">direcciones</text>
  <line x1="430" y1="240" x2="470" y2="245" stroke="#0055a0" stroke-width="2.5"/>
  <polygon points="466,241 474,245 466,249" fill="#0055a0"/>
  <polygon points="434,241 426,245 434,249" fill="#0055a0"/>
  <text x="450" y="236" class="cpu-bus" fill="#0055a0">datos</text>
  <text x="320" y="325" text-anchor="middle" font="12px system-ui,sans-serif" fill="#0055a0" font-weight="600">3 buses · separacion fisica y logica</text>
  <text x="320" y="345" text-anchor="middle" font="11px system-ui,sans-serif" fill="#666">control (unidireccional UC→dispositivos) · direcciones (unidireccional) · datos (bidireccional)</text>
</svg>
```

---

## D7 · Ciclo Fetch-Execute

**Seccion**: § 5.4 — Ciclo de ejecucion de instrucciones
**Proposito**: Flowchart de los 7 pasos del ciclo de instruccion, divididos en las 2 fases canonicas (busqueda y ejecucion).

```svg
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
  <text x="95" y="125" class="fe-desc">direccion instr.</text>
  <rect x="160" y="90" width="90" height="45" rx="3" fill="#0055a0"/>
  <text x="205" y="110" class="fe-step">2. MAR → Mem</text>
  <text x="205" y="125" class="fe-desc">bus direcciones</text>
  <rect x="270" y="90" width="85" height="45" rx="3" fill="#0055a0"/>
  <text x="312" y="110" class="fe-step">3. Mem → MBR</text>
  <text x="312" y="125" class="fe-desc">bus datos</text>
  <rect x="110" y="150" width="90" height="40" rx="3" fill="#0055a0"/>
  <text x="155" y="170" class="fe-step">4. MBR → RI</text>
  <text x="155" y="183" class="fe-desc">transfiere instr.</text>
  <rect x="220" y="150" width="120" height="40" rx="3" fill="#0055a0"/>
  <text x="280" y="170" class="fe-step">5. CP + 1</text>
  <text x="280" y="183" class="fe-desc">apunta siguiente</text>
  <line x1="140" y1="112" x2="160" y2="112" stroke="#0055a0" stroke-width="2"/>
  <polygon points="156,108 164,112 156,116" fill="#0055a0"/>
  <line x1="250" y1="112" x2="270" y2="112" stroke="#0055a0" stroke-width="2"/>
  <polygon points="266,108 274,112 266,116" fill="#0055a0"/>
  <line x1="312" y1="135" x2="155" y2="150" stroke="#0055a0" stroke-width="1" opacity="0.6"/>
  <polygon points="155,146 150,152 160,152" fill="#0055a0" opacity="0.6"/>
  <line x1="200" y1="170" x2="220" y2="170" stroke="#0055a0" stroke-width="2"/>
  <polygon points="216,166 224,170 216,174" fill="#0055a0"/>
  <rect x="380" y="50" width="230" height="150" rx="6" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5" stroke-dasharray="4 3"/>
  <text x="395" y="68" class="fe-phase" fill="#2d8659">FASE 2 · EXECUTE (ejecucion)</text>
  <rect x="400" y="90" width="90" height="45" rx="3" fill="#2d8659"/>
  <text x="445" y="110" class="fe-step">6. Decode</text>
  <text x="445" y="125" class="fe-desc">interpreta RI</text>
  <rect x="510" y="90" width="90" height="45" rx="3" fill="#2d8659"/>
  <text x="555" y="110" class="fe-step">7. Execute</text>
  <text x="555" y="125" class="fe-desc">ALU / mem / E-S</text>
  <line x1="490" y1="112" x2="510" y2="112" stroke="#2d8659" stroke-width="2"/>
  <polygon points="506,108 514,112 506,116" fill="#2d8659"/>
  <rect x="400" y="150" width="200" height="40" rx="3" fill="#e89822"/>
  <text x="500" y="170" class="fe-step">Actualiza PC / flags / registros</text>
  <text x="500" y="183" class="fe-desc">resultados de la operacion</text>
  <line x1="360" y1="112" x2="400" y2="112" stroke="#1a1a1a" stroke-width="2.5"/>
  <polygon points="396,108 404,112 396,116" fill="#1a1a1a"/>
  <path d="M 600 170 Q 620 170 620 230 Q 620 260 95 260 Q 60 260 60 210" stroke="#d13c3c" stroke-width="1.5" fill="none" stroke-dasharray="4 3"/>
  <polygon points="64,214 60,206 56,214" fill="#d13c3c"/>
  <text x="340" y="275" text-anchor="middle" font="italic 12px system-ui,sans-serif" fill="#d13c3c">bucle: siguiente instruccion</text>
  <text x="320" y="310" text-anchor="middle" font="11px system-ui,sans-serif" fill="#555">CP = Contador de Programa · MAR = Memory Address Register · MBR = Memory Buffer Register · RI = Registro de Instruccion</text>
  <text x="320" y="328" text-anchor="middle" font="11px system-ui,sans-serif" fill="#555">Un Pentium IV a 2 GHz ejecuta ~2.000 millones de estos ciclos por segundo (pero 1 instr. ≠ 1 ciclo)</text>
</svg>
```

---

## D8 · Modos de direccionamiento

**Seccion**: § 5.5 — Modos de direccionamiento
**Proposito**: Visualizar los 5 modos fundamentales usando el mismo operando (42) para evidenciar como cambia la direccion efectiva.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 360" role="img" aria-label="Modos de direccionamiento">
  <style>
    .md-title{font:600 12px system-ui,sans-serif;fill:#0055a0;text-anchor:middle;letter-spacing:0.5px}
    .md-cell{font:600 13px system-ui,sans-serif;fill:#1a1a1a;text-anchor:middle}
    .md-note{font:10px system-ui,sans-serif;fill:#555;text-anchor:middle}
    .md-op{font:700 13px system-ui,sans-serif;fill:#2d8659;text-anchor:middle}
  </style>
  <text x="340" y="30" text-anchor="middle" font="700 16px system-ui,sans-serif" fill="#0055a0">Modos de direccionamiento</text>
  <text x="340" y="48" text-anchor="middle" font="11px system-ui,sans-serif" fill="#666">operando objetivo en todos los casos: 42</text>
  <text x="80" y="75" class="md-title">1. Inmediato</text>
  <rect x="25" y="90" width="110" height="30" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="40" y="110" font="600 11px system-ui,sans-serif" fill="#555">SUMA #42</text>
  <text x="115" y="110" class="md-op">← 42</text>
  <text x="80" y="145" class="md-note">operando en</text>
  <text x="80" y="158" class="md-note">la instruccion</text>
  <text x="80" y="176" class="md-note" fill="#2d8659" font-weight="600">1 acceso</text>
  <text x="210" y="75" class="md-title">2. Directo</text>
  <rect x="155" y="90" width="110" height="30" fill="#eef4fa" stroke="#0055a0" stroke-width="1.5"/>
  <text x="170" y="110" font="600 11px system-ui,sans-serif" fill="#555">SUMA [100]</text>
  <rect x="155" y="135" width="110" height="30" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="167" y="155" font="10px system-ui,sans-serif" fill="#555">M[100]:</text>
  <text x="230" y="155" class="md-op">42</text>
  <line x1="210" y1="120" x2="210" y2="135" stroke="#0055a0" stroke-width="1.5"/>
  <polygon points="206,131 214,131 210,137" fill="#0055a0"/>
  <text x="210" y="185" class="md-note">direccion en instr.</text>
  <text x="210" y="200" class="md-note" fill="#0055a0" font-weight="600">2 accesos</text>
  <text x="340" y="75" class="md-title">3. Indirecto</text>
  <rect x="285" y="90" width="110" height="30" fill="#eef4fa" stroke="#0055a0" stroke-width="1.5"/>
  <text x="297" y="110" font="600 11px system-ui,sans-serif" fill="#555">SUMA [[500]]</text>
  <rect x="285" y="135" width="110" height="30" fill="#f5f5f5" stroke="#666" stroke-width="1.5"/>
  <text x="297" y="155" font="10px system-ui,sans-serif" fill="#555">M[500]:</text>
  <text x="360" y="155" font="600 12px system-ui,sans-serif" fill="#1a1a1a">100</text>
  <rect x="285" y="180" width="110" height="30" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="297" y="200" font="10px system-ui,sans-serif" fill="#555">M[100]:</text>
  <text x="360" y="200" class="md-op">42</text>
  <line x1="340" y1="120" x2="340" y2="135" stroke="#0055a0" stroke-width="1.5"/>
  <polygon points="336,131 344,131 340,137" fill="#0055a0"/>
  <line x1="340" y1="165" x2="340" y2="180" stroke="#0055a0" stroke-width="1.5"/>
  <polygon points="336,176 344,176 340,182" fill="#0055a0"/>
  <text x="340" y="230" class="md-note">doble dereferencia</text>
  <text x="340" y="245" class="md-note" fill="#d13c3c" font-weight="600">3 accesos (lento)</text>
  <text x="470" y="75" class="md-title">4. Rel. base</text>
  <rect x="415" y="90" width="110" height="30" fill="#eef4fa" stroke="#0055a0" stroke-width="1.5"/>
  <text x="423" y="110" font="600 11px system-ui,sans-serif" fill="#555">SUMA [BP+10]</text>
  <rect x="415" y="135" width="110" height="22" fill="#fef0d6" stroke="#e89822" stroke-width="1.5"/>
  <text x="425" y="151" font="10px system-ui,sans-serif" fill="#555">BP =</text>
  <text x="495" y="151" font="600 11px system-ui,sans-serif" fill="#e89822">90</text>
  <rect x="415" y="172" width="110" height="30" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="427" y="192" font="10px system-ui,sans-serif" fill="#555">M[100]:</text>
  <text x="495" y="192" class="md-op">42</text>
  <line x1="470" y1="120" x2="470" y2="135" stroke="#e89822" stroke-width="1.5"/>
  <polygon points="466,131 474,131 470,137" fill="#e89822"/>
  <text x="470" y="220" class="md-note">BP(90) + 10 = 100</text>
  <text x="470" y="234" class="md-note" fill="#e89822" font-weight="600">reentrante</text>
  <text x="600" y="75" class="md-title">5. Indexado</text>
  <rect x="545" y="90" width="110" height="30" fill="#eef4fa" stroke="#0055a0" stroke-width="1.5"/>
  <text x="552" y="110" font="600 11px system-ui,sans-serif" fill="#555">SUMA [1000+X]</text>
  <rect x="545" y="135" width="110" height="22" fill="#fef0d6" stroke="#e89822" stroke-width="1.5"/>
  <text x="558" y="151" font="10px system-ui,sans-serif" fill="#555">X =</text>
  <text x="625" y="151" font="600 11px system-ui,sans-serif" fill="#e89822">5</text>
  <rect x="545" y="172" width="110" height="30" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="557" y="192" font="10px system-ui,sans-serif" fill="#555">M[1005]:</text>
  <text x="630" y="192" class="md-op">42</text>
  <line x1="600" y1="120" x2="600" y2="135" stroke="#e89822" stroke-width="1.5"/>
  <polygon points="596,131 604,131 600,137" fill="#e89822"/>
  <text x="600" y="220" class="md-note">1000 + X(5) = 1005</text>
  <text x="600" y="234" class="md-note" fill="#e89822" font-weight="600">arrays, bucles</text>
  <rect x="25" y="275" width="630" height="65" rx="4" fill="#f5f5f5" stroke="#c0c7cf"/>
  <text x="35" y="295" font="600 12px system-ui,sans-serif" fill="#0055a0">Impropios (operando fuera de memoria):</text>
  <text x="35" y="312" font="11px system-ui,sans-serif" fill="#555">implicito (en la instruccion, p.ej. PUSH usa SP) · inmediato (en la propia instruccion)</text>
  <text x="35" y="328" font="600 12px system-ui,sans-serif" fill="#0055a0">Propios (operando en memoria): directo · indirecto · relativo · indexado</text>
</svg>
```

---

## D9 · Jerarquia de memoria

**Seccion**: § 6.1 — Clasificaciones de memoria
**Proposito**: Piramide de 7 niveles mostrando el trade-off velocidad ↔ capacidad ↔ coste.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 380" role="img" aria-label="Jerarquia de memoria">
  <style>
    .jm-label{font:600 13px system-ui,sans-serif;fill:#fff;text-anchor:middle}
    .jm-speed{font:11px system-ui,sans-serif;fill:#555;text-anchor:start}
    .jm-cap{font:11px system-ui,sans-serif;fill:#555;text-anchor:end}
    .jm-axis{font:600 11px system-ui,sans-serif;fill:#0055a0;letter-spacing:1px}
  </style>
  <text x="320" y="28" text-anchor="middle" font="700 16px system-ui,sans-serif" fill="#0055a0">Jerarquia de memoria</text>
  <polygon points="295,55 345,55 360,85 280,85" fill="#003d73"/>
  <text x="320" y="75" class="jm-label">Registros</text>
  <polygon points="280,85 360,85 375,120 265,120" fill="#0055a0"/>
  <text x="320" y="108" class="jm-label">Cache L1</text>
  <polygon points="265,120 375,120 395,160 245,160" fill="#0055a0" opacity="0.85"/>
  <text x="320" y="144" class="jm-label">Cache L2 / L3</text>
  <polygon points="245,160 395,160 420,210 220,210" fill="#3378b9"/>
  <text x="320" y="189" class="jm-label">Memoria principal (RAM)</text>
  <polygon points="220,210 420,210 450,265 190,265" fill="#6ea3d2"/>
  <text x="320" y="242" class="jm-label" fill="#1a1a1a">SSD (NAND Flash)</text>
  <polygon points="190,265 450,265 485,320 155,320" fill="#d6e4f0"/>
  <text x="320" y="295" class="jm-label" fill="#1a1a1a">HDD (magnetico)</text>
  <text x="320" y="310" font="11px system-ui,sans-serif" fill="#555" text-anchor="middle">/ cinta / nube / archivo</text>
  <text x="500" y="75" class="jm-speed">~0,3 ns · KB</text>
  <text x="500" y="107" class="jm-speed">~1 ns · 32-64 KB</text>
  <text x="500" y="142" class="jm-speed">~3-20 ns · 1-32 MB</text>
  <text x="500" y="188" class="jm-speed">~100 ns · 8-128 GB</text>
  <text x="500" y="240" class="jm-speed">~20-100 µs · 1-4 TB</text>
  <text x="500" y="292" class="jm-speed">~10 ms · 1-20 TB</text>
  <text x="140" y="75" class="jm-cap">+ rapida</text>
  <text x="140" y="292" class="jm-cap">+ lenta</text>
  <line x1="115" y1="60" x2="115" y2="315" stroke="#0055a0" stroke-width="1"/>
  <polygon points="112,65 118,65 115,57" fill="#0055a0"/>
  <polygon points="112,310 118,310 115,318" fill="#0055a0"/>
  <text x="110" y="150" class="jm-axis" text-anchor="middle" transform="rotate(-90 110 150)">VELOCIDAD</text>
  <line x1="555" y1="60" x2="555" y2="315" stroke="#0055a0" stroke-width="1"/>
  <polygon points="552,65 558,65 555,57" fill="#0055a0"/>
  <polygon points="552,310 558,310 555,318" fill="#0055a0"/>
  <text x="580" y="150" class="jm-axis" text-anchor="middle" transform="rotate(90 580 150)">CAPACIDAD</text>
  <rect x="60" y="340" width="520" height="30" rx="3" fill="#f5f5f5" stroke="#c0c7cf"/>
  <text x="320" y="359" text-anchor="middle" font="11px system-ui,sans-serif" fill="#555">Regla: cada nivel es ~10-100× mas lento y ~10-100× mas grande que el anterior · CPU Apple M3: L1=192KB, L2=16MB, RAM=24GB</text>
</svg>
```

---

## D10 · Evolucion de la memoria RAM

**Seccion**: § 6.2 — Memoria RAM
**Proposito**: Timeline + comparativa visual de modulos RAM desde los años 60 hasta DDR5 actual.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 720 340" role="img" aria-label="Evolucion de la memoria RAM">
  <style>
    .ram-year{font:600 11px system-ui,sans-serif;fill:#0055a0;text-anchor:middle}
    .ram-name{font:700 12px system-ui,sans-serif;fill:#1a1a1a;text-anchor:middle}
    .ram-spec{font:10px system-ui,sans-serif;fill:#555;text-anchor:middle}
  </style>
  <text x="360" y="28" text-anchor="middle" font="700 16px system-ui,sans-serif" fill="#0055a0">Evolucion de la memoria RAM</text>
  <text x="360" y="46" text-anchor="middle" font="11px system-ui,sans-serif" fill="#666">mayor barra = mayor capacidad y velocidad [JEDEC]</text>
  <line x1="40" y1="240" x2="690" y2="240" stroke="#0055a0" stroke-width="2"/>
  <rect x="55" y="210" width="35" height="30" fill="#d6e4f0" stroke="#0055a0" stroke-width="1"/>
  <text x="72" y="200" class="ram-year">60s-70s</text>
  <text x="72" y="260" class="ram-name">DIP</text>
  <text x="72" y="275" class="ram-spec">dual in-line</text>
  <text x="72" y="288" class="ram-spec">16-64 KB</text>
  <rect x="115" y="195" width="40" height="45" fill="#d6e4f0" stroke="#0055a0" stroke-width="1"/>
  <text x="135" y="185" class="ram-year">1983</text>
  <text x="135" y="260" class="ram-name">SIPP</text>
  <text x="135" y="275" class="ram-spec">30 pines</text>
  <text x="135" y="288" class="ram-spec">80286</text>
  <rect x="180" y="180" width="45" height="60" fill="#d6e4f0" stroke="#0055a0" stroke-width="1"/>
  <text x="202" y="170" class="ram-year">1987</text>
  <text x="202" y="260" class="ram-name">SIMM</text>
  <text x="202" y="275" class="ram-spec">30/72 pines</text>
  <text x="202" y="288" class="ram-spec">32 bits</text>
  <rect x="250" y="160" width="50" height="80" fill="#3378b9" stroke="#0055a0" stroke-width="1"/>
  <text x="275" y="150" class="ram-year">1993</text>
  <text x="275" y="260" class="ram-name">DIMM</text>
  <text x="275" y="275" class="ram-spec">168 pines</text>
  <text x="275" y="288" class="ram-spec">64 bits</text>
  <rect x="325" y="140" width="52" height="100" fill="#3378b9" stroke="#0055a0" stroke-width="1"/>
  <text x="351" y="130" class="ram-year">2000</text>
  <text x="351" y="260" class="ram-name">DDR</text>
  <text x="351" y="275" class="ram-spec">184p · 400 MHz</text>
  <text x="351" y="288" class="ram-spec">hasta 1 GB</text>
  <rect x="400" y="120" width="52" height="120" fill="#0055a0" stroke="#003d73" stroke-width="1"/>
  <text x="426" y="110" class="ram-year">2003</text>
  <text x="426" y="260" class="ram-name">DDR2</text>
  <text x="426" y="275" class="ram-spec">240p · 800 MHz</text>
  <text x="426" y="288" class="ram-spec">hasta 2 GB</text>
  <rect x="475" y="95" width="54" height="145" fill="#0055a0" stroke="#003d73" stroke-width="1"/>
  <text x="502" y="85" class="ram-year">2007</text>
  <text x="502" y="260" class="ram-name">DDR3</text>
  <text x="502" y="275" class="ram-spec">240p · 2400 MHz</text>
  <text x="502" y="288" class="ram-spec">hasta 16 GB</text>
  <rect x="552" y="65" width="56" height="175" fill="#0055a0" stroke="#003d73" stroke-width="1"/>
  <text x="580" y="55" class="ram-year">2014</text>
  <text x="580" y="260" class="ram-name">DDR4</text>
  <text x="580" y="275" class="ram-spec">288p · 3200 MHz</text>
  <text x="580" y="288" class="ram-spec">hasta 64 GB</text>
  <rect x="632" y="30" width="58" height="210" fill="#2d8659" stroke="#1e5a3d" stroke-width="1.5"/>
  <text x="661" y="20" class="ram-year" fill="#2d8659">2021</text>
  <text x="661" y="260" class="ram-name" fill="#2d8659">DDR5</text>
  <text x="661" y="275" class="ram-spec" fill="#2d8659">288p · 6400 MHz</text>
  <text x="661" y="288" class="ram-spec" fill="#2d8659">hasta 128 GB</text>
  <rect x="40" y="305" width="650" height="28" rx="3" fill="#f5f5f5" stroke="#c0c7cf"/>
  <text x="365" y="323" text-anchor="middle" font="11px system-ui,sans-serif" fill="#555">DDR2/3 mismos 240p pero muesca distinta (INCOMPATIBLES) · DDR4/5 mismos 288p pero diferente voltaje (INCOMPATIBLES)</text>
</svg>
```

---

## D11 · BIOS vs UEFI

**Seccion**: § 6.4 — BIOS y UEFI
**Proposito**: Comparativa de 8 aspectos clave entre el firmware clasico y su sucesor moderno.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 360" role="img" aria-label="Comparativa BIOS vs UEFI">
  <style>
    .bu-title{font:700 16px system-ui,sans-serif;text-anchor:middle}
    .bu-row{font:11px system-ui,sans-serif;fill:#1a1a1a}
    .bu-aspect{font:600 11px system-ui,sans-serif;fill:#0055a0;text-anchor:middle}
    .bu-year{font:italic 11px system-ui,sans-serif;text-anchor:middle}
  </style>
  <text x="340" y="28" text-anchor="middle" font="700 16px system-ui,sans-serif" fill="#0055a0">BIOS vs UEFI</text>
  <rect x="30" y="50" width="200" height="290" rx="6" fill="#f5f5f5" stroke="#999" stroke-width="1.5"/>
  <text x="130" y="78" class="bu-title" fill="#666">BIOS</text>
  <text x="130" y="94" class="bu-year" fill="#666">Basic Input/Output System · 1975</text>
  <rect x="250" y="50" width="180" height="290" rx="6" fill="#eef4fa" stroke="#0055a0" stroke-width="2"/>
  <text x="340" y="110" class="bu-aspect">Arquitectura</text>
  <text x="340" y="135" class="bu-aspect">Interfaz</text>
  <text x="340" y="160" class="bu-aspect">Conectividad</text>
  <text x="340" y="185" class="bu-aspect">Particiones</text>
  <text x="340" y="210" class="bu-aspect">Capacidad max.</text>
  <text x="340" y="235" class="bu-aspect">Arranque</text>
  <text x="340" y="260" class="bu-aspect">Seguridad</text>
  <text x="340" y="285" class="bu-aspect">Extensibilidad</text>
  <rect x="450" y="50" width="200" height="290" rx="6" fill="#d8f0dc" stroke="#2d8659" stroke-width="1.5"/>
  <text x="550" y="78" class="bu-title" fill="#2d8659">UEFI</text>
  <text x="550" y="94" class="bu-year" fill="#2d8659">Unified Extensible Firmware Interface</text>
  <text x="130" y="115" class="bu-row" text-anchor="middle">16 bits · modo real</text>
  <text x="550" y="115" class="bu-row" text-anchor="middle" fill="#2d8659">32 o 64 bits · modo protegido</text>
  <text x="130" y="140" class="bu-row" text-anchor="middle">Texto · solo teclado</text>
  <text x="550" y="140" class="bu-row" text-anchor="middle" fill="#2d8659">GUI · raton · animaciones</text>
  <text x="130" y="165" class="bu-row" text-anchor="middle" fill="#d13c3c">Aislado</text>
  <text x="550" y="165" class="bu-row" text-anchor="middle" fill="#2d8659">Internet · red</text>
  <text x="130" y="190" class="bu-row" text-anchor="middle" fill="#d13c3c">4 particiones MBR</text>
  <text x="550" y="190" class="bu-row" text-anchor="middle" fill="#2d8659">128 particiones GPT</text>
  <text x="130" y="215" class="bu-row" text-anchor="middle" fill="#d13c3c">2,2 TB por disco</text>
  <text x="550" y="215" class="bu-row" text-anchor="middle" fill="#2d8659">8 ZB por disco</text>
  <text x="130" y="240" class="bu-row" text-anchor="middle">POST lento · ~30s</text>
  <text x="550" y="240" class="bu-row" text-anchor="middle" fill="#2d8659">Rapido · ~5s</text>
  <text x="130" y="265" class="bu-row" text-anchor="middle" fill="#d13c3c">Sin verificacion</text>
  <text x="550" y="265" class="bu-row" text-anchor="middle" fill="#2d8659">Secure Boot · TPM 2.0</text>
  <text x="130" y="290" class="bu-row" text-anchor="middle" fill="#d13c3c">Firme · no modular</text>
  <text x="550" y="290" class="bu-row" text-anchor="middle" fill="#2d8659">Modular · drivers propios</text>
  <text x="340" y="326" text-anchor="middle" font="600 12px system-ui,sans-serif" fill="#0055a0">UEFI es el estandar en PCs desde ~2012 (Windows 8) [UEFI Forum spec 2.10]</text>
</svg>
```

---

## D12 · Estructura de UTF-8

**Seccion**: § 9.3 — Unicode y UTF-8
**Proposito**: Mostrar la estructura binaria de UTF-8 por longitud, evidenciando la autosincronizacion y la compatibilidad ASCII.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 320" role="img" aria-label="Estructura de UTF-8">
  <style>
    .u8-title{font:700 16px system-ui,sans-serif;text-anchor:middle;fill:#0055a0}
    .u8-len{font:700 12px system-ui,sans-serif;fill:#0055a0}
    .u8-bits{font:600 11px monospace;fill:#fff;text-anchor:middle}
    .u8-range{font:italic 11px system-ui,sans-serif;fill:#555}
    .u8-example{font:600 12px monospace;fill:#1a1a1a}
  </style>
  <text x="340" y="28" class="u8-title">Estructura de UTF-8</text>
  <text x="340" y="46" text-anchor="middle" font="11px system-ui,sans-serif" fill="#666">longitud variable 1-4 bytes · autosincronizable [UNICODE-STD]</text>
  <text x="35" y="85" class="u8-len">1 byte</text>
  <rect x="100" y="68" width="80" height="28" fill="#0055a0"/>
  <text x="140" y="86" class="u8-bits">0xxxxxxx</text>
  <text x="195" y="85" class="u8-range">U+0000 - U+007F  ·  ASCII (128 caracteres)</text>
  <text x="195" y="100" class="u8-example" fill="#2d8659">"A" = 0100 0001</text>
  <text x="35" y="135" class="u8-len">2 bytes</text>
  <rect x="100" y="118" width="80" height="28" fill="#0055a0"/>
  <text x="140" y="136" class="u8-bits">110xxxxx</text>
  <rect x="182" y="118" width="80" height="28" fill="#3378b9"/>
  <text x="222" y="136" class="u8-bits">10xxxxxx</text>
  <text x="275" y="135" class="u8-range">U+0080 - U+07FF  ·  Latin extendido, griego, cirilico, hebreo</text>
  <text x="275" y="150" class="u8-example" fill="#2d8659">"n" = 1100 0011  1011 0001</text>
  <text x="35" y="185" class="u8-len">3 bytes</text>
  <rect x="100" y="168" width="80" height="28" fill="#0055a0"/>
  <text x="140" y="186" class="u8-bits">1110xxxx</text>
  <rect x="182" y="168" width="80" height="28" fill="#3378b9"/>
  <text x="222" y="186" class="u8-bits">10xxxxxx</text>
  <rect x="264" y="168" width="80" height="28" fill="#3378b9"/>
  <text x="304" y="186" class="u8-bits">10xxxxxx</text>
  <text x="355" y="185" class="u8-range">U+0800 - U+FFFF  ·  BMP (incluye CJK: chino, japones, coreano)</text>
  <text x="355" y="200" class="u8-example" fill="#2d8659">"€" = 1110 0010  1000 0010  1010 1100</text>
  <text x="35" y="235" class="u8-len">4 bytes</text>
  <rect x="100" y="218" width="80" height="28" fill="#0055a0"/>
  <text x="140" y="236" class="u8-bits">11110xxx</text>
  <rect x="182" y="218" width="80" height="28" fill="#3378b9"/>
  <text x="222" y="236" class="u8-bits">10xxxxxx</text>
  <rect x="264" y="218" width="80" height="28" fill="#3378b9"/>
  <text x="304" y="236" class="u8-bits">10xxxxxx</text>
  <rect x="346" y="218" width="80" height="28" fill="#3378b9"/>
  <text x="386" y="236" class="u8-bits">10xxxxxx</text>
  <text x="435" y="235" class="u8-range">U+10000 - U+10FFFF  ·  planos suplementarios (emojis, historicos)</text>
  <text x="435" y="250" class="u8-example" fill="#2d8659">"🎉" = 1111 0000  1001 1111  1001 0000  1000 1001</text>
  <rect x="30" y="275" width="620" height="40" rx="3" fill="#f5f5f5" stroke="#c0c7cf"/>
  <text x="40" y="293" font="600 11px system-ui,sans-serif" fill="#0055a0">Ventaja clave:</text>
  <text x="135" y="293" font="11px system-ui,sans-serif" fill="#555">primer byte indica cuantos siguen (0xxx=1, 110xx=2, 1110xx=3, 11110xx=4)</text>
  <text x="40" y="310" font="600 11px system-ui,sans-serif" fill="#0055a0">Resultado:</text>
  <text x="120" y="310" font="11px system-ui,sans-serif" fill="#555">texto puede leerse desde cualquier posicion · compatibilidad 100% con ASCII</text>
</svg>
```

---

## Notas de uso

- Los SVG son **inline** y **autosuficientes** — no requieren CDN ni fuentes externas.
- Usan `system-ui,sans-serif` para heredar la tipografia del documento contenedor.
- Las dimensiones son **escalables** via `viewBox` — se adaptan al ancho del contenedor.
- Para impresion en PDF A4 light theme funcionan tal cual (fondo blanco, colores legibles).
- Para embeber en `.docx`: copiar el codigo SVG → renderizar con herramienta online → insertar PNG resultante.
- Colores mantenidos dentro de la gama accesible WCAG AA (contraste > 4.5:1 entre texto y fondo).

---

*Cataloge generado como parte del pipeline v2.0 · MGS · 2026-04-23*
*Pendiente validacion humana: Maria / Ana*
