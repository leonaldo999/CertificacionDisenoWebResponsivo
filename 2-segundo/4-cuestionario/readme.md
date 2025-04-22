# Aprende accesibilidad construyendo un cuestionario

Accesibilidad es hacer que tu página web sea sencilla de usar para todas las personas, incluyendo a aquellas con discapacidades.

En este curso, construirás una página web de cuestionarios. Aprenderás herramientas de accesibilidad como atajos de teclado, atributos ARIA y mejores prácticas de diseño.

## Paso 1

Te damos la bienvenida a la primera parte del Quiz de Accesibilidad. Como te estás convirtiendo en un desarrollador experimentado de HTML y CSS, te hemos proporcionado una plantilla básica inicial.

Comienza este paso proporcionando un atributo `lang` al elemento `html`. Esto ayudará a los lectores de pantalla a identificar el idioma de la página.

```html
<html lang="en">
  <head>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>

  </body>
</html>
```

## Paso 2

Puede que ya estés familiarizado con el elemento `meta`; es usado para especificar información sobre la página, como el título, descripción, palabras clave y el autor.

Dale a tu página un elemento `meta` con un valor `charset` apropiado.

El atributo `charset` especifica la codificación de los caracteres de la página, y actualmente `UTF-8` es la única codificación soportada por la mayoría de navegadores.

```html
  <head>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="styles.css" />
  </head>
```

## Paso 3

Continuando con los elementos `meta`, una definición de `viewport` le dice al navegador cómo renderizar la página. Incluyendo una mejor accesibilidad visual en móvil, y mejora SEO (optimización del motor de búsqueda).

Agrega una definición de `viewport` con un atributo `content` que detalla el `width` y `initial-scale` de la página.

```html
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css" />
  </head>
```

## Paso 4

Otro elemento `meta` importante para la accesibilidad y SEO es la definición de `description`. El valor del atributo `content` es usado por los motores de búsqueda para proporcionar una descripción de tu página.

Agrega un elemento `meta` con el atributo `name` establecido a `description`, y dale un útil atributo `content`.

```html
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="Cuestionario de Diseño Web Responsivo">
    <link rel="stylesheet" href="styles.css" />
  </head>
```

## Paso 5

Por último, en `head`, el elemento `title` es útil para los lectores de pantalla para entender el contenido de la página. Además, es una parte importante del SEO.

Dale a tu página un `title` que sea descriptivo y conciso.

```html
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="freeCodeCamp Accessibility Quiz practice project" />
    <title>freeCodeCamp Accessibility Quiz practice project</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
```

## Paso 6

La navegación es una parte fundamental de la accesibilidad, y los lectores de pantalla confían en que proporciones la estructura de tu página. Esto se consigue con elementos HTML semánticos.

Agrega un elemento `header` y un elemento `main` a tu página.

El elemento `header` se utilizará para introducir la página, así como para proporcionar un menú de navegación.

El elemento `main` contendrá el contenido principal de tu página.

```html
  <body>
    <header></header>
    <main></main>
  </body>
```

## Paso 7

En el `header`, proporciona contexto sobre la página anidando los elementos `img`, `h1` y `nav`.

La etiqueta `img` debe apuntar a `<https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg>`, tener un `id` `logo` y un texto `alt` `freeCodeCamp`.

El `h1` debe contener el texto `HTML/CSS Quiz`.

```html
  <header>
    <img src="https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg" alt="freeCodeCamp" id="logo">
    <h1>HTML/CSS Quiz</h1>
    <nav></nav>
  </header>
```

## Paso 8

Una propiedad útil de un *SVG* (gráfico vectorial escalable) es que contiene un atributo `path`, el cual permite escalar la imagen sin afectar la resolución de la imagen resultante.

Actualmente, `img` asume su tamaño predeterminado, que es demasiado grande. CSS tiene una función `max`, que devuelve el elemento más grande de un conjunto de valores separados por comas.

- *Por ejemplo*:

  ```css
  img {
  width: max(250px, 25vw);
  }
  ```

En el ejemplo anterior, el ancho de la imagen será 250px si el ancho de la vista es inferior a 1000 píxeles. Si el ancho de la vista es mayor que 1000 píxeles, el ancho de la imagen será 25vw. Esto ocurre porque 25vw es igual que 25% del ancho de la vista.

Escala la imagen usando su `id` como selector y estableciendo el valor de `width` al máximo de `10rem` o `18vw`.

```css
#logo {
  width: max(10rem, 18vw);
}
```

## Paso 9

Como se describe en la [Guía de Estilo de freeCodeCamp](https://design-style-guide.freecodecamp.org/), el logotipo debe mantener una proporción de aspecto de `35 / 4` y tener un espacio alrededor del texto.

En primer lugar, cambia el `background-color` a `#0a0a23` para que pueda ver el logo. Luego, usa la propiedad `aspect-ratio` para establecer la relación de aspecto a `35 / 4`. Finalmente, agrega alrededor un `padding` de `0.4rem`.

```css
#logo {
  width: max(10rem, 18vw);
  background-color: #0a0a23;
  aspect-ratio: 35 / 4;
  padding: 0.4rem;
}
```

## Paso 10

Haz que el `header` ocupe todo el ancho de tu contenedor principal, establece su `height` a `50px` y el `background-color` a `#1b1b32`. Luego, establece el `display` para usar *Flexbox*.

```css
header {
 width: 100%;
 height: 50px;
 background-color: #1b1b32;
 display: flex;
}
```

## Paso 11

Cambia el color de fuente del `h1` a `#f1be32`, y establece el tamaño de la fuente a `min(5vw, 1.2em)`.

```css
h1 {
  color: #f1be32;
  font-size: min(5vw, 1.2em);
}
```

## Paso 12

Para habilitar la navegación en la página, agrega una lista desordenada con los tres elementos de la lista siguientes:

- `INFO`
- `HTML`
- `CSS`

El texto de los elementos de la lista debe estar envuelto en etiquetas de anclaje.

```html
  <nav>
    <ul>
      <li><a href="#">INFO</a></li>
      <li><a href="#">HTML</a></li>
      <li><a href="#">CSS</a></li>
    </ul>
  </nav>
```

## Paso 13

El selector del combinador hijo `>` se utiliza entre selectores para apuntar solo a elementos que coincidan con el segundo selector y sean hijos directos del primer selector.

Esto puede ser útil si tienes elementos anidados profundamente y quieres controlar el alcance de tu estilo.

Usa el selector `>` para seleccionar los elementos desordenados dentro de los elementos `nav`, y usa Flexbox para espaciar de manera uniforme a los hijos.

```css
nav > ul {
  display: flex;
  justify-content: space-evenly;
}
```

## Paso 14

Como este es un cuestionario, necesitaras un formulario para que los usuarios envíen sus respuestas. Puedes separar semánticamente el contenido dentro del formulario usando elementos `section`.

Dentro del elemento `main`, crea un formulario con tres elementos `section` anidados. Luego, haga que el formulario se envíe a `<https://freecodecamp.org/practice-project/accessibility-quiz>`, usando el método correcto.

```html
  <main>
    <form action="https://freecodecamp.org/practice-project/accessibility-quiz" method="post">
      <section></section>
      <section></section>
      <section></section>
    </form>
  </main>
```

## Paso 15

Para aumentar la accesibilidad de la página, el atributo `role` puede ser usado para indicar el propósito detrás de un elemento en la página para las tecnologías de asistencia. El atributo `role` es una parte de la *Iniciativa de Accesibilidad Web* (WAI, por sus siglas en inglés), y acepta valores predefinidos.

Dale a cada elemento `section` el rol `region`.

```html
    <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
      <section role="region"></section>
      <section role="region"></section>
      <section role="region"></section>
    </form>
```

## Paso 16

Cada rol `region` requiere una etiqueta que ayuda a los usuarios de lectores de pantalla a entender el propósito de la región. Un método para agregar una etiqueta es agregar un elemento de encabezado dentro de la región y luego referenciarlo con el atributo `aria-labelledby`.

Agrega los siguientes atributos `aria-labelledby` a los elementos `section`:

- `student-info`
- `html-questions`
- `css-questions`

Luego, dentro de cada elemento `section`, anida un elemento h2 con un `id` que coincida con su atributo `aria-labelledb`y correspondiente. Da a cada `h2` un contenido de texto adecuado.

```html
    <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
      <section role="region" aria-labelledby="student-info">
        <h2 id="student-info">Student Info</h2>
      </section>
      <section role="region" aria-labelledby="html-questions">
        <h2 id="html-questions">HTML Questions</h2>
      </section>
      <section role="region" aria-labelledby="css-questions">
        <h2 id="css-questions">CSS Questions</h2>
      </section>
    </form>
```

## Paso 17

El tipo de letra juega un rol importante en la accesibilidad de una página. Algunas fuentes son más fáciles de leer que otras, y esto es especialmente cierto en pantallas de resolución baja.

Cambia la fuente para ambos elementos `h1` y `h2` a `Verdana`, y usa otra fuente web segura de la familia sans-serif como un respaldo.

Además, agrega un `border-bottom` de `4px solid #dfdfe2` a los elementos `h2` para distinguir las secciones.

```css
h1,
h2 {
 font-family: Verdana, sans-serif;
}

h2 {
 border-bottom: 4px solid #dfdfe2;
}
```

## Paso 18

Para poder navegar dentro de la página, dale a cada elemento ancla un `href` correspondiente al `id` de los elementos `h2`.

```html
  <ul>
    <li><a href="#student-info">INFO</a></li>
    <li><a href="#html-questions">HTML</a></li>
    <li><a href="#css-questions">CSS</a></li>
  </ul>
```

## Paso 19

Rellenando el contenido del cuestionario, debajo de `#student-info`, agrega tres elementos `div` con un `class` de `info`.

Luego, dentro de cada `div` anida un elmento `label` y un elemento `input`.

```html
  <section role="region" aria-labelledby="student-info">
    <h2 id="student-info">Student Info</h2>
    <div class="info">
      <label></label>
      <input>
    </div>
    <div class="info">
      <label></label>
      <input>
    </div>
    <div class="info">
      <label></label>
      <input>
    </div>
  </section>
```

## Paso 20

Es importante vincular cada `input` con su elemento `label` correspondiente. Esto proporciona a los usuarios de tecnologías de asistencia una referencia visual del input.

Esto se hace dando al `label` un atributo `for`, que contiene el `id` del `input`.

Esta sección tomará el nombre del estudiante, correo electrónico y la fecha de nacimiento. Da a los elementos `label` un atributo `for` apropiado, así como contenido de texto. Luego, vincula los elemento `input` con sus elementos `label` correspondientes.

```html
  <section role="region" aria-labelledby="student-info">
    <h2 id="student-info">Student Info</h2>
    <div class="info">
      <label for="student-name">Name:</label>
      <input id="student-name" />
    </div>
    <div class="info">
      <label for="student-email">Email:</label>
      <input id="student-email" />
    </div>
    <div class="info">
      <label for="birth-date">Date of Birth:</label>
      <input id="birth-date" />
    </div>
  </section>
```

## Paso 21

Teniendo en cuenta las mejores prácticas para las entradas de formularios, da a cada `input` un atributo `type` y `name` apropiados. Luego, da al primer `input` un atributo `placeholder`.

```html
  <div class="info">
    <label for="student-name">Name:</label>
    <input id="student-name" type="text" name="name" placeholder="e.g. Quincy Larson"/>
  </div>

  <div class="info">
    <label for="student-email">Email:</label>
    <input id="student-email" type="email" name="email" />
  </div>

  <div class="info">
    <label for="birth-date">Date of Birth:</label>
    <input id="birth-date" type="date" name="birth-date" />
  </div>
```

## Paso 22

A pesar de que agregaste un `placeholder` al primer elemento `input` en la lección anterior, actualmente no es la mejor práctica para la accesibilidad; muy a menudo, los usuarios confunden el texto del marcador de posición con un valor de entrada real - creen que ya hay un valor en la entrada.

Elimina el texto del marcador de posición del primer elemento `input`, confiando en que el `label` es la mejor práctica.

```html
  <div class="info">
    <label for="student-name">Name:</label>
    <input type="text" name="student-name" id="student-name" placeholder="" />
  </div>
```

## Paso 23

Dentro del segundo elemento `section`, añade dos elementos `div` con una clase `question-block`.

Después, dentro de cada elemento `div`.`question-block`, añade un elemento `h3` con texto de números incrementales, empezando por `1`, y un elemento `fieldset` con una clase de `question`.

```html
  <section role="region" aria-labelledby="html-questions">
    <div class="question-block">
      <h3>1</h3>
      <fieldset class="question"></fieldset>
    </div>
    <div class="question-block">
      <h3>2</h3>
      <fieldset class="question"></fieldset>
    </div>
  </section>
```

## Paso 24

Los números de las preguntas no son suficientemente descriptivos. Esto es especialmente cierto para los usuarios con deficiencias visuales. Una forma de evitar este problema, sin tener que añadir texto visible al elemento, es añadir texto que sólo pueda leer un lector de pantalla.

Añade un elemento `span` con la `class` `sr-only` a cada uno de los elementos `h3`.

```html
     <h3><span class="sr-only"></span>1</h3>
    <fieldset class="question"></fieldset>
  </div>
  <div class="question-block">
    <h3><span class="sr-only"></span>2</h3>
```

## Paso 25

Dentro del primer elemento `span`, agrega el texto `Question`.

En el segundo elemento `span`, agrega el texto `Question`.

```html
    <h3><span class="sr-only">Question</span>1</h3>
    <fieldset class="question"></fieldset>
  </div>
  <div class="question-block">
    <h3><span class="sr-only">Question</span>2</h3>
```

## Paso 26

El texto `.sr-only` sigue siendo visible. Es habitual ocultar visualmente el texto para que sólo lo lean los lectores de pantalla.

Este patrón consiste en establecer las siguientes propiedades CSS:

- **EJEMPLO**

  ```css
    position: absolute;
    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    white-space: nowrap;
    border: 0;
  ```

Utiliza lo anterior para definir la regla CSS `.sr-only`.

```css
.sr-only {
 position: absolute;
 width: 1px;
 height: 1px;
 padding: 0;
 margin: -1px;
 overflow: hidden;
 clip: rect(0, 0, 0, 0);
 white-space: nowrap;
 border: 0;
}
```

## Paso 27

Cada `fieldset` contendrá una pregunta true/false.

Dentro de cada `fieldset`, anida un elemento `legend` y un elemento `ul` con dos opciones.

```html
  <section role="region" aria-labelledby="html-questions">
    <h2 id="html-questions">HTML</h2>
    <div class="question-block">
      <h3><span class="sr-only"></span>1</h3>
      <fieldset class="question">
        <legend></legend>
      <ul>
        <li></li>
        <li></li>
      </ul>
      </fieldset>
    </div>
    <div class="question-block">
      <h3><span class="sr-only"></span>2</h3>
      <fieldset class="question">
        <legend></legend>
      <ul>
        <li></li>
        <li></li>
      </ul>
      </fieldset>
    </div>
  </section>
```

## Paso 28

Dale a cada `fieldset` un atributo `name` adecuado. Luego, dale a ambas listas desordenadas un `class` de `answers-list`.

Por último, usa el `legend` para titular el contenido del `fieldset`, colocando una pregunta de true/false como contenido de texto.

```html
  <section role="region" aria-labelledby="html-questions">
    <h2 id="html-questions">HTML</h2>
    <div class="question-block">
      <h3><span class="sr-only">Question</span>1</h3>
      <fieldset class="question" name="question">
        <legend>
          The legend element represents a caption for the content of its
          parent fieldset element
        </legend>
        <ul class="answers-list">
          <li></li>
          <li></li>
        </ul>
      </fieldset>
    </div>
    <div class="question-block">
      <h3><span class="sr-only">Question</span>2</h3>
      <fieldset class="question" name="question">
        <legend>
          A label element nesting an input element is required to have a
          for attribute with the same value as the input's id
        </legend>
        <ul class="answers-list">
          <li></li>
          <li></li>
        </ul>
      </fieldset>
    </div>
  </section>
```

## Paso 29

Para proporcionar funcionalidad a las preguntas de true/false, necesitamos un conjunto de entradas que no permitan ser seleccionadas al mimo tiempo.

Dentro de cada elemento de lista, anida un elemento label, y dentro de cada elemento `label`, anida un elemento `input` con un `type` apropiado.

```html
      <ul class="answers-list">
        <li>
          <label for="">
            <input type="radio" name="" id="">
          </label>
        </li>
        <li>
          <label for="">
            <input type="radio" name="" id="">
          </label>
        </li>
      </ul>
    </fieldset>
  </div>
  <div class="question-block">
    <h3><span class="sr-only">Question</span>2</h3>
    <fieldset class="question" name="html-question-two">
      <legend>
        A label element nesting an input element is required to have a
        for attribute with the same value as the input's id
      </legend>
      <ul class="answers-list">
        <li>
          <label for="">
            <input type="radio" name="" id="">
          </label>
        </li>
        <li>
          <label for="">
            <input type="radio" name="" id="">
          </label>
        </li>
      </ul>
```

## Paso 30

Agrega un `id` a todos tus radios `input`s así puedes linkear tus labels a ellos. Da a prime un `id` de `q1-a1`. Da al resto de ellos `id` de `q1-a2`, `q2-a1`, y `q2-a2`, respectivamente.

```html
      <ul class="answers-list">
        <li>
          <label>
            <input type="radio" id="q1-a1"/>
          </label>
        </li>
        <li>
          <label>
            <input type="radio" id="q1-a2"/>
          </label>
        </li>
      </ul>
    </fieldset>
  </div>
  <div class="question-block">
    <h3><span class="sr-only">Question</span>2</h3>
    <fieldset class="question" name="html-question-two">
      <legend>
        A label element nesting an input element is required to have a
        for attribute with the same value as the input's id
      </legend>
      <ul class="answers-list">
        <li>
          <label>
            <input type="radio" id="q2-a1"/>
          </label>
        </li>
        <li>
          <label>
            <input type="radio" id="q2-a2"/>
          </label>
        </li>
      </ul>
```

## Paso 31

Aunque no es necesario para los elementos `label` con una `input` anidada, sigue siendo una buena práctica vincular explícitamente una `label` con su correspondiente elemento `input`.

Ahora, agregue un atributo `for` a cada una de sus cuatro `label` que vincule la `label` a su `input` de radio correspondiente.

```html
      <ul class="answers-list">
        <li>
          <label for="q1-a1">
            <input type="radio" name="question1" id="q1-a1">
          </label>
        </li>
        <li>
          <label for="q1-a2">
            <input type="radio" name="question1" id="q1-a2">
          </label>
        </li>
      </ul>
    </fieldset>
  </div>
  <div class="question-block">
    <h3><span class="sr-only">Question</span>2</h3>
    <fieldset class="question" name="question">
      <legend>
        A label element nesting an input element is required to have a
        for attribute with the same value as the input's id
      </legend>
      <ul class="answers-list">
        <li>
          <label for="q2-a1">
            <input type="radio" name="" id="q2-a1">
          </label>
        </li>
        <li>
          <label for="q2-a2">
            <input type="radio" name="" id="q2-a2">
          </label>
        </li>
      </ul>
```

## Paso 32

Provee a los elementos `label` texto de tal manera que el `input` este antes del texto. A continuación, dale a los elementos `input` un `value` que coincida con el texto.

El texto debe ser `True` o `False`.

```html
      <ul class="answers-list">
        <li>
          <label for="q1-a1">
              <input type="radio" id="q1-a1" value="true"/>True
            </label>
        </li>
        <li>
          <label for="q1-a2">
              <input type="radio" id="q1-a2" value="false"/>False
            </label>
        </li>
      </ul>
    </fieldset>
  </div>
  <div class="question-block">
    <h3><span class="sr-only">Question</span>2</h3>
    <fieldset class="question" name="html-question-two">
      <legend>
        A label element nesting an input element is required to have a
        for attribute with the same value as the input's id
      </legend>
      <ul class="answers-list">
        <li>
          <label for="q2-a1">
              <input type="radio" id="q2-a1" value="true"/>True
            </label>
        </li>
        <li>
          <label for="q2-a2">
              <input type="radio" id="q2-a2" value="false"/>False
            </label>
        </li>
      </ul>
```

## Paso 33

Si hace clic en las entradas de radio, notara que ambas entradas dentro del mismo grupo de campos true/false pueden seleccionarse al mismo tiempo.

Agrupe las entradas relevantes de tal forma que solo se pueda seleccionar una entrada de un par a la vez.

```html
        <ul class="answers-list">
          <li>
            <label for="q1-a1">
              <input type="radio" id="q1-a1" value="true" name="question1"/>
              True
            </label>
          </li>
          <li>
            <label for="q1-a2">
              <input type="radio" id="q1-a2" value="false" name="question1"/>
              False
            </label>
          </li>
        </ul>
      </fieldset>
    </div>
    <div class="question-block">
      <h3><span class="sr-only">Question</span>2</h3>
      <fieldset class="question" name="html-question-two">
        <legend>
          A label element nesting an input element is required to have a
          for attribute with the same value as the input's id
        </legend>
        <ul class="answers-list">
          <li>
            <label for="q2-a1">
              <input type="radio" id="q2-a1" value="true" name="question2"/>
              True
            </label>
          </li>
          <li>
            <label for="q2-a2">
              <input type="radio" id="q2-a2" value="false" name="question2"/>
              False
            </label>
          </li>
        </ul>
```

## Paso 34

Para prevenir la repetición innecesaria, apunta al pseudoelemento `before` del elemento `h3`, y dale una propiedad `content` de `"Question #"`.

```css
h3::before {
 content: "Question #";
}
```

## Paso 35

La sección final de este cuestionario contendrá un desplegable y un cuadro de texto.

Empieza anidando un `div` con un `class` de `formrow`, y anida cuatro elementos `div` dentro, alternando sus atributos `class` con `question-block` y `answer`.

```html
  <section role="region" aria-labelledby="css-questions">
    <h2 id="css-questions">CSS</h2>
    <div class="formrow">
      <div class="question-block"></div>
      <div class="answer"></div>
      <div class="question-block"></div>
      <div class="answer"></div>
    </div>
  </section>
```

## Paso 36

Dentro de los elementos `div.question-block`, anida un elemento `label` y agrega una pregunta relacionada con `CSS` al texto en el elemento `label`.

```html
  <div class="formrow">
    <div class="question-block">`
      <label for="">
        Can the CSS margin property accept negative values?
      </label>
    </div>
    <div class="answer"></div>
    <div class="question-block">`
      <label for="">
        Do you have any questions:
      </label>
    </div>
    <div class="answer"></div>
  </div>
```

## Paso 37

Dentro del primer elemento `div.answer`, anida un elemento `select` requerido con tres elementos `option`.

Dale al elemento `option` un `value` de `""` y el texto `Select an option`. Dale al segundo elemento `option` un `value` de `yes` y el texto `Yes`. Dale al tercer elemento `option` un elemento `value` de `no` y el texto `No`.

```html
    <div class="answer">
      <select required>
        <option value="">Select an option</option>
        <option value="yes">Yes</option>
        <option value="no">No</option>
      </select>
    </div>
```

## Paso 38

Vincula el primer elemento `label` al elemento `select` y asigna un atributo `name` al elemento `select`.

```html
    <div class="question-block">
      <label for="selector">Can the CSS margin property accept negative values?</label>
    </div>
    <div class="answer">
      <select name="selector" id="selector" required>
        <option value="">Select an option</option>
        <option value="yes">Yes</option>
        <option value="no">No</option>
      </select>
    </div>
```

## Paso 39

Anida un elemento `textarea` dentro del segundo elemento `div.answer`, y establece el número de filas y columnas que tiene.

```html
    <div class="answer">
      <textarea rows="5" cols="24"></textarea>
    </div>
```

## Paso 40

Al igual que con los demás elementos `input` y `label`, vincula el elemento `textarea` a su elemento `label` correspondiente y asígnale un atributo `name`.

```html
    <div class="question-block">`
      <label for="css-textarea">
        Do you have any questions:
      </label>
    </div>
    <div class="answer">
      <textarea name="css-textarea" id="css-textarea" rows="5" cols="24"></textarea>
    </div>
```

## Paso 41

No te olvides de dar al `form` un botón de tipo submit con el texto `Send`.

```html
  <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
    <section role="region" aria-labelledby="student-info">
      <h2 id="student-info">Student Info</h2>
      <div class="info">
        <label for="student-name">Name:</label>
        <input type="text" name="student-name" id="student-name" />
      </div>
      <div class="info">
        <label for="student-email">Email:</label>
        <input type="email" name="student-email" id="student-email" />
      </div>
      <div class="info">
        <label for="birth-date">Date of Birth:</label>
        <input type="date" name="birth-date" id="birth-date" />
      </div>
    </section>
    <section role="region" aria-labelledby="html-questions">
      <h2 id="html-questions">HTML</h2>
      <div class="question-block">
        <h3><span class="sr-only">Question</span>1</h3>
        <fieldset class="question" name="html-question-one">
          <legend>
            The legend element represents a caption for the content of its
            parent fieldset element
          </legend>
          <ul class="answers-list">
            <li>
              <label for="q1-a1">
                <input type="radio" id="q1-a1" name="q1" value="true" />
                True
              </label>
            </li>
            <li>
              <label for="q1-a2">
                <input type="radio" id="q1-a2" name="q1" value="false" />
                False
              </label>
            </li>
          </ul>
        </fieldset>
      </div>
      <div class="question-block">
        <h3><span class="sr-only">Question</span>2</h3>
        <fieldset class="question" name="html-question-two">
          <legend>
            A label element nesting an input element is required to have a
            for attribute with the same value as the input's id
          </legend>
          <ul class="answers-list">
            <li>
              <label for="q2-a1">
                <input type="radio" id="q2-a1" name="q2" value="true" />
                True
              </label>
            </li>
            <li>
              <label for="q2-a2">
                <input type="radio" id="q2-a2" name="q2" value="false" />
                False
              </label>
            </li>
          </ul>
        </fieldset>
      </div>
    </section>
    <section role="region" aria-labelledby="css-questions">
      <h2 id="css-questions">CSS</h2>
      <div class="formrow">
        <div class="question-block">
          <label for="selector">Can the CSS margin property accept negative values?</label>
        </div>
        <div class="answer">
          <select name="selector" id="selector" required>
            <option value="">Select an option</option>
            <option value="yes">Yes</option>
            <option value="no">No</option>
          </select>
        </div>
        <div class="question-block">
          <label for="css-textarea">Do you have any questions:</label>
        </div>
        <div class="answer">
          <textarea id="css-textarea" name="css-questions" rows="5" cols="24"></textarea>
        </div>
      </div>
    </section>
    <button type="submit">Send</button>
  </form>
```

## Paso 42

Los dos últimos elementos HTML semánticos para este proyecto son `footer` y `address`. El elemento `footer` es un contenedor para una colección de contenidos relacionados de la página, y el elemento `address` es un contenedor para la información de contacto del autor de página.

Después del elemento `main`, agrega un elemento `footer`, y anida un elemento `address` dentro de él.

```html
  <footer>
    <address></address>
  </footer>
```

## Paso 43

Dentro del elemento `address`, agrega lo siguiente:

- **Código de ejemplo**

  ```html
  freeCodeCamp<br />
  San Francisco<br />
  California<br />
  USA
  ```

Las etiquetas `br` permitirán que cada parte de la dirección esté en su propia línea y son útiles para presentar correctamente los elementos `address`.

```html
  <footer>
    <address>
      freeCodeCamp<br />
      San Francisco<br />
      California<br />
      USA
    </address>
  </footer>
```

## Paso 44

El elemento `address` no tiene por qué contener una ubicación geográfica física. Puede usarse para proporcionar un enlace hacia el tema.

Envuelve un enlace alrededor del texto `freeCodeCamp`, y establece su ubicación hacia `https://freecodecamp.org`.

```html
  <footer>
    <address>
      <a href="https://freecodecamp.org">freeCodeCamp</a><br />
      San Francisco<br />
      California<br />
      USA
    </address>
  </footer>
```

## Paso 45

Volvemos a estilizar la página. Selecciona los elementos de lista dentro de la barra de navegación, y dales los siguientes estilos:

- **Código de ejemplo**

  ```css
  color: #dfdfe2;
  margin: 0 0.2rem;
  padding: 0.2rem;
  display: block;
  ```

```css
nav > ul > li {
 color: #dfdfe2;
 margin: 0 0.2rem;
 padding: 0.2rem;
 display: block;
}
```

## Paso 46

En el tema de la accesibilidad visual, el contraste entre elementos es un factor clave. Por ejemplo, el contraste entre el texto y el fondo de un encabezado debe ser de al menos 4.5:1.

Cambia el color de la fuente de todos los elementos de anclaje dentro de los elementos de lista, a algo con una relación de contraste de al menos 7:1.

```css
li > a {
  color: inherit;
}
```

## Paso 47

Para hacer que los botones de navegación se parezcan más a los botones típicos, elimine el subrayado de las etiquetas de anclaje.

Luego, cree un selector que apunte a los elementos de lista de navegación para que cuando el cursor pase sobre ellos, el color de fondo y el color del texto son cambiados, y el cursor se convierte en un puntero.

```css
nav > ul > li:hover {
  background-color: #dfdfe2;
 color: #1b1b32;
 cursor: pointer;
}

li > a {
 color: inherit;
 text-decoration: none;
}
```

## Paso 48

Ordena el `header`, usando Flexbox para colocar espacio entre los hijos y centrarlos verticalmente.

```css
header {
  width: 100%;
  height: 50px;
  background-color: #1b1b32;
  display: flex;
 justify-content: space-between;
 align-items: center;
 top: 0;
}
```

## Paso 49

Cuando el ancho de la pantalla es pequeño, el `h1` no envuelve su contenido de texto como debería. Alinea el texto del elemento `h1` en el centro.

Luego, da al `main` un relleno de tal manera que el encabezado de la sección `Student Info` pueda ser completamente visto.

```css
h1 {
  color: #f1be32;
  font-size: min(5vw, 1.2em);
 text-align: center;
}

main {
 padding-top: 25px;
 
}
```

## Paso 50

En pantallas pequeñas, la lista desordenada en la barra de navegación desborda el lado derecho de la pantalla.

Soluciona esto usando Flexbox para envolver el contenido de ul. Luego, establezca las siguientes propiedades CSS para alinear correctamente el texto:

- **Código de ejemplo**

  ```css
    align-items: center;
    padding-inline-start: 0;
    margin-block: 0;
    height: 100%;
  ```

```css
nav > ul {
  display: flex;
  justify-content: space-evenly;
 flex-wrap: wrap;
 align-items: center;
 padding-inline-start: 0;
 margin-block: 0;
 height: 100%;
}
```

## Paso 51

Establece el ancho de los elementos `section` al `80%` de su contenedor padre. Luego, utilice los margenes para centar los elementos `section`, agregando `10px` al margen inferior.

Además, asegúrese de que los elementos `section` no puedan tener más de `600px` de ancho.

```css
section {
 width: 80%;
 max-width: 600px;
 margin: 0 auto 10px auto;
}
```

## Paso 52

Reemplaza el margen superior del elemento `h2` con `60px` de relleno superior.

```css
h2 {
 border-bottom: 4px solid #dfdfe2;
 margin-top: 0px;
 padding-top: 60px;
}
```

## Paso 53

Agrega relleno a la parte superior y a la parte izquierda de los elementos `.info`, y establece los demás valores a `0`.

```css
.info {
 padding: 1px 0 0 10px;
}
```

## Paso 54

Da a los elementos `.formrow` margen superior y relleno izquierdo y derecho. Los demás valores de relleno deben ser `0`.

Luego, incremente el tamaño de fuente para todos los elementos `input`.

```css
.formrow {
  margin-top: 30px;
  padding: 0px 15px;
}

input {
  font-size: 1rem;
}
```

## Paso 55

Para hacer que la primera sección se vea más en línea, apunte solo a los elementos `input` dentro de los elementos `.info`, y establezca su `width` a `50%`, y alinee su texto a la izquierda.

```css
.info input {
 width: 50%;
 text-align: left;
}
```

## Paso 56

Apunta a todos los elementos `label` dentro de los elementos `.info`, y establece su `width` a `10%`, y haga que no ocupen menos de `55px`.

```css
.info input {
  width: 50%;
  text-align: left;
}

.info label {
 width: 10%;
 min-width: 55px;
}
```

## Paso 57

Para alinear los elementos input entre sí, crea una nueva regla css para modificar a todos los elementos `input` y `label` dentro de `.info`, agregando una propiedad `display` con el valor `inline-block`.

Alinea también el texto del elemento `label` a la derecha.

```css
.info label, .info input {
  display: inline-block;
}

.info input {
  width: 50%;
  text-align: left;
}

.info label {
  width: 10%;
  min-width: 55px;
  text-align: right;
}
```

## Paso 58

Para ordenar los elementos `.question-block`, establece las siguientes propiedades CSS:

- **Código de ejemplo**
  
  ```css
  text-align: left;
  display: block;
  width: 100%;
  margin-top: 20px;
  padding-top: 5px;
  ```

```css
.question-block {
 text-align: left;
 display: block;
 width: 100%;
 margin-top: 20px;
 padding-top: 5px;
}
```

## Paso 59

Haz que los elementos h3 aparezcan como una prioridad más alta, con las siguientes propiedades de CSS:

- **Código de ejemplo**

  ```css
  margin-top: 5px;
  padding-left: 15px;
  font-size: 1.375rem;
  ```

```css
h3 {
 margin-top: 5px;
 padding-left: 15px;
 font-size: 1.375rem;
}
```

## Paso 60

Es útil ver el borde por defecto alrededor de los elementos `fieldset`, durante el desarrollo. Sin embargo, puede que no sea el estilo que quieras.

Elimina el borde y el relleno inferior de los elementos `.question`.

```css
.question {
 border: none;
 padding-bottom: 0;
}
```

## Paso 61

Mientras que los elementos `ul/li` son excelentes para proporcionar viñetas a los elementos de una lista, tus botones de radio no los necesitan. Puedes controlar cómo se ven las viñetas con la propiedad `list-style`. Por ejemplo puedes transformar tus viñetas en círculos con lo siguiente:

- **Código de ejem**:

  ```css
  ul {
  list-style: circle;
  }
  ```

Elimina el estilo predeterminado para los elementos `.answers-list` al establecer su estilo a `none`, y elimina el relleno de la lista desordenada.

```css
.answers-list {
 list-style: none;
 padding: 0;
}
```

## Paso 62

Dale al botón de envío un diseño al estilo freeCodeCamp, con las siguientes propiedades CSS:

- **Código de ejemplo**:

  ```css
  {
  display: block;
  margin: 40px auto;
  width: 40%;
  padding: 15px;
  font-size: 1.438rem;
  background: #d0d0d5;
  border: 3px solid #3b3b4f;
  }
  ```

```css
button {
  display: block;
  margin: 40px auto;
  width: 40%;
  padding: 15px;
  font-size: 1.438rem;
  background: #d0d0d5;
  border: 3px solid #3b3b4f;
}
```

## Paso 63

Establece el color de fondo del `footer` a `#2a2a40`, y usa Flexbox para centrar horizontalmente el texto.

```css
footer {
  background-color: #2a2a40;
  display: flex;
  justify-content: center;
}
```

## Paso 64

Ahora, no podemos leer el texto. Apunta al `footer` y al elemento ancla dentro para establecer el color de la fuente a un color de relación de contraste adecuado.

```css
footer, footer a {
 color: #dfdfe2;
}
```

## Paso 65

Centra horizontalmente todo el texto dentro del elemento `address` y agrega un poco de relleno.

```css
address {
  text-align: center;
  padding: 0.3em;
}
```

## Paso 66

Al hacer clic en los enlaces de navegación, la ventana gráfica debería saltar a la sección correspondiente. Sin embargo, este salto puede desorientar a algunos usuarios.

Selecciona todos los elementos y establece el `scroll-behavior` a `smooth`.

```css
* {
  scroll-behavior: smooth;
}
```

## Paso 67

Finalmente, ciertos tipos de animaciones basadas en movimiento pueden causar incomodidad a algunos usuarios. En particular, personas con trastornos *vestibulares* tienen sensibilidad a ciertos desencadenantes del movimiento.

La regla-at `@media` tiene una característica de medios llamada `prefers-reduced-motion` para establecer CSS basado en las preferencias del usuario. Puede tomar uno de los siguientes valores:

- *reduce*
- *no-preference*

  - **Código de ejemplo**:

    ```css
    @media (feature: value) {
      selector {
        styles
      }
    }
    ```

Envuelve la regla de estilo que establece `scroll-behavior: smooth` dentro de una regla `@media` con la característica de medios `prefers-reduced-motion` configurada con el valor `no-preference`.

>[!NOTE]
>
>Bien hecho. Has completado el proyecto de práctica del cuestionario de accesibilidad.

```css
@media (prefers-reduced-motion: no-preference) {
 * {
  scroll-behavior: smooth;
 }
}
```
