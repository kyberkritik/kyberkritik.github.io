# Mercurio en los engranajes
### Fragmentos y latencia de Zettelkasten — J.C. Latenz

Blog de fragmentos de texto organizado como un Zettelkasten digital. Cada entrada es una ficha de pensamiento con fecha y localización aproximada. Las fichas se conectan entre sí mediante vínculos que al presionarse muestran el pasaje relevante del texto referenciado, sin abandonar la lectura actual.

**→ [kyberkritik.github.io](https://kyberkritik.github.io)**

---

## Estructura

```
/
├── index.html              — sitio completo (CSS + motor JS)
├── entries/                — textos en Markdown, editables directamente
│   └── Z-XXX_titulo.md
├── illustrations/          — ilustraciones 8-bit pixel art en SVG
│   └── Z-XXX.svg
├── IDEAS.md                — ideas pendientes de desarrollo
└── .nojekyll               — deshabilita Jekyll para que fetch() funcione
```

## Agregar una entrada

1. Crear `entries/Z-XXX_titulo.md` con este frontmatter:

```yaml
---
id: Z-XXX
title: Título
date: DD de mes de AAAA
location: Ciudad, País
excerpt: Primera oración o frase que aparece en la tarjeta.
links: [Z-001, Z-002]
---

Texto en Markdown...
```

2. Crear `illustrations/Z-XXX.svg` — pixel art 320×200, estética 8-bit Castlevania
3. Añadir `'Z-XXX_titulo'` al array `ENTRY_IDS` en `index.html`

## Vínculos entre entradas

En el cuerpo del texto se usan WikiLinks:

```
[[Z-002|la música de elevador]]
```

Al hacer click aparece un popup con el pasaje exacto del texto referenciado donde aparece el concepto vinculado, con opción de abrir la entrada al lado para lectura paralela.

## Previsualización local

Requiere servidor HTTP (no funciona abriendo el archivo directamente):

```bash
python -m http.server 8000
# o usar VS Code Live Server
```

---

*Influencias: Zettelkasten (Luhmann) · revistas de Weimar (Brecht, Benjamin) · Futurismo italiano · pixel art gótico*
