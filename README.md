# Ejercicios Prácticos — M2_L1 Desarrollo Web

> **Objetivo:** practicar los conceptos de HTML vistos en la presentación *M2_L1 Desarrollo Web*: la naturaleza de HTML como lenguaje de marcado, su estructura jerárquica (DOM), las etiquetas básicas del `<body>`, las etiquetas semánticas de HTML5 y el uso del inspector del navegador.
>
> **Reglas del juego:**
>
> - Cada ejercicio se entrega como un archivo `.html` (excepto el Ejercicio 5, que es de exploración).
> - Trabaja en VS Code con la extensión **Live Server** para ver tus cambios en tiempo real.
> - No hace falta usar CSS todavía: el foco es la **estructura** y la **semántica**.
> - Antes de pedir ayuda, abre las DevTools (F12) y revisa la pestaña **Elements** para entender qué está pasando.

---

## Ejercicio 1 — Tu primer documento HTML válido

**Contexto.** En la presentación vimos que HTML se organiza como un árbol genealógico: `<html>` es el abuelo, dentro vive `<head>` (la cédula de identidad invisible de la página) y `<body>` (todo lo que el usuario ve).

**Qué debes hacer:**

1. Crea un archivo llamado `ejercicio-01.html`.
2. Construye la estructura mínima de un documento HTML5 correcto. Tu archivo debe:
   - Declarar que es un documento HTML5.
   - Tener un elemento raíz `<html>` con un atributo `lang` que indique que la página está en español.
   - Contener una sección `<head>` con un título que aparezca en la pestaña del navegador: **"Mi primera página"**.
   - Contener una sección `<body>` con un único encabezado de nivel 1 que diga tu nombre completo.
3. Abre el archivo con Live Server y verifica que el título de la pestaña del navegador sea efectivamente "Mi primera página".

**Criterios de éxito:**

- El archivo abre sin errores.
- Al validar el documento en [validator.w3.org](https://validator.w3.org/) no aparecen errores.
- La pestaña del navegador muestra el título correcto.

---

## Ejercicio 2 — Encabezados, párrafos y listas

**Contexto.** En el slide 22 vimos varias etiquetas que viven dentro del `<body>`: encabezados (`<h1>` a `<h3>`), párrafos (`<p>`) y listas (`<ul>`, `<ol>`, `<li>`). El orden y la jerarquía importan: un `<h1>` no es lo mismo que un `<h2>`, y una lista ordenada no es lo mismo que una desordenada.

**Qué debes hacer:**

Crea un archivo `ejercicio-02.html` que contenga una **biografía corta de un personaje real o ficticio que admires**. La biografía debe respetar esta estructura informativa:

1. Un **título principal** con el nombre del personaje.
2. Un **subtítulo** que diga "Biografía".
3. Un **párrafo** de 3 o 4 oraciones contando quién es y por qué es relevante.
4. Un **subtítulo** que diga "Logros más importantes".
5. Una **lista ordenada** con al menos 4 logros (porque están rankeados de más a menos importante).
6. Un **subtítulo** que diga "Frases célebres".
7. Una **lista desordenada** con al menos 3 frases (porque el orden no importa).
8. Un **subtítulo más pequeño** que diga "Fuentes" y un párrafo final indicando de dónde sacaste la información.

**Criterios de éxito:**

- Hay exactamente **un** `<h1>` en toda la página.
- Los `<h2>` y `<h3>` se usan respetando su jerarquía (no saltes niveles arbitrariamente).
- Eliges correctamente entre `<ul>` y `<ol>` según el sentido del contenido.
- Inspecciona la página con DevTools y observa el árbol del DOM: debe verse como un árbol limpio y anidado.

---

## Ejercicio 3 — Hipertexto: enlaces e imágenes

**Contexto.** La "H" de HTML es de **HyperText**: la idea original de la web es conectar documentos entre sí mediante enlaces. En el slide 7 vimos que esta es la característica que hizo nacer la web tal como la conocemos. Las imágenes (`<img>`) y los enlaces (`<a>`) son los protagonistas.

**Qué debes hacer:**

Crea un archivo `ejercicio-03.html` titulado **"Mis tres lugares favoritos del mundo"**. La página debe:

1. Tener un encabezado principal con el título de la página.
2. Tener una breve introducción en un párrafo.
3. Por cada uno de los **tres lugares**, incluir:
   - Un subtítulo con el nombre del lugar.
   - Una **imagen** representativa (puede ser de internet o local). La imagen debe tener un texto alternativo que la describa para personas que no puedan verla.
   - Un párrafo breve explicando por qué te gusta.
   - Un **enlace** que abra el artículo de Wikipedia (u otra fuente) sobre ese lugar **en una pestaña nueva**.
4. Al final de la página, un enlace que diga **"Volver al inicio"** y que al hacer clic regrese al encabezado principal de la misma página (pista: investiga sobre el atributo `id` y los enlaces internos `#`).

**Criterios de éxito:**

- Las tres imágenes cargan correctamente.
- Todas las imágenes tienen texto alternativo descriptivo (no escribas "imagen" o "foto").
- Los enlaces externos abren en una pestaña nueva.
- El enlace "Volver al inicio" funciona como ancla interna.

---

## Ejercicio 4 — HTML semántico (sin `<div>` por todas partes)

**Contexto.** El slide 26 dejó claro que la gran revolución de HTML5 fue la llegada de las **etiquetas semánticas**: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>` y `<footer>`. Antes todo era `<div>` con clases; hoy escribir HTML semántico es una marca de seniority (slide 6).

**Qué debes hacer:**

Crea un archivo `ejercicio-04.html` que sea la **portada de un blog ficticio** sobre el tema que prefieras (videojuegos, cocina, viajes, etc.). La página debe respetar la siguiente estructura **sin usar ni un solo `<div>`**:

1. Una cabecera de la página con el nombre del blog y un eslogan corto.
2. Un menú de navegación con al menos 4 enlaces (los enlaces pueden ir a `#` por ahora).
3. Una zona principal de contenido que contenga **tres artículos**. Cada artículo debe tener:
   - Un título del artículo.
   - Una fecha de publicación.
   - Un párrafo de resumen.
   - Un enlace "Leer más".
4. Una sección lateral o secundaria con el título "Sobre el autor" y un par de oraciones.
5. Un pie de página con el copyright y el año actual.

**Criterios de éxito:**

- Cada bloque utiliza la etiqueta semántica adecuada (`<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`). Si no conoces alguna, investígala: están todas pensadas para describir el rol del contenido.
- Cuando inspecciones el DOM con DevTools, el árbol debe ser legible "leyendo solo las etiquetas", sin necesidad de mirar el contenido.
- **Prohibido** usar `<div>` o `<span>`. Si crees que necesitas uno, vuelve a leer este ejercicio.

---

## Ejercicio 5 — Disección con DevTools

**Contexto.** En la presentación dedicamos varios slides al **inspector del navegador**: las pestañas Elements, Console, Network, Sources, etc. Un buen desarrollador front-end aprende a leer páginas que no escribió.

**Qué debes hacer:**

No vas a escribir código en este ejercicio. Vas a investigar una página real. Elige **una de estas dos**:

- [https://es.wikipedia.org](https://es.wikipedia.org)
- [https://developer.mozilla.org/es/](https://developer.mozilla.org/es/)

Y responde, **dentro de un archivo `ejercicio-05.md`**, las siguientes preguntas. Debes incluir capturas de pantalla (puedes pegarlas o adjuntarlas) que demuestren cada hallazgo:

1. ¿Qué valor tiene el atributo `lang` del elemento `<html>` de esta página?
2. ¿Cuántos elementos `<h1>` tiene la página? ¿Es lo recomendable? Justifica.
3. Identifica al menos **tres etiquetas semánticas de HTML5** presentes en la página y describe brevemente qué contienen.
4. Encuentra una imagen (`<img>`) en la página y reporta:
   - Su atributo `src`.
   - Su atributo `alt` (si lo tiene).
5. Encuentra un enlace (`<a>`) que apunte a otro sitio externo y otro que apunte a una sección interna. Comparte el HTML de ambos.
6. Abre la pestaña **Network**, recarga la página y reporta:
   - Cuántos archivos se descargaron en total.
   - Cuánto pesó la página completa.
7. Abre la pestaña **Console** y ejecuta `document.querySelectorAll('a').length`. ¿Qué número devuelve? ¿Qué significa ese número?
8. **Pregunta final de reflexión:** ¿qué decisión de diseño semántico te llamó la atención de esta página? ¿Qué harías diferente?

**Criterios de éxito:**

- Las respuestas vienen acompañadas de capturas de pantalla del inspector.
- Las respuestas demuestran que entendiste la diferencia entre HTML escrito por una persona y el DOM final renderizado por el navegador.

---

## Entrega

Comprime los 5 archivos en una carpeta llamada `apellido-nombre-M2L1` y súbela al sistema de entrega del curso. Si no puedes terminar alguno, entrega lo que tengas con un comentario al inicio del archivo explicando hasta dónde llegaste y qué te bloqueó.

> **Pista general:** cuando dudes sobre una etiqueta o atributo, la fuente oficial siempre es [MDN Web Docs](https://developer.mozilla.org/es/docs/Web/HTML). Acostúmbrate a abrirla — un desarrollador profesional la consulta varias veces al día.

