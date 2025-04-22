# Aprende diseno web adaptativo costruyendo un piano

El diseño adaptativo indica a tu página web cómo debe verse en pantallas de distintos tamaños.

En este curso, usarás CSS y Diseño Adaptativo para programar un piano. También aprenderás más sobre las consultas de medios y pseudoselectores.

## Paso 1

Empieza con la estructura básica de HTML. Add a `DOCTYPE` declaration and `html`, `head`, `body`, and `title` elements.

Establezca el idioma de esta página a inglés. Establece el `title` a `Piano`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Piano</title>
</head>
<body>
  
</body>
</html>
```

## Paso 2

Agrega dos etiquetas `meta`, una para optimizar tu página para dispositivos móviles y una para especificar el `charset` aceptado de la página.

```html
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
```

## Paso 3

Es hora de empezar a trabajar en el piano. Create a `div` element within your `body` element with the `id` set to `piano`.

```html
  <div id="piano"></div>
```

## Paso 4

Nest a second `div` within your existing `div`, and set the `class` to be `keys`.

```html
    <div class="keys"></div>
```

## Paso 5

Dentro de tu elemento `.keys`, agrega siete elementos `div`. Dales a todos la clase `key`.

```html
  <div id="piano">
    <div class="keys">
      <div class="key"></div>
      <div class="key"></div>
      <div class="key"></div>
      <div class="key"></div>
      <div class="key"></div>
      <div class="key"></div>
      <div class="key"></div>
    </div>
  </div>
```

## Paso 6

Recuerda que un atributo `class` puede tener varios valores. Para separar tus teclas blancas de tus teclas negras, debes agregar un segundo valor al `class`, el valor es `black--key`. Agrega esto a tu segundo, tercer, quinto, sexto y séptimo elemento `.key`.

```html
  <div id="piano">
    <div class="keys">
      <div class="key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
      <div class="key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
    </div>
  </div>
```

## Paso 7

Ahora copia el conjunto de siete elementos `.key`, y pega otros dos conjuntos en el div `.keys`.

```html
  <div id="piano">
    <div class="keys">
      <div class="key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
      <div class="key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
      
      <div class="key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
      <div class="key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
      
      <div class="key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
      <div class="key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
      <div class="key black--key"></div>
    </div>
  </div>
```

## Paso 8

Agrega un elemento `link` dentro del elemento `head`. Dale un atributo `rel` con el valor `stylesheet` y un atributo `href` con el valor `styles.css`.

```html
    <meta charset="UTF-8" />
    <title>Piano</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="./styles.css">
```

## Paso 9

Los navegadores pueden aplicar valores de margen y relleno por defecto a elementos específicos. Para asegurarte de que tu piano tiene un aspecto correcto, debe reajustar el modelo de caja.

Agrega una regla que tenga el selector `html` a tu archivo CSS y establece la propiedad `box-sizing` en `border-box`.

```css
html {
  box-sizing: border-box;
}
```

## Paso 10

Ahora que has restablecido el modelo de caja del `html`, tienes que pasarlo también a los elementos de su interior. Para ello, puedes establecer la propiedad `box-sizing` en `inherit`, lo que indicará a los elementos apuntados que utilicen el mismo valor que el elemento padre.

También tendrás que apuntar a los pseudo-elementos, que son palabras clave especiales que siguen a un selector. Los dos pseudo-elementos que usaras son `::before` y `::after`.

El selector `::before` crea un pseudo-elemento que es el primer hijo del elemento seleccionado, mientras que el selector `::after` crea un pseudo-elemento que es el último hijo del elemento seleccionado. Estos pseudo-elementos a menudo se usan para crear contenido cosmético, que verás más adelante en este proyecto.

Por ahora, crea un selector CSS para apuntar a todos los elementos con `*`, e incluye los pseudo-elementos con `::before` y `::after`. Establece la propiedad `box-sizing` en `inherit`.

```css
*,
*:before,
*:after {
  box-sizing: inherit;
}
```

## Paso 11

Ahora apunta a tu elemento `#piano` con un selector de `id`. Set `background-color` property to `#00471b`, the `width` property to `992px` and the `height` property to `290px`.

```css
#piano {
  background-color: #00471b;
  width: 992px;
  height: 290px;
}
```

## Paso 12

Set the `margin` of the `#piano` to `80px auto`.

```css
#piano {
  background-color: #00471b;
  width: 992px;
  height: 290px;
  margin: 80px auto;
}
```

## Paso 13

Es hora de estilizar las teclas. Debajo de la regla `#piano`, apunta al elemento `.keys` con un selector de `clase`. Dale a la nueva regla una propiedad `background-color` de `#040404`, una propiedad `width` de `949px` y una propiedad `height` de `180px`.

```css
.keys {
  background-color: #040404;
  width: 949px;
  height: 180px;
}
```

## Paso 14

Give the `.keys` a `padding-left` of `2px`.

```css
.keys {
  background-color: #040404;
  width: 949px;
  height: 180px;
  padding-left: 2px;
}
```

## Paso 15

Mueve las teclas a la posición correcta ajustando el selector `#piano`. Establece la propiedad `padding` a `90px 20px 0 20px`.

```css
#piano {
  background-color: #00471b;
  width: 992px;
  height: 290px;
  margin: 80px auto;
  padding: 90px 20px 0 20px;
}
```

## Paso 16

Es hora de estilizar las teclas en sí. Crea un selector `class` para los elementos `.key`. Set the `background-color` set to the value `#ffffff`, the `position` property to `relative`, the `width` property to `41px`, and the `height` property to `175px`.

```css
.key {
  background-color: #ffffff;
  position: relative;
  width: 41px;
  height: 175px;
}
```

## Paso 17

Give the `.key` a `margin` of `2px` and a `float` property set to `left`.

```css
.key {
  background-color: #ffffff;
  position: relative;
  width: 41px;
  height: 175px;
  margin: 2px;
  float: left;
}
```

## Paso 18

Ahora es el momento de utilizar los pseudo-selectores que has preparado antes. Para crear las teclas negras, agrega un nuevo selector `.key.black--key::after`. Esto apuntará a los elementos con la clase `key black--key`, y seleccionará el pseudo-elemento después de estos elementos en el HTML.

En el nuevo selector, establece el `background-color` en `#1d1e22`. También establece la propiedad `content` en `""`. Esto hará que los pseudo-elementos estén vacíos.

La propiedad `content` se utiliza para establecer o anular el contenido de un elemento. Por defecto, los pseudo-elementos creados por los pseudo-selectores `::before` y `::after` están vacíos, y los elementos no serán renderizados en la página. Establecer la propiedad `content` a una cadena vacía `""` asegurará que el elemento se renderice en la página aunque siga estando vacío.

Si quieres experimentar, prueba eliminando la propiedad `background-color` y a establecer valores diferentes para la propiedad `content`, como `"♥"`. Recuerde deshacer estos cambios cuando haya terminado para que las pruebas pasen.

```css
.key.black--key::after {
  background-color: #1d1e22;
  content: "";
}
```

## Paso 19

Give the `.key.black--key::after` a `position` property set to `absolute` and a `left` property set to `-18px`.

```css
.key.black--key::after {
  background-color: #1d1e22;
  content: "";
  position: absolute;
  left: -18px;
}
```

## Paso 20

For the `.key.black--key::after`, set the `width` to `32px` and the `height` to `100px`.

```css
.key.black--key::after {
  background-color: #1d1e22;
  content: "";
  position: absolute;
  left: -18px;
  width: 32px;
  height: 100px;
}
```

## Paso 21

El piano necesita el logo de freeCodeCamp para hacerlo oficial.

Agrega un elemento `img` antes de tu elemento `.keys`. Dale al `img` un `class` de `logo`, y establece el `src` en `https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg`. Dale un texto `alt` de `freeCodeCamp Logo`.

```html
    <div id="piano">
      <img src="https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg" alt="freeCodeCamp Logo" class="logo">
      <div class="keys">
```

## Paso 22

Empieza a estilizar el logo creando un selector `.logo`. Set the `width` to `200px`, a `position` of `absolute` and a `top` set to `23px`.

```css
.logo {
  width: 200px;
  position: absolute;
  top: 23px;
}
```

## Paso 23

El elemento `img` necesita que su elemento padre tenga un `position` establecido como un punto de referencia. Set the `position` of the `#piano` selector to `relative`.

```css
#piano {
  background-color: #00471b;
  width: 992px;
  height: 290px;
  margin: 80px auto;
  padding: 90px 20px 0 20px;
 position: relative;
}
```

## Paso 24

Para suavizar los bordes afilados del piano y las teclas, empieza dando al `#piano` un `border-radius` de `10px`.

```css
#piano {
  background-color: #00471b;
  width: 992px;
  height: 290px;
  margin: 80px auto;
  padding: 90px 20px 0 20px;
  position: relative;
 border-radius: 10px;
}
```

## Paso 25

Dale al selector `.key` un valor `border-radius` de `0 0 3px 3px`.

```css
.key {
  background-color: #ffffff;
  position: relative;
  width: 41px;
  height: 175px;
  margin: 2px;
  float: left;
 border-radius: 0 0 3px 3px;
}
```

## Paso 26

Dale al selector `.key.black--key::after` un `border-radius` de `0 0 3px 3px` para que coincida con las teclas.

```css
.key.black--key::after {
  background-color: #1d1e22;
  content: "";
  position: absolute;
  left: -18px;
  width: 32px;
  height: 100px;
 border-radius: 0 0 3px 3px;
}
```

## Paso 27

La regla-at (declaración CSS que comienza con el símbolo arroba) `@media`, también conocida como media query, se utiliza para aplicar CSS de forma condicional. Las media queries se utilizan comúnmente para aplicar CSS basado en el ancho del viewport utilizando las propiedades `max-width` y `min-width`.

En el siguiente ejemplo, el relleno se aplica a la clase `.card` cuando el viewport tiene un ancho de `960px` o inferior.

- **CODIGO DE EJEMPLO**
  
  ```css
  @media (max-width: 960px) {
    .card {
      padding: 2rem;
    }

  }
  ```

Agrega una media query que se aplicará cuando el viewport tenga `768px` de ancho o menos.

```css
@media (max-width: 768px) {
  
}
```

## Paso 28

Agrega un nuevo selector `#piano` dentro de tu `@media` query, y establece el `width` en `358px`.

```css
@media (max-width: 768px) {
  #piano {
  width: 358px;
 }
}
```

## Paso 29

Within the `@media` query, add a `.keys` selector and set the `width` to `318px`.

```css
@media (max-width: 768px) {
  #piano {
    width: 358px;
  }

  .keys {
  width: 318px;
 }
}
```

## Paso 30

Now add a `.logo` selector to the `@media` query, and set the `width` property to `150px`.

```css
@media (max-width: 768px) {
  #piano {
    width: 358px;
  }

  .keys {
    width: 318px;
  }

  .logo {
  width: 150px;
 }
}
```

## Paso 31

Puede que hayas notado que las teclas se colapsan cuando la ventana del navegador es menor de `768px`. Establece el `overflow` a `hidden` en el primer selector `.keys`, para solucionar este problema. Esta propiedad ocultará cualquier elemento que sea empujado fuera del valor del `width` establecido en el `.keys`.

```css
.keys {
  background-color: #040404;
  width: 949px;
  height: 180px;
  padding-left: 2px;
  overflow: hidden;
}
```

## Paso 32

Es posible aumentar la complejidad de las media queries usando operadores lógicos. El operador lógico `and` es utilizado para combinar en una sola consulta dos características de medios.

Por ejemplo, una media query cuyo objetivo es una anchura de pantalla entre 500px y 1000px podría ser:

- **CODIGO DE EJEMPMPLO**

  ```css
  @media (min-width: 500px) and (max-width: 1000px){

  }
  ```

Añade otra regla `@media` que se aplique si la pantalla del navegador tiene una anchura mayor que `769px` pero menor que `1199px`.

```css
@media (min-width: 769px) and (max-width: 1199px) {
  
}
```

## Paso 33

For the new `@media` rule, set the width of the `#piano` to `675px` and the `width` of the `.keys` to `633px`.

>[!NOTE]
>
>**Con esto, ¡tu piano está completo!**

```css
@media (max-width: 1199px) and (min-width: 769px) {
  #piano {
   width: 675px;
 }

 .keys {
   width: 633px;
 }
}
```
