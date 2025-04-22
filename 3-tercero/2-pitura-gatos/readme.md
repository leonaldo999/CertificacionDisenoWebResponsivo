# Aprende CSS Intermedio haciendo una pitura de gatos

Dominar la posición CSS es esencial para crear diseños web visualmente atractivos y receptivos

En este curso construirás una pintura para gatos, aprenderás cómo trabajar con la posición absoluta, la propiedad z-index y la propiedad transform.

## Paso 1

Empieza con la estructura básica de HTML. Añade una referencia `DOCTYPE` de `html` y un elemento `html` con su atributo `lang` establecido en `en`. Además, agrega un `head` y un elemento `body` dentro del elemento `html`.

```css
<!DOCTYPE html>
<html lang="en">
<head>
  
</head>
<body>
  
</body>
</html>
```

## Paso 2

Dentro de tu elemento `head`, añade una etiqueta `meta` con el atributo `charset de utf-8`. Añade también un elemento `title` con el texto `fCC Cat Painting`.

```css
  <meta charset="UTF-8">
  <title>fCC Cat Painting</title>
```

## Paso 3

Agrega un elemento `link` dentro de tu elemento `head`. Para ese elemento `link`, establece el atributo `rel` a `stylesheet` y el `href` a `./styles.css`.

```css
<link rel="stylesheet" href="./styles.css">
```

## Paso 4

Usa el selector universal para agregar `box-sizing: border-box;` a tu CSS. Esto asegura que los elementos incluyan padding y bordes en sus anchos y largos especificados.

```css
* {
  box-sizing: border-box;
}
```

## Paso 5

Dale a tu elemento `body` un `background-color` de `#c9d2fc`.

```css
body {
  background-color: #c9d2fc;
}
```

## Paso 6

Dentro de tu HTML, crea un elemento `main`. Dentro de ese elemento `main`, añade un elemento `div` con la clase `cat-head`.

```css
<main>
  <div class="cat-head"></div>
</main>
```

## Paso 7

Usando un selector de clase, da al elemento `.cat-head` un ancho de `205px` y una altura de 180px. Además, dale un borde de `1px solid #000` y un `border-radius` del `46%`.

```css
.cat-head {
  width: 205px;
  height: 180px;
  border: 1px solid #000;
  border-radius: 46%;
}
```

## Paso 8

Para ver el elemento `.cat-head`, dale un fondo de gradiente lineal con `#5e5e5e` al `85%` y `#45454f` al `100%`.

Es posible que no notes la diferencia entre estos dos colores, pero están ahí.

```css
.cat-head {
  width: 205px;
  height: 180px;
  border: 1px solid #000;
  border-radius: 46%;
  background: linear-gradient(#5e5e5e 85%, #45454f 100%);
}
```

## Paso 9

El posicionamiento CSS te permite establecer cómo quieres posicionar un elemento en el navegador. Tiene una propiedad position a la que puedes dar un valor `static`, `absolute`, `relative`, `sticky` o `fixed`.

Una vez que estableces la propiedad `position` del elemento, puedes mover éste indicando un píxel o un valor porcentual para una o más de las propiedades `top`, `right`, `left` o `bottom`.

`static` es la posición predeterminada para todos los elementos. Si la asignas a un elemento, no podrás moverlo con `top`, `right`, `left`, o `bottom`.

Dale a `.cat-head` una propiedad `position` de `static`, luego establece las propiedades `top` y `left` a `100px` cada una.

```css
.cat-head {
  position: static;
  top: 100px;
  left: 100px;


  background: linear-gradient(#5e5e5e 85%, #45454f 100%);
  width: 205px;
  height: 180px;
  border: 1px solid #000;
  border-radius: 46%;
}
```

## Paso 10

Puedes ver que no sucede nada. El elemento `.cat-head` no se movió a pesar de establecer un `top` y un `left` de `100px` cada uno. Pero ese no es el caso con el posicionamiento `relative`.

Cuando usas el valor `relative`, el elemento todavía está posicionado acorde con el flujo normal del documento, pero los valores `top`, `left`, `bottom`, y `right` se activan.

En lugar de `static`, dale a tu `.cat-head` una posición de `relative`, y deja las propiedades `top` y `left` tal como están.

```css
  position: relative;
  top: 100px;
  left: 100px;
```

## Paso 11

La siguiente propiedad de posición es `absolute`. Cuando usas el valor `absolute` para tu propiedad `position`, el elemento se saca del flujo normal del documento, y luego su posición es determinada por las propiedades `top`, `right`, `bottom`, y `left`.

Establece la propiedad `position` de tu elemento `.cat-head` en `absolute` y, después, establece las propiedades `top` e `left` en cualquier valor de píxel positivo.

```css
  position: absolute;
  top: 100px;
  left: 100px;
```

## Paso 12

`fixed` es un valor de la propiedad `position` que te permite hacer un elemento fijado a la página sin importar dónde el usuario se desplace en la página.

Tendrás que hacer más marcas para ver como funciona el posicionamiento `fixed`. En tu HTML, crea un elemento `div` con la clase `box`.

```html
    <div class="box"></div>
```

## Paso 13

Usa un selector de clase para darle a tu elemento `.box` un ancho de `200px`, una altura de `600px`, y un color de fondo de `#000`. También, dale un `position` de `absolute`, un `top` de `800px` y un `left` de `650px`.

```css
.box {
  width: 200px;
  height: 600px;
  background-color: #000;
  position: absolute;
  top: 800px;
  left: 650px;
}
```

## Paso 14

Ahora reemplaza el valor de la propiedad position de tu .cat-head con fixed. Deja top y left como están.

Después de eso, desplázate hacia arriba y abajo para ver cómo funciona el valor fixed.

```css
  position: fixed;
  top: 100px;
  left: 100px;
```

## Paso 15

El último valor de la propiedad de posición es `sticky`. El posicionamiento `sticky` es un híbrido de los posicionamientos `relative` y `fixed`. Permite a un elemento **pegarse** a una posición específica dentro de su elemento contenedor o ventana, basada en la posición del desplazamiento.

Cambia el valor de la propiedad `position` de `.cat-head` a `sticky`, establece `top` a `0`, luego elimina `left` y su valor.

>[!NOTE]
>
>Para ver como `sticky` funciona, tienes que colocar un par de textos antes y despues de tu elemento `.cat-head` `div`. Si haces scroll hacia abajo después de eso, verás que `.cat-head` se queda pegado en la parte superior y permanece allí.

```css
  position: sticky;
  top: 0;
```

## Paso 16

Ahora debes centrar la cabeza del gato.

Asigne al elemento `.cat-head` una propiedad de `position` `absolute`. Establece un valor de `0` para las propiedades `right`, `left`, `top` y `bottom`, luego establece su propiedad `margin` en todos los lados a `auto`. Esa es una manera de centrar un elemento vertical y horizontalmente usando posicionamiento CSS.

```css
  position: absolute;
  right: 0;
  left: 0;
  top: 0;
  bottom: 0;
  margin: auto;
```

## Paso 17

Elimina el elemento `div` con clase `box` porque ya no lo necesitas.

```html
<!-- 
 Se elimina 

  <div class="box"></div>
 -->
```

## Paso 18

También, elimina la regla CSS de `.box` y sus declaraciones porque ya no los necesitas.

```css
/* 
sE ELIMINA

.box {
  width: 200px;
  height: 600px;
  background-color: #000;
  position: absolute;
  top: 800px;
  left: 650px;
}
*/
```

## Paso 19

Ahora deberías trabajar en las orejas del gato. Habrá una oreja derecha y otra izquierda y dentro de cada una, habrá a oreja interior.

Dentro de tu elemento `.cat-head`, crea un elemento `div` con la clase `cat-ears`.

```html
    <div class="cat-head">
      <div class="cat-ears"></div>
    </div>
```

## Paso 20

Dentro de tu elemento `.cat-ears`, crea dos elementos `div` con las clases `cat-left-ear` y `cat-right-ear` respectivamente.

```html
      <div class="cat-ears">
        <div class="cat-left-ear"></div>
        <div class="cat-right-ear"></div>
      </div>
```

## Paso 21

Crea dos elementos `div`, el primero, dentro del elemento `.cat-left-ear`, con una clase `cat-left-inner-ear` y el segundo, dentro del elemento `.cat-right-ear`, con una clase `cat-right-inner-ear`.

```html
  <div class="cat-left-ear">
    <div class="cat-left-inner-ear"></div>
  </div>
  <div class="cat-right-ear">
    <div class="cat-right-inner-ear"></div>
  </div>
```

## Paso 22

Ahora aprenderás un truco CSS para dibujar triángulos.

Se utilizará para dibujar las orejas del gato.

Mediante un selector de clase, asigna al elemento `.cat-right-ear` las propiedades `height` y `width` establecidas en `100px`. Establece el `background-color` a `white`. Establece los bordes izquierdo y derecho en `35px solid blue`. Establece los bordes superior e inferior en `35px solid red`.

```css
.cat-right-ear {
  height: 100px;
  width: 100px;
  background-color: white;
  border-left: 35px solid blue;
  border-right: 35px solid blue;
  border-top: 35px solid red;
  border-bottom: 35px solid red;
}
```

## Paso 23

Observa que ahora tienes un cuadrado blanco con bordes gruesos. Los bordes tienen esquinas diagonales que pueden utilizarse para crear triángulos.

Dentro del mismo selector de clase ajusta la `height` y la `width` a `0`. Establece los bordes izquierdo, derecho y superior como `transparent`.

Elimina la propiedad `background-color`, y debes ver un triángulo.

```css
.cat-right-ear {
  height: 0;
  width: 0;
  border-left: 35px solid transparent;
  border-right: 35px solid transparent;
  border-top: 35px solid transparent;
  border-bottom: 35px solid red;
}
```

## Paso 24

Ahora puedes empezar a trabajar en las orejas de tu gato.

Limpia tu código de revisión eliminando el selector `.cat-right-ear` y todas sus propiedades.

Utilizando un selector de clase, da al elemento `.cat-left-ear` un borde izquierdo y derecho de `35px solid transparent` a cada uno. También, establece el borde inferior a `70px solid #5e5e5e`.

```css
.cat-left-ear {
  border-left: 35px solid transparent;
  border-right: 35px solid transparent;
  border-bottom: 70px solid #5e5e5e;
}
```

## Paso 25

Mueve la oreja izquierda a la posición estableciento una posición de `absolute`, un `top` de `-26px`, y un `left` de `-31px`.

```css
.cat-left-ear {
  position: absolute;
  top: -26px;
  left: -31px;

  border-left: 35px solid transparent;
  border-right: 35px solid transparent;
  border-bottom: 70px solid #5e5e5e;
}
```

## Paso 26

Esos bordes son demasiado afilados para una oreja. Por lo tanto, ajusta el `border-top-left-radius` a `90px` y el `border-top-right-radius` a `10px`.

```ccs
  border-top-left-radius: 90px;
  border-top-right-radius: 10px;
```

## Paso 27

Para posicionar la oreja izquierda adecuadamente, puedes utilizar CSS transform para rotarla en cierto grado.

La propiedad `transform` te permite modificar la forma, posición, y tamaño de un elemento sin cambiar el diseño o afectar a los elementos en su alrededor. Posee funciones como `translate()`, `rotate()`, `scale()`, `skew()`, y `matrix()`.

Establece la propiedad `transform` a `rotate(-45deg)` y mira lo que sucede.

```css
 transform: rotate(-45deg);
```

## Paso 28

Ahora puedes trabajar en la oreja derecha del gato. Ya tienes el HTML para ello.

Usando un selector de clase, dale al elemento `.cat-right-ear` un borde izquierdo y derecho de `35px solid transparent` cada uno. También, ajusta el borde inferior a `70px solid #5e5e5e`.

```css
.cat-right-ear {
  border-left: 35px solid transparent;
  border-right: 35px solid transparent;
  border-bottom: 70px solid #5e5e5e;
}
```

## Paso 29

Mueve la oreja derecha a la posición con una propiedad `position` establecida a `absolute`, un `top` de `-26px`, y un `left` de `163px`.

```css
  position: absolute;
  top: -26px;
  left: 163px;
```

## Paso 30

Como hiciste con la oreja izquierda, rote la oreja derecha a 45 grados.

```css
  transform: rotate(45deg);
```

## Paso 31

Elimina el borde afilado de la oreja derecha estableciendo el `border-top-left-radius` a `90px` y el `border-top-right-radius` a `10px`.

```css
  border-top-left-radius: 90px;
  border-top-right-radius: 10px;
```

## Paso 32

Las orejas siempre deben de colocarse sobre la parte de la cabeza que superpone. Puedes hacer esto con la propiedad `z-index`.

`z-index` es una propiedad que puedes usar para definir el orden de la superposición de elementos HTML. Cualquier elemento con un `z-index` mayor siempre será colocado sobre un elemento con un `z-index` menor.

Para ver a `z-index` en acción, dale a la propiedad `z-index` de la oreja izquierda (left ear) un valor dé `-1`.

```css
  z-index: -1;
```

## Paso 33

Ese no es el comportamiento que quieres. Debes hacer que las orejas se muestren sobre la cabeza para que los bordes que se superponen con ellos no se muestren.

En lugar de `-1`, ajusta la propiedad `z-index` de la oreja izquierda a `1`.

```css
  z-index: 1;
```

## Paso 34

Dale a la propiedad `z-index` de la oreja derecha (`right ear`) un valor de `1` para que siempre permanezca sobre la cabeza.

```css
  z-index: 1;
```

## Paso 35

La mayoría de los gatos tienen colores diferentes en su oreja y la parte interior de la misma oreja. También puedes implementar lo mismo. Por eso definiste un elemento `div` para las orejas interiores derecha e izquierda hace un momento.

Usando un selector de clase, dale a tu elemento .`cat-left-inner-ear` un borde izquierdo y derecho de `20px solid transparent` cada uno. También dale un borde inferior de `40px solid #3b3b4f`.

```css
.cat-left-inner-ear {
  border-left: 20px solid transparent;
  border-right: 20px solid transparent;
  border-bottom: 40px solid #3b3b4f;
}
```

## Paso 36

Mueve el interior de la oreja a la posición con una propiedad `position` establecida en `absolute`, un `top` de `22px`, y un `left` de `-20px`.

```css
  position: absolute;
  top: 22px;
  left: -20px;
```

## Paso 37

Para quitar todos los bordes puntiagudos de la oreja, establece un radio del borde inferior derecho e inferior izquierdo a `40%` cada uno, un radio del borde superior izquierdo de `90px`, y un radio del borde superior derecho de `10px`.

```css
  border-bottom-right-radius: 40%;
  border-bottom-left-radius: 40%;
  border-top-left-radius: 90px;
  border-top-right-radius: 10px;
```

## Paso 38

Es hora de trabajar en la oreja interior derecha. Usando un selector de clase, dale a tu elemento `.cat-right-inner-ear` un borde izquierdo y derecho de `20px solid transparent`. También, dale un borde inferior de `40px solid #3b3b4f`.

```css
.cat-right-inner-ear {
  border-left: 20px solid transparent;
  border-right: 20px solid transparent;
  border-bottom: 40px solid #3b3b4f;
}
```

## Paso 39

Mueve la oreja interior derecha a la posición con una propiedad `position` establecida en `absolute`, un `top` de `22px` y un `left` de `-20px`.

```css
.cat-right-inner-ear {
  position: absolute;
  top: 22px;
  left: -20px;

  border-left: 20px solid transparent;
  border-right: 20px solid transparent;
  border-bottom: 40px solid #3b3b4f;
}
```

## Paso 40

Como hiciste para oreja interior izquierda, quita los bordes afilados de la oreja interior derecha estableciendo un radio del borde inferior derecho e inferior izquierdo de `40%`, un radio del borde superior izquierdo de `90px`, y un radio del borde superior derecho de `10px`.

```css
.cat-right-inner-ear {
  position: absolute;
  top: 22px;
  left: -20px;

  border-bottom-right-radius: 40%;
  border-bottom-left-radius: 40%;
  border-top-left-radius: 90px;
  border-top-right-radius: 10px;

  border-left: 20px solid transparent;
  border-right: 20px solid transparent;
  border-bottom: 40px solid #3b3b4f;
}
```

## Paso 41

Ahora empezarás a trabajar en los ojos del gato. Al igual que las orejas, los ojos tendrán ojos internos.

Crea un elemento div con la clase cat-eyes. Dentro del elemento .cat-eyes, crea dos elementos `div` con las clases `cat-left-eye` y `cat-right-eye` respectivamente.

```html
<div class="cat-eyes">
  <div class="cat-left-eye"></div>
  <div class="cat-right-eye"></div>
</div>
```

## Paso 42

Crea dos elementos `div`, uno con la clase `cat-left-inner-eye` dentro del elemento `.cat-left-eye` y otro con la clase `cat-right-inner-eye` dentro del elemento `.cat-right-eye`.

```html
  <div class="cat-left-eye">
    <div class="cat-left-inner-eye"></div>
  </div>
  <div class="cat-right-eye">
    <div class="cat-right-inner-eye"></div>
  </div>
```

## Paso 43

Usando un selector de clase, dale a tu elemento `.cat-left-eye` un `width` de `30px` y un `height` de `40px`. También, dale un `background-color` de `#000`.

```css
.cat-left-eye {
  width: 30px;
  height: 40px;
  background-color: #000;
}
```

## Paso 44

Mueve el ojo izquierdo (left eye) a la posición correcta con una propiedad `position` con el valor `absolute`, un `top` con el valor `54px`, y un `left` con el valor `39px`.

```css
.cat-left-eye {
  position: absolute;
  top: 54px;
  left: 39px;

  width: 30px;
  height: 40px;
  background-color: #000;
}
```

## Paso 45

Para hacer que el ojo izquierdo parezca un ojo, dale un radio de borde de `60%`. Además, usando la propiedad `transform`, gíralo `25` grados.

```css
.cat-left-eye {
  position: absolute;
  top: 54px;
  left: 39px;

  border-radius: 60%;
  transform: rotate(25deg);

  width: 30px;
  height: 40px;
  background-color: #000;
}
```

## Paso 46

Ahora trabajarás en el ojo derecho utilizando el mismo enfoque.

Usando un selector de clase, dale a tu elemento `.cat-right-eye` un ancho de `30px` y una altura de `40px`. También, dale un color de fondo de `#000`.

```css
.cat-right-eye {
  width: 30px;
  height: 40px;
  background-color: #000;
}

```

## Paso 47

Mueve el ojo derecho a la posición correcta con una propiedad `position` de `absolute`, `top` de `54px`, y `left` de `134px`.

```css
.cat-right-eye {
  position: absolute;
  top: 54px;
  left: 134px;

  width: 30px;
  height: 40px;
  background-color: #000;
}
```

## Paso 48

Para hacer que el ojo derecho parezca un ojo, dale un radio de borde de `60%`. También, usando la propiedad `transform`, rótalo a `-25` grados.

```css
.cat-right-eye {
  position: absolute;
  top: 54px;
  left: 134px;

  border-radius: 60%;
  transform: rotate(-25deg);

  width: 30px;
  height: 40px;
  background-color: #000;
}
```

## Step 49

Those look like eyes, but you can still make them better. That's why you created two inner eyes `div` elements.

Using a class selector, give your `.cat-left-inner-eye` element a width of `10px` and a height of `20px`. Also, give it a background color of `#fff`.

```css
.cat-left-inner-eye {
  width: 10px;
  height: 20px;
  background-color: #fff;
}
```

## Paso 50

Mueve el ojo interno izquierdo a la posición con una propiedad `position` de `absolute`, un `top` de `8px`, y un `left` de `2px`. También, dale un radio de borde de `60%` y gíralo a `10` grados.

```css
.cat-left-inner-eye {
  position: absolute;
  top: 8px;
  left: 2px;
  border-radius: 60%;
  transform: rotate(10deg);

  width: 10px;
  height: 20px;
  background-color: #fff;
}
```

## Paso 51

Usando un selector de clase, dale a tu elemento `.cat-right-inner-eye` un ancho de `10px` y una altura de `20px`. También, dale un color de fondo de `#fff`.

```css
.cat-right-inner-eye { 
  width: 10px;
  height: 20px;
  background-color: #fff;
}
```

## Paso 52

Mueve el ojo interior derecho a la posición con un `position` de `absolute`, un `top` de `8px`, y un `lef`t de `18px`. También, dale un radio de borde de `60%` y gíralo a `-5deg`.

```css
.cat-right-inner-eye {
  position: absolute;
  top: 8px;
  left: 18px;
  border-radius: 60%;
  transform: rotate(-5deg);

  width: 10px;
  height: 20px;
  background-color: #fff;
}
```

## Paso 53

Es hora de trabajar en la nariz. En tu HTML, crea un elemento `div` con la clase `cat-nose`.

```html
    <div class="cat-nose"></div>
```

## Paso 54

Usando un selector de clase, dale a tu elemento `.cat-nose` un borde izquierdo y derecho de `15px solid transparent` cada uno. También dale un borde inferior de `20px solid #442c2c`.

```css
.cat-nose {
  border-left: 15px solid transparent;
  border-right: 15px solid transparent;
  border-bottom: 20px solid #442c2c;
}
```

## Paso 55

Mueve la nariz a la posición con la propiedad `position` de `absolute`, un `top` de `108px`, y un `left` de `85px`.

```css
  position: absolute;
  top: 108px;
  left: 85px;
```

## Paso 56

Quita los bordes afilados de la nariz con radio de borde de `50%` cada uno en las esquinas superior izquierda, inferior derecha, e inferior izquierda. También, gíralo a `180` grados.

```css
  border-radius: 50%;
  transform: rotate(180deg);
```

## Paso 57

Ahora comenzarás a trabajar en la boca. Habrá una linea derecha y una linea izquierda para la boca.

Crea un elemento `div` con la clase `cat-mouth`.

```html
    <div class="cat-mouth"></div>
```

## Paso 58

Dentro de tu elemento `.cat-mouth`, crea un elemento `div` con la clase `cat-mouth-line-left` y otro `div` con la clase `cat-mouth-line-right`.

```html
  <div class="cat-mouth">
    <div class="cat-mouth-line-left"></div>
    <div class="cat-mouth-line-right"></div>
  </div>
```

## Paso 59

Usando un selector descendiente, seleccione los dos elementos `div` dentro del `div` con la clase `cat-mouth`. Dale un ancho de `30px`, una altura de `50px`, y un borde de `2px solid #000`.

```css
.cat-mouth div {
  width: 30px;
  height: 50px;
  border: 2px solid #000;
}
```

## Paso 60

Vas a convertir las dos líneas de la boca en una elipse. Por lo tanto, dale al selector `.cat-mouth div` un borde de color `black transparent transparent` y un radio de borde de `190%/190px 150px 0 0`.

```css
.cat-mouth div {
  width: 30px;
  height: 50px;
  border: 2px solid #000;

  border-color: black transparent transparent transparent;
  border-radius: 190%/190px 150px 0 0;
}
```

## Paso 61

Usando un selector de clase, dale a tu elemento `.cat-mouth-line-left` un `position` de `absolute`, un `top` de `88px` y un `left` de `74px`. Esto lo llevaría a la posición correcta.

```css
.cat-mouth-line-left {
  position: absolute;
  top: 88px;
  left: 74px;
}
```

## Paso 62

Usando la propiedad `transform`, gira la linea izquierda de la boca a `170` grados.

```css
.cat-mouth-line-left {
  position: absolute;
  top: 88px;
  left: 74px;

  transform: rotate(170deg);
}
```

## Paso 63

Accede a tu elemento `.cat-mouth-line-right` con un selector de clase, luego muévelo a la posición correcta con un `position` de `absolute`, un `top` de `88px` y un `left` de `91px`.

```css
.cat-mouth-line-right {
  position: absolute;
  top: 88px;
  left: 91px;
}
```

## Paso 64

Gira la línea derecha de la boca a `165` grados.

```css
.cat-mouth-line-right {
  position: absolute;
  top: 88px;
  left: 91px;

  transform: rotate(165deg);
}
```

## Paso 65

Lo último en lo que trabajarás son los bigotes. Habrán 6 de ellos, lo que significa que habrán tres en cada lado.

Crea un elemento `div` con la clase `cat-whiskers`.

```html
    <div class="cat-whiskers"></div>
```

## Paso 66

Dentro del elemento `.cat-whiskers`, crea dos elementos `div` con la clase `cat-whiskers-left` y `cat-whiskers-right`.

```html
  <div class="cat-whiskers">
    <div class="cat-whiskers-left"></div>
    <div class="cat-whiskers-right"></div>
  </div>
```

## Paso 67

Dentro del elemento `.cat-whiskers-left`, crea tres elementos `div` con las clases `cat-whisker-left-top`, `cat-whisker-left-middle`, y `cat-whisker-left-bottom`.

```html
  <div class="cat-whiskers-left">
    <div class="cat-whisker-left-top"></div>
    <div class="cat-whisker-left-middle"></div>
    <div class="cat-whisker-left-bottom"></div>
  </div>
```

## Paso 68

Dentro de tu elemento `.cat-whiskers-right`, crea 3 elementos `div` con la clase `cat-whisker-right-top`, `cat-whisker-right-middle`, y `cat-whisker-right-bottom`.

```html
  <div class="cat-whiskers-right">
    <div class="cat-whisker-right-top"></div>
    <div class="cat-whisker-right-middle"></div>
    <div class="cat-whisker-right-bottom"></div>
  </div>
```

## Paso 69

Usa un selector descendiente para apuntar a los tres elementos `div` dentro de tu elemento `.cat-whiskers-left`. Dale un `width` de `40px`, un `height` de `1px`, y un `background-color` de `#000`.

```css
.cat-whiskers-left div  {
  width: 40px;
  height: 1px;
  background-color: #000;
}
```

## Paso 70

Como hiciste en el paso anterior, usa un selector descendiente para apuntar a los tres elementos `div` dentro de tu elemento `.cat-whiskers-right`. Dale un `width` de `40px`, un `height` de `1px`, y un `background-color` de `#000`.

```css
.cat-whiskers-right div {
  width: 40px;
  height: 1px;
  background-color: #000;
}
```

## Paso 71

Usando un selector de clase, mueve el elemento `.cat-whisker-left-top` a su lugar con un `position` de `absolute`, un `top` de `120px`, y un `left` de `52px`.

```css
.cat-whisker-left-top {
  position: absolute;
  top: 120px;
  left: 52px;
}
```

## Paso 72

Gira el bigote superior izquierdo a `10` grados.

```css
.cat-whisker-left-top {
  position: absolute;
  top: 120px;
  left: 52px;
  transform: rotate(10deg);
}
```

## Paso 73

Usa un selector de clase para apuntar al elemento `.cat-whisker-left-middle`. Luego muévelo a su lugar con una propiedad `position` establecida en `absolute`, un `top` de `127px`, y un `left` de `52px`.

```css
.cat-whisker-left-middle {
  position: absolute;
  top: 127px;
  left: 52px;
}
```

## Paso 74

Gira el bigote central izquierdo a `3` grados.

```css
  transform: rotate(3deg);
```

## Paso 75

Usando un selector de clase, mueve el `.cat-whisker-left-bottom` a la posición con un `position` de `absolute`, un `top` de `134px`, y un `left` de `52px`.

```css
.cat-whisker-left-bottom {
  position: absolute;
  top: 134px;
  left: 52px;
}
```

## Paso 76

Gira el bigote inferior izquierdo a `-3` grados.

```css
  transform: rotate(-3deg);
```

## Paso 77

Ahora trabajarás en mover los bigotes derechos a su lugar. Usa el selector de clase para apuntar al elemento `.cat-whisker-right-top` y dale un `position` de `absolute`, un `top` de `120px`, y un `left` de `109px`.

```css
.cat-whisker-right-top {
  position: absolute;
  top: 120px;
  left: 109px;
}
```

## Paso 78

Gira el bigote superior derecho a `-10` grados.

```css
  transform: rotate(-10deg);
```

## Paso 79

Utiliza un selector de clase para apuntar al elemento `.cat-whisker-right-middle` y, después, mueve el bigote central derecho a la posición con una `position` `absolute`, con `top` de `127px` y una `left` de `109px`.

```css
.cat-whisker-right-middle {
  position: absolute;
  top: 127px;
  left: 109px;
}
```

## Paso 80

Gira el bigote central derecho a `-3` grados.

```css
  transform: rotate(-3deg);
```

## Paso 81

Usa el selector de clase para apuntar al elemento `.cat-whisker-right-bottom`, luego muévelo a su lugar con un `position` de `absolute`, un `top` de `134px`, y un `left` de `109px`.

```css
.cat-whisker-right-bottom{
  position: absolute;
  top: 134px;
  left: 109px;
}
```

## Paso 82

Gira el bigote inferior derecho a 3 grados.

```css
  transform: rotate(3deg);
```

>[!NOTE]
>
>Con este paso final, tu pintura de gato está ahora completa.
