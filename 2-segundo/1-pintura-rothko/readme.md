# Aprende el Modelos de Cajas de CSS construyendo una pintura Rothko

Cada elemento HTML es su propia caja – con su propio espaciado y borde. A esto se le llama Modelo de Caja.

En este curso, utilizarás CSS y el Modelo de Cajas para crear tus propias piezas de arte rectangulares al estilo de Rothko.

## Paso 1

A estas alturas, debería estar familiarizado con los elementos básicos que debería tener una página HTML.

Configure su código con una declaración de `DOCTYPE`, un elemento `html` con el idioma establecido en inglés, un elemento `head` y un elemento `body`.

```html
<!DOCTYPE html>
<html lang="en">

<head>
</head>

<body>
</body>

</html>
```

## Paso 2

Within the `head` element, add a `meta` tag which sets the `charset` to `UTF-8`, and a `title` element with the value `Rothko Painting`.

Dentro del elemento `body`, agregue un elemento `img` con un `src` de `<https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-1.png>`.

```html
<head>
  <meta charset="UTF-8">
  <title>Rothko Painting</title>
</head>

<body>
  <img src="https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-1.png" alt="">
</body>
```

## Paso 3

En el modelo de cuadro CSS, cada elemento HTML se trata como un cuadro con cuatro áreas.

Imagine que recibe una caja de su minorista en línea favorito: el contenido es el elemento en la caja, o en nuestro caso, un encabezado, párrafo o elemento de imagen.

Cambie el atributo `src` en el atributo `<img>` de `https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-1.png` a `https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-2.png`.

```html
    <img src="https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-2.png">
```

## Paso 4

El contenido está rodeado por un espacio llamado relleno, similar a cómo el plástico de burbujas separa un elemento de la caja que lo rodea.

Piense en el borde como la caja de cartón en la que se envió su artículo.

Cambie el atributo `src` a `https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-3.png`

```html
    <img src="https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-3.png">
```

## Paso 5

El margen es el área fuera de la caja, y se puede utilizar para controlar el espacio entre otras cajas o elementos.

Aquí el elemento inferior tiene un margen superior más grande, empujándolo más abajo en la página.

Ahora que entiendes el modelo de caja CSS, comencemos con la pintura de Rothko.

Elimine el elemento`<img>`.

```html
<!-- Se elimina la etiqueta img -->
```

## Paso 6

Add a `div` element in the `body`.

Al atributo `class` dale el valor `canvas`.

Esto actuará como el lienzo para su pintura.

```html
  <div class="canvas"></div>
```

## Paso 7

Antes de que pueda comenzar a aplicar estilo al `div` que agregó, debe vincular su CSS a su HTML.

Agregue un elemento `link` para vincular el archivo `styles.css`. Establezca el `href` en `styles.css` y recuerde establecer el atributo `rel` en `stylesheet`.

```html
  <link rel="stylesheet" href="styles.css">
```

## Paso 8

Tiempo para CSS.

Aunque tu `<div>` no tenga texto, todavía se trata como un cuadro con contenido. Escribe una regla CSS que use el selector de clase `.canvas` y establece su `width` en 500 píxeles. Aquí hay una regla CSS que establece el ancho de la clase `card` en 300 píxeles:

- EJEMPLO

```css
.card {
  width: 300px;
}
```

- PAGINA

```css
.canvas {
  width: 500px;
}
```

## Paso 9

Agregue la propiedad `height` con el valor `600px` a la regla `.canvas`.

```css
.canvas {
  width: 500px;
  height: 600px;
}
```

## Paso 10

Cambie el `background-color` del lienzo a `#4d0f00`.

```css
.canvas {
  width: 500px;
  height: 600px;
  background-color: #4d0f00;
}
```

## Paso 11

Cada pintura necesita un marco.

Ajuste el elemento `.canvas` en otro `div`. Asigne a ese `div` la clase `frame`.

```html
  <div class="frame">
    <div class="canvas"></div>
  </div>
```

## Paso 12

Escribe una nueva regla usando el selector de clase `.frame`.

Usa la declaración abreviada `border` para darle al elemento `.frame` un borde negro sólido con un ancho de `50px`.

```css
.frame {
 border: 50px solid black;
}
```

## Paso 13

El marco es demasiado ancho.

En `.frame`, establezca su `width` en 500 píxeles.

```css
.frame {
 border: 50px solid black;
  width: 500px;
}
```

## Paso 14

Utilice el relleno para ajustar el espaciado dentro de un elemento.

En `.frame`, use la abreviatura `padding` para aumentar el espacio entre los elementos `.frame` y `.canvas` por `50px`. La taquigrafía aumentará el espacio en la parte superior, inferior, izquierda y derecha del borde y el lienzo del elemento dentro.

```css
 padding: 50px;
```

## Paso 15

Use márgenes para ajustar el espaciado fuera de un elemento.

Usando la propiedad `margin`, proporcione al elemento `.frame` un margen vertical de `20px` y un margen horizontal de `auto`. Esto moverá el marco 20 píxeles hacia abajo y lo centrará horizontalmente en la página.

```css
 margin: 20px auto;
```

## Paso 16

Agrega un nuevo elemento `div` dentro de tu elemento `.canvas`.

Asigne al nuevo atributo `div` el atributo `class` con un valor de `one`. Este será tu primer rectángulo.

```html
  <div class="frame">
    <div class="canvas">
      <div class="one"></div>
    </div>
  </div>
```

## Paso 17

Escribe una nueva regla que apunte a `.one` y establezca su `width` en 425 píxeles.

```css
.one {
 width: 425px;
}
```

## Paso 18

Ahora establezca el `height` para `.one` en 150 píxeles.

```css
.one {
 width: 425px;
 height: 150px;
}
```

## Paso 19

Set the `background-color` of `.one` to `#efb762`.

```css
.one {
 width: 425px;
 height: 150px;
 background-color: #efb762;
}

```

## Paso 20

Utilice márgenes para colocar el elemento `.one` en el lienzo.

Agregue la propiedad abreviada `margin` con un margen vertical de `20px` y un margen horizontal de `auto`.

```css
.one {
 width: 425px;
 height: 150px;
 background-color: #efb762;
 margin: 20px auto;
}
```

## Paso 21

Ahora `.one` está centrado horizontalmente, pero su margen superior está empujando más allá del lienzo y hacia el borde del marco, desplazando todo el lienzo 20 píxeles hacia abajo.

Agregue `padding` de `1px` al elemento `.canvas` para darle al elemento `.one` algo sólido para empujar.

```css
.canvas {
 width: 500px;
 height: 600px;
 background-color: #4d0f00;
 padding: 1px;
}
```

## Paso 22

Agrega 1 píxel de relleno a la parte superior, inferior, izquierda y derecha del lienzo cambió sus dimensiones a 502 píxeles x 602 píxeles.

Reemplace la propiedad `padding` por `overflow` establecida en `hidden` - Cambiar el lienzo a sus dimensiones originales.

```css
.canvas {
 width: 500px;
 height: 600px;
 background-color: #4d0f00;
 overflow: hidden;
}
```

## Paso 23

Add another `div` with a `class` value of `two` just below your `one` element. Este será tu segundo rectángulo.

```html
  <div class="frame">
    <div class="canvas">
      <div class="one"></div>
      <div class="two"></div>
    </div>
  </div>
```

## Paso 24

Crea una nueva regla CSS usando el selector `.two` y establece su `width` a `475 píxeles`.

```css
.two {
 width: 475px;
}
```

## Paso 25

Establezca el height del elemento `.two` en 200 píxeles.

```css
.two {
 width: 475px;
 height: 200px;
}
```

## Paso 26

Set the background-color of the .two element to `#8f0401`.

```css
.two {
 width: 475px;
 height: 200px;
 background-color: #8f0401;
}
```

## Paso 27

Center the `.two` element by setting its `margin` to `auto`.

```css
.two {
 width: 475px;
 height: 200px;
 background-color: #8f0401;
 margin: auto;
}
```

## Paso 28

Create a new `div` with a `class` value of `three` right under the `.two` element. Este será tu tercer rectángulo.

```HTML
    <div class="canvas">
      <div class="one"></div>
      <div class="two"></div>
      <div class="three"></div>
    </div>
```

## Paso 29

No siempre tienes que usar píxeles al dimensionar un elemento.

Cree una nueva regla, `.three`, y establezca su width en `91%`.

```css
.three {
 width: 91%;
}
```

## Paso 30

Set the `height` of `.three` to `28%`.

```css
.three {
 width: 91%;
 height: 28%;
}
```

## Paso 31

Cambie el `background-color` de `.three` a `#b20403`.

```css
.three {
 width: 91%;
 height: 28%;
 background-color: #b20403;
}
```

## Paso 32

Centra el elemento `.three` en el lienzo estableciendo su `margin` en `auto`.

```css
.three {
 width: 91%;
 height: 28%;
 background-color: #b20403;
 margin: auto;
}
```

## Paso 33

Es útil que sus márgenes empujen en una dirección.

En este caso, el margen inferior del elemento `.one` empuja `.two` 20 píxeles hacia abajo.

En el selector `.two`, use la abreviatura `margin` para establecer el margen superior en `0`, el margen horizontal en `auto` y el margen inferior en `20px`. Esto eliminará su margen superior, lo centrará horizontalmente y establecerá su margen inferior en 20 píxeles.

```css
.two {
 width: 475px;
 height: 200px;
 background-color: #8f0401;
 margin: 0 auto 20px;
}
```

## Paso 34

Los colores y las formas de su pintura son demasiado nítidos para pasar como un Rothko.

Utilice la propiedad `filter` para `blur` la pintura por `2px` en el elemento `.canvas`.

Aquí hay un ejemplo de una regla que agrega un 3px `blur`:

- CODIGO DE EJEMPLO

  ```css
  p {
    filter: blur(3px);
  }
  ```

```CSS
.canvas {
  width: 500px;
  height: 600px;
  background-color: #4d0f00;
  overflow: hidden;
 filter: blur(2px);
}
```

## Paso 35

Cree una regla destinada tanto a `.one` como a `.two` y aumente su efecto `blur` en 1 píxel.

```css
.one,
.two {
 filter: blur(1px);
}
```

## Paso 36

Aumente el `blur` de `.three` en 2 píxeles.

```css
.three {
 width: 91%;
 height: 28%;
 background-color: #b20403;
 margin: auto;
 filter: blur(2px);
}
```

## Paso 37

Los rectángulos son demasiado pequeños y sus bordes no tienen la calidad suave de una pintura.

Aumente el área y suavice los bordes de `.one` estableciendo su `box-shadow` en `0 0 3px 3px #efb762`.

```css
.one {
 width: 425px;
 height: 150px;
 background-color: #efb762;
 margin: 20px auto;
 box-shadow: 0 0 3px 3px #efb762;
}
```

## Paso 38

Utilice la misma declaración `box-shadow` para `.two`, pero cambie el color de `#efb762` a `#8f0401`.

```css
.two {
 width: 475px;
 height: 200px;
 background-color: #8f0401;
 margin: 0 auto 20px;
 box-shadow: 0 0 3px 3px #8f0401;
}
```

## Paso 39

Agregue un `box-shadow` a `.three` con los valores `0 0 5px 5px #b20403`.

```css
.three {
 width: 91%;
 height: 28%;
 background-color: #b20403;
 margin: auto;
 filter: blur(2px);
 box-shadow: 0 0 5px 5px #b20403;
}
```

## Paso 40

Las esquinas de cada rectángulo siguen siendo demasiado afiladas.

Redondee cada esquina del elemento `.one` 9 píxeles, utilizando la propiedad `border-radius`.

```css
.one {
 width: 425px;
 height: 150px;
 background-color: #efb762;
 margin: 20px auto;
 box-shadow: 0 0 3px 3px #efb762;
 border-radius: 9px;
}
```

## Paso 41

Utiliza la propiedad `border-radius` en el selector `.two`, y a los radios superior izquierdo (top-left radius) e inferior derecho (bottom-right radius) dales un valor de `8px` y a los radios superior derecho (top-right radius) e inferior izquierdo (bottom-left radius) dales un valor dé `10px`.

```css
.two {
 width: 475px;
 height: 200px;
 background-color: #8f0401;
 margin: 0 auto 20px;
 box-shadow: 0 0 3px 3px #8f0401;
 border-radius: 8px 10px 8px 10px;
}
```

## Paso 42

La propiedad `border-radius` acepta hasta cuatro valores para redondear las esquinas superior izquierda, superior derecha, inferior derecha e inferior izquierda.

Redondee la esquina superior izquierda de `.three` 30 píxeles, la parte superior derecha 25 píxeles, la parte inferior derecha 60 píxeles y la parte inferior izquierda 12 píxeles.

```css
.three {
 width: 91%;
 height: 28%;
 background-color: #b20403;
 margin: auto;
 filter: blur(2px);
 box-shadow: 0 0 5px 5px #b20403;
 border-radius: 30px 25px 60px 12px;
}
```

## Paso 43

Gire cada rectángulo para darles un aspecto más imperfecto y pintado a mano.

Utilice la propiedad `
` del selector `.one` para `rotate` en sentido contrario a las agujas del reloj en 0,6 grados.

```css
.one {
 width: 425px;
 height: 150px;
 background-color: #efb762;
 margin: 20px auto;
 box-shadow: 0 0 3px 3px #efb762;
 border-radius: 9px;
 transform: rotate(-0.6deg);
}
```

## Paso 44

Gire el elemento `.two` en el sentido de las agujas del reloj en 0,4 grados.

```css
.two {
 width: 475px;
 height: 200px;
 background-color: #8f0401;
 margin: 0 auto 20px;
 box-shadow: 0 0 3px 3px #8f0401;
 border-radius: 8px 10px 8px 10px;
 transform: rotate(0.4deg);
}
```

## Paso 45

Gire `.three` en sentido contrario a las agujas del reloj en 0,2 grados.

Con este paso final, tu pintura de Rothko ha sido completada.

```css
.three {
 width: 91%;
 height: 28%;
 background-color: #b20403;
 margin: auto;
 filter: blur(2px);
 box-shadow: 0 0 5px 5px #b20403;
 border-radius: 30px 25px 60px 12px;
 transform: rotate(-0.2deg);
}
```
