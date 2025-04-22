# Aprende CSS basico construyendo un menu de una cafeteria

CSS le dice al navegador cómo presentar tu página web. Puedes usar CSS para definir el color, fuente, tamaño, y otros aspectos de los elementos HTML.

En este curso, aprenderás CSS diseñando una página para el menú de la página web de un café.

## Paso 1

En este proyecto aprenderás los conceptos básicos de CSS (Hojas de Estilo en Cascada) construyendo un menú de café. CSS es el idioma utilizado para dar estilo a un documento HTML. Describe cómo se deben mostrar los elementos HTML en la pantalla.

Como has aprendido en los pasos anteriores del proyecto Cat Photo App, hay una estructura básica necesaria para comenzar a construir tu página web. Cada documento HTML debe tener una declaración DOCTYPE y un elemento html. El DOCTYPE le indica al navegador qué versión del código HTML está en el documento. Y el elemento html representa el elemento raíz que contiene todos los demás elementos.

```html
<!DOCTYPE html>
<html lang="en">
<!--all other elements go here-->
</html>
```

>[!NOTE]
>
>Añade la `etiqueta` <!DOCTYPE html> y un elemento `html` con un atributo `lang` con el valor `en`.

## Paso 2

Añade un elemento `head` dentro del elemento `html`, para que puedas añadir un elemento `title`. El texto del elemento `title` deber ser
`Cafe Menu.`

```html
  <head>
    <title>Cafe Menu</title>
  </head>
```

## Paso 3

El elemento `title` es uno de los varios elementos que proporcionan información adicional no visible en la página web, pero que es útil para los motores de búsqueda o en cómo es mostrada la página.

Dentro del elemento `head`, anida un elemento `meta` con un atributo llamado `charset` con el valor `utf-8` para decirle al navegador cómo se codificarán los caracteres para la página.

```html
  <meta charset="UTF-8">
```

## Paso 4

Para comenzar a crear contenido real, añade un elemento `body` debajo del elemento `head`.

```html
  <body>
  </body>
```

## Paso 5

Es hora de darle contenido al menú. Añade un elemento `main` dentro del elemento `body` existente. Contendrá información sobre los precios de los cafés y postres ofrecidos en la cafetería.

```html
  <main>
  </main>
```

## Paso 6

El nombre del café es `CAMPER CAFE`. Añade un elemento `h1` dentro del elemento `main`. Su contenido será el nombre de la cafetería, con todas las letras mayúsculas para que destaque.

```html
    <h1>CAMPER CAFE</h1>
```

## Paso 7

Para que los clientes sepan que la cafetería se fundó en 2020, añade un elemento `p` debajo del elemento `h1` con el texto `Est. 2020`.

```HTML
    <P>Est. 2020</P>
```

## Paso 8

Habrá dos secciones en el menú, una para cafés (coffes) y otra para postres (desserts). Añade un elemento `section` dentro del elemento `main` para que tengas un lugar donde poner todos los cafés disponibles.

```HTML
    <section>
    </section>
  
```

## Paso 9

Crea un elemento `h2` en el elemento `section` y dale el texto `Coffee`.

```html
      <h2>Coffee</h2>
```

## Paso 10

Hasta ahora, has estado limitado en cuanto a la presentación y apariencia del contenido que creas. Para empezar a tomar control, añade un elemento `style` dentro del elemento `head`.

```html
  <style>
  </style>
```

## Paso 11

Puedes darle estilo a un elemento, especificándolo en el elemento `style` y añadiendo una propiedad para el elemento, de esta forma:

```css
  h1 {
      text-align: center;
  }
```

>Centra el contenido del elemento h1 estableciendo su propiedad text-align en el valor center.

## Paso 12

En el paso anterior, utilizaste un selector de tipo para darle estilo al elemento `h1`. Centra el contenido de los elementos `h2` y `p` agregando un nuevo selector de tipo para cada uno al elemento `style`.

```css
  h2 {
      text-align: center;
  }
  p {
      text-align: center;
  }
```

## Paso 13

Ahora tienes tres selectores de tipo con exactamente el mismo estilo. Puede añadir el mismo grupo de estilos a varios elementos creando una lista de selectores. Cada selector se separa con comas, de esta forma:

```css
  selector1, selector2 {
  property: value;
  }
```

>Elimina los tres selectores de tipo existentes y reemplázalos con una sola lista de selectores, que centre el texto de los elementos `h1`, `h2` y `p`.

```css
  h1 {
        text-align: center;
  }
  h2 {
        text-align: center;
  }
  p {
        text-align: center;
  }

  // Reemplaza esto con la siguiente línea

  h1, h2, p {
    text-align: center;
  }
```

## Paso 14

Has dado estilo a tres elementos escribiendo CSS dentro de la etiqueta `style`. Esto funciona, pero dado que habrá muchos más estilos, es mejor poner todos los estilos dentro de un archivo separado y enlazarlo.

Hemos creado un archivo separado `styles.css` por ti y cambiamos la vista del editor a ese archivo. Puedes moverte entre los archivos mediante las pestañas en la parte superior del editor.

Comienza reescribiendo, los estilos que ya has creado, en el archivo `styles.css`. Asegúrate de excluir las etiquetas `style` de apertura y cierre.

```css
  // styles.css
  h1, h2, p {
  text-align: center;
  }
```

## Paso 15

Ahora que tienes el código CSS en el archivo `styles.css`, puedes proseguir a eliminar el elemento `style` y todo su contenido. Una vez eliminado, el texto que estaba centrado regresara hacia la izquierda.

```html
  // index.html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="utf-8" />
      <title>Cafe Menu</title>
    </head>
    <body>
      <main>
        <h1>CAMPER CAFE</h1>
        <p>Est. 2020</p>
        <section>
          <h2>Coffee</h2>
        </section>
      </main>
    </body>
  </html>
```

## Paso 16

Ahora tienes que vincular el archivo `styles.css` para que los estilos se apliquen de nuevo. Dentro del elemento `head`, añade un elemento `link`. Give it a `rel` attribute with the value of `"stylesheet"` and an `href` attribute with the value of `"styles.css"`.

```html
  // index.html
  <link rel="stylesheet" href="styles.css">
```

## Paso 17

Para que el estilo de la página se vea similar tanto en móvil como en ordenador de escritorio o portátil, necesitas añadir un elemento `meta` con un atributo especial `content`.

Añade lo siguiente dentro del elemento `head`:

```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

## Paso 18

El texto está centrado nuevamente, por lo tanto el vínculo al archivo CSS está funcionando. Añade otro estilo al archivo que cambie la propiedad `background-color` a `brown` para el elemento `body`.

```css
  body {
    background-color: brown;
  }
```

## Paso 19

Ese fondo color café hace difícil leer el texto. Cambia el color de fondo (background color) del elemento `body` para que sea `burlywood` para que tenga algo de color, pero se pueda leer el texto.

```css
  body {
    background-color: burlywood;
  }
```

## Paso 20

El elemento `div` se utiliza principalmente para própositos de diseño a diferencia de los otros elementos de contenido que has usado hasta ahora. Añade un elemento `div` dentro del elemento `body` y luego mueve todos los demás elementos dentro del nuevo `div`.

Dentro de la etiqueta `div` de apertura, añade el atributo `id` con un valor de `menu`.

```html
  <body>
    <!-- Se agrega -->
    <div id="menu">
      <main>
        <h1>CAMPER CAFE</h1>
        <P>Est. 2020</P>
        <section>
          <h2>Coffee</h2>
        </section>
      </main>
    </div>
  </body>
```

## Paso 21

El objetivo ahora, es hacer que él `div` no ocupe todo el ancho de la página. La propiedad CSS `width`, es perfecta para esto.

Puedes usar el selector `id` para apuntar a un elemento específico con un atributo `id`. Un selector `id` se define colocando el símbolo de numeral `#` directamente delante del valor del `id`. Por ejemplo, si un elemento tiene un `id` con el valor `cat`, entonces se apuntaría a ese elemento así:

```css
  #cat {
    width: 250px;
  }
```

>Usa el selector `#menu` para darle a tu elemento, un ancho `(width)` de `300px`.

```css
  #menu {
    width: 300px;
  }
```

## Paso 22

Los comentarios en CSS se ven así:

```css
  /* comment here */
```

En tu hoja de estilos, convierte a un comentario la línea con el valor y la propiedad `background-color`, así podrás ver el efecto de solo darle estilo al elemento `#menu`. Esto hará que el fondo vuelva a ser blanco.

```css
  /* background-color: burlywood; */
```

## Paso 23

Ahora utiliza el selector `#menu` existente, para darle un color de fondo (background color) `burlywood` al elemento `div`.

```css
  #menu {
    width: 300px;
    // se agrega
    background-color: burlywood;
  }
```

## Paso 24

Ahora es fácil ver que el texto está centrado dentro del elemento `#menu`. Por ahora, el `ancho` (`width`) del elemento `#menu` está en `píxeles` (`px`).

Cambia el valor de la propiedad `width` a `80%`, para que tenga el `80%` del ancho de su elemento padre (`body`).

```css
  #menu {
    // se cambia
    width: 80%;
    background-color: burlywood;
  }
```

## Paso 25

Ahora centrarás horizontalmente el elemento `#menu`. Puedes hacer esto, dándole el valor `auto` a las propiedades `margin-left` y `margin-right` (margen-izquierdo y margen-derecho). Piensa en el margen como un espacio invisible alrededor de un elemento. Usando estas dos propiedades de margen (margin), centra el elemento `#menu` dentro del elemento `body`.

```css
  #menu {
    width: 80%;
    background-color: burlywood;
    // se agrega
    margin-left: auto;
    margin-right: auto;
  }
```

## Paso 26

Hasta ahora has estado usando selectores de tipo y id para darle estilo a los elementos. Sin embargo, es más común usar un selector diferente para dar estilo a tus elementos.

Un selector de clase (class selector) se define con un nombre y un punto directamente en frente, así:

```css
  .class-name {
    styles
  }
```

>Cambia el selector existente `#menu` a un selector de clase, reemplazando `#menu` con una clase llamada `.menu`.

```css
  .menu {
    width: 80%;
    background-color: burlywood;
    margin-left: auto;
    margin-right: auto;
  }
```

## Paso 27

Para aplicar el estilo de clase (class) al elemento `div`, elimina el atributo `id` y añade un atributo `class` a la etiqueta de apertura del elemento `div`. Asegúrate de darle el valor `menu` al atributo class.

```html
  <div class="menu">
```

## Paso 28

Ya que el producto principal a la venta en la cafetería es el café, podrías utilizar una imagen de granos de café como imagen de fondo.

Elimina el comentario y su contenido dentro del selector de tipo `body`. Ahora añade una propiedad `background-image` y dale el valor `url(<https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg>)`.

```css
  body {
   background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
  }
```

## Paso 29

Se ve bien. Es hora de empezar a añadir algunos elementos al menú. Añade un elemento `article` vacío debajo del encabezado `Coffee`. Contendrá el sabor y precio de cada café que estás ofreciendo.

```html
  <h2>Coffee</h2>
  <article></article>
```

## Paso 30

Los elementos `article` comúnmente contienen múltiples elementos que tienen información relacionada. En este caso, contendrá un sabor de café y un precio para ese sabor. Anida dos elementos `p` dentro de tu elemento `article`. El texto del primero será `French Vanilla`, y el texto del segundo será `3.00`.

```html
  <article>
    <p>French Vanilla</p>
    <p>3.00</p>
  </article>
```

## Paso 31

Empezando debajo del par café/precio existente, añade los siguientes cafés y precios, utilizando elementos `article` con dos elementos `p` anidados dentro de cada uno. Al igual que antes, el texto del primer elemento `p` debe ser el sabor al café y el texto del segundo elemento `p` debe ser el precio.

```html
  <!-- Se crea estos tres articles con sus dos parrafos 
  
  Caramel Macchiato 3.75
  Pumpkin Spice 3.50
  Hazelnut 4.00
  Mocha 4.50
  -->

  <article>
    <p>Caramel Macchiato</p>
    <p>3.75</p>
  </article>
  <article>
    <p>Pumpkin Spice</p>
    <p>3.50</p>
  </article>
  <article>
    <p>Hazelnut</p>
    <p>4.00</p>
  </article>
  <article>
    <p>Mocha</p>
    <p>4.50</p>
  </article>
```

## Paso 32

Por ahora, los sabores (flavors) y precios (prices) están uno encima del otro y se centran con su respectivo elemento `p`. Sería mejor si el sabor estuviera en la izquierda y el precio estuviera en la derecha.

Al elemento `p` con el texto `French Vanilla` agrégale un atributo `class` con el valor `flavor`.

```html
  <article>
    <p class="flavor">French Vanilla</p>
    <p>3.00</p>
  </article>
```

## Paso 33

Utilizando la nueva clase (`class`) `flavor` como un selector de clase, a la propiedad `text-align` dale el valor `left`.

```css
  .flavor {
    text-align: left;
  }
```

## Paso 34

Ahora, alinea el precio hacia la derecha. Añade una clase `price` al elemento `p` con el texto `3.00`.

```html
  <p class="price">3.00</p>
```

## Paso 35

Ahora alinea a la derecha los elementos con la clase `price` utilizando la propiedad text-align y el valor `right`.

```css
  .price {
    text-align: right;
  }
```

## Paso 36

Esto es más o menos lo que queremos lograr, pero sería mejor si el sabor y el precio estuvieran en la misma línea. Los elementos `p` son elementos block-level (elementos de bloque), esto quiere decir que ocupan todo el ancho de su elemento padre.

Para colocarlos en la misma línea, necesitas aplicar un estilo a los elementos `p` para que se comporten como elementos inline (en línea). Para hacer eso, comienza añadiendo un atributo `class` con el valor `item` al primer elemento `article` bajo del encabezado `Coffee`.

```html
  <article class="item">
```

## Paso 37

Los elementos `p` están anidados en un elemento `article` con un atributo class con el valor `item`. Puedes darle estilo a todos los elementos `p` que estén anidados en cualquiera de los elementos con la clase `item` de la siguiente forma:

```css
  .item p { }
```

>Utilizando el selector de arriba, añade una propiedad `display` con valor `inline-block` para que los elementos `p` se comporten como elementos inline (en línea).

```css
  .item p {
  display: inline-block;
}
```

## Paso 38

Así está mejor, pero el precio no se quedó en la derecha. Esto se debe a que los elementos de `inline-block` solo ocupan el ancho de su contenido. Para extenderlos, añade una propiedad `width` a los selectores de clase `flavor` y `price` dándoles un valor de `50%` a cada uno.

```css
  .flavor {
   text-align: left;
    width: 50%;
  }

  .price {
   text-align: right;
    width: 50%;
  }
```

## Paso 39

Bueno, eso no funcionó. Cambiar los elementos `p` a `inline-block` y colocarlos en líneas diferentes, crea un espacio extra a la derecha del primer elemento `p`, haciendo que el segundo se mueva a la siguiente línea. White space characters can cause this issue as well.

Una forma de arreglar esto, es hacer que el ancho (width) de cada elemento `p` sea un poco menor que `50%`. Cambia el valor de la propiedad `width` a `49%` en cada clase para ver qué sucede.

```css
  .flavor {
    text-align: left;
    width: 49%;
  }

  .price {
    text-align: right;
    width: 49%;
  }
```

## Paso 40

Eso funcionó, pero todavía hay un pequeño espacio a la derecha del precio.

Podrías seguir probando diferentes porcentajes para la propiedad width (ancho). En cambio, usa la tecla de retroceso (borrar) en tu teclado para mover el elemento `p` con la clase `price` hasta colocarlo al lado del elemento `p` con la clase `flavor` para que estén en la misma línea en el editor. Asegúrate de que no haya espacio entre los dos elementos.

```html
  <p class="flavor">French Vanilla</p><p class="price">3.00</p>
```

## Paso 41

Ahora, sigue adelante y cambia la anchura de las clases `flavor` y `price` de nuevo a `50%`.

```css
  .flavor {
    text-align: left;
    width: 50%;
  }

  .price {
    text-align: right;
    width: 50%;
  }
```

## Paso 42

Ahora que sabes que funciona, puedes modificar los elementos `article` y `p` restantes para que coincidan con el primer conjunto. Empieza añadiendo la clase `item` a los demás elementos `article`.

```html
  <article class="item">
    <p >Caramel Macchiato</p>
    <p >3.75</p>
  </article>
  <article class="item">
    <p>Pumpkin Spice</p>
    <p>3.50</p>
  </article>
  <article class="item">
    <p>Hazelnut</p>
    <p>4.00</p>
  </article>
  <article class="item">
    <p>Mocha</p>
    <p>4.50</p>
  </article>
```

## Paso 43

A continuación, mueve los otros elementos `p` para que estén en la misma línea sin espacios entre ellos.

```html
  <article class="item">
    <p>Caramel Macchiato</p><p>3.75</p>
  </article>
  <article class="item">
    <p>Pumpkin Spice</p><p>3.50</p>
  </article>
  <article class="item">
    <p>Hazelnut</p><p>4.00</p>
  </article>
  <article class="item">
    <p>Mocha</p><p>4.50</p>
  </article>
```

## Paso 44

Para terminar de agregar estilos, agrega las clases `flavor` y `price` a todos los elementos `p` restantes.

```html
  <article class="item">
    <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
  </article>
  <article class="item">
    <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
  </article>
  <article class="item">
    <p class="flavor">Hazelnut</p><p class="price">4.00</p>
  </article>
  <article class="item">
    <p class="flavor">Mocha</p><p class="price">4.50</p>
  </article>
```

## Paso 45

Si reduces el ancho de la ventana donde se muestra la vista previa, llegara un punto donde parte del texto de la izquierda saltará a la siguiente línea. Esto se debe a que el ancho de los elementos `p` del lado izquierdo solo pueden tomar `50%` del espacio.

Como sabemos que los precios de la derecha tienen menos caracteres, cambia el valor de la propiedad `width` del selector de clase flavor a `75%` y el valor de la propiedad `width` del selector de clase `price` a `25%`.

```css
  .flavor {
    text-align: left;
    width: 75%;
  }

  .price {
    text-align: right;
    width: 25%;
  }
```

## Paso 46

En los siguientes pasos volverás a darle estilo al menú, pero por ahora; debajo del primer elemento section, añade un nuevo elemento `section`para mostrar los postres que ofrece la cafetería.

```html
  <section>
    <h2>Coffee</h2>
    <article class="item">
      <p class="flavor">French Vanilla</p><p class="price">3.00</p>
    </article>
    <article class="item">
      <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
    </article>
    <article class="item">
      <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
    </article>
    <article class="item">
      <p class="flavor">Hazelnut</p><p class="price">4.00</p>
    </article>
    <article class="item">
      <p class="flavor">Mocha</p><p class="price">4.50</p>
    </article>
  </section>
  <section></section>
```

## Paso 47

Añade un elemento `h2` con el texto `Desserts` dentro del nuevo elemento section.

```html
  <section>
    <h2>Desserts</h2>
  </section>
```

## Paso 48

Añade un elemento `article` vacío debajo del título `Desserts`. Dale un atributo `class` con el valor `item`.

```html
  <h2>Desserts</h2>
  <article class="item"></article>
```

## Paso 49

Anida dos elementos `p` dentro de tu elemento `article`. El texto del primero será `Donut`, y el texto del segundo será `1.50`. Coloca ambos elementos p en la misma línea, asegurándote de que no haya ningún espacio entre ellos.

```html
  <article class="item">
    <p>Donut</p>
    <p>1.50</p>
  </article>
```

## Paso 50

A los elementos `p` que acabas de añadir, agrega `dessert` como valor del atributo `class` en el primer elemento `p` y `price` como valor del atributo `class` en el segundo elemento `p`.

```html
  <p class="dessert">Donut</p><p class="price">1.50</p>
```

## Paso 51

Algo no se ve bien. Añadiste un atributo `class` con el valor correcto al elemento `p` con el texto `Donut`, pero aún no has definido un selector.

La regla CSS para la clase `flavor` ya establece las propiedades que deseas. Añade la clase `dessert` como un selector adicional para esta regla CSS.

```css
  .flavor, .dessert {
    text-align: left;
    width: 75%;
  }
```

## Paso 52

Debajo del postre (dessert) que acabas de añadir, añade el resto de los postres y precios; usando tres elementos `article` cada uno con dos elementos `p` anidados. Cada elemento debe tener el postre y precio correcto. Y todos ellos deben tener las clases correctas.

```html
  <!-- 
  Se agrga tres articles con sus 2 parrafos y sus clases respectivas
  
  Cherry Pie 2.75
  Cheesecake 3.00
  Cinnamon Roll 2.50
  -->

  <article class="item">
    <p class="dessert">Donut</p><p class="price">1.50</p>
  </article>
  <article class="item">
    <p class="dessert">Cherry Pie</p><p class="price">2.75</p>
  </article>
  <article class="item">
    <p class="dessert">Cheesecake</p><p class="price">3.00</p>
  </article>
  <article class="item">
    <p class="dessert">Cinnamon Roll</p><p class="price">2.50</p>
  </article>
```

## Paso 53

Puedes darle a tu menú algo de espacio interno entre el contenido y los lados, añadiendo algunas propiedades de tipo `padding` (espaciado interno).

En la clase `menu` agrega las propiedades `padding-left` y `padding-right` ambas con un valor dé `20px`.

```css
  .menu {
    width: 80%;
    background-color: burlywood;
    margin-left: auto;
    margin-right: auto;
    padding-left: 20px;
    padding-right: 20px;
  }
```

## Paso 54

Se ve mejor. Ahora intenta añadir un espaciado interno superior (padding top) y espaciado interno inferior (padding bottom) de `20px` al menú.

```CSS
  .menu {
    width: 80%;
    background-color: burlywood;
    margin-left: auto;
    margin-right: auto;
    padding-left: 20px;
    padding-right: 20px;
    padding-top: 20PX;
    padding-bottom: 20PX;
  }
```

## Paso 55

Ya que los 4 lados del menú tienen el mismo espaciado interno, puedes borrar las cuatro propiedades y utilizar una sola propiedad `padding` con el valor `20px`.

```CSS
  .menu {
    width: 80%;
    background-color: burlywood;
    margin-left: auto;
    margin-right: auto;
    padding: 20PX;
  }
```

## Paso 56

El ancho actual del menú siempre tomará un 80% del ancho del elemento `body`. En una pantalla muy amplia, el café y el postre aparecerán demasiado lejos de sus precios.

Añade una propiedad `max-width` (ancho-máximo) a la clase `menu` con un valor de `500px` para prevenir que se expanda más de lo necesario.

```css
  .menu {
    width: 80%;
    max-width: 500px;
    background-color: burlywood;
    margin-left: auto;
    margin-right: auto;
    padding: 20px;
  }
```

## Paso 57

Puedes cambiar la fuente (`font-family`) del texto, para que luzca diferente de la fuente predeterminada de tu navegador. Cada navegador cuenta con algunas fuentes comunes disponibles.

Cambia todo el texto de tu elemento `body`, añadiendo una propiedad `font-family` con el valor `sans-serif`. Esta es una fuente común, la cual es bastante legible.

```css
  body {
    background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
    font-family: sans-serif;
  }
```

## Paso 58

Es un poco aburrido que todo el texto tenga el mismo tipo de fuente (`font-family`). Aún puedes tener la mayoría del texto con la fuente `sans-serif` y hacer que solo los elementos `h1` y `h2` se vean diferentes utilizando otro selector.

Cambia el estilo de los elementos `h1` y `h2`, utilizando un solo selector, dándoles un tipo de fuente `Impact`.

```css
  h1, h2 {
    font-family: Impact;
  }
```

## Paso 59

Puedes añadir un valor de respaldo para la propiedad font-family añadiendo una fuente extra separada por una coma. Una fuente de respaldo es utilizada en el caso de que la fuente principal no esté disponible o no se pueda encontrar.

Añade la fuente `serif` como un respaldo después de la fuente `Impact`.

```css
  h1, h2 {
    font-family: Impact, serif;
  }
```

## Paso 60

Haga que el texto `Est. 2020` esté en cursiva creando un selector de clase `established` y asignándole la propiedad `font-style` con el valor `italic`.

```css
  .established {
    font-style: italic;
  }
```

## Paso 61

Now apply the `established` class to the `Est. 2020` text.

```html
  <h1>CAMPER CAFE</h1>
  <p class="established">Est. 2020</p>
```

## Paso 62

La tipografía de los elementos de título (por ejemplo `h1`, `h2`) se establece por defecto en los valores preestablecidos de los navegadores de los usuarios.

Añade dos nuevos selectores de tipo (`h1` y `h2`). Utiliza la propiedad `font-size` (tamaño de fuente) para ambos, pero usa el valor `40px` para el elemento `h1` y `30px` para el elemento `h2`.

```css
  h1 {
    font-size: 40px;
  }

  h2 {
    font-size: 30px;
  }
```

## Paso 63

Añade un elemento `footer` debajo del elemento `main`, donde podrás añadir información adicional.

```html
  <main>
    <h1>CAMPER CAFE</h1>
    <p class="established">Est. 2020</p>
    <section>
      <h2>Coffee</h2>
      <article class="item">
        <p class="flavor">French Vanilla</p><p class="price">3.00</p>
      </article>
      <article class="item">
        <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
      </article>
      <article class="item">
        <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
      </article>
      <article class="item">
        <p class="flavor">Hazelnut</p><p class="price">4.00</p>
      </article>
      <article class="item">
        <p class="flavor">Mocha</p><p class="price">4.50</p>
      </article>
    </section>
    <section>
      <h2>Desserts</h2>
      <article class="item">
        <p class="dessert">Donut</p><p class="price">1.50</p>
      </article>
      <article class="item">
        <p class="dessert">Cherry Pie</p><p class="price">2.75</p>
      </article>
      <article class="item">
        <p class="dessert">Cheesecake</p><p class="price">3.00</p>
      </article>
      <article class="item">
        <p class="dessert">Cinnamon Roll</p><p class="price">2.50</p>
      </article>
    </section>
  </main>
  <footer></footer>
```

## Paso 64

Dentro del elemento footer, añade un elemento p. Después, anida un elemento anchor (`a`) en el elemento `p` que enlace a `https://www.freecodecamp.org` y tenga el texto `Visit our website`.

Asegúrate de que el enlace se abre en una nueva pestaña agregando un atributo `target` con el valor `_blank`.

```html
  <footer>
    <p>
      <a href="https://www.freecodecamp.org" target="_blank">Visit our website</a>
    </p>
  </footer>
```

## Paso 65

Añade un segundo elemento `p` con el texto `123 Free Code Camp Drive`, debajo del que tiene el enlace.

```html
  <p>
    <a href="https://www.freecodecamp.org" target="_blank">
      Visit our website
    </a>
  </p>
  <p>
    123 Free Code Camp Drive
  </p>
```

## Paso 66

Puedes usar un elemento `hr` para mostrar una línea divisora entre secciones con diferente contenido.

En primer lugar, añada un elemento `hr` entre el elemento `p` con la clase `established` y el primer elemento `section`.

```html
  <main>
    <h1>CAMPER CAFE</h1>
    <p class="established">Est. 2020</p>
    <hr>
    <section>
      <h2>Coffee</h2>
      <article class="item">
        <p class="flavor">French Vanilla</p><p class="price">3.00</p>
      </article>
      <article class="item">
        <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
      </article>
      <article class="item">
        <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
      </article>
      <article class="item">
        <p class="flavor">Hazelnut</p><p class="price">4.00</p>
      </article>
      <article class="item">
        <p class="flavor">Mocha</p><p class="price">4.50</p>
      </article>
    </section>

    <section>
      <h2>Desserts</h2>
      <article class="item">
        <p class="dessert">Donut</p><p class="price">1.50</p>
      </article>
      <article class="item">
        <p class="dessert">Cherry Pie</p><p class="price">2.75</p>
      </article>
      <article class="item">
        <p class="dessert">Cheesecake</p><p class="price">3.00</p>
      </article>
      <article class="item">
        <p class="dessert">Cinnamon Roll</p><p class="price">2.50</p>
      </article>
    </section>
  </main>
```

## Paso 67

Las propiedades predeterminadas de un elemento `hr` harán que luzca como una línea delgada color gris claro. Puede cambiar la altura de la línea añadiendo una propiedad `height` y dándole un valor.

Cambia la altura del elemento `hr` para que sea dé `3px`.

```css
  hr {
    height: 3px;
  }
```

## Paso 68

Cambia el color de fondo (background color) del elemento `hr` a café o `brown` en inglés para que coincida con el color de los granos de café.

```css
  hr {
    height: 3px;
    background-color: brown;
  }
```

## Paso 69

Observa el color gris a lo largo de los bordes de la línea. Esos bordes son conocidos como border. Cada lado de un elemento puede tener un color diferente o todos pueden ser iguales.

Haz que todos los bordes del elemento `hr` tengan el mismo color que el fondo; utilizando la propiedad `border-color`.

```css
  hr {
    height: 3px;
    background-color: brown;
    border-color: brown;
  }
```

## Paso 70

¿Observa cómo el grosor de la línea se ve más grande? El valor predeterminado de la propiedad `border-width` (ancho de borde) es `1px` para todos los lados de los elementos `hr`. Cambiando el borde al mismo color de la línea, la altura total de la línea es de `5px` (`3px` más el ancho del borde superior e inferior de `1px` cada uno).

Cambia la propiedad `height` (altura) del elemento `hr` para que sea `2px`, así su altura total será `4px`.

```css
  hr {
    height: 2px;
    background-color: brown;
    border-color: brown;
  }
```

## Paso 71

Ahora añade otro elemento `hr` entre el elemento `main` y el elemento `footer`.

```html
  <main>
    <h1>CAMPER CAFE</h1>
    <p class="established">Est. 2020</p>
    <hr>
    <section>
      <h2>Coffee</h2>
      <article class="item">
        <p class="flavor">French Vanilla</p><p class="price">3.00</p>
      </article>
      <article class="item">
        <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
      </article>
      <article class="item">
        <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
      </article>
      <article class="item">
        <p class="flavor">Hazelnut</p><p class="price">4.00</p>
      </article>
      <article class="item">
        <p class="flavor">Mocha</p><p class="price">4.50</p>
      </article>
    </section>
    <section>
      <h2>Desserts</h2>
      <article class="item">
        <p class="dessert">Donut</p><p class="price">1.50</p>
      </article>
      <article class="item">
        <p class="dessert">Cherry Pie</p><p class="price">2.75</p>
      </article>
      <article class="item">
        <p class="dessert">Cheesecake</p><p class="price">3.00</p>
      </article>
      <article class="item">
        <p class="dessert">Cinnamon Roll</p><p class="price">2.50</p>
      </article>
    </section>
  </main>

  <hr>

  <footer>
    <p>
      <a href="https://www.freecodecamp.org" target="_blank">Visit our website</a>
    </p>
    <p>123 Free Code Camp Drive</p>
  </footer>
```

## Paso 72

Para crear poco más de espacio alrededor del menú, añade `20px` de espacio en el interior del elemento `body` usando la propiedad `padding`.

```css
  body {
    background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
    font-family: sans-serif;
    padding: 20px;
  }
```

## Paso 73

Enfocándose en los elementos del menú y los precios, hay un espacio considerablemente grande entre cada línea.

Utiliza el selector existente que apunta a todos los elementos `p` anidados en una clase (class) `item` y dales un margen superior (top) e inferior (bottom) dé `5px`.

```css
  h1, h2 {
    font-family: Impact, serif;
  }

  .item p {
    display: inline-block;
    margin-top: 5px;
    margin-bottom: 5px;
  }

  .flavor, .dessert {
    text-align: left;
    width: 75%;
  }

  .price {
    text-align: right;
    width: 25%;
  }
```

## Paso 74

Utilizando el mismo selector de estilo del paso anterior, haz que el tamaño de la fuente (font size) de los artículos y precios sea mayor, usando un valor dé `18px`.

```css
  .item p {
    display: inline-block;
    margin-top: 5px;
    margin-bottom: 5px;
    font-size: 18px;
  }
```

## Paso 75

Al cambiar el margen inferior (`margin-bottom`) a `5px` se ve mejor. Sin embargo, ahora el espacio entre la opción del menú `Cinnamon Roll` y el segundo elemento `hr` no coincide con el espacio entre el elemento `hr` superior y el título `Coffee`.

Añade algo de espacio, creando una clase llamada `bottom-line` (línea inferior) y usando `25px` para el valor de la propiedad `margin-top`.

```css
  .bottom-line {
    margin-top: 25px;
  }
```

## Paso 76

Ahora añade la clase `bottom-line` al segundo elemento `hr` para que se aplique el estilo.

```html
  <hr class="bottom-line">
```

## Paso 77

A continuación, le darás estilo al elemento `footer`. Para mantener el código CSS organizado, añade un comentario al final de `styles.css` con el texto `FOOTER`.

```css
  /* FOOTER */
```

## Paso 78

Ve al elemento `footer` y has que todo el texto tenga un tamaño de fuente (font size) dé `14px`.

```css
  footer {
    font-size: 14px;
  }
```

## Paso 79

Usualmente, color predeterminado de un enlace en el que aún no se ha hecho clic es azul. El color predeterminado de un enlace que ya ha sido visitado es morado/púrpura.

Para hacer que los enlaces del `footer` tengan el mismo color sin importar si ya han sido visitados o no, utiliza un selector de tipo para el elemento anchor (`a`) y usa el valor `black` para la propiedad `color`.

```css
  a {
    color: black;
  }
```

## Paso 80

Para cambiar las propiedades de un enlace cuando el enlace ya ha sido visitado utilizas un pseudo-selector, el cual luce así `a:visited { propertyName: propertyValue; }`.

Cambia el color del enlace del footer `Visit our website` para que sea gris (grey) cuando un usuario ya ha visitado el enlace.

```css
  a:visited {
    color: gray;
  }
```

## Paso 81

Puedes cambiar las propiedades de un enlace cuando el ratón pasa sobre él utilizando un pseudo-selector, que luce así `a:hover { propertyName: propertyValue; }`.

Cambia el color del enlace del footer `Visit our website` para sea café (`brown`) cuando un usuario pase sobre él.

```css
  a:hover {
    color: brown;
  }
```

## Paso 82

Para cambiar las propiedades de un enlace, cuando el enlace está siendo presionado, utilizas un pseudo-selector, el cual luce así `a:active { propertyName: propertyValue; }`.

Cambia el color del enlace del footer `Visit our website`, para que sea blanco (`white`) cuando esté siendo presionado.

```css
  a:active {
    color: white;
  }
```

## Paso 83

Para mantener los mismos colores que has estado utilizando (negro y café), has que el enlace cambie a color negro (`black`) cuando ya ha sido visitado y sea color café (`brown`) cuando el enlace está siendo presionado.

```css
  a:visited {
    color: black;
  }

  a:hover {
    color: brown;
  }

  a:active {
    color: brown;
  }
```

## Paso 84

El texto `CAMPER CAFE` del menú, tiene un espaciado diferente en la parte superior que el espaciado entre la dirección en la parte inferior. Esto se debe a que el navegador tiene un margen superior predeterminado para el elemento `h1`.

Cambia el margen superior (top margin) del elemento `h1` a `0` para eliminar todo el margen superior.

```css
  h1 {
    font-size: 40px;
    margin-top: 0;
  }
```

## Paso 85

Para eliminar parte del espacio vertical entre el elemento `h1` y el texto `Est. 2020`, cambie el margen inferior (margin-bottom) del `h1` a `15px`.

```css
  h1 {
    font-size: 40px;
    margin-top: 0;
    margin-bottom: 15px;
  }
```

## Paso 86

Ahora el espaciado superior se ve bien. El espacio debajo de la dirección en la parte inferior del menú es un poco más grande que el espacio en la parte superior del menú y el elemento `h1`.

Para disminuir el valor del margen debajo del elemento `p` con la dirección, crea un selector de clase llamado `address` y usar el valor `5px` para la propiedad `margin-bottom`.

```css
  .address {
    margin-bottom: 5px;
  }
```

## Paso 87

Ahora aplica la clase `address` al elemento `p` que contiene la dirección `123 Free Code Camp Drive`.

```html
  <footer>
    <p>
      <a href="https://www.freecodecamp.org" target="_blank">Visit our website</a>
    </p>
    <p class="address">
      123 Free Code Camp Drive
    </p>
  </footer>
```

## Paso 88

El menú se ve bien, pero aparte de la imagen de fondo con los granos de café, es prácticamente solo texto.

En el encabezado `Coffee`, añade una imagen usando la url `https://cdn.freecodecamp.org/curriculum/css-cafe/coffee.jpg`. Dale a la imagen un atributo `alt` con el valor `coffee icon`.

```html
  <h2>Coffee</h2>
  <img src="https://cdn.freecodecamp.org/curriculum/css-cafe/coffee.jpg" alt="coffee icon">
```

## Paso 89

La imagen que añadiste no está centrada horizontalmente como el título `Coffee` sobre ella. Los elementos `img` son similares a los elementos en línea.

Para hacer que la imagen se comporte como un elemento título (elementos de tipo bloque), crea un selector de tipo `img` y añádele una propiedad `display` con el valor `block` y aplica las propiedades `margin-left` y `margin-right` con los valores necesarios para centrar horizontalmente.

```css
  img {
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
```

## Paso 90

Añade una última imagen bajo el título `Desserts` utilizando la url `https://cdn.freecodecamp.org/curriculum/css-cafe/pie.jpg`. Dale a la imagen un atributo `alt` con el valor `pie icon` (icono de pay).

```html
  <h2>Desserts</h2>
  <img src="https://cdn.freecodecamp.org/curriculum/css-cafe/pie.jpg" alt="pie icon">
```

## Paso 91

Sería mejor si el espacio vertical entre los elementos `h2` y sus respectivos íconos fuera más pequeño. Los elementos `h2` tienen un margen superior e inferior predeterminado, porque no cambias el margen inferior del elemento `h2` a `0` ó algún otro número.

Hay una forma más fácil, simplemente añade un margen superior negativo a los elementos `img` para moverlos de sus posiciones actuales. Los valores negativos se crean usando un `-` delante del valor. Para completar este proyecto, utiliza un margen superior (margin top) negativo de `25px` en el selector de tipo `img`.

```css
  img {
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-top: -25px;
  }
```
