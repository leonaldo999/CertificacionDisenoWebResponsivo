# Aprende CSS Transforms construyendo un pinguino

Puedes transformar elementos **HTML** para crear diseños atractivos que atraigan la atención de tu lector. Puedes utilizar las transformaciones para girar elementos, escalarlos y mucho más.

En este curso, construirás un pingüino. Utilizarás transformaciones **CSS** para posicionar y cambiar el tamaño de las partes de tu pingüino, crearás un fondo y animarás tu trabajo.

## Paso 1

Estarás construyendo un feliz pingüino Flappy y explorando aún más las transformaciones y animaciones CSS en el proceso.

Comience con su plantilla HTML básica. Incluya la declaración `DOCTYPE`, el elemento `html` con un idioma establecido en inglés, las etiquetas `meta` apropiadas, un `head`, `body` y elemento `title`. Además, vincule su hoja de estilo a la página.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="stylesheet" href="styles.css">
</head>

<body>

</body>

</html>
```

## Paso 2

Apunte al elemento `body` para establecer el `background` en un degradado lineal inclinado 45 grados en el sentido de las agujas del reloj, comenzando en `rgb(118, 201, 255)` y terminando en `rgb(247, 255, 222)`.

```css
body {
  background:linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
}
```

## Paso 3

Normaliza el tamaño de tu página, eliminando el elemento `body` `margin` y `padding` del elemento.

```css
body {
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
  margin: 0;
  padding: 0;
}
```

## Paso 4

Normaliza tu página, estableciendo el `width` a `100%` y el `height` a `100vh`.

```css
body {
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100vh;
}
```

## Paso 5

Elimine las barras de desplazamiento horizontal y vertical, usando solo una propiedad.

```css
body {
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}
```

## Paso 6

Dentro del `body`, agregue un `div` con una `class` de `ground`.

```html
<body>
  <div class="ground"></div>
</body>
```

## Paso 7

Apunte al elemento `.ground` y establezca su `width` para que ocupe todo el ancho de la ventanilla. A continuación, establezca la `height` en `400px`.

```css
.ground {
  width: 100vw;
  height: 400px;
}
```

## Paso 8

Asigne al elemento `.ground` un `background` con un degradado lineal en ángulo de 90 grados en el sentido de las agujas del reloj, comenzando en `rgb(88, 175, 236)` y terminando en `rgb(182, 255, 255)`.

```css
.ground {
  width: 100vw;
  height: 400px;
  background: linear-gradient(90deg, rgb(88, 175, 236), rgb(182, 255, 255));
}
```

## Paso 9

Como `.ground` elemento será tercero en el contexto de apilamiento del diseño de la página, establezca `z-index` a `3` y `position` a `absolute`.

```css
.ground {
  width: 100vw;
  height: 400px;
  background: linear-gradient(90deg, rgb(88, 175, 236), rgb(182, 255, 255));
  z-index: 3;
  position: absolute;
}
```

## Paso 10

Sobre el `.ground` elemento, agregue un `div` con la `class` de `penguin`. Este `div` contendrá al Flappy Penguin.

```html
<body>
  <div class="penguin"></div>
  <div class="ground"></div>
</body>
```

## Paso 11

Seleccione `.penguin` el elemento y establezca su `width` y `height` en `300px`.

```css
.penguin {
  width: 300px;
  height: 300px;
}
```

## Paso 12

Utilice la propiedad `margin` para centrar horizontalmente el elemento `.penguin` y establezca el `margin-top` en `75px`.

```css
.penguin {
  width: 300px;
  height: 300px;
  margin: auto;
  margin-top: 75px;
}
```

## Paso 13

Para crear un paisaje de fondo, agregará dos montañas.

Sobre el elemento `.penguin`, agrega un `div` con una `class` de `left-mountain`.

```html
<body>
  <div class="left-mountain"></div>
  <div class="penguin"></div>
  <div class="ground"></div>
</body>
```

## Paso 14

Seleccione `.left-mountainelemento` y establezca su `width` y `height` en `300px`. Luego, establece el `background` en un degradado lineal que comienza en `rgb(203, 241, 228)` y termina en `rgb(80, 183, 255)`.

```css
.left-mountain {
 width: 300px;
 height: 300px;
 background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
}
```

## Paso 15

Para evitar que la montaña empuje el elemento `.ground`, ajusta su `position` para evitar que ocupe espacio en el diseño de la página.

```css
.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
}
```

## Paso 16

Para hacer que la montaña se parezca más a una montaña, puedes usar la función de transformación `skew`, que toma dos argumentos. El primero es un ángulo por el que se corta el eje x, y el segundo es un ángulo por el que se corta el eje y.

Usa la propiedad `transform` para sesgar la montaña `0deg` en el eje x y `44deg` en el eje y.

```css
.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
  transform: skew(0deg, 44deg);
}
```

## Paso 17

Establezca el nivel de pila del elemento de la montaña de modo que permanezca directamente detrás del elemento `.ground`.

```css
.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
  transform: skew(0deg, 44deg);
  z-index: 2;
}
```

## Paso 18

Para superponer la montaña y mejor los elementos `.ground`, dé a la montaña un `margin-top` de `100px`, y el `.ground` un elemento `margin-top` de `-58px`.

```css
.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
  transform: skew(0deg, 44deg);
  z-index: 2;
  margin-top: 100px;
}

.penguin {
  width: 300px;
  height: 300px;
  margin: auto;
  margin-top: 75px;
}

.ground {
  width: 100vw;
  height: 400px;
  background: linear-gradient(90deg, rgb(88, 175, 236), rgb(182, 255, 255));
  z-index: 3;
  position: absolute;
  margin-top: -58px;
}
```

## Paso 19

Para dar el efecto de una cadena montañosa, agregue otra montaña creando un nuevo `div` inmediatamente después de `.left-mountain`, y asigne el nuevo `div` la `class` de `back-mountain`.

```html
<body>
  <div class="left-mountain"></div>
  <div class="back-mountain"></div>
  <div class="penguin"></div>
  <div class="ground"></div>
</body>
```

## Paso 20

Seleccione el elemento `.back-mountain` y establezca su `width` y `height` en `300px`. Luego, establece el `background` en un degradado lineal que comienza en `rgb(203, 241, 228)` y termina en `rgb(47, 170, 255)`.

```css
.back-mountain{
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
}
```

## Paso 21

Establezca la propiedad `position` de `.back-mountain` para evitar que ocupe espacio en el diseño de la página.

```css
.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
  position: absolute;
}
```

## Paso 22

Cambie el nivel de pila del elemento `.back-mountain` de modo que quede directamente detrás del elemento `.left-mountain`.

```css
.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
  position: absolute;
  z-index: 1;
}
```

## Paso 23

Gire el elemento `.back-mountain` por `45deg` en el sentido de las agujas del reloj. Luego, asígnele una propiedad `left` de `110px`, y una propiedad `top` de `225px`.

```css
.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
  position: absolute;
  z-index: 1;
  transform: rotate(45deg);
  left: 110px;
  top: 225px;
}
```

## Paso 24

Para terminar el fondo, agregue un sol, creando un nuevo elemento `div` inmediatamente después del elemento `.back-mountain`, y asígnele la clase de `sun`.

```html
<body>
  <div class="left-mountain"></div>
  <div class="back-mountain"></div>
  <div class="sun"></div>
  <div class="penguin"></div>
  <div class="ground"></div>
</body>
```

## Paso 25

Dale la `.sun` un `width` y `height` de `200px`, y un `background-color` de `yellow`.

```css
.sun {
  width: 200px;
  height: 200px;
  background-color: yellow;
}
```

## Paso 26

Establezca la propiedad `position` del sol para evitar que ocupe espacio en el diseño de página y establezca el `border-radius` de modo que la forma del sol sea un círculo.

```css
.sun {
  width: 200px;
  height: 200px;
  background-color: yellow;
  position: absolute;
  border-radius: 50%;
}
```

## Paso 27

Coloque el sol en la esquina superior derecha de la pantalla a `75px` de modo que sus bordes superior y derecho queden fuera de la pantalla.

```css
.sun {
  width: 200px;
  height: 200px;
  background-color: yellow;
  position: absolute;
  border-radius: 50%;
  top: -75px;
  right: -75px;
}
```

## Paso 28

Tu pingüino constará de dos secciones principales: la cabeza y el cuerpo.

Dentro de `.penguin`, agregue dos nuevos elementos `div`. El primero con un `class` de `penguin-head`, y el segundo con un `class` de `penguin-body`.

```html
  <div class="penguin">
    <div class="penguin-head"></div>
    <div class="penguin-body"></div>
  </div>
```

## Paso 29

Cambie el nivel de pila del elemento `.penguin` de modo que aparezca delante del elemento `.ground` y asígnele una `position` de `relative`.

```css
.penguin {
  width: 300px;
  height: 300px;
  margin: auto;
  margin-top: 75px;
  z-index: 4;
  position: relative;
}
```

## Paso 30

Apunte al elemento `.penguin-head` y asígnele un `width` la mitad del de su padre y un `height` de `45%`. Luego, establece el `background` en un degradado lineal a `45deg` comenzando en `gray` y terminando en `rgb(239, 240, 228)`.

```css
.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(45deg, gray, rgb(239, 240, 228));
}
```

## Paso 31

La mayoría de los pingüinos no tienen la cabeza cuadrada.

Dale al pingüino una cabeza ligeramente ovalada estableciendo el radio de las esquinas superiores en `70%` y el radio de las esquinas inferiores en `65%`.

```css
.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(
    45deg,
    gray,
    rgb(239, 240, 228)
  );
  border-radius: 70% 70% 65% 65%;
}
```

## Paso 32

Seleccione `.penguin-body` y asígnele un `width` de `53%`, y una `height` de `45%`. Luego, establezca el `background` en un degradado lineal a `45deg`, `rgb(134, 133, 133)` desde `0%`, `rgb(234, 231, 231)` del `25%`, y `white` del `67%`.

```css
.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(45deg, rgb(134, 133, 133) 0%, rgb(234, 231, 231) 25%, white 67%);
}
```

## Paso 33

Otro dato interesante sobre los pingüinos es que no tienen cuerpos cuadrados.

Usa la propiedad `border-radius` con un valor de `80% 80% 100% 100%`, para darle al pingüino un cuerpo ligeramente redondeado.

```css
.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(
    45deg,
    rgb(134, 133, 133) 0%,
    rgb(234, 231, 231) 25%,
    white 67%
  );
 border-radius: 80% 80% 100% 100%;
}
```

## Paso 34

Diríjase a todos los elementos descendientes del elemento `.penguin` y asígneles una `position` de `absolute`.

```css
.penguin * {
 position: absolute;
}
```

## Paso 35

Coloque el elemento `.penguin-head` `10%` desde la parte superior y `25%` a la izquierda de su padre.

```css
.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(
    45deg,
    gray,
    rgb(239, 240, 228)
  );
  border-radius: 70% 70% 65% 65%;
  top: 10%;
  left: 25%;
}
```

## Paso 36

Coloque el elemento `.penguin-body` `40%` desde la parte superior, y `23.5%` desde la izquierda de su padre.

```css
.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(
    45deg,
    rgb(134, 133, 133) 0%,
    rgb(234, 231, 231) 25%,
    white 67%
  );
  border-radius: 80% 80% 100% 100%;
  top: 40%;
  left: 23.5%;
}
```

## Paso 37

Cambie el nivel de pila del elemento `.penguin-head` de modo que aparezca delante del elemento `.penguin-body`.

```css
.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(
    45deg,
    gray,
    rgb(239, 240, 228)
  );
  border-radius: 70% 70% 65% 65%;
  top: 10%;
  left: 25%;
  z-index: 1;
}
```

## Paso 38

Para darle una cresta al cuerpo del pingüino, cree un pseudoelemento que sea el primer hijo del elemento `.penguin-body`. Establezca la propiedad `content` del pseudoelemento en una cadena vacía.

```css
.penguin-body::before {
  content: "";
}
```

## Paso 39

Posiciona el pseudo-elemento relativo a su antepasado posicionado más cercano.

```css
.penguin-body::before {
  content: "";
  position: absolute;
}
```

## Paso 40

Dale al pseudo-elemento un `width` que sea la mitad del de su elemento principal, una `height` de `45%`, y un `background-color` de `gray`.

```css
.penguin-body::before {
  content: "";
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: gray;
}
```

## Paso 41

Coloque el pseudo-elemento `10%` desde la parte superior y `25%` desde la izquierda de su padre.

```css
.penguin-body::before {
  content: "";
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: gray;
  top: 10%;
  left: 25%;
}
```

## Paso 42

Redondea la cresta dando a las esquinas inferiores del pseudo-elemento un radio de `100%`, dejando las esquinas superiores en `0%`.

```css
.penguin-body::before {
  content: "";
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: gray;
  top: 10%;
  left: 25%;
  border: none;
  border-radius: 0% 0% 100% 100%;
}
```

## Paso 43

Aumenta la transparencia del pseudo-elemento en `30%`.

```css
.penguin-body::before {
  content: "";
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: gray;
  top: 10%;
  left: 25%;
  border-radius: 0% 0% 100% 100%;
  opacity: 70%;
}
```

## Paso 44

Comience la cara del pingüino, agregando dos elementos `div` dentro de `.penguin-head`, y dándoles a ambos una `class` de `face`.

```html
<div class="penguin-head">
  <div class="face"></div>
  <div class="face"></div>
</div>
```

## Paso 45

Dale a los elementos `.face` un `width` de `60%`, una `height` de `70%`, y un `background-color` de `white`.

```css
.face {
 width: 60%;
 height: 70%;
 background-color: white;
}
```

## Paso 46

Haz que las esquinas superiores de los elementos `.face` tengan un radio de `70%` y las esquinas inferiores tengan un radio de `60%`.

```css
.face {
  width: 60%;
  height: 70%;
  background-color: white;
  border: none;
  border-radius: 70% 70% 60% 60%;
}
```

## Paso 47

Coloque los elementos `.face` de modo que estén `15%` desde la parte superior.

```css
.face {
  width: 60%;
  height: 70%;
  background-color: white;
  border-radius: 70% 70% 60% 60%;
  top: 15%;
}
```

## Paso 48

Actualmente, los dos elementos `.face` están uno encima del otro.

Corrija esto, agregando un `class` de `left` al primer elemento `.face` y un `class` de `right` al segundo elemento `.face`.

```html
<div class="penguin-head">
  <div class="face left"></div>
  <div class="face right"></div>
</div>
```

## Paso 49

Apunte al elemento `.face` con la `clase` `left` y colóquelo `5%` a la izquierda de su padre.

```css
.face.left {
 left: 5%;
}
```

## Paso 50

Apunte al elemento `.face` con la clase `right` y colóquelo `5%` a la derecha de su padre.

```css
.face.right {
  right: 5%;
}
```

## Paso 51

Debajo del elemento `.face.right`, agrega un elemento `div` con una `class` de `chin`.

```html
<div class="penguin-head">
  <div class="face left"></div>
  <div class="face right"></div>
  <div class="chin"></div>
</div>
```

## Paso 52

Dirígete al elemento `.chin` y asígnale un `width` de `90%`, una `height` de `70%`, y un `background-colo`r de `white`.

```css
.chin {
  width: 90%;
  height: 70%;
  background-color: white;
}
```

## Paso 53

Coloque el elemento `.chin` de tal manera que sea `25%` desde la parte superior y `5%` desde la izquierda de su elemento primario. Luego, asigne a las esquinas superiores un radio de `70%` y a las esquinas inferiores un radio de `100%`.

```css
.chin {
  width: 90%;
  height: 70%;
  background-color: white;
  top: 25%;
  left: 5%;
  border: none;
  border-radius: 70% 70% 100% 100%;
}
```

## Paso 54

Hasta ahora, los elementos `.face` y `.chin` tienen el mismo `background-color`.

Cree una propiedad CSS personalizada llamada `--penguin-face` y establézcala en `white`.

```css
:root {
  --penguin-face: white;
}
```

## Paso 55

Cuando sea relevante, reemplace los valores de propiedad con su variable `--penguin-face`.

```css
:root {
  --penguin-face: white;
}

body {
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
  transform: skew(0deg, 44deg);
  z-index: 2;
  margin-top: 100px;
}

.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
  position: absolute;
  z-index: 1;
  transform: rotate(45deg);
  left: 110px;
  top: 225px;
}

.sun {
  width: 200px;
  height: 200px;
  background-color: yellow;
  position: absolute;
  border-radius: 50%;
  top: -75px;
  right: -75px;
}

.penguin {
  width: 300px;
  height: 300px;
  margin: auto;
  margin-top: 75px;
  z-index: 4;
  position: relative;
}

.penguin * {
  position: absolute;
}

.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(
    45deg,
    gray,
    rgb(239, 240, 228)
  );
  border-radius: 70% 70% 65% 65%;
  top: 10%;
  left: 25%;
  z-index: 1;
}

.face {
  width: 60%;
  height: 70%;
  background-color: var(--penguin-face);
  border-radius: 70% 70% 60% 60%;
  top: 15%;
}

.face.left {
  left: 5%;
}

.face.right {
  right: 5%;
}

.chin {
  width: 90%;
  height: 70%;
  background-color: var(--penguin-face);
  top: 25%;
  left: 5%;
  border-radius: 70% 70% 100% 100%;
}

.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(
    45deg,
    rgb(134, 133, 133) 0%,
    rgb(234, 231, 231) 25%,
    white 67%
  );
  border-radius: 80% 80% 100% 100%;
  top: 40%;
  left: 23.5%;
}

.penguin-body::before {
  content: "";
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: gray;
  top: 10%;
  left: 25%;
  border-radius: 0% 0% 100% 100%;
  opacity: 70%;
}

.ground {
  width: 100vw;
  height: 400px;
  background: linear-gradient(90deg, rgb(88, 175, 236), rgb(182, 255, 255));
  z-index: 3;
  position: absolute;
  margin-top: -58px;
}
```

## Paso 56

Debajo del elemento `.chin`, agrega dos elementos `div`, cada uno con una `class` de `eye`. Además, asigna al primer elemento `.eye` una `class` de `left`, y al segundo elemento `.eye` una `class` de `right`.

```html
<div class="penguin-head">
  <div class="face left"></div>
  <div class="face right"></div>
  <div class="chin"></div>
  <div class="eye left"></div>
  <div class="eye right"></div>
</div>
```

## Paso 57

Dirígete a los elementos `.eye` y asígnales un `width` de `15%`, una `height` de `17%`, y un `background-color` de `black`.

```css
.eye {
  width: 15%;
  height: 17%;
  background-color: black;
}
```

## Paso 58

Coloque los elementos `.eye` `45%` desde la parte superior de su padre, y dé a todas las esquinas un radio de `50%`.

```css
.eye {
  width: 15%;
  height: 17%;
  background-color: black;
  top: 45%;
  border: none;
  border-radius: 50%;
}
```

## Paso 59

Apunte al elemento `.eye` con la clase `left` y colóquelo `25%` desde la izquierda de su elemento primario. Luego, apunte al elemento `.eye` con la clase `right` y colóquelo `25%` desde la derecha de su padre.

```css
.eye.left {
  left: 25%;
}

.eye.right {
  right: 25%;
}
```

## Paso 60

Dentro de cada elemento `.eye`, agrega un `div` con una `class` de `eye-lid`.

```html
<div class="penguin-head">
  <div class="face left"></div>
  <div class="face right"></div>
  <div class="chin"></div>
  <div class="eye left">
    <div class="eye-lid"></div>
  </div>
  <div class="eye right">
    <div class="eye-lid"></div>
  </div>
</div>
```

## Paso 61

Dirígete a los elementos `.eye-lid` y asígnales un `width` de `150%`, una `height` de `100%`, y un `background-color` de `--penguin-face`.

```css
.eye-lid {
  width: 150%;
  height: 100%;
  background-color: var(--penguin-face);
}
```

## Paso 62

Coloca los elementos `.eye-lid` `25%` desde la parte superior, y `-23%` a la izquierda de sus padres. Luego, asigna a todas las esquinas un radio de `50%`.

```css
.eye-lid {
  width: 150%;
  height: 100%;
  background-color: var(--penguin-face);
  top: 25%;
  left: -23%;
  border: none;
  border-radius: 50%;
}
```

## Paso 63

Debajo del elemento `.eye.right`, agregue dos elementos `div` cada uno con un `class` de `blush`. También, asigna al primer elemento `.blush` una `class` de `left`, y al segundo elemento `.blush` una `class` de `right`.

```html
<div class="blush left"></div>
<div class="blush right"></div>
```

## Paso 64

Dirígete a los elementos `.blush` y asígnales un `width` de `15%`, una `height` de `10%`, y un `background-color` de `pink`.

```css
.blush {
  width: 15%;
  height: 10%;
  background-color: pink;
}
```

## Paso 65

Coloque los elementos `.blush` `65%` desde la parte superior de su elemento principal y asigne a todas las esquinas un radio de `50%`.

```css
.blush {
  width: 15%;
  height: 10%;
  background-color: pink;
  top: 65%;
  border: none;
  border-radius: 50%;
}
```

## Paso 66

Apunte al elemento `.blush` con una `class` de `left` y colóquelo `15%` a la izquierda de su padre. Luego, apunte al elemento `.blush` con una `class` de `right`, y colóquelo `15%` a la derecha de su padre.

```css
.blush.left {
  left: 15%;
}

.blush.right {
  right: 15%;
}
```

## Paso 67

Debajo del elemento `.blush.right`, agregue dos elementos `div` cada uno con una `class` de `beak`. También, asigna al primer elemento .`beak` una `class` de `top`, y al segundo elemento `.beak` una `class` de `bottom`.

```html
<div class="beak top"></div>
<div class="beak bottom"></div>
```

## Paso 68

Dirígete a los elementos `.beak`, asígnales una `height` de `10%`, un `background-color` de `orange`, y da a todas sus esquinas un radio de `50%`.

```css
.beak {
  height: 10%;
  background-color: orange;
  border: none;
  border-radius: 50%;
}
```

## Paso 69

Dirígete al elemento `.beak` con una `class` de `top`, asígnale un `width` de `20%`, y posiciónalo a `60%` desde la parte superior y a `40%` desde la izquierda de su elemento principal.

```css
.beak.top {
  width: 20%;
  top: 60%;
  left: 40%;
}
```

## Paso 70

Dirígete al elemento `.beak` con una `class` de `bottom`, asígnale un `width` que sea un `4%` más pequeño que el de `.beak.top`, y posiciónalo a `5%` más abajo desde la parte superior, y a `2%` más hacia la izquierda de su elemento principal que el de ``.beak.top``.

```css
.beak.top {
  width: 20%;
  top: 60%;
  left: 40%;
}

.beak.bottom {
  width: 16%;
  top: 65%;
  bottom: 5%;
  left: 42%;
}
```

## Paso 71

El cuerpo del pingüino se ve un poco simple. Arréglalo agregando un elemento `div` con una `class` de `shirt`, inmediatamente antes del elemento `.penguin-body`.

```html
<div class="shirt"></div>
```

## Paso 72

Dentro del elemento `.shirt`, agrega un `div` con el siguiente emoji como contenido: 💜

```html
<div class="shirt">
  <div>💜</div>
</div>
```

## Paso 73

Dentro de `.shirt`, después del elemento `div`, agregue un elemento `p` con el siguiente contenido: `I CSS`

```html
<div class="shirt">
  <div>💜</div>
  <p>I CSS</p>
</div>
```

## Paso 74

Dirígete al elemento `.shirt`, asígnale un `font-size` de `25px`, una `font-family` de `Helvetica` con una opción de reserva de `sans-serif`, y un `font-weight` de `bold`.

```css
.shirt {
  font-size: 25px;
  font-family: "Helvetica", sans-serif;
  font-weight: bold;
}
```

## Paso 75

En algunos navegadores, el emoji corazón puede verse ligeramente diferente al paso anterior. Esto se debe a que algunas de las propiedades del carácter fueron anuladas por el estilo `font-weight` de `bold`.

Solucione esto, apuntando al `div` con el emoji del corazón y estableciendo su `font-weight` a su valor original.

```css
.shirt {
  font: bold 25px Helvetica, sans-serif;
}

.shirt div {
  font-weight: normal;
}
```

## Paso 76

Coloca el `div` con el emoji del corazón `22.5px` desde la parte superior, y `12px` a la izquierda de su padre.

```css
.shirt {
  font: bold 25px Helvetica, sans-serif;
}

.shirt div {
  font-weight: initial;
  top: 22.5px;
  left: 12px;
}
```

## Paso 77

Coloque el elemento `.shirt` `165px` desde la parte superior y `127.5px` desde la izquierda de su elemento primario. Luego, aumente su orden de apilamiento de modo que aparezca encima del elemento `.penguin-body`.

```css
.shirt {
  font: bold 25px Helvetica, sans-serif;
  top: 165px;
  left: 127.5px;
  z-index: 1;
}

.shirt div {
  font-weight:  initial;
  top: 22.5px;
  left: 12px;
}
```

## Paso 78

Para el toque final de la camiseta, configura el `color` en `#6a6969`.

```css
.shirt {
  font: bold 25px Helvetica, sans-serif;
  top: 165px;
  left: 127.5px;
  z-index: 1;
  color: #6a6969;
}

.shirt div {
  font-weight:  initial;
  top: 22.5px;
  left: 12px;
}
```

## Paso 79

Dato curioso: los pingüinos no pueden pararse sin al menos dos pies.

Dentro del elemento `.penguin-body`, agregue dos elementos div cada uno con una `class` de `foot`. Dale al primer `.foot` una `class` de `left`, y al segundo `.foot` una `class` de `right`.

```html
<div class="penguin-body">
  <div class="foot left"></div>
  <div class="foot right"></div>
</div>
```

## Paso 80

Dirígete a los elementos `.foot` y asígnales un `width` de `15%`, una `height` de `30%`, y un `background-color` de `orange`.

```css
.foot {
  width: 15%;
  height: 30%;
  background-color: orange;
}
```

## Paso 81

Coloque los elementos `.foot` `85%` desde la parte superior de su elemento principal y asigne a todas las esquinas un radio de `50%`.

```css
.foot {
  width:  15%;
  height: 30%;
  background-color: orange;
  top: 85%;
  border: none;
  border-radius: 50%;
}
```

## Paso 82

El pico y las patas del pingüino comparten el mismo `color`.

Crea una nueva variable CSS personalizable llamada `--penguin-picorna` y reemplaza todos los valores de propiedades que sean relevantes también.

```css
:root {
  --penguin-face: white;
 --penguin-picorna: orange;
}

body {
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
  transform: skew(0deg, 44deg);
  z-index: 2;
  margin-top: 100px;
}

.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
  position: absolute;
  z-index: 1;
  transform: rotate(45deg);
  left: 110px;
  top: 225px;
}

.sun {
  width: 200px;
  height: 200px;
  background-color: yellow;
  position: absolute;
  border-radius: 50%;
  top: -75px;
  right: -75px;
}

.penguin {
  width: 300px;
  height: 300px;
  margin: auto;
  margin-top: 75px;
  z-index: 4;
  position: relative;
}

.penguin * {
  position: absolute;
}

.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(
    45deg,
    gray,
    rgb(239, 240, 228)
  );
  border-radius: 70% 70% 65% 65%;
  top: 10%;
  left: 25%;
  z-index: 1;
}

.face {
  width: 60%;
  height: 70%;
  background-color: var(--penguin-face);
  border-radius: 70% 70% 60% 60%;
  top: 15%;
}

.face.left {
  left: 5%;
}

.face.right {
  right: 5%;
}

.chin {
  width: 90%;
  height: 70%;
  background-color: var(--penguin-face);
  top: 25%;
  left: 5%;
  border-radius: 70% 70% 100% 100%;
}

.eye {
  width: 15%;
  height: 17%;
  background-color: black;
  top: 45%;
  border-radius: 50%;
}

.eye.left {
  left: 25%;
}

.eye.right {
  right: 25%;
}

.eye-lid {
  width: 150%;
  height: 100%;
  background-color: var(--penguin-face);
  top: 25%;
  left: -23%;
  border-radius: 50%;
}

.blush {
  width: 15%;
  height: 10%;
  background-color: pink;
  top: 65%;
  border-radius: 50%;
}

.blush.left {
  left: 15%;
}

.blush.right {
  right: 15%;
}

.beak {
  height: 10%;
  background-color: var(--penguin-picorna);
  border-radius: 50%;
}

.beak.top {
  width: 20%;
  top: 60%;
  left: 40%;
}

.beak.bottom {
  width: 16%;
  top: 65%;
  left: 42%;
}

.shirt {
  font: bold 25px Helvetica, sans-serif;
  top: 165px;
  left: 127.5px;
  z-index: 1;
  color: #6a6969;
}

.shirt div {
  font-weight:  initial;
  top: 22.5px;
  left: 12px;
}

.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(
    45deg,
    rgb(134, 133, 133) 0%,
    rgb(234, 231, 231) 25%,
    white 67%
  );
  border-radius: 80% 80% 100% 100%;
  top: 40%;
  left: 23.5%;
}

.penguin-body::before {
  content: "";
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: gray;
  top: 10%;
  left: 25%;
  border-radius: 0% 0% 100% 100%;
  opacity: 70%;
}

.foot {
  width:  15%;
  height: 30%;
  background-color: var(--penguin-picorna);
  top: 85%;
  border-radius: 50%;
}
```

## Paso 83

Dirígete al elemento `.foot` con una `class` de `left`, y posiciónalo a `25%` desde la izquierda de su elemento principal. Luego, apunte al elemento `.foot` con una `class` de `right`, y colóquelo `25%` a la derecha de su padre.

```css
.foot {
  width:  15%;
  height: 30%;
  background-color: var(--penguin-picorna);
  top: 85%;
  border-radius: 50%;
}

.foot.left {
  left: 25%;
}

.foot.right {
  right: 25%;
}
```

## Paso 84

Para que las patas del pingüino se vean más penguiny, gira el pie izquierdo por `80deg`, y el derecho por `-80deg`.

```css
.foot.left {
  left: 25%;
  transform: rotate(80deg);
}

.foot.right {
  right: 25%;
  transform: rotate(-80deg);
}
```

## Paso 85

Cambia el orden de apilamiento de los elementos `.foot` de modo que aparezcan debajo del elemento `.penguin-body`.

```css
.foot {
  width:  15%;
  height: 30%;
  background-color: var(--penguin-picorna);
  top: 85%;
  border-radius: 50%;
  z-index: -1;
}
```

## Paso 86

Dato curioso: los pingüinos no pueden volar sin alas.

Dentro de `.penguin-body`, antes de los elementos `.foot`, agregue dos elementos `div` cada uno con un `class` de `arm`. Dé al primer `.arm` un `class` de `left`, y al segundo `.arm` un `class` de `right`.

```html
<div class="penguin-body">
  <div class="arm left"></div>
  <div class="arm right"></div>
  <div class="foot left"></div>
  <div class="foot right"></div>
</div>
```

## Paso 87

Dirígete a los elementos `.arm`, asígnales un `width` de `30%`, una `height` de `60%`, y un `background` de un gradiente lineal a `90deg` en sentido horario, comenzando con `gray` y terminando en `rgb(209, 210, 199)`.

```css
.arm {
  width: 30%;
  height: 60%;
  background: linear-gradient(90deg, gray, rgb(209, 210, 199));
}
```

## Paso 88

Cree una variable CSS personalizada llamada --penguin-skin y configúrela en gray. Luego, vuelva a colocar todos los valores de la propiedad con ella.

```css
:root {
  --penguin-face: white;
  --penguin-picorna: orange;
 --penguin-skin: gray;
}

body {
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
  transform: skew(0deg, 44deg);
  z-index: 2;
  margin-top: 100px;
}

.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
  position: absolute;
  z-index: 1;
  transform: rotate(45deg);
  left: 110px;
  top: 225px;
}

.sun {
  width: 200px;
  height: 200px;
  background-color: yellow;
  position: absolute;
  border-radius: 50%;
  top: -75px;
  right: -75px;
}

.penguin {
  width: 300px;
  height: 300px;
  margin: auto;
  margin-top: 75px;
  z-index: 4;
  position: relative;
}

.penguin * {
  position: absolute;
}

.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(
    45deg,
    var(--penguin-skin),
    rgb(239, 240, 228)
  );
  border-radius: 70% 70% 65% 65%;
  top: 10%;
  left: 25%;
  z-index: 1;
}

.face {
  width: 60%;
  height: 70%;
  background-color: var(--penguin-face);
  border-radius: 70% 70% 60% 60%;
  top: 15%;
}

.face.left {
  left: 5%;
}

.face.right {
  right: 5%;
}

.chin {
  width: 90%;
  height: 70%;
  background-color: var(--penguin-face);
  top: 25%;
  left: 5%;
  border-radius: 70% 70% 100% 100%;
}

.eye {
  width: 15%;
  height: 17%;
  background-color: black;
  top: 45%;
  border-radius: 50%;
}

.eye.left {
  left: 25%;
}

.eye.right {
  right: 25%;
}

.eye-lid {
  width: 150%;
  height: 100%;
  background-color: var(--penguin-face);
  top: 25%;
  left: -23%;
  border-radius: 50%;
}

.blush {
  width: 15%;
  height: 10%;
  background-color: pink;
  top: 65%;
  border-radius: 50%;
}

.blush.left {
  left: 15%;
}

.blush.right {
  right: 15%;
}

.beak {
  height: 10%;
  background-color: var(--penguin-picorna);
  border-radius: 50%;
}

.beak.top {
  width: 20%;
  top: 60%;
  left: 40%;
}

.beak.bottom {
  width: 16%;
  top: 65%;
  left: 42%;
}

.shirt {
  font: bold 25px Helvetica, sans-serif;
  top: 165px;
  left: 127.5px;
  z-index: 1;
  color: #6a6969;
}

.shirt div {
  font-weight:  initial;
  top: 22.5px;
  left: 12px;
}

.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(
    45deg,
    rgb(134, 133, 133) 0%,
    rgb(234, 231, 231) 25%,
    white 67%
  );
  border-radius: 80% 80% 100% 100%;
  top: 40%;
  left: 23.5%;
}

.penguin-body::before {
  content: "";
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: var(--penguin-skin);
  top: 10%;
  left: 25%;
  border-radius: 0% 0% 100% 100%;
  opacity: 70%;
}

.arm {
  width: 30%;
  height: 60%;
  background: linear-gradient(
    90deg,
    var(--penguin-skin),
    rgb(209, 210, 199)
  );
}
```

## Paso 89

Dirígete al elemento `.arm` con una `class` de `left`, y posiciónalo a `35%` desde la parte superior y a `5%` desde la izquierda de su elemento principal. Luego, apunte al elemento `.arm` con una `class` de `right`, y colóquelo `0%` desde la parte superior, y `-5%` desde la derecha de su padre.

```css
.arm.left {
  top: 35%;
  left: 5%;
}

.arm.right {
  top: 0%;
  right: -5%;
}
```

## Paso 90

Dentro del selector `.arm.left`, modifique el origen de la función `transform` para que sea la esquina superior izquierda de su padre.

```css
.arm.left {
  top: 35%;
  left: 5%;
  transform-origin: 0% 0%;
}

.arm.right {
  top: 0%;
  right: -5%;
}
```

## Paso 91

Para mantener el degradado lineal en el lado correcto del brazo izquierdo del pingüino, primero gírelo `130deg` y luego invierta el eje x.

```css
.arm.left {
  top: 35%;
  left: 5%;
  transform-origin: top left; 
  transform: rotate(130deg) scaleX(-1);
}
```

## Paso 92

Gire el brazo derecho `45deg`en sentido contrario a las agujas del reloj.

```css
.arm.right {
  top: 0%;
  right: -5%;
  transform: rotate(-45deg);
}
```

## Paso 93

Dato curioso: la mayoría de las aletas, si no todas, no son naturalmente rectangulares.

Del elemento `.arm` a las esquinas superior-izquierda, superior-derecha e inferior-derecha un radio del `30%`, y la esquina inferior-izquierda un radio del `120%`.

```css
.arm {
  width: 30%;
  height: 60%;
  background: linear-gradient(
    90deg,
    var(--penguin-skin),
    rgb(209, 210, 199)
  );
  border: none;
  border-radius: 30% 30% 30% 120%;
}
```

## Paso 94

Cambia el orden de apilamiento de los elementos `.arm`para que aparezcan detrás del elemento `.penguin-body`.

```css
.arm {
  width: 30%;
  height: 60%;
  background: linear-gradient(
    90deg,
    var(--penguin-skin),
    rgb(209, 210, 199)
  );
  border-radius: 30% 30% 30% 120%;
  z-index: -1;
}
```

## Paso 95

Ahora, vas a usar animaciones CSS para hacer que el pingüino se agite.

Defina un nuevo `@keyframes` llamado `wave`.

```css
@keyframes wave {
 
}
```

## Paso 96

Asigne a `wave` cuatro puntos de ruta que comiencen en `10%` e incrementen en `10%`.

```css
@keyframes wave {
 10%{}
 20%{}
 30%{}
 40%{}
}
```

## Paso 97

Dentro del primer punto de referencia, gire a `110deg` y mantenga la escala del brazo izquierdo.

```css
@keyframes wave {
  10% {
  transform: rotate(110deg) scaleX(-1);
    
  }
  20% {

  }
  30% {

  }
  40% {

  }
}
```

## Paso 98

Dentro del segundo punto de referencia, gire a `130deg`, y conserve la escala del brazo izquierdo.

```css
@keyframes wave {
  10% {
    transform: rotate(110deg) scaleX(-1);
  }
  20% {
    transform: rotate(130deg) scaleX(-1);
  }
  30% {

  }
  40% {

  }
}
```

## Paso 99

Para el tercer y cuarto waypoints, repita el patrón `transform` una vez más.

```css
@keyframes wave {
  10% {
    transform: rotate(110deg) scaleX(-1);
  }
  20% {
    transform: rotate(130deg) scaleX(-1);
  }
  30% {
    transform: rotate(110deg) scaleX(-1); 
  }
  40% {
    transform: rotate(130deg) scaleX(-1);
  }
}
```

## Paso 100

Usa la animación `wave` en el brazo izquierdo. Haga que la animación dure `3s`, itere infinitamente y tenga una función de tiempo lineal.

```css
.arm.left {
  top: 35%;
  left: 5%;
  transform-origin: top left; 
  transform: rotate(130deg) scaleX(-1);
  animation: wave 3s infinite;
  animation-timing-function: linear;
} 
```

## Paso 101

Apunte al elemento `.penguin` cuando esté activo y aumente su tamaño en `50%` en ambas dimensiones.

```css
.penguin:active {
 transform: scale(1.5);
}
```

## Paso 102

Cuando activa el elemento `.penguin`, puede parecer que puede arrastrarlo. Esto no es cierto.

Indíquelo a los usuarios, dando al elemento activo una propiedad `cursor` de `not-allowed`.

```css
.penguin:active {
  transform: scale(1.5);
  cursor: not-allowed;
}
```

## Paso 103

Cambie el comportamiento del `transition` del elemento `.penguin` durante la transformación para que tenga una duración de `1s`, una función de temporización de `ease-in-out` y un retraso de `0ms`.

```css
.penguin {
  width: 300px;
  height: 300px;
  margin: auto;
  margin-top: 75px;
  z-index: 4;
  position: relative;
  transition: 1s ease-in-out;
  transition-delay: 0ms;
}
```

## Paso 104

Finalmente, calcule que el `height` del elemento `.ground` sea el alto de la ventana gráfica menos el alto del elemento `.penguin`.

¡**Felicidades! Has completado la certificación de Diseño Web Adaptivo.**

```css
.ground {
  width: 100vw;
  height: calc(100vh - 300px);
  background: linear-gradient(90deg, rgb(88, 175, 236), rgb(182, 255, 255));
  z-index: 3;
  position: absolute;
  margin-top: -58px;
}
```
