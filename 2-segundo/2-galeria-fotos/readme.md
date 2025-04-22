# Aprende CSS Flexbox constuyendo una galeria de fotos

Flexbox te ayuda a diseñar tu página web para que se vea bien en cualquier tamaño de pantalla.

En este curso, usarás Flexbox para crear una página web de una galería de fotos adaptativa.

## Paso 1

Comience con su plantilla HTML estándar. Añade una declaración `DOCTYPE`, un elemento `html`, un elemento `head` y un elemento `body`.

Añade el atributo `lang` a la etiqueta `<html>` de apertura con el valor `en`.

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

Dentro de tu elemento `head`, agrega una etiqueta `meta` con el `name` establecido en `viewport` y el `content` establecido en `width=device-width, initial-scale=1`.

También añade una etiqueta `meta` y a `charset` dale el valor `UTF-8`.

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

## Paso 3

Dentro de tu elemento `head`, agrega un elemento `title` con el texto establecido en `Photo Gallery`, y un elemento `link` para agregar tu archivo `styles.css` a la página.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Photo Gallery</title>
  <link rel="stylesheet" href="styles.css">
  </head>
  <body>
  </body>
</html>
```

## Paso 4

Añade un elemento `header` dentro del elemento `body` y asígnale la clase `header`.

Dentro del `header`, crea un `h1` que tenga el texto `css flexbox photo gallery`.

```html
<!DOCTYPE html>
<html>

<head lang="en">
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Photo Gallery</title>
  <link rel="stylesheet" href="./styles.css">
</head>

<body>
  <header class="header">
    <h1>
      css flexbox photo gallery
    </h1>
  </header>
</body>

</html>
```

## Paso 5

Debajo de tu elemento `.header`, crea un nuevo elemento `div` y asígnale una `class` de `gallery`. Este `div` actuará como contenedor de las imágenes de la galería.

Dentro de ese elemento `.gallery`, crea nueve elementos `img`.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Photo Gallery</title>
    <link rel="stylesheet" href="./styles.css">
  </head>
  <body>
    <header class="header">
      <h1>css flexbox photo gallery</h1>
    </header>
      <div class="gallery">
    <img src="" alt="">
    <img src="" alt="">
    <img src="" alt="">
    <img src="" alt="">
    <img src="" alt="">
    <img src="" alt="">
    <img src="" alt="">
    <img src="" alt="">
    <img src="" alt="">
  </div>
  </body>
</html>
```

## Paso 6

A continuación, dale a cada img un atributo src de acuerdo con su orden en el documento. El primer `img` debe tener un atributo `src` con el valor `<https://cdn.freecodecamp.org/curriculum/css-photo-gallery/1.jpg>`. El resto debe ser igual, excepto que hay que sustituir el `1` por el número en el que se encuentra el `img` en el documento.

```html
    <div class="gallery">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/1.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/2.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/3.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/4.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/5.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/6.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/7.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/8.jpg">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/9.jpg">
    </div>
```

## Paso 7

Para visualizar mejor el tamaño de los elementos, puede ser útil añadir un borde.

Dale al elemento `.gallery` un `width` de `50%` y un `border` de `5px solid red`.

Luego da a tus elementos `img` un `width` de `100%`, un `padding` de `5px` y un `border` de `5px solid blue`.

```css
.gallery {
 width: 50%;
 padding: 5px;
 border: 5px solid red;
}

img {
  width: 100%;
  padding: 5px;
  border: 5px solid blue;
}
```

## Paso 8

Observa cómo los bordes azules de la imagen se extienden más allá del borde rojo de la galería. Esto se debe a la forma en que los navegadores calculan el tamaño de los elementos contenedores.

La propiedad `box-sizing` se utiliza para establecer este comportamiento. Por defecto, se utiliza el modelo `content-box`. Con este modelo, cuando un elemento tiene un ancho específico, esa anchura se calcula únicamente basándose en el contenido del elemento. Los valores de relleno (padding) y borde (border) se añaden al ancho total, por lo que el elemento crece para acpplarse a estos valores.

Intenta configurar `box-sizing` con el valor `content-box` explícitamente, en el selector global `*`. Por ahora, no verás ningún cambio, porque está utilizando el valor por defecto.

```css
* {
  box-sizing: content-box;
}
```

## Paso 9

El modelo de tamaño `border-box` hace lo contrario que `content-box`. El ancho total del elemento, incluido el relleno (padding) y el borde (border), será el ancho establecido explícitamente. El contenido del elemento se reducirá para hacer espacio para el relleno (padding) y al borde (border).

Cambia la propiedad `box-sizing` a `border-box`. Observa cómo tus bordes azules de la imagen ahora encajan dentro de su borde rojo de la galería.

```css
 * {
  box-sizing: border-box;
}
```

## Paso 10

Ahora que has entendido el enfoque de tu `box-sizing`, puedes vaciar el CSS que añadiste para ver los cambios.

Elimina tus selectores `.gallery` y `img` y todas las reglas que llevan dentro.

- **SE ELIMINA EL CODIGO**

## Paso 11

Ahora tus imágenes son demasiado grandes.

Crea un selector `.gallery img` para seleccionarlas. Dales a todas un (ancho) `width` de `100%` y un (ancho máximo) `max-width` dé `350px`.

También establece la propiedad `height` a `300px` para mantener las imágenes en un tamaño uniforme.

```css
.gallery img {
 width: 100%;
 max-width: 350px;
 height: 300px;
}

```

## Paso 12

Elimina el margen de tu elemento body, a `font-family` dale el valor `sans-serif`, y agrega un `background-color` con el valor `#f5f6f7`.

```css
body {
  margin: 0;
  font-family: sans-serif;
  background-color: #f5f6f7;
}
```

## Paso 13

Alinea tu texto `.header` en el centro. Pone el texto en mayúsculas usando la propiedad `text-transform` con `uppercase` como valor.

Dale un relleno de `32px` en todos los lados. Establece el fondo en `#0a0a23` y el texto en `#fff` como valores de color.

Añade un `border-bottom` con `4px solid #fdb347` como valor.

```css
.header {
  text-align: center;
  text-transform: uppercase;
  padding: 32px;
  background-color: #0a0a23;
  color: #fff;
  border-bottom: 4px solid#fdb347;
}
```

## Paso 14

Flexbox es un diseño CSS unidimensional que puede controlar la forma en que los elementos se espacian y alinean dentro de un contenedor.

Para utilizarlo, dale a un elemento una propiedad `display` con el valor `flex`. Esto hará que el elemento sea un flex container (contenedor flexible). Todos los hijos directos de un contenedor flex se llaman flex items (elementos flex).

Crea un selector `.gallery` y conviértelo en un contenedor flex.

```css
.gallery {
  display: flex;
}
```

## Paso 15

Flexbox tiene un eje principal y otro transversal. El eje principal está definido por la propiedad `flex-direction`, que tiene cuatro valores posibles:

- `row` (por defecto): eje horizontal con elementos flex de izquierda a derecha
- `row-reverse`: eje horizontal con elementos flex de derecha a izquierda
- `column`: eje vertical con elementos flexibles de arriba a abajo
- `column-reverse`: eje vertical con elementos flexibles de abajo a arriba

>[!NOTE]
>
>Los ejes y direcciones serán diferentes dependiendo de la dirección del texto. Los valores mostrados son para una dirección de texto de izquierda a derecha.

Pruebe los diferentes valores para ver como afectan al diseño.

Cuando hayas terminado, establece un `flex-direction` explícito de `row` en el elemento `.gallery`.

```css
.gallery {
  display: flex;
  flex-direction: row;
}
```

## Paso 16

La propiedad `flex-wrap` determina como se comportan tus elementos flex cuando el contenedor flex es demasiado pequeño. Si se establece como `wrap`, los elementos se colocan en la siguiente fila o columna. `nowrap` (por defecto) evitará que los elementos se coloquen en varias líneas y los encogerá si es necesario.

Haga que sus elementos flexibles se coloquen en la siguiente fila cuando se queden sin espacio.

```css
.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
```

## Paso 17

La propiedad `justify-content` determina cómo se posicionan los elementos dentro de un contenedor flex a lo largo del eje principal, afectando a su posición y al espacio que los rodea.

Dale a tu selector `.gallery` una propiedad `justify-content` con el valor `center`.

```css
.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
```

## Paso 18

La propiedad `align-items` posiciona el contenido flex a lo largo del eje transversal. En este caso, con tu `flex-direction` establecido en `row`, el eje transversal sería vertical.

Para centrar verticalmente tus imágenes, dale a tu selector `.gallery` una propiedad `align-items` con el valor `center`.

```css
.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
 align-items: center;
}
```

## Paso 19

Dale a tu selector `.gallery` una propiedad `padding` establecida en `20px 10px` para crear algo de espacio alrededor del contenedor.

Luego, dale un `max-width` de `1400px` y añade un margin de `0 auto` para centrarlo.

```css
.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  padding: 20px 10px;
 max-width: 1400px;
 margin: 0 auto;
}
```

## Paso 20

Observe como algunas de sus imágenes se han distorsionado. Esto se debe a que las imágenes tienen diferentes relaciones de aspecto. En lugar de establecer cada relación de aspecto individualmente, puedes utilizar la propiedad `object-fit` para determinar como deben comportarse las imágenes.

Dale a tu selector `.gallery img` la propiedad `object-fit` establecida en `cover`. Esto le dirá a la imagen que llene el contenedor `img` mientras mantiene la relación de aspecto, lo que resulta en un recorte para ajustarse.

```css
.gallery img {
  width: 100%;
  max-width: 350px;
  height: 300px;
  object-fit: cover;
}
```

## Paso 21

Tus imágenes necesitan algo de espacio entre ellas.

La propiedad abreviada CSS `gap` especifica los espacios, también conocidos como canales, entre filas y columnas. La propiedad `gap` y sus subpropiedades `row-gap` y `column-gap` proporcionan esta funcionalidad para los diseños flex, grid, y multicolumna. La propiedad se aplica al elemento contenedor.

Dale a tu contenedor flex `.gallery` una propiedad `gap` con un valor de `16px`.

```css
.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  max-width: 1400px;
  margin: 0 auto;
  padding: 20px 10px;
 gap: 16px;
}
```

## Paso 22

Suaviza un poco tus imágenes dándole al selector `.gallery img` la propiedad `border-radius` con un valor de `10px`.

```css
.gallery img {
  width: 100%;
  max-width: 350px;
  height: 300px;
  object-fit: cover;
  border-radius: 10px;
}
```

## Paso 23

El pseudo-elemento `::after` crea un elemento que es el último hijo del elemento seleccionado. Puedes hacer uso de él para añadir un elemento vacío a continuación de la ultima imagen. Si en su propiedad `width` se le asigna el mismo valor que tiene en las imágenes, empujará la última imagen hacia la izquierda cuando la galería tenga un diseño de dos columnas. En este momento, está en el centro porque se ha establecido `justify-content: center` en el contenedor flex.

- EJEMPLO

  ```css
  .container::after {
    content: "";
    width: 860px;
  }
  ```

Cree un nuevo selector utilizando un pseudo-elemento `::after` en el elemento `.gallery`. Añade una propiedad `content` establecida a una cadena vacía `""` y `350px` establecidos para la propiedad `width`.

```css
.gallery::after {
 content: "";
 width: 350px;
}
```

## Paso 24

El atributo de imagen alt debe describir el contenido de la imagen. Los lectores de pantalla leen el texto alternativo en lugar de las imágenes. Si la imagen no puede ser cargada, se muestra el texto en lugar de la imagen.

Para completar el proyecto, añade un atributo alt a las nueve imágenes de tus gatos para describirlas. Utiliza un valor de al menos 5 caracteres de longitud para cada uno.

```html
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/1.jpg" alt="cats1">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/2.jpg" alt="cats2">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/3.jpg" alt="cats3">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/4.jpg" alt="cats4">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/5.jpg" alt="cats5">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/6.jpg" alt="cats6">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/7.jpg" alt="cats7">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/8.jpg" alt="cats8">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/9.jpg" alt="cats9">
```
