# Mercurio en los engranajes

Sitio estático publicado en GitHub Pages.

**→ [kyberkritik.github.io](https://kyberkritik.github.io)**

## Política del repositorio

Este repositorio ahora versiona solo lo indispensable para mostrar la página publicada tal como existe en producción.

Se quedan en Git únicamente:

- `index.html`
- `es.html`
- `nosthoff.html`
- `entries/` usados por `index.html`
- `illustrations/` usadas por `index.html`
- `diagrams/` que sí aparecen en la lectura pública
- `images/` que sí aparecen en la interfaz pública
- `.nojekyll`

No se versionan borradores, notas, variantes descartadas, fuentes intermedias ni materiales de trabajo. Esos archivos se mantienen solo en la máquina local mediante `.gitignore`.

## Archivos solo locales

Actualmente quedan fuera del repositorio:

- `IDEAS.md`
- `el_muzak_borrador_benjaminiano.md`
- `nosthoff_techne_asimil_1abr26.md`
- `entries/Z-002.md`
- `illustrations/Z-002-arqueologia.svg`
- `diagrams/forma-mercancia.dot`
- `images/mercur copy.png`
- `images/20260405_1844_01kng3xsb2eg5vfxfkf14mexsm.mp4`

Para futuros materiales no públicos, usa `local/` o añade la ruta correspondiente a `.gitignore` antes de versionarla por error.

## Estructura publicada

```text
/
├── index.html
├── es.html
├── nosthoff.html
├── entries/
│   ├── Z-001_la-estacion-intermedia.md
│   └── Z-002_el-muzak.md
├── illustrations/
│   ├── Z-001.svg
│   └── Z-002.svg
├── diagrams/
│   └── forma-mercancia.png
├── images/
│   └── mercur.png
└── .nojekyll
```

## Agregar contenido público

1. Crear el archivo de entrada en `entries/`.
2. Crear su ilustración en `illustrations/` si la entrada la necesita.
3. Añadir el identificador al array `ENTRY_IDS` en `index.html`, o crear una tarjeta en `PAGE_CARDS` si será una página HTML independiente.
4. Confirmar que cualquier imagen o diagrama nuevo esté referenciado desde una página publicada.

Si un archivo no participa directamente en la web visible, no debe entrar al repositorio.

## Previsualización local

Requiere servidor HTTP:

```bash
python -m http.server 8000
```
