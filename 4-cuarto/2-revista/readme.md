# Aprende la cuadricula de CSS construyendo una revista

CSS Grid le brinda control sobre las filas y columnas del diseño de su página web.

En este curso, construirás un artículo de revista. Aprenderás como usar CSS Grid, incluidos los conceptos como filas de cuadrícula y columnas de cuadrícula.

## Paso 1

Comience con su plantilla HTML estándar. Agregue una declaración `DOCTYPE`, un elemento `html` que especifique que esta página está en inglés, un elemento `head` y un elemento `body`.

Agregue una etiqueta `<meta>` con el `charset` apropiado y una etiqueta `<meta>` para la capacidad de respuesta móvil dentro del elemento `head`.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

<body>

</body>

</html>
```

## Paso 2

Agregue un elemento `title` con el texto `Magazine`, un elemento `link` para la hoja de estilo de fuente `https://fonts.googleapis.com/css?family=Anton%7CBaskervville%7CRaleway&display=swap`, una hoja de estilos `link` para la hoja de estilos `https://use.fontawesome.com/releases/v5.8.2/css/all.css` FontAwesome, y un `link` para su hoja de estilos `./styles.css`.

La hoja de estilo de fuente cargará tres fuentes separadas: `Anton`, `Baskervville` y `Raleway`.

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Magazine</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Anton%7CBaskervville%7CRaleway&display=swap">
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.8.2/css/all.css">
  <link rel="stylesheet" href="styles.css">
</head>
```

## Paso 3

Dentro de tu `body`, crea un elemento `main`. Luego, en ese elemento, crea una sección `section` con una clase `class` establecida en `heading`.

```html
<main>
  <section class="heading"></section>
</main>
```

## Paso 4

Dentro de tu elemento `.heading`, crea un elemento `header` con la `class` establecida en `hero`.

En ese elemento, cree un elemento `img` con el `src` establecido en `https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png`, el `alt` establecido en `freecodecamp logo` y el `class` establecido en `hero-img`.

El atributo `loading` de un elemento `img` puede establecerse como `lazy` para indicar al navegador que no recupere el recurso de la imagen hasta que sea necesario (por ejemplo, cuando el usuario se desplace para ver la imagen). Como beneficio adicional, los elementos de carga lenta no se cargarán hasta que los elementos no lentos se carguen - esto significa que los usuarios con conexiones de Internet lentas pueden ver el contenido de su página sin tener que esperar a que las imágenes se carguen.

Dale a tu nuevo elemento `img` un atributo `loading` establecido en `lazy.`

```html
  <main>
    <section class="heading">
      <header class="hero">
        <img src="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png" alt="freecodecamp logo"
          class="hero-img" loading="lazy">
      </header>
    </section>
  </main>
```

## Paso 5

Después de tu elemento `img`, agrega un elemento `h1` con la `class` establecida en `hero-title` y el texto establecido en `OUR NEW CURRICULUM`, seguido de un elemento `p` con la `class` establecida en `hero-subtitle` y el texto establecido en `Our efforts to restructure our curriculum with a more project-based focus`.

```html
  <main>
    <section class="heading">
      <header class="hero">
        <img
            src="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
            alt="freecodecamp logo"
            loading="lazy"
            class="hero-img"
          />
        <h1 class="hero-title">OUR NEW CURRICULUM</h1>
        <p class="hero-subtitle">Our efforts to restructure our curriculum with a more project-based focus</p>
      </header>
    </section>
  </main>
```

## Paso 6

Su imagen actualmente ocupa mucho espacio. Para ver mejor en qué está trabajando, agregue un atributo `width` al elemento `img`, con un valor de `400`.

Lo eliminará más adelante cuando haya trabajado en el CSS.

```html
<main>
  <section class="heading">
    <header class="hero">
      <img
        src="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
        alt="freecodecamp logo"
        loading="lazy"
        class="hero-img" width="400"
      />
      <h1 class="hero-title">OUR NEW CURRICULUM</h1>
      <p class="hero-subtitle">
        Our efforts to restructure our curriculum with a more project-based
        focus
      </p>
    </header>
  </section>
</main>
```

## Paso 7

Después de tu elemento `header`, crea un `div` con la `class` establecida en `author`.

Dentro de ese `div`, crea un elemento `p` con la `class` configurada en `author-name` y dale el texto `By freeCodeCamp`. Envuelva la porción `freeCodeCamp` en un elemento `a` con `href` establecido en `https://freecodecamp.org`, y el `target` establecido en `_blank`.

Debajo de eso, agregue un segundo elemento `p` con la clase `publish-date` y el texto `March 7, 2019`.

```html
      <div class="author">
        <p class="author-name">By <a href="https://freecodecamp.org" target="_blank">freeCodeCamp</a></p>
        <p class="publish-date">March 7, 2019</p>
      </div>
    </section>
  </main>
```

## Paso 8

El encabezado HTTP `Referer` contiene información sobre la dirección o URL de una página desde la que un usuario podría estar visitando. Esta información se puede usar en análisis para rastrear cuántos usuarios de su página visitan freecodecamp.org, por ejemplo. Establecer el atributo `rel` en `noreferrer` omite esta información de la solicitud HTTP. Asigna al elemento `a` un atributo `rel` establecido en `noreferrer`.

```html
        <div class="author">
          <p class="author-name">
            By
            <a href="https://freecodecamp.org" target="_blank" rel="noreferrer"
              >freeCodeCamp</a
            >
          </p>
          <p class="publish-date">March 7, 2019</p>
        </div>
      </section>
    </main>
```

## Paso 9

Debajo de su elemento .author, crea un nuevo elemento div con la clase `social-icons`.

Agregue cinco elementos `a` dentro de ese nuevo `div` y asígneles los siguientes atributos `href`.

El primer elemento `a` debe tener un ``hre`f` establecido en `https://www.facebook.com/freecodecamp`.
El segundo elemento `a` debe tener un `href` establecido en `https://twitter.com/freecodecamp`.
El tercer elemento `a` debe tener un `href` establecido en `https://instagram.com/freecodecamp`.
El cuarto elemento `a` debe tener un `href` establecido en `https://www.linkedin.com/school/free-code-camp`.
El quinto elemento `a` debe tener un `href` establecido en `https://www.youtube.com/freecodecamp`

```html
<div class="social-icons">
  <a href="https://www.facebook.com/freecodecamp"></a>
  <a href="https://twitter.com/freecodecamp"></a>
  <a href="https://instagram.com/freecodecamp"></a>
  <a href="https://www.linkedin.com/school/free-code-camp"></a>
  <a href="https://www.youtube.com/freecodecamp"></a>
</div>
```

## Paso 10

Dentro de cada uno de sus nuevos elementos `a`, agregue un elemento `i` y asígneles las siguientes clases:

- Su primer elemento `i` debe tener la class `fab fa-facebook-f`
- Su segundo elemento `i` debe tener la clase `fab fa-twitter`
- Su tercer elemento `i` debe tener la clase `fab fa-instagram`
- Su cuarto elemento `i` debe tener la clase `fab fa-linkedin-in`
- Su quinto elemento `i`debería tener la clase `fab fa-youtube`

```html
<div class="social-icons">
  <a href="https://www.facebook.com/freecodecamp">
    <i class="fab fa-facebook-f"></i>
  </a>
  <a href="https://twitter.com/freecodecamp">
    <i class="fab fa-twitter"></i>
  </a>
  <a href="https://instagram.com/freecodecamp">
    <i class="fab fa-instagram"></i>
  </a>
  <a href="https://www.linkedin.com/school/free-code-camp">
    <i class="fab fa-linkedin-in"></i>
  </a>
  <a href="https://www.youtube.com/freecodecamp">
    <i class="fab fa-youtube"></i>
  </a>
</div>
```

## Paso 11

Debajo de tu elemento `.heading`, crea un nuevo elemento `section` con la `class` establecida en `text`. Dentro de eso, crea un elemento `p` con la `class` establecida en `first-paragraph` y el siguiente texto:

- Código de ejemplo

  ```text
  Soon the freeCodeCamp curriculum will be 100% project-driven learning. Instead of a series of coding challenges, you'll learn through building projects - step by step. Before we get into the details, let me emphasize: we are not changing the certifications. All 6 certifications will still have the same 5 required projects. We are only changing the optional coding challenges.
  ```

```html
<section class="text">
  <p class="first-paragraph">
    Soon the freeCodeCamp curriculum will be 100% project-driven learning. Instead of a series of coding challenges,
    you'll learn through building projects - step by step. Before we get into the details, let me emphasize: we are
    not changing the certifications. All 6 certifications will still have the same 5 required projects. We are only
    changing the optional coding challenges.
  </p>
</section>
```

## Paso 12

Cree otro elemento `p` debajo de su elemento `.first-paragraph` y asígnele el siguiente texto:

- Código de ejemplo

  ```text
  After years - years - of pondering these two problems and how to solve them, I slipped, hit my head on the sink, and when I came to I had a revelation! A vision! A picture in my head! A picture of this! This is what makes time travel possible: the flux capacitor!
  ```

```html
<section class="text">
  <p class="first-paragraph">
    Soon the freeCodeCamp curriculum will be 100% project-driven learning. Instead of a series of coding challenges,
    you'll learn through building projects - step by step. Before we get into the details, let me emphasize: we are
    not changing the certifications. All 6 certifications will still have the same 5 required projects. We are only
    changing the optional coding challenges.
  </p>
  <p>
    After years - years - of pondering these two problems and how to solve them, I slipped, hit my head on the sink,
    and when I came to I had a revelation! A vision! A picture in my head! A picture of this! This is what makes
    time travel possible: the flux capacitor!
  </p>
</section>
```

## Paso 13

Agregue un tercer elemento `p` al final de su elemento `.text` y asígnele el siguiente texto:

- Código de ejemplo

  ```text
  It wasn't as dramatic as Doc's revelation in Back to the Future. It just occurred to me while I was going for a run. The revelation: the entire curriculum should be a series of projects. Instead of individual coding challenges, we'll just have projects, each with their own seamless series of tests. Each test gives you just enough information to figure out how to get it to pass. (And you can view hints if that isn't enough.)
  ```

```html
<p>
  It wasn't as dramatic as Doc's revelation in Back to the Future. It just occurred to me while I was going for a
  run. The revelation: the entire curriculum should be a series of projects. Instead of individual coding
  challenges, we'll just have projects, each with their own seamless series of tests. Each test gives you just
  enough information to figure out how to get it to pass. (And you can view hints if that isn't enough.)
</p>
```

## Paso 14

Después de los tres elementos `p` dentro de su elemento `.text`, cree un elemento `blockquote`. Dentro de eso, agrega un elemento `hr`, un elemento `p` con la `class` establecida en `quote`, y un segundo elemento `hr`.

Asigne al elemento `.quote` el texto `The entire curriculum should be a series of projects`.

```html
<blockquote>
  <hr>
  <p class="quote">The entire curriculum should be a series of projects</p>
  <hr>
</blockquote>
```

## Paso 15

Debajo de su elemento `blockquote`, agregue otro elemento `p` con el siguiente texto:

- Código de ejemplo

  ```text
  No more walls of explanatory text. No more walls of tests. Just one test at a time, as you build up a working project. Over the course of passing thousands of tests, you build up projects and your own understanding of coding fundamentals. There is no transition between lessons and projects, because the lessons themselves are baked into projects. And there's plenty of repetition to help you retain everything because - hey - building projects in real life has plenty of repetition.
  ```

```html
<p>
  No more walls of explanatory text. No more walls of tests. Just one test at a time, as you build up a working
  project. Over the course of passing thousands of tests, you build up projects and your own understanding of
  coding fundamentals. There is no transition between lessons and projects, because the lessons themselves are
  baked into projects. And there's plenty of repetition to help you retain everything because - hey - building
  projects in real life has plenty of repetition.
</p>
```

## Paso 16

Cree un quinto elemento `p` al final de su elemento `.text` y asígnele el siguiente texto:

- Código de ejemplo

  ```text
  The main design challenge is taking what is currently paragraphs of explanation and instructions and packing them into a single test description text. Each project will involve dozens of tests like this. People will be coding the entire time, rather than switching back and forth from "reading mode" to "coding mode".
  ```

```html
<p>
  The main design challenge is taking what is currently paragraphs of explanation and instructions and packing
  them into a single test description text. Each project will involve dozens of tests like this. People will be
  coding the entire time, rather than switching back and forth from "reading mode" to "coding mode".
</p>
```

## Paso 17

Cree un elemento final `p` al final de su elemento `.text` y asígnele el siguiente texto:

- Código de ejemplo

  ```text
  Instead of a series of coding challenges, people will be in their code editor passing one test after another, quickly building up a project. People will get into a real flow state, similar to what they experience when they build the required projects at the end of each certification. They'll get that sense of forward progress right from the beginning. And freeCodeCamp will be a much smoother experience.
  ```

```html
<section class="text">
  <p class="first-paragraph">
    Soon the freeCodeCamp curriculum will be 100% project-driven learning. Instead of a series of coding challenges,
    you'll learn through building projects - step by step. Before we get into the details, let me emphasize: we are
    not changing the certifications. All 6 certifications will still have the same 5 required projects. We are only
    changing the optional coding challenges.
  </p>
  <p>
    After years - years - of pondering these two problems and how to solve them, I slipped, hit my head on the sink,
    and when I came to I had a revelation! A vision! A picture in my head! A picture of this! This is what makes
    time travel possible: the flux capacitor!
  </p>
  <p>
    It wasn't as dramatic as Doc's revelation in Back to the Future. It
    just occurred to me while I was going for a run. The revelation: the entire curriculum should be a series of
    projects. Instead of individual coding challenges, we'll just have projects, each with their own seamless series
    of tests. Each test gives you just enough information to figure out how to get it to pass. (And you can view
    hints if that isn't enough.)
  </p>
  <blockquote>
    <hr />
    <p class="quote">
      The entire curriculum should be a series of projects
    </p>
    <hr />
  </blockquote>
  <p>
    No more walls of explanatory text. No more walls of tests. Just one
    test at a time, as you build up a working project. Over the course of passing thousands of tests, you build up
    projects and your own understanding of coding fundamentals. There is no transition between lessons and projects,
    because the lessons themselves are baked into projects. And there's plenty of repetition to help you retain
    everything because - hey - building projects in real life has plenty of repetition.
  </p>
  <p>
    The main design challenge is taking what is currently paragraphs of explanation and instructions and packing
    them into a single test description text. Each project will involve dozens of tests like this. People will be
    coding the entire time, rather than switching back and forth from "reading mode" to "coding mode".
  </p>
  <p>
    Instead of a series of coding challenges, people will be in their code editor passing one test after another,
    quickly building up a project. People will get into a real flow state, similar to what they experience when they
    build the required projects at the end of each certification. They'll get that sense of forward progress right
    from the beginning. And freeCodeCamp will be a much smoother experience.
  </p>
</section>
```

## Paso 18

Debajo de su elemento `.text`, cree un nuevo elemento `section` y asígnele una `class` de `text text-with-images`. Dentro de ese div crea un elemento `article` con una `class` establecida en `brief-history`, y un elemento `aside` con la `class` establecida en `image-wrapper`.

```html
    <section class="text text-with-images">
      <article class="brief-history"></article>
      <aside class="image-wrapper"></aside>
    </section>
```

## Paso 19

Dentro de tu elemento `article`, crea un elemento `h3` con la `class` establecida en `list-title` y el texto `A Brief History`. Debajo de eso, crea un elemento `p` con el texto `Of the Curriculum`. Luego crea un elemento `ul` con la clase `lists`.

```html
  <article class="brief-history">
    <h3 class="list-title">A Brief History</h3>
    <p>Of the Curriculum</p>
    <ul class="lists"></ul>
  </article>
```

## Paso 20

Dentro de su elemento `ul`, cree seis elementos `li`. Agrega un elemento `h4` con una `class` establecida en `list-subtitle` y un elemento `p` a cada uno de tus elementos `li`.

Luego asigne a los elementos `h4` y `p` el siguiente contenido de texto, en orden, con cada `h4` usando lo que está en el lado izquierdo de los dos puntos, y cada `p` usando lo que está a la derecha:

- `V1 - 2014`: `We launched freeCodeCamp with a simple list of 15 resources, including Harvard's CS50 and Stanford's Database Class.`
- `V2 - 2015`: `We added interactive algorithm challenges.`
- `V3 - 2015`: `We added our own HTML+CSS challenges (before we'd been relying on General Assembly's Dash course for these).`
- `V4 - 2016`: `We expanded the curriculum to 3 certifications, including Front End, Back End, and Data Visualization. They each had 10 required projects, but only the Front End section had its own challenges. For the other certs, we were still using external resources like Node School.`
- `V5 - 2017`: `We added the back end and data visualization challenges.`
- `V6 - 2018`: `We launched 6 new certifications to replace our old ones. This was the biggest curriculum improvement to date.`

```html
<article class="brief-history">
  <h3 class="list-title">A Brief History</h3>
  <p>Of the Curriculum</p>
  <ul class="lists">
    <li>
      <h4 class="list-subtitle">V1 - 2014</h4>
      <p>
        We launched freeCodeCamp with a simple list of 15 resources, including Harvard's CS50 and Stanford's
        Database Class.
      </p>
    </li>
    <li>
      <h4 class="list-subtitle">V2 - 2015</h4>
      <p>
        We added interactive algorithm challenges.
      </p>
    </li>
    <li>
      <h4 class="list-subtitle">V3 - 2015</h4>
      <p>
        We added our own HTML+CSS challenges (before we'd been relying on General Assembly's Dash course for
        these).
      </p>
    </li>
    <li>
      <h4 class="list-subtitle">V4 - 2016</h4>
      <p>
        We expanded the curriculum to 3 certifications, including Front End, Back End, and Data Visualization.
        They each had 10 required projects, but only the Front End section had its own challenges. For the other
        certs, we were still using external resources like Node School.
      </p>
    </li>
    <li>
      <h4 class="list-subtitle">V5 - 2017</h4>
      <p>
        We added the back end and data visualization challenges.
      </p>
    </li>
    <li>
      <h4 class="list-subtitle">V6 - 2018</h4>
      <p>
        We launched 6 new certifications to replace our old ones. This was the biggest curriculum improvement to
        date.
      </p>
    </li>
  </ul>
</article>
```

## Paso 21

Dentro de su elemento `aside`, crear dos elementos `img` un elemento `blockquote`, y un tercer elemento `img`. Asigna al elemento `blockquote` una `class` establecida en `image-quote`.

```html
<aside class="image-wrapper">
  <img src="" alt="">
  <img src="" alt="">
  <blockquote class="image-quote"></blockquote>
  <img src="" alt="">
</aside>
```

## Paso 22

Dentro del elemento `.image-wrapper`, asigne a su primer elemento `img` un `src` de `https://cdn.freecodecamp.org/testable-projects-fcc/images/random-quote-machine.png`, una `alt` de `image of the quote machine project`, una `class` de `image-1`, un atributo `loading` establecido en `lazy`, un atributo `width` de `600` y un atributo `height` de `400`.

```html
<aside class="image-wrapper">
  <img src="https://cdn.freecodecamp.org/testable-projects-fcc/images/random-quote-machine.png"
  alt="image of the quote machine project" class="image-1" loading="lazy" width="600" height="400">
  <img />
  <blockquote class="image-quote"></blockquote>
  <img />
</aside>
```

## Paso 23

Dentro de su elemento `.image-wrapper`, asigne al segundo elemento `img` un `src` de `https://cdn.freecodecamp.org/testable-projects-fcc/images/calc.png`, un `alt` de `image of a calculator project`, un conjunto de atributos `loading` a `lazy`, una `class` establecida en `image-2`, un atributo `width` establecido en `400`, y un atributo `height` establecido en `400`.

```html
<aside class="image-wrapper">
  <img
    src="https://cdn.freecodecamp.org/testable-projects-fcc/images/random-quote-machine.png"
    alt="image of the quote machine project"
    loading="lazy"
    class="image-1"
    width="600"
    height="400"
  />
  <img src="https://cdn.freecodecamp.org/testable-projects-fcc/images/calc.png" alt="image of a calculator project"
  class="image-2" loading="lazy" width="400" height="400">
  <blockquote class="image-quote"></blockquote>
  <img />
</aside>
```

## Paso 24

Dentro de su elemento `.image-wrapper`, asigna a tu tercer elemento `img` un `src` de `https://cdn.freecodecamp.org/testable-projects-fcc/images/survey-form-background.jpeg`, un `alt` de `four people working on code`, un atributo `loading` de `lazy`, una `class` establecida en `image-3`, un atributo `width` establecido en `600` y un atributo `height` establecido en `400`.

```html
  <img src="https://cdn.freecodecamp.org/testable-projects-fcc/images/survey-form-background.jpeg"
  alt="four people working on code" class="image-3" loading="lazy" width="600" height="400">
```

## Paso 25

Dentro de su elemento `.image-quote`, anide un elemento `hr`, un elemento `p` y un segundo elemento `hr`. Asigne al elemento `p` una `class` establecida en `quote` y el texto `The millions of people who are learning to code through freeCodeCamp will have an even better resource to help them learn these fundamentals.`.

```html
<blockquote class="image-quote">
  <hr>
  <p class="quote">
    The millions of people who are learning to code through freeCodeCamp will have an even better resource to
    help them learn these fundamentals.
  </p>
  <hr>
</blockquote>
```

## Paso 26

Para iniciar tu CSS, normaliza las reglas CSS apuntando a todos los elementos con `*`, incluye los pseudo-selectores `::before` y `::after`.

A las propiedades `padding` y `margin` dales un valor de `0` y a `box-sizing` dale el valor `border-box`.

```css
*, 
::before, 
::after {
 padding: 0;
 margin: 0;
 box-sizing: border-box;
}
```

## Paso 27

Cree un selector `html` y asígnele una propiedad `font-size` establecida en `62.5%`. Esto establecerá el tamaño de fuente predeterminado para su página web en 10 px (el valor predeterminado del navegador es 16 px).

Esto te facilitará trabajar con unidades `rem` más adelante, ya que `2rem` serían 20 píxeles.

```css
html {
 font-size: 62.5%;
}
```

## Paso 28

Cree un selector `body`. Establezca la propiedad `font-family` en `Baskervville`, con una alternativa de `serif`. Establezca la propiedad `color` en `linen` y la propiedad `background-color` en `rgb(20, 30, 40)`.

```css
body {
 font-family: "Baskervville", serif;
 color: linen;
 background-color: rgb(20, 30, 40);
}
```

## Paso 29

Cree un selector `h1` y establezca la propiedad `font-family` en `Anton` con el respaldo de `sans-serif`.

```css
h1 {
  font-family: "Anton", sans-serif;
}
```

## Paso 30

Cree un selector `h2, h3, h4, h5, h6`. Dale una propiedad `font-family` establecida en `Raleway` con un respaldo de `sans-serif`.

```css
h2,
h3,
h4,
h5,
h6 {
 font-family: "Raleway", sans-serif;
}
```

## Paso 31

Crea un selector `a` y asígnale una propiedad `text-decoration` establecida en `none` y una propiedad `color` establecida en `linen`.

```css
a {
  text-decoration: none;
  color: linen;
}
```

## Paso 32

Ahora está listo para comenzar a armar el diseño de la cuadrícula. **CSS Grid** ofrece un diseño bidimensional basado en cuadrículas, lo que le permite centrar elementos horizontal y verticalmente mientras conserva el control para hacer cosas como elementos superpuestos.

Comience creando un selector `main` y asignándole una propiedad `display` establecida en `grid`.

```css
main{
  display: grid;
}
```

## Paso 33

Ahora puede diseñar el diseño de su cuadrícula. CSS Grid es similar a Flexbox en que tiene una propiedad especial para los elementos padre e hijo.

En este caso, su elemento principal es el elemento `main`. Configure el contenido para que tenga un diseño de tres columnas agregando una propiedad `grid-template-columns` con un valor de `1fr 94rem 1fr`. Esto creará tres columnas donde la columna del medio tiene un ancho de `94rem`, y la primera y la última columna son ambas 1 fracción del espacio restante en el contenedor de cuadrícula.

```css
main {
  display: grid;
  grid-template-columns: 1fr 94rem 1fr;
}
```

## Paso 34

Utiliza la función `minmax` para hacer tus columnas adaptables en cualquier dispositivo. La función `minmax` toma dos argumentos, siendo el primero el valor mínimo y el segundo el máximo. Estos valores pueden ser una longitud, un porcentaje, `fr` o incluso una palabra clave como `max-content`.

Envuelve cada uno de tus valores ya definidos de la propiedad `grid-template-columns` en una función `minmax`, usando cada valor como segundo argumento. El primer argumento debe ser `2rem`, `min-content` y `2rem` respectivamente.

```css
main {
  display: grid;
  grid-template-columns: minmax(2rem, 1fr) minmax(min-content, 94rem) minmax(2rem, 1fr);
}
```

## Paso 35

Para agregar espacio entre filas en el diseño de cuadrícula, puede usar la propiedad `row-gap`. Dale al selector `main` una propiedad `row-gap` de `3rem`.

```css
main {
  display: grid;
  grid-template-columns: minmax(2rem, 1fr) minmax(min-content, 94rem) minmax(2rem, 1fr);
  row-gap: 3rem;
}
```

## Paso 36

Su revista tendrá tres secciones principales. Ya configuró el diseño general en la regla `main`, pero puede ajustar la ubicación en las reglas secundarias.

Una opción es la propiedad `grid-column`, que es la abreviatura de `grid-column-start` y `grid-column-end`. La propiedad `grid-column` le dice al elemento de la cuadrícula en qué línea de cuadrícula debe comenzar y terminar.

Cree una regla `.heading` y establezca la propiedad `grid-column` en `2 / 3`. Esto le indicará al elemento `.heading` que comience en la línea de cuadrícula 2 y finalice en la línea de cuadrícula 3.

```css
.heading {
 grid-column: 2 / 3;
}
```

## Paso 37

Cree un selector `.text` y asígnele una propiedad `grid-column` establecida en `2 / 3`.

```css
.text {
  grid-column: 2 / 3;
}
```

## Paso 38

Para un control adicional sobre el diseño de su contenido, puede tener una cuadrícula CSS dentro de una cuadrícula CSS.

Establezca la propiedad `display` de su selector `.heading` en `grid`.

```css
.heading {
  grid-column: 2 / 3;
  display: grid;
}
```

## Paso 39

Ahora puede diseñar el contenido del elemento `.heading` con CSS Grid.

La función CSS `repeat()` se usa para repetir un valor, en lugar de escribirlo manualmente, y es útil para los diseños de cuadrícula. Por ejemplo, establecer la propiedad `grid-template-columns` en `repeat(20, 200px)` crearía 20 columnas cada una de `200px` de ancho.

Dale a tu elemento `.heading` una propiedad `grid-template-columns` establecida en `repeat(2, 1fr)` para crear dos columnas de igual ancho.

```csds
.heading {
  grid-column: 2 / 3;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
}
```

## Paso 40

Dale a tu selector `.heading` una propiedad `row-gap` establecida en `1.5rem`.

```css
.heading {
  grid-column: 2 / 3;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  row-gap: 1.5rem;
}
```

## Paso 41

Recuerda que la propiedad `grid-column` determina en qué columnas comienza y termina un elemento. Puede haber momentos en los que no esté seguro de cuántas columnas tendrá su cuadrícula, pero desea que un elemento se detenga en la última columna. Para hacer esto, puede usar `-1` para la columna final.

Cree un selector `.hero` y asígnele una propiedad `grid-column` establecida en `1 / -1`. Esto le indicará al elemento que abarque todo el ancho de la cuadrícula.

```css
.hero {
 grid-column: 1 / -1;
}
```

## Paso 42

Dale al selector `.hero` una propiedad `position` establecida en `relative`.

```css
.hero {
  grid-column: 1 / -1;
  position: relative;
}
```

## Paso 43

Debe eliminar el atributo temporal `width` antes de escribir el CSS para su `.hero-img`.

```html
<img
  src="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
  alt="freecodecamp logo"
  loading="lazy"
  class="hero-img"
/>
<h1 class="hero-title">OUR NEW CURRICULUM</h1>
<p class="hero-subtitle">
  Our efforts to restructure our curriculum with a more project-based
  focus
</p>
```

## Paso 44

Crea un selector `img` y asígnale una propiedad `width` establecida en `100%` y una propiedad `object-fit` establecida en `cover`.

La propiedad `object-fit` le dice al navegador cómo colocar el elemento dentro de su contenedor. En este caso, `cover` configurará la imagen para llenar el contenedor, recortándola según sea necesario para evitar cambiar la relación de aspecto.

```css
img {
 width: 100%;
 object-fit: cover;
}
```

## Paso 45

Cree un selector `.hero-title` y asígnele una propiedad `text-align` establecida en `center`, una propiedad `color` establecida en `orangered` y una propiedad `font-size` establecida en `8rem`.

```css
.hero-title {
 text-align: center;
 color: orangered;
 font-size: 8rem;
}
```

## Paso 46

El subtítulo también necesita ser diseñado. Cree un selector `.hero-subtitle` y asígnele una propiedad `font-size` establecida en `2.4rem`, un `color` propiedad establecida en `orangered`, y una propiedad `text-align` establecida en `center`.

```css
.hero-subtitle {
 font-size: 2.4rem;
 color: orangered;
 text-align: center;
}
```

## Paso 47

Cree un selector `.author` y asígnele una propiedad `font-size` establecida en `2rem` y una propiedad `font-family` establecido en `Raleway` con un respaldo de `sans-serif`.

```css
.author {
 font-size: 2rem;
 font-family: "Raleway", sans-serif;
}
```

## Paso 48

Cree un selector `.author-name a:hover` y asígnele una propiedad `background-color` establecida en `#306203`.

Esto creará un efecto de desplazamiento solo para el elemento `a` dentro de `.author-name`, mostrando el freeCodeCamp verde original en el fondo.

```css
.author-name a:hover {
 background-color: #306203;
}
```

## Paso 49

Cree un selector `.publish-date` y asígnele una propiedad `color` de `rgba(255, 255, 255, 0.5)`.

```css
.publish-date {
 color: rgba(255, 255, 255, 0.5);
}
```

## Paso 50

Cree un selector `.social-icons`. Dale una propiedad `display` establecida en `grid` y una propiedad `font-size` establecida en `3rem`.

```css
.social-icons {
 display: grid;
 font-size: 3rem;
}
```

## Paso 51

La configuración predeterminada para CSS Grid creará filas adicionales según sea necesario, a diferencia de Flexbox. Asigne al selector `.social-icons` una propiedad `grid-template-columns` establecida en `repeat(5, 1fr)` para organizar los íconos en una sola fila.

```css
.social-icons {
  display: grid;
  font-size: 3rem;
  grid-template-columns: repeat(5, 1fr);
}
```

## Paso 52

Si desea agregar más íconos sociales, pero mantenerlos en la misma fila, deberá actualizar `grid-template-columns` para crear columnas adicionales. Como alternativa, puede utilizar la propiedad `grid-auto-flow`.

Esta propiedad toma `row` o `column` como primer valor, con un segundo valor opcional de `dense`. `grid-auto-flow` utiliza un algoritmo de colocación automática para ajustar el diseño de la cuadrícula. Establecerlo en `column` le indicará al algoritmo que cree nuevas columnas para el contenido según sea necesario. El valor `dense` permite que el algoritmo retroceda y rellene los huecos en la cuadrícula con elementos más pequeños, lo que puede provocar que los elementos aparezcan desordenados.

Para su selector `.social-icons`, establezca la propiedad `grid-auto-flow` en `column`.

```css
.social-icons {
  display: grid;
  font-size: 3rem;
  grid-template-columns: repeat(5, 1fr);
  grid-auto-flow: column;
}
```

## Paso 53

Ahora, el algoritmo de colocación automática se activará cuando agregue un nuevo elemento de icono. Sin embargo, el algoritmo establece por defecto que el ancho de la nueva columna sea `auto`, que no coincidirá con sus columnas actuales.

Puede anular esto con la propiedad `grid-auto-columns`. Asigne al selector `.social-icons` una propiedad `grid-auto-columns` establecida en `1fr`.

```css
.social-icons {
  display: grid;
  font-size: 3rem;
  grid-template-columns: repeat(5, 1fr);
  grid-auto-flow: column;
  grid-auto-columns: 1fr;
}
```

## Paso 54

Al igual que Flexbox, con CSS Grid puedes alinear el contenido de los elementos de la cuadrícula con `align-items` y `justify-items`. `align-items` alineará los elementos secundarios a lo largo del eje de la columna, y `justify-items` alineará los elementos secundarios a lo largo del eje de la fila.

Asigne al selector `.social-icons` una propiedad `align-items` establecida en `center`.

```css
.social-icons {
  display: grid;
  font-size: 3rem;
  grid-template-columns: repeat(5, 1fr);
  grid-auto-flow: column;
  grid-auto-columns: 1fr;
  align-items: center;
}
```

## Paso 55

Asigne al selector `.text` una propiedad `font-size` establecida en `1.8rem` y una propiedad `letter-spacing` establecida en `0.6px`.

```css
.text {
  grid-column: 2 / 3;
  font-size: 1.8rem;
  letter-spacing: 0.6px;
}
```

## Paso 56

Su elemento `.text` no es una cuadrícula CSS, pero puede crear columnas dentro de un elemento sin usar Grid usando la propiedad `column-width`.

Dale a tu selector `.text` una propiedad `column-width` establecida en `25rem`.

```css
.text {
  grid-column: 2 / 3;
  font-size: 1.8rem;
  letter-spacing: 0.6px;
  column-width: 25rem;
}
```

## Paso 57

Las revistas a menudo usan texto justificado en su contenido impreso para estructurar su diseño y controlar el flujo de su contenido. Si bien esto funciona en forma impresa, el texto justificado en los sitios web puede ser un problema de accesibilidad, por ejemplo, presenta desafíos para las personas con dislexia.

Para hacer que su proyecto parezca una revista impresa, asigne al selector `.text` una propiedad `text-align` establecida en `justify`.

```css
.text {
  grid-column: 2 / 3;
  font-size: 1.8rem;
  letter-spacing: 0.6px;
  column-width: 25rem;
  text-align: justify;
}
```

## Paso 58

El pseudo-selector `::first-letter` le permite apuntar a la primera letra en el contenido de texto de un elemento.

Cree un selector `.first-paragraph::first-letter` y establezca la propiedad `font-size` en `6rem`. También asígnele una propiedad `color` establecida en `orangered` para que se destaque.

```css
.first-paragraph::first-letter {
  font-size: 6rem;
  color: orangered;
}
```

## Paso 59

El otro texto se ha desplazado fuera de lugar. Muévalo a su posición dándole al selector `.first-paragraph::first-letter` una propiedad `float` establecida en `left` y un `margin-right` establecida en `1rem`.

```css
.first-paragraph::first-letter {
  font-size: 6rem;
  color: orangered;
  float: left;
 margin-right: 1rem;
}
```

## Paso 60

Cree un selector `hr` y asígnele una propiedad `margin` establecida en `1.5rem 0`.

```CSS
hr{
 margin: 1.5rem 0;
}
```

## Paso 61

Para darle un color a `hr`, debe ajustar la propiedad `border`. Dale al selector `hr` una propiedad `border` establecida en `1px solid rgba(120, 120, 120, 0.6)`.

```css
hr {
  margin: 1.5rem 0;
  border: 1px solid rgba(120, 120, 120, 0.6);
}
```

## Paso 62

Crea un selector `.quote`. Asígnale una propiedad `color` establecida en `#00beef`, una propiedad `font-size` establecida en `2.4rem` y una Propiedad `text-align` establecida en `center`.

```css
.quote {
 color: #00beef;
 font-size: 2.4rem;
 text-align: center;
} 
```

## Paso 63

Para que el texto de la cita se destaque más, asigne al selector `.quote` una propiedad `font-family` establecida en `Raleway` con un respaldo de `sans-serif`.

```css
.quote {
  color: #00beef;
  font-size: 2.4rem;
  text-align: center;
 font-family: "Raleway", sans-serif;
}
```

## Paso 64

Una cita no es realmente una cita sin las comillas adecuadas. Puede agregarlos con pseudo-selectores de CSS.

Cree un selector `.quote::before` y establezca la propiedad `content` en " con un espacio a continuación.

Además, cree un selector `.quote::after` y establezca la propiedad `content` en " con un espacio antes.

```css
.quote::before {
 content: '" ';
}

.quote::after {
 content: ' "';
}
```

## Paso 65

Ahora es el momento de diseñar tu tercera `section`. Tenga en cuenta que tiene los valores `text` y `text-with-images` para el atributo `class`, lo que significa que ya hereda los estilos de su regla `.text`.

Cree un selector `.text-with-images` y establezca la propiedad `display` en `grid`.

```css
.text-with-images {
 display: grid;
}
```

## Paso 66

Debe tener una columna para el texto y una columna para las imágenes. Asigna al selector `.text-with-images` una propiedad `grid-template-columns` establecida en `1fr 2fr`. También establezca la propiedad `column-gap` en `3rem` para proporcionar más espacio entre las columnas.

```css
.text-with-images {
 display: grid;
 grid-template-columns: 1fr 2fr;
 column-gap: 3rem;
}
```

## Paso 67

Dale al selector `.text-with-images` una propiedad `margin-bottom` establecida en `3rem`.

```css
.text-with-images {
  display: grid;
  grid-template-columns: 1fr 2fr;
  column-gap: 3rem;
 margin-bottom: 3rem;
}
```

## Paso 68

Cree un selector `.lists` y establezca la propiedad `list-style-type` en `none`. Esto eliminará las viñetas en los elementos de la lista.

```css
.lists {
 list-style-type: none;
}
```

## Paso 69

Asigne al selector `.lists` una propiedad `margin-top` establecida en `2rem`.

```css
.lists {
  list-style-type: none;
 margin-top: 2rem;
}
```

## Paso 70

Cree una regla `.lists li` para apuntar a los elementos de la lista dentro de su elemento `.lists`. Dale una propiedad `margin-bottom` establecida en `1.5rem`.

```css
.lists li {
 margin-bottom: 1.5rem;
}
```

## Paso 71

Cree un selector `.list-title, .list-subtitle` y establezca la propiedad `color` en `#00beef`.

```css
.list-title,
.list-subtitle {
 color: #00beef;
}
```

## Paso 72

Es hora de diseñar la última sección de la revista: las imágenes.

Las imágenes se envuelven con un elemento `aside` utilizando la clase `image-wrapper`, así que crea un selector `.image-wrapper`. Establezca la propiedad `display` en `grid`.

```css
.image-wrapper {
 display: grid;
}
```

## Paso 73

Las imágenes deben estar dentro de un diseño de dos columnas y tres filas.

Asigne al selector `.image-wrapper` una propiedad `grid-template-columns` establecida en `2fr 1fr` y `grid-template-rows` propiedad establecida en `repeat(3, min-content)`. Esto le dará a nuestra cuadrícula filas que se ajustan en altura según el contenido, pero columnas que mantienen un ancho fijo según el contenedor.

```css
.image-wrapper {
 display: grid;
 grid-template-columns: 2fr 1fr;
 grid-template-rows: repeat(3, min-content);
}
```

## Paso 74

La propiedad `gap` es una forma abreviada de establecer el valor de `column-gap` y `row-gap` al mismo tiempo. Si se le da un valor, establece `column-gap` y `row-gap` en ese valor. Si se le dan dos valores, establece el `row-gap` en el primer valor y el `column-gap` en el segundo.

Dale al selector `.image-wrapper` una propiedad `gap` establecida en `2rem`.

```css
.image-wrapper {
 display: grid;
 grid-template-columns: 2fr 1fr;
 grid-template-rows: repeat(3, min-content);
 gap: 2rem;
}
```

## Paso 75

La propiedad `place-items` se puede usar para establecer los valores `align-items` y `justify-items` al mismo tiempo. La propiedad `place-items` toma uno o dos valores. Si se proporciona un valor, se utiliza para las propiedades `align-items` y `justify-items`. Si se proporcionan dos valores, el primer valor se usa para la propiedad `align-items` y el segundo valor se usa para la propiedad `justify-items`.

Asigne al selector `.image-wrapper` una propiedad `place-items` establecida en `center`.

```css
.image-wrapper {
 display: grid;
 grid-template-columns: 2fr 1fr;
 grid-template-rows: repeat(3, min-content);
 gap: 2rem;
 place-items: center;
}
```

## Paso 76

Cree una regla `.image-1, .image-3` y asígnele una propiedad `grid-column` establecida en `1 / -1`. Esto permitirá que la primera y la tercera imagen abarquen todo el ancho de la cuadrícula.

```css
.image-1, 
.image-3 {
 grid-column: 1 / -1;
}
```

## Paso 77

Ahora que el diseño de la revista está terminado, debe hacerlo adaptable.

Comience con una consulta `@media` para `only screen` con un `max-width` de `720px`. Dentro, crea un selector `.image-wrapper` y dale una propiedad `grid-template-columns` de `1fr`.

Esto colapsará las tres imágenes en una columna en pantallas más pequeñas.

```css
@media only screen and (max-width: 720px) {
 .image-wrapper {
  grid-template-columns: 1fr;
 }
}
```

## Paso 78

Crea otra consulta `@media` para `only screen` con un `max-width` de `600px`. Dentro, cree una regla `.text-with-images` y asígnele una propiedad `grid-template-columns` de `1fr`.

Esto colapsará el área de texto inferior en una sola columna en pantallas más pequeñas.

```css
@media only screen and (max-width: 600px) {
 .text-with-images {
  grid-template-columns: 1fr;
 }
}
```

## Paso 79

Cree una tercera consulta `@media` para `only screen` con un `max-width` de `550px`. Dentro de eso, crea un selector `.hero-title` con un `font-size` establecido en `6rem`, un selector `.hero-subtitle, .author, .quote, .list-title` con un `font-size` establecido en `1.8rem`, un selector `.social-icons` con un `font-size` establecido en `2rem`, y un selector `.text` con un `font-size` establecido en `1.6rem`.

```css
@media only screen and (max-width: 550px) {
 .hero-title {
  font-size: 6rem;
 }
 .hero-subtitle,
 .author,
 .quote,
 .list-title {
  font-size: 1.8rem;
 }
 .social-icons {
  font-size: 2rem;
 }
 .text {
  font-size: 1.6rem;
 }
}
```

## Paso 80

Cree una consulta final de `@media` para `only screen` con un `max-width` de `420px`. Dentro, cree un selector `.hero-title` con una propiedad `font-size` establecida en `4.5rem`.

**¡Felicidades! Su revista ahora está completa**.

```css
@media only screen and (max-width: 420px) {
 .hero-title {
  font-size: 4.5rem;
 }
}
```
