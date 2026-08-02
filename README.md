# PP-01 — Planta de Inyección de Agua

### Animación 3D interactiva del sistema neumático e hidráulico

**Proyecto final · 2026**

| | |
|---|---|
| **Carrera** | Tecnicatura Superior en Mantenimiento Industrial — Plan 685 |
| **Módulo** | Sistemas Hidráulicos y Neumáticos |
| **Docente** | Ing. Cr. Germán Emanuel Paniagua |
| **Alumnos** | Carro · Puca · Torres · Seguel |
| **Institución** | ISETPN — Plaza Huincul, Neuquén |
| **Lugar** | Yacimiento Rincón del Mangrullo Norte — Cuenca Neuquina |
| **Documento base** | P&ID-PP01-001 · Rev. C |

---

## ▶ Ver la animación

**https://mrpuca.github.io/PP-01-Sistema-neumatico-hidraulico/**

Se abre directamente en el navegador. No requiere instalar nada ni tener conexión una vez cargada.

> Si el enlace todavía no funciona, hay que activar GitHub Pages: **Settings → Pages → Source: `main` / carpeta `/ (root)` → Save**. Tarda un par de minutos en publicarse.

---

## Qué muestra

La animación recorre cuatro secuencias seleccionables, cada una con cinco pasos narrados:

**1 · Recorrido del proceso**
Ingreso de agua de producción por la línea de 8" → tanque skimmer TK-051 → separación → tanques TKAG-052 y TKAG-053 → bombas → salida de petróleo y agua a inyección.

**2 · Cadena del aire de instrumentos**
Compresor Sullair S-Energy 1110 → secadora por adsorción → pulmones BOGE → colector de 2" → FRL → actuadores y posicionadores.

**3 · Falla del compresor y ESD2**
El compresor se detiene y el panel de instrumentación descuenta en vivo la presión de 10 a 4 kg/cm² y la autonomía de 33,4 minutos. Al alcanzar el límite, el PLC/ESD dispara el shutdown y todas las válvulas cierran por resorte: falla segura.

**4 · Contingencia hidráulica HPU-100**
Ante un derrame, la central Prayco eleva la rampa basculante con el cilindro Contarini y la tolva descarga los 1.500 kg de absorbente por gravedad.

---

## Cómo se usa

| Acción | Mouse | Táctil |
|---|---|---|
| Girar la vista | Arrastrar | Un dedo |
| Zoom | Rueda | Pellizco con dos dedos |
| Desplazar | Click derecho | Dos dedos |
| Ficha técnica de un equipo | Click sobre el equipo | Toque sobre el equipo |

**Atajos:** `I` datos del proyecto · `P` modo presentación (agranda el HUD para proyector) · `U` pantalla completa · `H` despeja los paneles · `Espacio` fija o suelta la cámara · `Esc` cierra.

En el teléfono los paneles se acomodan solos: la instrumentación pasa a una tira de datos arriba y los botones quedan como íconos. Si aun así molestan, el botón del **ojo** (👁) saca todo de la pantalla y deja la planta sola; se toca de nuevo para recuperarlos.

Hay **22 equipos con ficha técnica**: al hacer click aparecen sus datos nominales y el criterio de selección que lo justifica.

---

## Datos de diseño

**Sistema neumático**

- Compresor Sullair S-Energy 1110 — 15 HP · 1,4 m³/min · 10 kg/cm²
- Consumo de diseño: 0,71 m³/min (con 10 % de pérdidas y 30 % de ampliación)
- Dos pulmones BOGE de 2 m³ — 11,846 m³ de aire útil entre 10 y 4 kg/cm²
- Autonomía ante falla del compresor: **33,4 minutos**
- Red: 2" Sch40 · 162 m · longitud equivalente 191,84 m · ΔP = 0,141 bar

**Sistema hidráulico antiderrame**

- Central Prayco UVGM 60 — 7 HP · 15 L/min · tanque 60 L (ISO VG 46)
- Cilindro Contarini 92/80×50 — carrera 800 mm · 250 bar
- Presión de trabajo 180 bar · presión de bomba 194,5 bar · elevación ≈ 16 s
- Válvula de alivio pilotada a 241,3 bar
- Tolva esparcidora 7,5 m³ con 1.500 kg de absorbente (cubre 10 m³ de derrame)

---

## Nota técnica

Un solo archivo HTML de ~650 KB con **three.js r128 embebido**. Cero dependencias externas: no descarga librerías, imágenes ni fuentes. Toda la geometría se genera por código a partir del P&ID.

Funciona sin conexión a internet en cualquier navegador con WebGL.
