# Aprende tipografia construllendo una etiqueta de nutricion

La tipografía es el arte de diseñar tu texto haciéndolo de fácil lectura y adaptado a su propósito.

En este curso, usarás tipografía para compilar una página web de etiqueta. Aprenderás cómo estilizar el texto, ajustar altura de línea y la posición de tu texto usando CSS.

## Paso 1

Hemos proporcionado una plantilla HTML básica para usted.

Cree un elemento `h1` dentro de su elemento `body` y asígnele el texto `Nutrition Facts`.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Nutrition Label</title>
</head>

<body>
  <h1>Nutrition Facts</h1>
</body>
</html>
```

## Paso 2

Debajo del elemento `h1`, agregue un elemento `p` con el texto `8 servings per container`.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Nutrition Label</title>
</head>

<body>
  <h1>Nutrition Facts</h1>
  <p>8 servings per container</p>
</body>
</html>
```

## Paso 3

Agregue un segundo elemento `p` con el texto `Serving size 2/3 cup (55g)`.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Nutrition Label</title>
</head>

<body>
  <h1>Nutrition Facts</h1>
  <p>8 servings per container</p>
  <p>Serving size 2/3 cup (55g)</p>
</body>

</html>
```

## Paso 4

Dentro de su elemento `head`, agregue un elemento `link` con el atributo `rel` establecido en `stylesheet` y el `href` Atributo establecido en `<https://fonts.googleapis.com/css?family=Open+Sans:400,700,800>`.

Esto importará la familia de fuentes `Open Sans`, con los valores de peso de fuente `400`, `700` y `800`.

También agregue un elemento `link` para vincular su archivo `styles.css`.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Nutrition Label</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open+Sans:400,700,800">
  <link rel="stylesheet" href="styles.css">
</head>

<body>
  <h1>Nutrition Facts</h1>
  <p>8 servings per container</p>
  <p>Serving size 2/3 cup (55g)</p>
</body>

</html>
```

## Paso 5

Cree un selector `body` y asígnele una `font-family` establecida en `Open Sans` con un respaldo de `sans-serif`.

Recuerda que las fuentes con espacios en el nombre deben estar entre comillas para CSS.

```css
body {
  font-family: Open Sans, sans-serif;
}
```

## Paso 6

La fuente es un poco pequeña. Crea un selector `html` y configura la fuente para que tenga un tamaño de `16px`.

```css
html {
 font-size: 16px;
}
```

## Paso 7

Wrap your `h1` and `p` elements in a `div` element. Give that `div` a `class` attribute set to `label`.

```html
<body>
  <div class="label">
    <h1>Nutrition Facts</h1>
    <p>8 servings per container</p>
    <p>Serving size 2/3 cup (55g)</p>
  </div>
</body>
```

## Paso 8

Los bordes se pueden usar para agrupar y priorizar contenido.

Cree un selector `.label` y asígnele un `border` establecido en `2px solid black`.

```css
.label {
  border: 2px solid black;
}
```

## Paso 9

El buen uso del espacio en blanco puede enfocar los elementos importantes de su página y ayudar a guiar la vista de su usuario a través de su texto.

Dale a tu selector `.label` una propiedad `width` establecida en `270px`.

```css
.label {
  border: 2px solid black;
  width: 270px;
}
```

## Paso 10

Dale a tu selector `.label` una propiedad `margin` establecida en `20px auto`, y una propiedad `padding` establecida en `0 7px`.

```css
.label {
  border: 2px solid black;
  width: 270px;
  margin: 20px auto;
 padding: 0 7px;
}
```

## Paso 11

Si inspecciona su elemento `.label` con las herramientas de desarrollo de su navegador, puede notar que en realidad tiene 288 píxeles de ancho en lugar de 270. Esto se debe a que, de forma predeterminada, el navegador incluye el borde y el relleno al determinar el tamaño de un elemento.

Para resolver esto, restablezca el modelo de caja creando un selector `*` y dándole una propiedad `box-sizing` de `border-box`.

```css
* {
  box-sizing: border-box;
}
```

## Paso 12

Recuerde que el uso de `h1`, `h2` y etiquetas similares determinan la estructura semántica de su HTML. Sin embargo, puede ajustar el CSS de estos elementos para controlar el flujo visual y la jerarquía.

Cree una regla `h1` y establezca la propiedad `font-weight` en `800`. Esto hará que su texto `h1` sea más audaz.

```css
h1 {
  font-weight: 800;
}
```

## Paso 13

Asigne al selector `h1` una propiedad `text-align` de `center`.

```css
h1 {
  font-weight: 800;
  text-align: center;
}
```

## Paso 14

Ajuste la ubicación de su `h1` dándole un margen superior e inferior de `-4px` y un margen izquierdo y derecho de `0`.

```css
h1 {
  font-weight: 800;
  text-align: center;
  margin: -4px 0;
}
```

## Paso 15

Crea un selector de `p` y elimina todos los margenes.

```css
p {
 margin: 0;
}
```

## Paso 16

Las líneas pueden ayudar a separar y agrupar contenido importante, especialmente cuando el espacio es limitado.

Cree un elemento `div` debajo de su elemento `h1` y asígnele un atributo `class` establecido en `divider`.

```html
  <div class="label">
    <h1>Nutrition Facts</h1>
    <div class="divider"></div>
    <p>8 servings per container</p>
    <p>Serving size 2/3 cup (55g)</p>
  </div>
```

## Paso 17

Cree un selector para su nuevo `.divider` y establezca la propiedad `border-bottom` en `1px solid #888989`. También déle un margen superior e inferior de `2px`. No debe tener ningún margen izquierdo o derecho.

```css
.divider {
  border-bottom: 1px solid #888989;
  margin: 2px 0;
}
```

## Paso 18

La propiedad `letter-spacing` se puede usar para ajustar el espacio entre cada carácter de texto en un elemento.

Dale a tu selector `h1` una propiedad `letter-spacing` establecida en `0.15px` para espaciarlas un poco más.

```css
h1 {
  font-weight: 800;
  text-align: center;
  margin: -4px 0;
  letter-spacing: 0.15px;
}
```

## Paso 19

Las etiquetas de nutrición tienen mucho texto en negrita para llamar la atención sobre información importante. En lugar de apuntar a cada elemento que debe estar en negrita, es más eficiente usar una clase para aplicar el estilo en negrita a cada elemento.

Dale a tu segundo elemento `p` un atributo `class` establecido en `bold`.

```html
  <div class="label">
    <h1>Nutrition Facts</h1>
    <div class="divider"></div>
    <p>8 servings per container</p>
    <p class="bold">Serving size 2/3 cup (55g)</p>
  </div>
```

## Paso 20

Su nueva clase aún no tiene ningún estilo. Cree un selector `.bold` y asígnele una propiedad `font-weight` establecida en `800` para poner el texto en negrita.

Continúe y elimine la propiedad `font-weight` de su selector `h1` también.

```css
h1 {
  text-align: center;
  margin: -4px 0;
  letter-spacing: 0.15px;
}

p {
  margin: 0;
}

.divider {
  border-bottom: 1px solid #888989;
  margin: 2px 0;
}

.bold {
  font-weight: 800;
}
```

## Paso 21

Give your `h1` element a `class` attribute set to `bold`. Esto hará que el texto vuelva a negrita.

```html
  <div class="label">
    <h1 class="bold">Nutrition Facts</h1>
    <div class="divider"></div>
    <p>8 servings per container</p>
    <p class="bold">Serving size 2/3 cup (55g)</p>
  </div>
```

## Paso 22

El espaciado horizontal entre elementos igualmente importantes puede aumentar la legibilidad de su texto.

Envuelve el texto `2/3 cup (55g)` en un elemento `span`.

```html
  <div class="label">
    <h1 class="bold">Nutrition Facts</h1>
    <div class="divider"></div>
    <p>8 servings per container</p>
    <p class="bold">Serving size <span>2/3 cup (55g)</span></p>
  </div>
```

## Paso 23

Ahora podemos añadir el espaciado horizontal usando `flex`. In your `p` selector, add a `display` property set to `flex` and a `justify-content` property set to `space-between`.

```css
p {
  margin: 0;
  display: flex;
  justify-content: space-between;
}
```

## Paso 24

Envuelva todo dentro del elemento `.label` en un nuevo elemento `header`.

```html
  <div class="label">
    <header>
      <h1 class="bold">Nutrition Facts</h1>
      <div class="divider"></div>
      <p>8 servings per container</p>
      <p class="bold">Serving size <span>2/3 cup (55g)</span></p>
    </header>
  </div>
```

## Paso 25

Ahora actualice su selector `h1` para que sea `header h1` para apuntar específicamente a su elemento `h1` dentro de su nuevo `header`.

```css
header h1 {
  text-align: center;
  margin: -4px 0;
  letter-spacing: 0.15px
}
```

## Paso 26

Crea un nuevo elemento `div` debajo del elemento `header`, estableciendo su atributo `class` con el valor `divider large`.

```html
<div class="divider large"></div>
```

## Paso 27

Cree un nuevo selector `.large` y asígnele una propiedad `height` establecida en `10px`. También cree un selector `.large, .medium` y establezca la propiedad `background-color` en `black`.

```css
.large {
  height: 10px;
}

.large, .medium {
  background-color: black;
}
```

## Paso 28

Puede notar que todavía hay un pequeño borde en la parte inferior de su elemento `.large`. Para restablecer esto, asigne a su selector `.large, .medium` una propiedad `border` establecida en `0`.

>[!NOTE]
>
>la clase `medium`(medio) será utilizada mas tarde para las barras más delgadas de la etiqueta de nutrición.

```css
.large, .medium {
  background-color: black;
  border: 0;
}
```

## Paso 29

Create a new `div` below your `.large` element and give it a `class` attribute set to `calories-info`.

```html
    <div class="calories-info"></div>
```

## Paso 30

Dentro de su elemento `.calories-info`, cree un elemento `div`. Give that `div` element a `class` attribute set to `left-container`. Within the newly created `div` element, create an `h2` element with the text `Amount per serving`. Asigne al elemento `h2` un atributo `class` establecido en bold `small-text`.

```html
    <div class="calories-info">
      <div class="left-container">
        <h2 class="bold small-text">Amount per serving</h2>
      </div>
    </div>
```

## Paso 31

La unidad `rem` significa `root em`, y es relativa al tamaño de fuente del elemento `html`.

Crea un selector `.small-text` y establezca el `font-size` a 0.`85rem`, que calcularía aproximadamente `13.6px` (recuerde que configuró su `html` para tener un `font-size` de `16px`).

```css
.small-text {
  font-size: 0.85rem;
}
```

## Paso 32

Crea el selector `.calories-info h2` y elimina todos los márgenes.

```css
.calories-info h2 {
 margin: 0;
}
```

## Paso 33

Debajo de su elemento `.small-text`, cree un nuevo elemento `p` con el texto `Calories`. Debajo de su elemento `.left-container`, cree un nuevo elemento `span` con el texto `230`.

```html
    <div class="calories-info">
      <div class="left-container">
        <h2 class="bold small-text">Amount per serving</h2>
        <p>Calories</p>
      </div>
      <span>230</span>
    </div>
```

## Paso 34

Crea un nuevo selector `.calories-info` y dale una propiedad `display` establecida a `flex`. También dale una propiedad `justify-content` establecida en `space-between` y una propiedad `align-items` establecida en `flex-end`.

```css
.calories-info {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
}
```

## Paso 35

Cree un nuevo selector `.left-container p` configurando el margen superior e inferior en `-5px`, y el margen izquierdo y derecho en `-2px`. Also set the `font-size` to `2em` and `font-weight` to `700`.

```css
.left-container p {
 margin: -5px -2px;
 font-size: 2em;
 font-weight: 700;
}
```

## Paso 36

Crea un selector `.calories-info span`, establece su `font-size` a `2.4em` y `font-weight` a `700`.

```css
.calories-info span {
  font-size: 2.4em;
  font-weight: 700;
}
```

## Paso 37

La tipografía es a menudo más arte que ciencia. Es posible que deba ajustar cosas como la alineación hasta que se vea correcta.

En el selector `.calories-info span`, establece `margin` con el valor `-7px -2px`. Esto cambiará su texto `230` a su lugar.

```css
.calories-info span {
  font-size: 2.4em;
  font-weight: 700;
  margin: -7px -2px;
}
```

## Paso 38

Below your `.calories-info` element, add a `div` with the `class` attribute set to `divider medium`.

```html
    <div class="divider medium"></div>
```

## Paso 39

Cree un selector `.medium` y asígnele una propiedad `height` de `5px`.

```css
.medium {
  height: 5px;
}
```

## Paso 40

Cree un nuevo elemento `div` debajo de su elemento `.medium`. Asígnele un atributo `class` establecido en `daily-value small-text`. Within this new `div`, add a `p` element with the text `% Daily Value *`, and set the `class` attribute to `bold right`.

```html
    <div class="divider medium"></div>
    <div class="daily-value small-text">
      <p class="bold right">% Daily Value *</p>
    </div>
```

## Paso 41

El texto `% Daily Value *` debe estar alineado a la derecha. Crea un selector `.right` y usa la propiedad `justify-content` para hacerlo.

```css
.right {
  justify-content: flex-end;
}
```

## Paso 42

Use su elemento `.divider` existente como ejemplo para agregar un nuevo divisor después del elemento `p`.

```html
<p class="bold right">% Daily Value *</p>
<div class="divider medium"></div>
```

## Paso 43

Después de su último elemento `.divider`, cree un elemento `p` y asígnele el texto `Total Fat 8g 10%`. Después, envuelve el texto `Total Fat` en un elemento `span`, el texto `10%` en otro, y dales a cada uno una clase de `bold`.

```html
     <div class="daily-value small-text">
      <p class="bold right">% Daily Value *</p>
      <div class="divider"></div>
      <p><span class="bold">Total Fat</span> 8g <span class="bold">10%</span></p>
    </div>
```

## Paso 44

Observa cómo el texto `8g` aparece centrado en la vista previa. Anida el elemento `span` que contiene el texto `Total Fat` junto con el texto `8g`, en un elemento `span` adicional para alinearlo.

```html
<p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
```

## Paso 45

Debajo de su elemento con el texto `Total Fat`, cree un nuevo elemento `p` con el texto `Saturated Fat 1g` 5%. Wrap the `5%` in a `span` with the `class` attribute set to `bold`. En este caso, esto es suficiente para alinear el porcentaje al `5%`.

```html
    <div class="daily-value small-text">
      <p class="bold right">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p>Saturated Fat 1g <span class="bold">5%</span></p>
    </div>
```

## Paso 46

Este nuevo elemento `p` debe indentado. Give it a `class` set to `indent`.

```html
    <div class="daily-value small-text">
      <p class="bold right">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent">Saturated Fat 1g <span class="bold">5%</span></p>
    </div>
```

## Paso 47

Cree un nuevo selector `.indent` y asígnele una propiedad `margin-left` establecida en `1em`.

```css
.indent {
  margin-left: 1em;
}
```

## Paso 48

Cree un selector `.daily-value p` para orientar todos sus elementos `p` en la sección `daily-value`. Dale a este nuevo selector un `border-bottom` establecido en `1px solid #888989`.

```css
.daily-value p {
  border-bottom: 1px solid #888989;
}
```

## Paso 49

Los bordes inferiores debajo de los elementos `% Daily Value *` y `Saturated Fat 1g 5%` no se extienden por todo el ancho de la etiqueta. Agrega `no-divider` a la `class` para estos dos elementos.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
    </div>
```

## Paso 50

El pseudo-selector `:not` se puede utilizar para seleccionar todos los elementos que no coincidan con la regla CSS dada.

- EJEMPLO
  
  ```css
  div:not(#example) {
  color: red;
  }
  ```

Lo anterior selecciona todos los elementos `div` sin un `id` de `example`.

Modifique su selector `.daily-value p` para excluir los elementos `.no-divider`.

```css
.daily-value p:not(.no-divider) {
  border-bottom: 1px solid #888989;
}
```

## Paso 51

Ahora tendrá que agregar divisores separados debajo de sus elementos `.no-divider`.

Su primer elemento `.no-divider` tiene un `.divider` después de él. Cree otro `.divider` después de su segundo elemento `.no-divider`.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
    </div>    
```

## Paso 52

Después de su último `.divider`, cree otro elemento `p` con el texto `Trans Fat 0g`. Ponga en cursiva la palabra `Trans` envolviéndola en un elemento `i`. Asigne al nuevo elemento `p` el atributo `class` establecido en `indent no-divider`. Envolver `Trans Fat 0g` en un elemento `span` para alineamiento.Z

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
    </div>  
```

## Paso 53

Crea otro `.divider` después de tu último elemento `p`.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
    </div>   
```

## Paso 54

Después de su último `.divider`, cree un nuevo elemento `p` con el texto `Cholesterol 0mg 0%`. Después, envuelve el texto `Cholesterol` en un elemento `span`, `0%` en otro, y dale a cada uno de ellos una clase de `bold`.

Por último, anida el elemento `span` que contiene el texto `Cholesterol` junto con el texto `0mg`, en un elemento `span` adicional para la alineación.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
    </div> 
```

## Paso 55

Debajo de su último elemento `p`, cree otro elemento `p` con el texto `Sodium 160mg 7%`. Pon `Sodium` y `7%` cada uno en su propio `span` con una clase de una `bold` como hiciste con los otros.

Después, añada un elemento `span` alrededor de `Sodium 160mg` para la alineación de nuevo.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
    </div>    
```

## Paso 56

Debajo de su último elemento `p`, agregue otro elemento `p` con el texto `Total Carbohydrate 37g 13%`. Al igual que antes, utilice los elementos `span` para hacer que el texto `Total Carbohydrate` esté en negrita y que el texto `13%` esté en negrita y alineado a la derecha. Después, envolver el nutriente y la cantidad en un `span` para la alineación de nuevo.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
    </div>    
```

## Paso 57

Debajo de su último elemento `p`, agregue otro elemento `p` con el texto `Dietary Fiber 4g`. Dale al elemento `p` la `class` necesaria para sangrar y eliminar el borde divisorio. Luego crea un divisor debajo de ese elemento `p`.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
    </div>  
```

## Paso 58

Cree otro elemento `p` después de su último `.divider` y asígnele el texto `Total Sugars 12g`. Asigne a ese elemento `p` los valores de `class` necesarios para sangrar y eliminar el borde inferior. Luego crea otro `.divider` debajo de tu nuevo elemento `p`.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider"></div>
    </div>
```

## Paso 59

La ventaja de crear estos divisores es que puede aplicar clases específicas para diseñarlos individualmente. Add `double-indent` to the `class` for your last `.divider`.

```html
<div class="divider double-indent"></div>
```

## Paso 60

Crea un selector `.double-indent` y dale un margen izquierdo de `2em`.

```css
.double-indent {
  margin-left: 2em;
}
```

## Paso 61

Debajo de su elemento `.double-indent`, agregue un nuevo elemento p con el texto `Includes 10g Added Sugars 20%`. Su nuevo elemento `p` también debe tener doble sangría y no tener un borde inferior. Usa un `span` para hacer que el `20%` esté en negrita y alineado a la derecha.

Luego crea otro divisor después de ese elemento `p`.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider double-indent"></div>
      <p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold">20%</span></p>
      <div class="divider"></div>
    </div>
```

## Paso 62

Después de su último divisor, cree otro elemento `p` con el texto `Protein 3g`. Use las clases necesarias para eliminar el borde inferior y un `span` para poner la `Protein` en negrita. Luego envuelve el texto `Protein 3g`, incluyendo el nuevo elemento `span`, en un nuevo elemento `span`.

Siguiendo este elemento, cree un gran divisor.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider double-indent"></div>
      <p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold">20%</span></p>
      <div class="divider"></div>
      <p class="no-divider"><span><span class="bold">Protein</span> 3g</span></p>
    <div class="divider large"></div>
    </div>
```

## Paso 63

Crea otro elemento `p` debajo de tu divisor grande. Asigne al elemento `p` el texto `Vitamin D 2mcg 10%`.

El elemento `p` solo contiene texto, se puede envolver el porcentaje en un elemento `span` para que se considere una entidad separada del resto del texto, y se mueve a la derecha.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider double-indent"></div>
      <p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold">20%</span></p>
      <div class="divider"></div>
      <p class="no-divider"><span><span class="bold">Protein</span> 3g</span></p>
      <div class="divider large"></div>
      <p>Vitamin D 2mcg <span>10%</span></p>
    </div>
```

## Paso 64

Cree otro elemento `p`, asígnele el texto `Calcium 260mg 20%`. Alinea `20%` a la derecha. Debajo de eso, cree un elemento `p` con el texto `Iron 8mg 45%`, alineando el `45%` a la derecha.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider double-indent"></div>
      <p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold">20%</span></p>
      <div class="divider"></div>
      <p class="no-divider"><span><span class="bold">Protein</span> 3g</span></p>
      <div class="divider large"></div>
      <p>Vitamin D 2mcg <span>10%</span></p>
      <p>Calcium 260mg <span>20%</span></p>
      <p>Iron 8mg <span>45%</span></p>
    </div>
```

## Paso 65

Cree el elemento final `p` para su sección `.daily-value`. Dale el texto `Potassium 235mg 6%`. Alinee el texto `6%` a la derecha y elimine el borde inferior del elemento `p`.

```html
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider double-indent"></div>
      <p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold">20%</span></p>
      <div class="divider"></div>
      <p class="no-divider"><span><span class="bold">Protein</span> 3g</span></p>
      <div class="divider large"></div>
      <p>Vitamin D 2mcg <span>10%</span></p>
      <p>Calcium 260mg <span>20%</span></p>
      <p>Iron 8mg <span>45%</span></p>
      <p class="no-divider">Potassium 235mg <span>6%</span></p>
    </div>
```

## Paso 66

Agrega un divisor mediano después de su elemento `.daily-value`. Debajo de ese nuevo divisor, cree un elemento `p` con el atributo `class` establecido en `note`.

Dale al elemento `p` el siguiente texto:

- EJEMPLO
  
  ```txt
  * The % Daily Value (DV) tells you how much a nutrient in a serving of food contributes to a daily diet. 2,000 calories a day is used for general nutrition advice.
  ```

```html
    <div class="divider medium"></div>
    <p class="note">
      * The % Daily Value (DV) tells you how much a nutrient in a serving of food contributes to a daily diet. 2,000 calories a day is used for general nutrition advice.
    </p>
```

## Paso 67

Cree un selector `.note` y establezca el tamaño de la fuente en `0.6rem`. También establezca los márgenes superior e inferior en `5px`, eliminando los márgenes izquierdo y derecho.

```css
.note {
  font-size: 0.6rem;
  margin: 5px 0;
}
```

## Paso 68

Dale al selector `.note` un relleno izquierdo y derecho de `8px`, eliminando el relleno superior e inferior. También establezca la propiedad `text-indent` en `-8px`.

**¡Con estos últimos cambios, su etiqueta nutricional está completa!**

```css
.note {
  font-size: 0.6rem;
  margin: 5px 0;
  padding: 0 8px;
  text-indent: -8px;
}
```
