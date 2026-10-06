# CLAUDE.md — Proyecto AntonyMath

Contexto y preferencias para trabajar en este proyecto. Léeme antes de hacer cambios.

## Qué es este proyecto

Página web para alumnos de bachillerato, hecha por una maestra de matemáticas sin experiencia
en programación. Se publicará gratis con GitHub Pages.

- Nombre del sitio (el que aparece en encabezados, títulos de pestaña y pie de página):
  **AntonyMathClass**. No usar "AntonyMath" a secas en textos visibles del sitio.

## Sobre la maestra (usuaria)

- No sabe programar HTML/CSS/JavaScript. Explica los pasos técnicos en español sencillo,
  sin dar por hecho que conoce términos de programación o de Git/GitHub.
- Prefiere avanzar guiada paso a paso, con confirmación antes de cada paso importante.
- Antes de tocar Git/GitHub (crear cuenta, hacer push, cambiar configuración), pregunta y
  espera confirmación explícita — no asumir que un "sí" anterior aplica a pasos futuros.

## Estructura del sitio

- Una subcarpeta por materia: `matematicas-1` … `matematicas-5`, `optativa`, `interprepas`
  (Matemáticas 1-5, Optativa, Problemas Interprepas).
- Dentro de cada subcarpeta, un archivo `.html` por tema (uno por tema del temario), enlazado
  desde el `index.html` de esa materia (lista `ul.lista-temas`).
- Los temarios de cada curso los sube la maestra; no inventar temas ni contenido matemático
  sin que ella lo confirme o proporcione el material.

## Stack técnico

- HTML y CSS simples (sin frameworks ni build tools), para que sea fácil de mantener y
  editar sin conocimientos de programación.
- Si se necesita algo interactivo (ejercicios, calculadora, etc.), preferir JavaScript
  plano y comentado de forma mínima, evitando dependencias externas complejas.
- Publicación vía GitHub Pages desde este mismo repositorio.

## GitHub

- Cuenta: **AntonyMathClass**. Repositorio:
  https://github.com/AntonyMathClass/AntonyMathClass.github.io (público). Publicado con GitHub
  Pages en **https://antonymathclass.github.io** (se despliega solo con cada push a `main`,
  por el nombre especial del repo).
- **Carpeta del proyecto: `/Users/antonia/AntonyMath`** (ya NO está en el Escritorio). Hay un
  acceso directo (symlink) en `~/Desktop/AntonyMath` para que la maestra siga abriendo los
  archivos igual que antes, pero la carpeta real vive fuera del Escritorio — necesario porque
  macOS bloqueaba la escritura ahí (protección de privacidad de Archivos y Carpetas) y eso
  impedía crear el repositorio Git.
- Método de sincronización: **GitHub Desktop** (instalado en `/Applications/GitHub Desktop.app`
  tras moverlo ahí desde Descargas). Xcode Command Line Tools nunca se pudo instalar (falla
  persistente del servidor de Apple) y se descartó instalar Xcode completo.
  - Claude **no puede controlar GitHub Desktop** (es una app gráfica): la maestra da los clics
    de "Commit to main" y "Push origin"/"Fetch origin" ella misma. Claude solo puede guiarla
    paso a paso y, cuando aplica, editar los archivos directamente en disco antes de que ella
    los suba.
  - Antes de indicarle que haga push, resumir en una frase qué cambió.

## Flujo de trabajo con Claude

- Actualizar `BITACORA.md` con una entrada breve (fecha + qué se hizo/decidió/falta) cada
  vez que se complete un avance importante (nueva sección, cambio de estructura, decisión
  de la maestra, problema resuelto).
- Antes de publicar cambios (`git push`), resumir en una frase qué cambió.
- Preferir cambios pequeños y verificables (una página o sección a la vez) sobre construir
  todo el sitio de golpe, para que la maestra pueda revisar y dar retroalimentación.
- Si falta información de contenido (temario, ejercicios, texto de una materia), preguntar
  en vez de inventar contenido matemático.

## Preferencias de diseño

- **Paleta elegida: "Opción D — Púrpura Eléctrico y Fucsia"** (de 6 opciones mostradas en un
  Artifact de diseño). Variables en `style.css`: `--color-fondo:#faf5ff`,
  `--color-texto:#2d1b4e`, `--color-acento:#7b2ff7`, `--color-acento-2:#f72585`,
  `--color-acento-suave:#f0e5fe`, `--color-borde:#e5cffb`. El encabezado usa un degradado de
  acento a acento-2; el pie de página usa fondo acento sólido con texto blanco.
- **Tipografía:** Poppins (encabezados h1/h2/h3) y Quicksand (texto general), cargadas por
  Google Fonts. Cualquier página nueva debe incluir el mismo `<link>` de fuentes que las
  páginas existentes.
- **Iconito de la pestaña:** `favicon.png` y `favicon.svg` (π blanco sobre degradado morado-fucsia).
  Toda página nueva debe incluir, después del `<link>` de `style.css`, las mismas 3 líneas
  (`rel="icon"` png, `rel="icon"` svg y `rel="apple-touch-icon"`) que las páginas existentes.
- Estilo general: pastel/vibrante en morado y rosa, tarjetas blancas con bordes suaves,
  esquinas redondeadas, sin gradientes ni colores fuera de esta paleta salvo que la maestra
  lo pida.
