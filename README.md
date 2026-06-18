# Ya está jugando — Campaña ludopatía juvenil

Sitio web de campaña de concientización sobre **ludopatía juvenil**, implementado a partir del componente de Claude Design `Ya esta jugando.dc.html`.

Experiencia 3D scroll-driven (Three.js + Lenis), single-page, sin build: todo vive en `index.html`.

## Secciones

1. **Hero** — "Ya está jugando" + ruleta de luz.
2. **01 · El problema** — estadísticas animadas.
3. **02 · El doble sentido** — morph "JUGAR → APOSTAR".
4. **03 · La campaña** — galería 3D orbital de las 11 piezas (arrastrá para girar / botones ‹ ›).
5. **04 · Qué podés hacer** — señales de alerta, consejos y línea de ayuda.

## Ver online

Se sirve desde la raíz por GitHub Pages (`index.html`).

## Imágenes de la campaña (`piezas/`)

La galería 3D busca `piezas/pieza-01.png` … `pieza-11.png`. Si alguna falta, se
muestra un **placeholder** con franjas de advertencia y el nombre de la pieza
(diseño intencional, la web funciona igual).

Para usar las imágenes reales: exportá las 11 piezas desde el proyecto de Claude
Design (carpeta `piezas/`) y dejalas acá con esos nombres. Al hacer `git push`,
GitHub Pages las toma automáticamente.

## Editar

- **Textos** → directamente en el HTML de `index.html`.
- **Datos de las piezas** (título, formato, descripción) → array `PIEZAS` en el `<script>`.
- **Color de acento / densidad de objetos / reflejos / auto-rotación** → objeto `PROPS` al final del `<script>`.

---

Implementación autónoma: se reemplazó el runtime de Claude Design (`DCLogic` / `support.js`)
por un shim mínimo, para que el sitio corra como HTML estándar sin dependencias propietarias.
