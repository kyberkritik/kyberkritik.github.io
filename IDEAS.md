# Ideas pendientes — Mercurio en los engranajes

*Registro de posibilidades para desarrollar. No son tareas, son constelaciones.*

---

## Navegación y conexiones

### Mapa de constelaciones ⭐
Vista alternativa al grid donde las entradas son nodos y las conexiones WikiLink se dibujan como líneas pixel-art entre ellos. Al hover, la línea se ilumina y muestra el fragmento de conexión. Activable desde el header con un botón de toggle (grid ↔ mapa). Es la forma visual natural del Zettelkasten — en pixel-art, con nodos que parpadean y líneas que se trazan animadas, lo más cercano al ideal benjaminiano de constelaciones de ideas que se iluminan mutuamente.

### Historial de lectura visible
Una línea en el header que muestra el camino recorrido en la sesión: `Z-001 → Z-002 → …`. Cada entrada queda como rastro. El pensamiento como trayectoria, no como destino.

---

## Tipografía y texto

### Citas flotantes en margen
Si en el MD se marca un fragmento con `> texto` (blockquote), aparece en el margen derecho de la vista de lectura: tipografía más pequeña, cursiva, como las anotaciones marginales de Benjamin en sus cuadernos. En móvil, aparece inline con estilo diferenciado.

### Modo lectura con ruido
Filtro de grano sutil sobre el fondo del texto, como papel viejo o una transmisión analógica. Refuerza la idea de que se lee algo captado, no publicado. Activable/desactivable.

---

## 8-bit / Castlevania

### Transición de entrada por píxeles
Al abrir una entrada, la ilustración SVG aparece pixel a pixel, como si se "cargara" en una pantalla antigua. Efecto de barrido o dithering que construye la imagen en ~0.8 segundos. Posible con CSS clip-path animado o canvas.

### Cursor personalizado
Una cruceta pixel-art o un pequeño destello de mercurio que sigue el mouse. Pequeño detalle que define el tono desde el primer segundo.

### Sonido opcional
Un clic mecánico de máquina de escribir o un hum de radio al abrir una entrada. Activable/desactivable desde el header. Brecht habría amado que el aparato hiciera ruido.

---

## Estructura de contenido

### Entradas de segundo orden
Fichas `Z-001a`, `Z-001b` que son ampliaciones, objeciones o dudas sobre una entrada principal — como lo hacía Luhmann. En el grid se mostrarían más pequeñas, visualmente indentadas o con un marcador distinto. Se añaden al array con la misma lógica MD + SVG.

### Índice de conceptos (Fremdwörter)
Página separada `indices.html` que agrega automáticamente todos los términos en cursiva del texto (*Stimmung*, *epoché*, *Spätkapitalismus*, etc.) y los lista como entradas de diccionario con backlinks a las entradas donde aparecen. El extrañamiento lingüístico hecho visible.

### Fecha como eje — vista de línea de tiempo
Además del grid, una vista vertical estilo periódico: cada entrada ocupa su lugar cronológico, las del mismo mes se agrupan. El tiempo como espacio tipográfico. Toggle desde el header junto al mapa de constelaciones.

---

## Notas técnicas

- Todo sigue el mismo patrón: MD editable en VSCode → el sitio lo lee dinámicamente
- Para agregar una entrada: `entries/Z-XXX_titulo.md` + `illustrations/Z-XXX.svg` + línea en `ENTRY_IDS`
- El mapa de constelaciones requeriría una librería ligera de grafos (p.ej. `d3-force` solo el módulo de simulación) o implementación propia con canvas/SVG
- Los sonidos pueden ser Web Audio API generados en código (sin archivos externos)
