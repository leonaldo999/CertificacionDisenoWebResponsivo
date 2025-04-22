# Aprende variables CSS construyendo un horizonte de la ciudad

Las variables de CSS te ayudan a organizar tus estilos y a reorganizarlos.

En este curso, construirás un horizonte de ciudad. Aprenderás cómo configurar variables de CSS de forma que puedas reusarlas cuando quieras.

## Paso 1

Bienvenido al proyecto Skyline de variables de CSS! Para iniciar, añada la declaración `!DOCTYPE` html en la parte superior del documento para que el navegador sepa qué tipo de documento está utilizando.

```html
  <!DOCTYPE html>
```

## Paso 2

Añade una etiqueta de apertura y cierre `html` abajo del `DOCTYPE` para que tengas espacio para comenzar a poner código. Asegúrate de establecer el idioma al español.

```html
<html lang="en">

</html>
```

## Paso 3

A continuación, añadir etiquetas `head` y `body` dentro del elemento `html`.

```html
<html lang="en">

<head>

</head>

<body>

</body>

</html>
```

## Paso 4

Within the `head`, nest a `meta` element with a `charset` of `UTF-8`, a `title` element with a title of `City Skyline`, and a `link` element that links your `styles.css` file.

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>City Skyline</title>
  <link rel="stylesheet" href="styles.css">
</head>
```

## Paso 5

En CSS, puedes orientar todo con un asterisco. Agregue un borde a todo usando el selector `*` y dándole un `border` de `1px solid black`. Este es un truco que ayuda a visualizar dónde están los elementos y su tamaño. *Eliminará esto más tarde*.

```css
* {
  border: 1px solid black;
}
```

## Paso 6

También agrega un `box-sizing` de `border-box` a todo. Esto hará que el borde que agregó no agregue ningún tamaño a sus elementos.

```css
* {
  box-sizing: border-box;
  border: 1px solid black;
}
```

## Paso 7

Puedes ver el `body` (es el cuadro más interno de tu página); el cuadro que lo rodea es el elemento `html`. Haz que tu `body` llene toda la ventana gráfica dándole una `height` de `100vh`. Elimine el `margin` predeterminado del `body` estableciendo el `margin` en `0`. Finalmente, establezca la propiedad `overflow` en `hidden` para ocultar las barras de desplazamiento que aparecen cuando algo se extiende más allá de la ventana gráfica.

```css
body {
  height: 100vh;
  margin: 0;
  overflow: hidden;
}
```

## Paso 8

Crea un elemento `div` dentro del elemento `body` con una clase de `background-buildings`. Este será un contenedor para un grupo de edificios.

```html
<body>
  <div class="background-buildings"></div>
</body>
```

## Paso 9

Asigne a su elemento `.background-buildings` un `width` y `height` de `100%` para convertirlo en el ancho y alto completos de su padre, el `body`.

```css
.background-buildings {
  width: 100%;
  height: 100%;
}
```

## Paso 10

Anida un `div` con una clase de `bb1` en el contenedor de edificios en segundo plano. Open your `styles.css` file, and give `.bb1` a `width` of `10%` and `height` of `70%.` "bb" significa "edificio de fondo", este será su primer edificio.

```html
  <div class="background-buildings">
    <div class="bb1"></div>
  </div>
```

```css
.bb1 {
  width: 10%;
  height: 70%;
}
```

## Paso 11

Anida cuatro elementos `div` en el contenedor `.bb1`. Give them the classes `bb1a`, `bb1b`, `bb1c`, and bb1d in that order. Este edificio tendrá cuatro secciones.

```html
  <div class="bb1">
    <div class="bb1a"></div>
    <div class="bb1b"></div>
    <div class="bb1c"></div>
    <div class="bb1d"></div>
  </div>
```

## Paso 12

Give the parts of your building `width` and `height` properties with these values: `70%` and `10%` to `.bb1a`, `80%` and `10%` to `.bb1b`, `90%` and `10%` to `.bb1c`, and `100%` and `70%` to `.bb1d`. Recuerda que estos porcentajes son relativos al padre y tenga en cuenta que las alturas sumarán hasta el 100%, llenando verticalmente el contenedor.

```css
.bb1a {
  width: 70%;
  height: 10%;
}

.bb1b {
  width: 80%;
  height: 10%;
}

.bb1c {
  width: 90%;
  height: 10%;
}

.bb1d {
  width: 100%;
  height: 70%;
}
```

## Paso 13

Centra las partes del edificio convirtiendo el elemento `.bb1` en un elemento primario `flexbox`. Utilice las propiedades `flex-direction` y `align-items` para centrar los elementos secundarios.

```css
.bb1 {
  width: 10%;
  height: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
```

## Paso 14

Ahora tienes algo que se parece a un edificio. Estás listo para crear tu primera variable. Las declaraciones de variables comienzan con dos guiones (`-`) y se les asigna un nombre y un valor como este: `--variable-name: value;`. En la regla de la clase `bb1`, cree una variable denominada `--building-color1` y asígnele un valor de `#999`.

```css
.bb1 {
  width: 10%;
  height: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
  --building-color1: #999;
}
```

## Paso 15

Para usar una variable, ponga el nombre de la variable entre paréntesis con `var` delante de ellos de esta manera: `var(--variable-name)`. Cualquier valor que haya asignado a la variable se aplicará a cualquier propiedad en la que la use.

Agregue la variable `--building-color1` que creó en el paso anterior como el valor de la propiedad `background-color` de la clase `.bb1a`.

```css
.bb1a {
  background-color: var(--building-color1);
  width: 70%;
  height: 10%;
}
```

## Paso 16

Utilice la misma variable que las clases `background-color` de las clases `.bb1b`, `.bb1c` y `.bb1d` para rellenar el resto del edificio.

```css
.bb1b {
  width: 80%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1c {
  width: 90%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1d {
  width: 100%;
  height: 70%;
  background-color: var(--building-color1);
}
```

## Paso 17

Cambie el valor de su variable de `#999` a `#aa80ff` y podrá ver cómo se aplica en todos los lugares donde usó la variable. Esta es la principal ventaja de usar variables, pudiendo cambiar rápidamente muchos valores en su hoja de estilo simplemente cambiando el valor de una variable.

```css
--building-color1: #aa80ff;
```

## Paso 18

Tu primer edificio se ve bastante bien ahora. Anida tres nuevos elementos `div` en el contenedor `.background-buildings` y asígneles las clases de `bb2`, `bb3` y `bb4` en ese orden. Estos serán tres edificios más para el fondo.

```html
  <div class="bb2"></div>
  <div class="bb3"></div>
  <div class="bb4"></div>
```

## Paso 19

Give the new buildings `width` and `height` properties of: `10%` and `50%` for `.bb2`, `10%` and `55%` for `.bb3`, and `11%` and `58%` for `.bb4`. Utilizará casi todas las unidades basadas en porcentajes y algunos flexbox para este proyecto, por lo que todo será completamente adaptable.

```css
.bb2 {
  width: 10%;
  height: 50%;
}
.bb3 {
  width: 10%;
  height: 55%;
}
.bb4 {
  width: 11%;
  height: 58%;
}
```

## Paso 20

Los edificios están actualmente apilados uno encima del otro. Alinee los edificios convirtiendo el elemento `.background-buildings` en un padre flexbox. Utilice las propiedades `align-items` y `justify-content` para espaciar uniformemente los edificios en la parte inferior del elemento.

```css
.background-buildings {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-evenly;
}
```

## Paso 21

Los edificios están demasiado espaciados. Comprieta agregando dos elementos vacíos `div` en la parte superior del elemento `.background-buildings`, dos más en la parte inferior y uno más entre `.bb3` y `.bb4`. Estos se agregarán como elementos espaciados uniformemente a través del contenedor, moviendo efectivamente los edificios más cerca del centro.

```html
  <div class="background-buildings">
    <div></div>
    <div></div>
    <div class="bb1">
      <div class="bb1a"></div>
      <div class="bb1b"></div>
      <div class="bb1c"></div>
      <div class="bb1d"></div>
    </div>

    <div class="bb2"></div>
    <div class="bb3"></div>
    <div></div>
    <div class="bb4"></div>
    <div></div>
    <div></div>
  </div>
```

## aso 22

Cree una nueva variable debajo de su variable `--building-color1`. Asigne un nombre a su nueva variable `--building-color2` y asígnele un valor de `#66cc99`. Luego configúrelo como el `background-color` de `.bb2`.

```css
.bb1 {
  width: 10%;
  height: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
  --building-color1: #aa80ff;
  --building-color2: #66cc99;
}

.bb1a {
  width: 70%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1b {
  width: 80%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1c {
  width: 90%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1d {
  width: 100%;
  height: 70%;
  background-color: var(--building-color1);
}

.bb2 {
  width: 10%;
  height: 50%;
  background-color: var(--building-color2);
}
```

## Paso 23

Eso no funcionó. Debe agregar un valor de reserva a una variable poniéndolo como el segundo valor de donde usa la variable de esta manera: `var(--variable-name, fallback-value)`. La propiedad usará el valor de reserva cuando haya un problema con la variable. Agregue un valor de reserva de `green` al `background-color` de `.bb2`.

```css
.bb2 {
  width: 10%;
  height: 50%;
  background-color: var(--building-color2, green);
}
```

## Paso 24

Cree una nueva variable debajo de las otras llamadas `--building-color3` y asígnele un valor de `#cc6699`. Luego úselo como el `background-color` de la clase `.bb3` y asígnele un valor de reserva de `pink`.

```css
.bb1 {
  width: 10%;
  height: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
  --building-color1: #aa80ff;
  --building-color2: #66cc99;
 --building-color3: #cc6699;
}

.bb1a {
  width: 70%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1b {
  width: 80%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1c {
  width: 90%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1d {
  width: 100%;
  height: 70%;
  background-color: var(--building-color1);
}

.bb2 {
  width: 10%;
  height: 50%;
  background-color: var(--building-color2, green);
}

.bb3 {
  width: 10%;
  height: 55%;
  background-color: var(--building-color3, pink);
}
```

## Paso 25

Eso no funcionó, porque las variables que declaró en `.bb1` no caen en cascada a los elementos hermanos `.bb2` y `.bb3`. Así es como funciona CSS. Debido a esto, las variables a menudo se declaran en el selector `:root`. Este es el selector de nivel más alto en CSS; Poner sus variables allí las hará utilizables en todas partes. Agregue el selector `:root` a la parte superior de la hoja de estilos y mueva todas las declaraciones de variables allí.

```css
:root {
  --building-color1: #aa80ff;
  --building-color2: #66cc99;
  --building-color3: #cc6699;
}

* {
  border: 1px solid black;
  box-sizing: border-box;
}

body {
  height: 100vh;
  margin: 0;
  overflow: hidden;
}

.background-buildings {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-evenly;
}

.bb1 {
  width: 10%;
  height: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
```

## Paso 26

Ahora que ha solucionado los errores y los edificios tienen los colores correctos, puede eliminar los valores alternativos en los dos lugares en los que se usaron. Adelante y hazlo ahora.

```css
.bb2 {
  width: 10%;
  height: 50%;
  background-color: var(--building-color2);
}

.bb3 {
  width: 10%;
  height: 55%;
  background-color: var(--building-color3);
}
```

## Paso 27

Cree otra variable llamada `--building-color4` y asígnele un valor de `#538cc6`. Asegúrate de que esté en el selector `:root` esta vez. Luego úsalo para rellenar el último edificio.

```css
:root {
  --building-color1: #aa80ff;
  --building-color2: #66cc99;
  --building-color3: #cc6699;
  --building-color4: #538cc6;
}

* {
  border: 1px solid black;
  box-sizing: border-box;
}

body {
  height: 100vh;
  margin: 0;
  overflow: hidden;
}

.background-buildings {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-evenly;
}

.bb1 {
  width: 10%;
  height: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.bb1a {
  width: 70%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1b {
  width: 80%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1c {
  width: 90%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1d {
  width: 100%;
  height: 70%;
  background-color: var(--building-color1);
}

.bb2 {
  width: 10%;
  height: 50%;
  background-color: var(--building-color2);
}

.bb3 {
  width: 10%;
  height: 55%;
  background-color: var(--building-color3);
}

.bb4 {
  width: 11%;
  height: 58%;
  background-color: var(--building-color4);
}
```

## Paso 28

Los edificios de fondo están empezando a verse bastante bien. Cree un nuevo `div` debajo del elemento `.background-buildings` y asígnele una clase de `foreground-buildings`. Este será otro contenedor para más edificios.

```html
  <div class="foreground-buildings"></div>
```

## Paso 29

Desea que el contenedor `.foreground-buildings` se coloque directamente encima del elemento `.background-buildings`. Give it a `width` and `height` of `100%`, set the `position` to `absolute`, and the `top` to `0`. Esto lo hará del mismo tamaño que el cuerpo y moverá el inicio del mismo a la esquina superior izquierda.

```css
.foreground-buildings {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
}
```

## Paso 30

Anida seis elementos `div` dentro de `.foreground-buildings` y asígnales las clases de `fb1` a través de `fb6` en ese orden. "fb" significa "edificio en primer plano". Estos serán seis edificios más para el primer plano.

```html
  <div class="foreground-buildings">
    <div class="fb1"></div>
    <div class="fb2"></div>
    <div class="fb3"></div>
    <div class="fb4"></div>
    <div class="fb5"></div>
    <div class="fb6"></div>
  </div>
```

## Paso 31

Give the six new elements these `width` and `height` values: `10%` and `60%` to `.fb1`, `10%` and `40%` to `.fb2`, `10%` and `35%` to `.fb3`, `8%` and `45%` to `.fb4`, `10%` and `33%` to `.fb5`, and `9%` and `38%` to `.fb6`.

```css
.fb1 {
  width: 10%;
  height: 60%;
}

.fb2 {
  width: 10%;
  height: 40%
}

.fb3 {
  width: 10%;
  height: 35%
}

.fb4 {
  width: 8%;
  height: 45%;
}

.fb5 {
  width: 10%;
  height: 33%;
}

.fb6 {
  width: 9%;
  height: 38%;
}
```

## Step 32

Add the same `display`, `align-items`, and `justify-content` properties and values to `.foreground-buildings` that you used on `.background-buildings`. Again, this will use Flexbox to evenly space the buildings across the bottom of their container.

```CSS
.foreground-buildings {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  display: flex;
 align-items: flex-end;
 justify-content: space-evenly;
}
```

## Paso 33

Debe optimizar su código. Move the `position` and `top` properties and values from `.foreground-buildings` to `.background-buildings`. Luego seleccione `.background-buildings` y `.foreground-buildings` allí, aplicando efectivamente esos estilos a ambos elementos. Puede usar una coma (`,`) para separar selectores como este: `selector1, selector2`.

```css
.background-buildings,
.foreground-buildings {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-evenly;
  position: absolute;
  top: 0;
}

.bb1 {
  width: 10%;
  height: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.bb1a {
  width: 70%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1b {
  width: 80%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1c {
  width: 90%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1d {
  width: 100%;
  height: 70%;
  background-color: var(--building-color1);
}

.bb2 {
  width: 10%;
  height: 50%;
  background-color: var(--building-color2);
}

.bb3 {
  width: 10%;
  height: 55%;
  background-color: var(--building-color3);
}

.bb4 {
  width: 11%;
  height: 58%;
  background-color: var(--building-color4);
}

.foreground-buildings {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-evenly;
}

```

## Paso 34

Ahora que lo hizo, puede eliminar la antigua declaración `.foreground-buildings` y todas sus propiedades, ya que ya no son necesarias.

```CSS
.background-buildings,
.foreground-buildings {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-evenly;
  position: absolute;
  top: 0;
}
/* 
SE ELIMINA

.foreground-buildings {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-evenly;
}
*/
```

## Paso 35

El horizonte se está juntando. Rellena la propiedad background-color de los edificios en primer plano. Use your `--building-color1` variable to fill in `.fb3` and `.fb4`, `--building-color2` for `.fb5`, `--building-color3` for `.fb2` and `.fb6`, and `--building-color4` for `.fb1`.

```css
.fb1 {
  width: 10%;
  height: 60%;
  background-color: var(--building-color4);
}

.fb2 {
  width: 10%;
  height: 40%;
  background-color: var(--building-color3);
}

.fb3 {
  width: 10%;
  height: 35%;
  background-color: var(--building-color1);
}

.fb4 {
  width: 8%;
  height: 45%;
  background-color: var(--building-color1);
}

.fb5 {
  width: 10%;
  height: 33%;
  background-color: var(--building-color2);
}

.fb6 {
  width: 9%;
  height: 38%;
  background-color: var(--building-color3);
}
```

## Paso 36

Vuelva a juntar los edificios agregando dos elementos `div` vacíos en la parte superior e inferior del elemento `.foreground-buildings`, y uno más entre `.fb2` y `.fb3`.

```html
<div></div>
    <div></div>
    <div class="fb1"></div>
    <div class="fb2"></div>
    <div></div>
    <div class="fb3"></div>
    <div class="fb4"></div>
    <div class="fb5"></div>
    <div class="fb6"></div>
    <div></div>
    <div></div>
```

## Paso 37

Mueve la posición de `.fb4` relativa a donde está ahora agregando una `position` de `relative` y `left` de `10%` a él. Haz lo mismo para `.fb5` pero usa `right` en lugar de `left`. Esto cubrirá el espacio en blanco restante entre los edificios.

```css
.fb4 {
  width: 8%;
  height: 45%;
  background-color: var(--building-color1);
  position: relative; 
  left: 10%;
}

.fb5 {
  width: 10%;
  height: 33%;
  background-color: var(--building-color2);
  position: relative; 
  right: 10%;
}
```

## Paso 38

Su código está empezando a ser bastante largo. Agregue un comentario sobre la clase `.fb1` que diga `FOREGROUND BUILDINGS - "fb" stands for "foreground building"` para ayudar a las personas a comprender su código. Encima de la clase `.bb1` agregue otro comentario que diga `BACKGROUND BUILDINGS - "bb" stands for "background building"`. Si no lo recuerda, los comentarios en CSS se ven así: `/*Comment here*/`.

```css
/* FOREGROUND BUILDINGS - "fb" stands for "foreground building" */

.bb1 {
  width: 10%;
  height: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.bb1a {
  width: 70%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1b {
  width: 80%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1c {
  width: 90%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1d {
  width: 100%;
  height: 70%;
  background-color: var(--building-color1);
}

.bb2 {
  width: 10%;
  height: 50%;
  background-color: var(--building-color2);
}

.bb3 {
  width: 10%;
  height: 55%;
  background-color: var(--building-color3);
}

.bb4 {
  width: 11%;
  height: 58%;
  background-color: var(--building-color4);
}

/* BACKGROUND BUILDINGS - "bb" stands for "background building" */
.fb1 {
  width: 10%;
  height: 60%;
  background-color: var(--building-color4);
}
```

## Paso 39

Cree una nueva variable en :`root` llamada `--window-color1` y asígnele un valor de `black`. Este será un color secundario para los edificios morados.

```css
:root {
  --building-color1: #aa80ff;
  --building-color2: #66cc99;
  --building-color3: #cc6699;
  --building-color4: #538cc6;
 --window-color1: black;
}
```

## Paso 40

Los degradados en CSS son una forma de transición entre colores a lo largo de la distancia de un elemento. Se aplican a la propiedad `background` **y la sintaxis se ve así**:

- Código de ejemplo
  
  ```css
  gradient-type(
    color1,
    color2
  );
  ```

En el ejemplo, `color1` es sólido en la parte superior, `color2` es sólido en la parte inferior, y en el medio pasa uniformemente de uno a otro. En `.bb1a`, agregue una propiedad `background` debajo de la propiedad `background-color`. Establézcalo como un degradado de tipo `linear-gradient` que usa `--building-color1` como el primer color y `--window-color1` como el segundo.

```css
.bb1a {
  width: 70%;
  height: 10%;
  background-color: var(--building-color1);
  background: linear-gradient(var(--building-color1), var(--window-color1));
}
```

## Paso 41

Desea agregar el mismo degradado a las siguientes dos secciones. En lugar de hacer eso, cree un nuevo selector de clase llamado `bb1-window`, y mueva las propiedades y valores `height` y `background` de `.bb1a` al nuevo selector de clase.

```css

.bb1a {
  width: 70%;
  background-color: var(--building-color1);
}

.bb1b {
  width: 80%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1c {
  width: 90%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1d {
  width: 100%;
  height: 70%;
  background-color: var(--building-color1);
}

.bb1-window {
  height: 10%;
  background: linear-gradient( var(--building-color1),
    var(--window-color1)
  );
  }
```

## Paso 42

Agregue la nueva clase `bb1-window` a los elementos `.bb1a`, `.bb1b` y `.bb1c`. Esto les aplicará el degradado.

```html
  <div class="bb1">
    <div class="bb1a bb1-window"></div>
    <div class="bb1b bb1-window"></div>
    <div class="bb1c bb1-window"></div>
    <div class="bb1d"></div>
  </div>
```

## Paso 43

No necesita las propiedades `height` o `background-color` en `.bb1a`, `.bb1b` o `.bb1c` nunca más, así que adelante, elimínelos.

```css
.bb1a {
  width: 70%;
}

.bb1b {
  width: 80%;
}

.bb1c {
  width: 90%;
}
```

## Paso 44

Los degradados pueden usar tantos colores como quieras así:

- Código de ejemplo

  ```css
  gradient-type(
    color1,
    color2,
    color3
  );
  ```

Agrega un `linear-gradient` a `.bb1d` con `orange` como el primer color, `--building-color1` como el segundo, y `--window-color1` como tercero. Recuerda usar el degradado en la propiedad `background`.

```css
.bb1d {
  width: 100%;
  height: 70%;
  background-color: var(--building-color1);
  background: linear-gradient(orange, var(--building-color1), var(--window-color1));
}
```

## Paso 45

Está un poco escondido detrás de los edificios en primer plano, pero puedes ver el degradado de tres colores allí. Como lo está usando ahora, elimine la propiedad `background-color` de `.bb1d`.

```css
.bb1d {
  width: 100%;
  height: 70%;
  background: linear-gradient(
      orange,
      var(--building-color1),
      var(--window-color1)
    );
}
```

## Paso 46

Puede especificar dónde desea que se complete una transición de degradado agregándolo al color de esta manera:

- Código de ejemplo

  ```css
  gradient-type(
    color1,
    color2 20%,
    color3
  );
  ```

Aquí, pasará de `color1` a `color2` entre `0%` y `20%` del elemento y luego pasará a `color3` para el resto. Agrega `80%` al color `--building-color1` del degradado `.bb1d` para que puedas verlo en acción.

```css
.bb1d {
  width: 100%;
  height: 70%;
  background: linear-gradient(
      orange,
      var(--building-color1) 80%,
      var(--window-color1)
    );
}
```

## Paso 47

Remove `orange` from the `.bb1d` gradient and change the `80%` to `50%`. Esto hará que `--building-color1` sea sólido para la mitad superior y luego pasará a `--window-color1` para la mitad inferior.

```css
.bb1d {
  width: 100%;
  height: 70%;
  background: linear-gradient(
      var(--building-color1) 50%,
      var(--window-color1)
    );
}
```

## Paso 48

Anide dos nuevos elementos `div` dentro de `.bb2`, asígneles las clases de `bb2a` y `bb2b`, en ese orden. Estas serán dos secciones para este edificio.

```html
  <div class="bb2">
    <div class="bb2a"></div>
    <div class="bb2b"></div>
  </div>
```

## Paso 49

Give `.bb2b` a `width` and `height` of `100%` to make it fill the building container. Agregarás algo en la parte superior un poco más tarde.

```css
.bb2b {
  width: 100%;
  height: 100%;
}
```

## Paso 50

Cree una nueva variable en `:root` denominada `window-color2` con un valor de `#8cd9b3`. Esto se utilizará como el color secundario para este edificio.

```css
:root {
  --building-color1: #aa80ff;
  --building-color2: #66cc99;
  --building-color3: #cc6699;
  --building-color4: #538cc6;
  --window-color1: black;
  --window-color2: #8cd9b3;
}
```

## Paso 51

Las transiciones de gradiente a menudo cambian gradualmente de un color a otro. Cuando se requiere un cambio más brusco, la transición puede hacerse con un tope duro como éste:

- Código de ejemplo

  ```css
  linear-gradient(
    var(--first-color) 0%,
    var(--first-color) 40%,
    var(--second-color) 40%,
    var(--second-color) 80%
  );
  ```

Agregue un `linear-gradient` a `.bb2b` que use `--building-color2` de `0%` a `6%` y `--window-color2` de `6%` a `9%`.

```css
.bb2b {
  width: 100%;
  height: 100%;
  background: linear-gradient(
    var(--building-color2),
    var(--building-color2) 6%,
    var(--window-color2) 6%,
    var(--window-color2) 9%
  );
}
```

## Paso 52

Puede ver el cambio de color duro en la parte superior de la sección. Cambie el tipo de degradado de `linear-gradient` a `repeating-linear-gradient` para esta sección. Esto hará que los cuatro colores de su degradado se repitan hasta que llegue al fondo del elemento; dándote algunas rayas y ahorrándote tener que agregar un montón de elementos para crearlos.

```css
.bb2b {
  width: 100%;
  height: 100%;
  background: repeating-linear-gradient(
      var(--building-color2),
      var(--building-color2) 6%,
      var(--window-color2) 6%,
      var(--window-color2) 9%
    );
}
```

## Paso 53

En los siguientes pasos, usarás algunos trucos con bordes CSS para convertir la sección `.bb2a` en un triángulo en la parte superior del edificio. Primero, elimine el `background-color` de `.bb2` ya que ya no lo necesita.

```css
.bb2 {
  width: 10%;
  height: 50%;
}
```

## Paso 54

Crea y añade las siguientes propiedades a `.bb2a`:

- Código de ejemplo

  ````css
  {
  margin: auto;
  width: 5vw;
  height: 5vw;
  border-top: 1vw solid #000;
  border-bottom: 1vw solid #000;
  border-left: 1vw solid #999;
  border-right: 1vw solid #999;
  }
  ````

Después de agregar estos, puede ver cómo un borde grueso en un elemento le da algunos ángulos donde se encuentran dos lados. Vas a usar ese borde inferior como la parte superior del edificio.

```css
.bb2a {
  margin: auto;
  width: 5vw;
  height: 5vw;
  border-top: 1vw solid #000;
  border-bottom: 1vw solid #000;
  border-left: 1vw solid #999;
  border-right: 1vw solid #999;
}
```

## Paso 55

Next, remove the `width` and `height` from `.bb2a`, and change the `border-left` and `border-right` to use `5vw` instead of `1vw`. El elemento ahora tendrá un tamaño cero y los bordes se unirán en el medio.

```css
.bb2a {
  margin: auto;
  border-top: 1vw solid #000;
  border-bottom: 1vw solid #000;
  border-left: 5vw solid #999;
  border-right: 5vw solid #999;
}
```

## Paso 56

A continuación, cambie los dos `#999` de `.bb2a` a `transparent`. Esto hará invisibles las fronteras izquierda y derecha.

```css
.bb2a {
  margin: auto;
  border-top: 1vw solid #000;
  border-bottom: 1vw solid #000;
  border-left: 5vw solid transparent;
  border-right: 5vw solid transparent;
}
```

## Paso 57

Elimine las propiedades y valores `margin` y `border-top` de `.bb2a` para convertirlo en un triángulo para la parte superior del edificio.

```css
.bb2a {
  border-bottom: 1vw solid #000;
  border-left: 5vw solid transparent;
  border-right: 5vw solid transparent;
}
```

## Paso 58

Finally, on the `border-bottom` property of `.bb2a`, change the `1vw` to `5vh` and change the `#000` color to your `--building-color2` variable. ¡Ahí lo tienes, ahora se ve bien! En cualquier momento a lo largo de este proyecto, puede comentar o eliminar la propiedad `border` que agregó a todo al principio para ver cómo se verán los edificios cuando se elimine al final.

```css
.bb2a {
  border-bottom: 5vh solid var(--building-color2);
  border-left: 5vw solid transparent;
  border-right: 5vw solid transparent;
}
```

## Paso 59

¡Vamos al siguiente edificio! Cree una nueva variable llamada `--window-color3` en `:root` y asígnele un valor de `#d98cb3`. Este será el color secundario para los edificios rosas.

```css
:root {
  --building-color1: #aa80ff;
  --building-color2: #66cc99;
  --building-color3: #cc6699;
  --building-color4: #538cc6;
  --window-color1: black;
  --window-color2: #8cd9b3;
  --window-color3: #d98cb3;
}
```

## Paso 60

Hasta ahora, todos los degradados que creaste han ido de arriba a abajo, esa es la dirección predeterminada. Puede especificar otra dirección agregándola antes de sus colores de esta manera:

- Código de ejemplo

  ```css
  gradient-type(
    direction,
    color1,
    color2
  );
  ```

Rellene `.bb3` con un `repeating-linear-gradient`. Use `90deg` para la dirección, su `building-color3` para los dos primeros colores, y `window-color3` en `15%` para el tercero.

When you don't specify a distance for a color, it will use the values that makes sense. In this case, the first two colors will default to `0%` and `7.5%` because it starts at `0%`, and `7.5%` is half of the `15%`, so you do not need to set them.

```css
.bb3 {
  width: 10%;
  height: 55%;
  background-color: var(--building-color3);
  background: repeating-linear-gradient(
    90deg,
    var(--building-color3),
    var(--building-color3) ,
    var(--window-color3) 15%
 );
}
```

## Paso 61

Quite la propiedad y el valor `background-color` de `.bb3` ya que ahora está utilizando el degradado como fondo.

```css
.bb3 {
  width: 10%;
  height: 55%;
  background: repeating-linear-gradient(
    90deg,
    var(--building-color3),
    var(--building-color3),
    var(--window-color3) 15%
  );
}
```

## Paso 62

El próximo edificio tendrá tres secciones. Anida tres elementos `div` dentro de `.bb4`. Dales las clases de `bb4a`, `bb4b` y `bb4c` en ese orden.

```html
  <div class="bb4">
    <div class="bb4a"></div>
    <div class="bb4b"></div>
    <div class="bb4c"></div>
  </div>
```

## Paso 63

Dale a los nuevos elementos `div` estos valores de `width` y `height`: `3%` y `10%` a `.bb4a`, `80%` y `5%` a `.bb4b` y `100%` y `85%` a `.bb4c`.

```css
.bb4a{
  width: 3%;
  height: 10%;
}

.bb4b{
  width: 80%;
  height: 5%;
}

.bb4c{
  width: 100%;
  height: 85%;
}
```

## Paso 64

Elimine la propiedad y el valor `background-color` de `.bb4` y agréguelo a las tres nuevas secciones `.bb4a`, `.bb4b` y `.bb4c`, de modo que solo se rellenen las secciones.

```css
.bb4 {
  width: 11%;
  height: 58%;
}

.bb4a {
  width: 3%;
  height: 10%;
  background-color: var(--building-color4);
}

.bb4b {
  width: 80%;
  height: 5%;
  background-color: var(--building-color4);
}

.bb4c {
  width: 100%;
  height: 85%;
  background-color: var(--building-color4);
}
```

## Paso 65

Desea que `.bb4` comparta las propiedades de `.bb1` que centran las secciones. En lugar de duplicar ese código, cree una nueva clase encima del comentario de creación en segundo plano llamado `building-wrap`. Déjalo vacío por ahora; Esta clase se usará en algunos lugares para ahorrarle algo de codificación.

```css
.building-wrap {}
```

## Paso 66

Move the `display`, `flex-direction`, and `align-items` properties and values from `.bb1` to the new `building-wrap` class.

```css
.building-wrap {
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* BACKGROUND BUILDINGS - "bb" stands for "background building" */
.bb1 {
  width: 10%;
  height: 70%;
}
```

## Paso 67

Agregue la nueva clase `building-wrap` a los elementos `.bb1` y `.bb4`. Esto aplicará las propiedades de centrado a los edificios que lo necesiten.

```html
  <div class="bb1 building-wrap">
    <div class="bb1a bb1-window"></div>
    <div class="bb1b bb1-window"></div>
    <div class="bb1c bb1-window"></div>
    <div class="bb1d"></div>
  </div>
  <div class="bb2">
    <div class="bb2a"></div>
    <div class="bb2b"></div>
  </div>
  <div class="bb3"></div>
  <div></div>
  <div class="bb4 building-wrap">
```

## Paso 68

Crea una nueva variable llamada `--window-color4` en `:root` y asígnele un valor de `#8cb3d9`. Este será el color secundario para el último edificio de fondo.

```css
:root {
  --building-color1: #aa80ff;
  --building-color2: #66cc99;
  --building-color3: #cc6699;
  --building-color4: #538cc6;
  --window-color1: black;
  --window-color2: #8cd9b3;
  --window-color3: #d98cb3;
  --window-color4: #8cb3d9;
}
```

## Paso 69

Anida cuatro nuevos elementos `div` dentro de `.bb4c`, dales toda la clase de `bb4-window`. Estas serán las ventanas de este edificio.

```html
  <div class="bb4c">
    <div class="bb4-window"></div>
    <div class="bb4-window"></div>
    <div class="bb4-window"></div>
    <div class="bb4-window"></div>
  </div>
```

## Paso 70

Give the `bb4-window` class a `width` of `18%`, a `height` of `90%`, and add your `--window-color4` variable as the `background-color`.

```css
.bb4-window {
  width: 18%;
  height: 90%;
  background-color: var(--window-color4);
}
```

## Paso 71

Las ventanas están apiladas una encima de la otra a la izquierda de la sección, detrás del edificio púrpura. Agregue una nueva clase debajo de `.building-wrap` llamada `window-wrap`. Convierta `.window-wrap` en un contenedor flexbox y use las propiedades `align-items` y `justify-content` para centrar sus elementos secundarios verticalmente y espaciarlos uniformemente en su elemento primario, respectivamente.

```css
.window-wrap {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
```

## Paso 72

Agregue la nueva clase `window-wrap` al elemento `.bb4c`.

```html
  <div class="bb4c window-wrap">
    <div class="bb4-window"></div>
    <div class="bb4-window"></div>
    <div class="bb4-window"></div>
    <div class="bb4-window"></div>
  </div>
```

## Paso 73

¡Se ve bien! ¡A los edificios en primer plano! Convierta el edificio `.fb1` en tres secciones anidando tres nuevos elementos `div` dentro de él. Dales las clases de `fb1a`, `fb1b` y `fb1c`, en ese orden.

```html
  <div class="fb1">
    <div class="fb1a"></div>
    <div class="fb1b"></div>
    <div class="fb1c"></div>
  </div>
```

## Paso 74

Give `.fb1b` a `width` of `60%` and `height` of `10%`, and `.fb1c` a `width` of `100%` and `height` of `80%`.

```css
.fb1b {
  width: 60%;
  height: 10%;
}
.fb1c {
  width: 100%;
  height: 80%;
}
```

## Paso 75

Agregue la clase `building-wrap` al elemento `.fb1` para centrar las secciones.

```html
  <div class="fb1 building-wrap">
    <div class="fb1a"></div>
    <div class="fb1b"></div>
    <div class="fb1c"></div>
  </div>
```

## Paso 76

Mueva la propiedad y el valor `background-color` de `.fb1` a `.fb1b`.

```css
.fb1 {
  width: 10%;
  height: 60%;
}

.fb1b {
  width: 60%;
  height: 10%;
  background-color: var(--building-color4);
}
```

## Paso 77

No se preocupe por el espacio en la parte inferior, todo se moverá hacia abajo más tarde cuando agregue algo de altura al elemento en la parte superior del edificio.

Agregue un `repeating-linear-gradient` a `.fb1c` con un ángulo `90deg`, su `--building-color4` de `0%` a `10%` y `transparent` de `10%` a `15%`.

```css
.fb1c {
  width: 100%;
  height: 80%;
  background: repeating-linear-gradient(
    90deg,
    var(--building-color4),
    var(--building-color4) 10%,
    transparent 10%,
    transparent 15%
  );
}
```

## Paso 78

Puede agregar varios degradados a un elemento separándolos con una coma (`,`) como esta:

- Código de ejemplo

  ```css
   gradient1(
    colors
  ),
  gradient2(
    colors
  );
  ```

Agregue un `repeating-linear-gradient` a `.fb1c` debajo del que está allí; Use su `--building-color4` de `0%` a `10%` y `--window-color4` de `10%` y `90%`. Esto se completará detrás del degradado que agregó en último lugar.

```css
.fb1c {
  width: 100%;
  height: 80%;
  background: repeating-linear-gradient(
      90deg,
      var(--building-color4),
      var(--building-color4) 10%,
      transparent 10%,
      transparent 15%
    ),
  repeating-linear-gradient(
    var(--building-color4),
    var(--building-color4) 10%,
    var(--window-color4) 10%,
    var(--window-color4) 90%
  );
}
```

## Paso 79

Vas a usar algunos trucos de borde más para la sección superior. Agregue un `border-bottom` con un valor de `7vh solid var(--building-color4)` a `.fb1a`. Esto pondrá un borde de altura `7vh` en la parte inferior. Pero como el elemento tiene tamaño cero, solo aparece como una línea de 2px de ancho desde el borde de 1px que está en todos los elementos.

```css
.fb1a {
  border-bottom: 7vh solid var(--building-color4);
}
```

## Paso 80

Cuando aumente el tamaño de los bordes izquierdo y derecho, el borde de la parte inferior se expandirá para ser el ancho de los anchos de borde izquierdo y derecho combinados. Agrega `2vw solid transparent` como el valor de las propiedades `border-left` y `border-right` de `.fb1a`. Serán invisibles, pero hará que el borde en la parte inferior `4vw` ancho.

```css
.fb1a {
  border-bottom: 7vh solid var(--building-color4);
  border-left: 2vw solid transparent;
  border-right: 2vw solid transparent;
}
```

## Paso 81

¡Vamos al siguiente edificio! Anide dos elementos `div` dentro de `.fb2` y asígneles clases de `fb2a` y `fb2b`, en ese orden.

```html
  <div class="fb2">
    <div class="fb2a"></div>
    <div class="fb2b"></div>
  </div>
```

## Paso 82

Give `.fb2a` a `width` of `100%` and `.fb2b` a `width` of `100%` and `height` of `75%`.

```css
.fb2a {
  width: 100%;
}
.fb2b {
  width: 100%;
  height: 75%;
}
```

## Paso 83

Anida tres elementos `div` dentro de `.fb2b` y asígneles una clase de `fb2-window`. Estas serán ventanas para esta sección del edificio.

```html
  <div class="fb2b">
    <div class="fb2-window"></div>
    <div class="fb2-window"></div>
    <div class="fb2-window"></div>
  </div>
```

## Paso 84

Agregue la clase `window-wrap` a `.fb2b` para colocar los nuevos elementos de ventana.

```html
  <div class="fb2b window-wrap">
    <div class="fb2-window"></div>
    <div class="fb2-window"></div>
    <div class="fb2-window"></div>
  </div>
```

## Paso 85

Give the `.fb2-window` elements a `width` of `22%`, `height` of `100%`, and a `background-color` of your `--window-color3` variable.

```css
.fb2-window {
  width: 22%;
  height: 100%;
  background-color: var(--window-color3);
}
```

## Paso 86

Mueva la propiedad y el valor `background-color` de `.fb2` a `.fb2b` para colorear la sección y no el contenedor.

```css
.fb2 {
  width: 10%;
  height: 40%;
}

.fb2a {
  width: 100%;
}

.fb2b {
  width: 100%;
  height: 75%;
  background-color: var(--building-color3);
}
```

## Paso 87

Para `.fb2a`, agregue un `border-bottom` de `10vh solid var(--building-color3)`, y un `border-left` y `border-right` de `1vw solid transparent`. Esta vez el truco del borde creará una forma trapezoidal.

```css
.fb2a {
  width: 100%;
  border-bottom: 10vh solid var(--building-color3);
  border-left: 1vw solid transparent;
  border-right: 1vw solid transparent;
}
```

## Paso 88

Para el siguiente edificio, anide cuatro elementos `div` dentro de `.fb3` con clases de `fb3a`, `fb3b`, `fb3a` de nuevo, y `fb3b` de nuevo, en ese orden. Este edificio tendrá cuatro secciones, y las dos superiores serán casi las mismas que las dos inferiores.

```html
  <div class="fb3">
    <div class="fb3a"></div>
    <div class="fb3b"></div>
    <div class="fb3a"></div>
    <div class="fb3b"></div>
  </div>
```

## Paso 89

Give the `.fb3a` element a `width` of `80%` and `height` of `15%`. Then give the `.fb3b` element a `width` of `100%` and `height` of `35%`.

```css
.fb3a {
  width: 80%;
  height: 15%;
}
.fb3b {
  width: 100%;
  height: 35%;
}
```

## Paso 90

Quite la propiedad y el valor `background-color` de `.fb3` y agréguelos a `.fb3a` y `.fb3b`.

```css
.fb3 {
  width: 10%;
  height: 35%;
}

.fb3a {
  width: 80%;
  height: 15%;
  background-color: var(--building-color1);
}

.fb3b {
  width: 100%;
  height: 35%;
  background-color: var(--building-color1);
}
```

## Paso 91

Agrega la clase `building-wrap` al elemento `.fb3` para centrar las secciones.

```html
  <div class="fb3 building-wrap">
    <div class="fb3a"></div>
    <div class="fb3b"></div>
    <div class="fb3a"></div>
    <div class="fb3b"></div>
  </div>
```

## Paso 92

Anida tres nuevos elementos `div` en el primer elemento `.fb3a`. Dale a cada uno una clase de `fb3-window`. Estas serán ventanas para esta sección.

```html
  <div class="fb3a">
    <div class="fb3-window"></div>
    <div class="fb3-window"></div>
    <div class="fb3-window"></div>
  </div>
```

## Paso 93

Give the `.fb3-window` elements a `width` of `25%`, a `height` of `80%`, and use your `--window-color1` variable as the `background-color` value.

```css
.fb3-window {
  width: 25%;
  height: 80%;
  background-color: var(--window-color1);
}
```

## Paso 94

Agregue la clase `window-wrap` al elemento `.fb3a` para centrar y espaciar las ventanas.

```html
  <div class="fb3a window-wrap">
    <div class="fb3-window"></div>
    <div class="fb3-window"></div>
    <div class="fb3-window"></div>
  </div>
```

## Paso 95

Con las variables CSS puede cambiar los valores sin buscar en todas partes de la hoja de estilo. Cambie el valor `--window-color1` a `#bb99ff`.

```css
:root {
  --building-color1: #aa80ff;
  --building-color2: #66cc99;
  --building-color3: #cc6699;
  --building-color4: #538cc6;
  --window-color1: #bb99ff;
  --window-color2: #8cd9b3;
  --window-color3: #d98cb3;
  --window-color4: #8cb3d9;
}
```

## Paso 96

Solo quedan tres edificios más. Anida dos nuevos elementos `div` dentro del elemento `.fb4` y asígneles las clases de `fb4a` y `fb4b`, en ese orden. Recuerde que cambió la ubicación de `.fb4` y `.fb5`, por lo que es el edificio púrpura más a la derecha en el que está trabajando ahora.

```html
  <div class="fb4">
    <div class="fb4a"></div>
    <div class="fb4b"></div>
  </div>
```

## Paso 97

Give `.fb4b` a `width` of `100%` and `height` of `89%`.

```css
.fb4b {
  width: 100%;
  height: 89%;
}
```

## Paso 98

Agrega su variable `--building-color1` como valor de la propiedad `background-color` de `.fb4b`. A continuación, elimine el `background-color` de `.fb4`.

```css
.fb4 {
  width: 8%;
  height: 45%;
  position: relative;
  left: 10%;
}

.fb4b {
  width: 100%;
  height: 89%;
  background-color: var(--building-color1);
}
```

## Paso 99

Anida seis elementos `div` dentro de `.fb4b` y asígneles a todos una clase de `fb4-window`.

```html
  <div class="fb4b">
    <div class="fb4-window"></div>
    <div class="fb4-window"></div>
    <div class="fb4-window"></div>
    <div class="fb4-window"></div>
    <div class="fb4-window"></div>
    <div class="fb4-window"></div>
  </div>
```

## Paso 100

Give the `.fb4-window` elements a `width` of `30%`, `height` of `10%`, and `border-radius` of `50%`. Estos harán algunas ventanas circulares para este edificio.

```css
.fb4-window {
  width: 30%;
  height: 10%;
  border-radius: 50%;
}
```

## Paso 101

Rellene las ventanas con su color secundario para este edificio. También agregue un `margin` de `10%` para dar espacio a las ventanas.

```CSS
.fb4-window {
  width: 30%;
  height: 10%;
  border-radius: 50%;
  background-color: var(--window-color1);
  margin: 10%;
}
```

## Paso 102

Las ventanas están apiladas una encima de la otra en el edificio púrpura más a la derecha. Convierta el edificio en un padre flexbox y use la propiedad `flex-wrap` para colocar las ventanas una al lado de la otra y empujarlas hacia abajo a una nueva fila cuando no encajen.

```css
.fb4b {
  width: 100%;
  height: 89%;
  background-color: var(--building-color1);
  display: flex;
  flex-wrap: wrap;
}
```

## Paso 103

Este edificio va a tener otro triángulo en la parte superior. Asigne a la sección superior un `border-top` de `5vh solid transparent`, y un `border-left` que sea `8vw`, `solid`, y use la variable de color del edificio como color.

```css
.fb4a {
  border-top: 5vh solid transparent;
  border-left: 8vw solid var(--building-color1);
} 
```

## Paso 104

¡Vamos al siguiente edificio! Es el verde en primer plano. Give it a `repeating-linear-gradient` with your building color from `0%` to `5%`, and `transparent` from `5%` to `10%`.

```css
.fb5 {
  width: 10%;
  height: 33%;
  background-color: var(--building-color2);
  background: repeating-linear-gradient(
    var(--building-color2),
    var(--building-color2) 5%,
    transparent 5%,
    transparent 10%
  );
  position: relative;
  right: 10%;
}
```

## Paso 105

Agregue otro repeating-linear-gradient debajo del que acaba de agregar. Dale una dirección de 90deg, usa el color de tu edificio de `0%` a `12%` y el color de la ventana `12%` a `44%`. Esto hará un montón de ventanas rectangulares.

```css
.fb5 {
  width: 10%;
  height: 33%;
  background-color: var(--building-color2);
  position: relative;
  right: 10%;
  background: repeating-linear-gradient(
      var(--building-color2),
      var(--building-color2) 5%,
      transparent 5%,
      transparent 10%
    ),
    repeating-linear-gradient(
      90deg,
      var(--building-color2),
      var(--building-color2) 12%,
      var(--window-color2) 12%,
      var(--window-color2) 44%
    )
}
```

## Paso 106

Ya no necesita el `background-color` para este edificio, por lo que puede eliminar esa propiedad.

```css
.fb5 {
  width: 10%;
  height: 33%;
  position: relative;
  right: 10%;
  background: repeating-linear-gradient(
      var(--building-color2),
      var(--building-color2) 5%,
      transparent 5%,
      transparent 10%
    ),
    repeating-linear-gradient(
      90deg,
      var(--building-color2),
      var(--building-color2) 12%,
      var(--window-color2) 12%,
      var(--window-color2) 44%
    );
}
```

## Paso 107

¡Finalmente! ¡Llegaste al último edificio! Agregue un degradado repetitivo con una dirección de `90deg`. Use the building color from `0%` to `10%` and `transparent` from `10%` to `30%`.

```css
.fb6 {
  width: 9%;
  height: 38%;
  background-color: var(--building-color3);
  background: repeating-linear-gradient(
    90deg,
    var(--building-color3),
    var(--building-color3) 10%,
    transparent 10%,
    transparent 30%
  );
}
```

## Paso 108

Agregue otro degradado repetitivo a este edificio; Hágalo igual que el que acaba de agregar, excepto que no agregue la dirección `90deg` y use el color de la ventana en lugar de los dos colores `transparent`.

```css
.fb6 {
  width: 9%;
  height: 38%;
  background-color: var(--building-color3);
  background: repeating-linear-gradient(
    90deg,
    var(--building-color3),
    var(--building-color3) 10%,
    transparent 10%,
    transparent 30%
  ),
  repeating-linear-gradient(
    var(--building-color3),
    var(--building-color3)10%,
    var(--window-color3) 10%,
    var(--window-color3) 30%
  );
}
```

## Paso 109

Puede eliminar el `background-color` para este edificio ahora, ya que no es necesario.

```css
.fb6 {
  width: 9%;
  height: 38%;
  background: repeating-linear-gradient(
      90deg,
      var(--building-color3),
      var(--building-color3) 10%,
      transparent 10%,
      transparent 30%
    ),
    repeating-linear-gradient(
      var(--building-color3),
      var(--building-color3) 10%,
      var(--window-color3) 10%,
      var(--window-color3) 30%
    );
}
```

## Paso 110

Está bien, los edificios están hechos. Vuelve al selector `*` y elimine el `border` que aplicó a todo al principio y los edificios se unirán.

```css
* {
  box-sizing: border-box;
}
```

## Paso 111

Agregue `sky` como una segunda clase al elemento `.background-buildings`. Vas a hacer un fondo para el horizonte.

```html
    <div class="background-buildings sky">
      <div></div>
      <div></div>
      <div class="bb1 building-wrap">
        <div class="bb1a bb1-window"></div>
        <div class="bb1b bb1-window"></div>
        <div class="bb1c bb1-window"></div>
        <div class="bb1d"></div>
      </div>
      <div class="bb2">
        <div class="bb2a"></div>
        <div class="bb2b"></div>
      </div>
      <div class="bb3"></div>
      <div></div>
      <div class="bb4 building-wrap">
        <div class="bb4a"></div>
        <div class="bb4b"></div>
        <div class="bb4c window-wrap">
          <div class="bb4-window"></div>
          <div class="bb4-window"></div>
          <div class="bb4-window"></div>
          <div class="bb4-window"></div>
        </div>
      </div>
      <div></div>
      <div></div>
    </div>
```

## Paso 112

Dale a la clase `sky` un `radial-gradient`. Use `#ffcf33` from `0%` to `20%`, `#ffff66` at `21%`, and `#bbeeff` at `100%`. Esto agregará un degradado circular al fondo que será tu sol.

```css
.sky {
  background: radial-gradient(
  #ffcf33 0%,
  #ffcf33 20%,
  #ffff66 21%,
 #bbeeff 100%
  );
}
```

## Paso 113

En la parte superior de la lista de colores del degradado del cielo, donde pondrías una dirección para el degradado; Agregue `circle closest-corner at 15% 15%`,. Esto moverá el inicio del degradado a `15%` desde la parte superior e izquierda. Hará que termine en la `closest-corner` y mantendrá una forma de `circle`. Estas son algunas palabras clave integradas en gradientes para describir cómo se comporta.

```css
.sky {
  background: radial-gradient(
     circle closest-corner at 15% 15%,
    #ffcf33,
    #ffcf33 20%,
    #ffff66 21%,
    #bbeeff 100%
    );
}
```

## Paso 114

Una consulta de medios se puede usar para cambiar estilos en función de ciertas condiciones, y se ven así:

- Código de ejemplo

  ```css
  @media (condition) {

  }  
  ```

Agregue una consulta multimedia vacía en la parte inferior de la hoja de estilos con una condición de `max-width: 1000px`. Los estilos agregados aquí surtirán efecto cuando el tamaño del documento sea de 1000px de ancho o menos.

```css
@media (max-width: 1000px) {

} 
```

## Paso 115

Copia y pegue toda su clase `sky` junto con todas sus propiedades y valores en la consulta de medios. Vas a hacer otro esquema de color para el horizonte que lo cambie de día a noche.

>[!NOTE]
>
>Deberá desplazarse más allá de la región editable para copiar la clase.

```css
@media (max-width: 1000px) {
.sky {
  background: radial-gradient(
      closest-corner circle at 15% 15%,
      #ffcf33,
      #ffcf33 20%,
      #ffff66 21%,
      #bbeeff 100%
    );
}
}
```

## Paso 116

In the sky class of the media query, change the two #ffcf33 color values to #ccc, the #ffff66 to #445, and the #bbeeff to #223. Luego puede cambiar el tamaño de su ventana para ver los colores de cambio de fondo.

```css
@media (max-width: 1000px) {
 .sky {
  background: radial-gradient(
   closest-corner circle at 15% 15%,
   #ccc,
   #ccc 20%,
   #445 21%,
   #223 100%
  );
 }
}
```

## Paso 117

Agrega un selector `:root` en la parte superior de su consulta de medios. Luego redefina las cuatro variables `--building-color` para usar el valor `#000` allí.

```css
  :root {
    --building-color1: #000;
    --building-color2: #000;
    --building-color3: #000;
    --building-color4: #000;
  }
```

## Paso 118

Por último, en el selector `:root` de la consulta de medios, redefina las cuatro variables `--window-color` para usar `#777`. Cuando haya terminado, cambie el tamaño de la ventana y observe cómo pasa del día a la noche.

Las variables se usan principalmente con colores, y así es como las usaste aquí. Pero se les puede dar cualquier valor y usar en cualquier propiedad. Tu proyecto se ve genial!

```css
:root {
    --building-color1: #000;
    --building-color2: #000;
    --building-color3: #000;
    --building-color4: #000;
    --window-color1: #777;
    --window-color2: #777;
    --window-color3: #777;
    --window-color4: #777;
  }
```
