# Aprenda los colores de CSS construyendo un conjunto de marcadores de colores

- Seleccionar los colores correctos para tu página web puede mejorar enormemente el atractivo estético para tus lectores.

- En este curso, construirás un conjunto de marcadores de color. Aprenderás diferentes maneras de establecer valores de color y cómo combinar colores entre sí.

## Paso 1

Como has visto en los proyectos anteriores, las páginas web deben comenzar con la declaración `DOCTYPE html`, seguida de un elemento `html`.

Añade una declaración `DOCTYPE html` en la parte superior del documento y un elemento html después de la declaración. Dale al elemento `html` un atributo `lang` con el valor `en`.

```html
  <!DOCTYPE html>
  <html lang="en">
  </html>
```

## Paso 2

Anida un elemento `head` dentro del elemento `html`. Después del elemento `head` añade un elemento `body`.

```html
  <head></head>
  <body></body>
```

## Paso 3

Recuerda que el elemento `title` le da a los motores de búsqueda información extra sobre la página. También se muestra el contenido del elemento `title` de dos maneras más:

- en la barra de título cuando la página está abierta
- en la pestaña de navegador de la página cuando te muevas sobre ella. Incluso si esa pestaña no está activa, una vez que pases el cursor sobre la pestaña, el texto de `title` (el título) será mostrado.

Dentro del elemento `head`, anida un elemento `title` con el texto `Colored Markers`.

```html
  <head>
    <title>Colored Markers</title>
  </head>
```

## Paso 4

El atributo `charset` especifica la codificación de caracteres utilizada por el documento. `utf-8` (Formato de transformación Unicode – 8-bit) es un estándar de codificación de caracteres usado para la comunicación electrónica.

Dentro del elemento `head`, anida un elemento `meta` con un atributo `charset` con el valor `"utf-8"`.

```html
  <head>
    <meta charset="UTF-8">
    <title>Colored Markers</title>
  </head>
```

## Paso 5

En una página web puede haber varios elementos `meta`. Cada elemento `meta` añade información sobre la página que no puede ser expresada por otros elementos HTML.

Añade otro elemento `meta` dentro de la `head`. Dale un atributo `name` con el valor `"viewport"` y un atributo `content` con el valor `"width=device-width, initial-scale=1.0"` para que tu página tenga el mismo aspecto en todos los dispositivos.

```html
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Colored Markers</title>
  </head>
```

## Paso 6

Ahora estás listo para empezar a añadir contenido a la página.

Dentro del elemento `body`, anida un elemento `h1` con el texto `CSS Color Markers`.

```html
  <body>
    <h1>CSS Color Markers</h1>
  </body>
```

## Paso 7

En este proyecto trabajarás con un archivo CSS externo para darle estilo a la página. Ya creamos un archivo `styles.css` para ti. Pero antes de que puedas usarlo, necesitarás enlazarlo a la página.

Anida un elemento `link` dentro del elemento `head`. Dale un atributo `rel` con el valor `"stylesheet"` y un atributo `href` con el valor `"styles.css"`.

```html
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Colored Markers</title>
    <link rel="stylesheet" href="styles.css">
  </head>
```

## Paso 8

Ahora que tu archivo CSS externo está configurado, puedes comenzar a darle estilo a la página.

Como recordatorio, aquí está cómo apuntar un elemento de párrafo y alinearlo a la derecha:

```css
  // codigo de ejemplo

  p {
    text-align: right;
  }
```

>Crea una nueva regla CSS que apunta al elemento `h1`, y establece su propiedad `text-align` al `center`.

```css
  h1 {
    text-align: center;
  }
```

## Paso 9

Ahora añadirás algunos elementos, a los que darás forma de marcadores o plumones en los siguientes pasos.

Primero, dentro del elemento `body`, añade un elemento `div` ya su atributo `class` dale el valor `container`. Asegúrate que el elemento `div` esté debajo del elemento `h1`.

```html
  <body>
    <h1>CSS Color Markers</h1>
    <div class="container">
    </div>
  </body>
```

## Paso 10

Después, dentro del elemento `div`, añade otro elemento `div` con la clase (class) `marker`.

```html
  <body>
    <h1>CSS Color Markers</h1>
    <div class="container">
      <div class="marker"></div>
    </div>
  </body>
```

## Paso 11

Es hora de agregar algo de color al marcador. Recuerda que una forma de añadir color a un elemento es utilizando el nombre del color en inglés, como `black` (negro), `cyan` (cian) o `yellow` (amarillo).

Como recordatorio, aquí está cómo vincular la clase `freecodecamp`:

```css
  .freecodecamp {
    
  }
```

Crea una nueva regla CSS que apunta a la clase markery establezca la background-color a red.

>[!NOTE]
>
>No verás ningún cambio después de agregar el CSS.

```css
  .marker {
   background-color: red;
  }
```

## Paso 12

Se aplicó el color de fondo, pero dado que el elemento `div` del marcador está vacío, no tiene ninguna altura por defecto.

En la regla CSS `.marker`, establezca la propiedad `height` en `25px` y la propiedad `width` en `200px`

```css
  .marker {
    background-color: red;
    height: 25px;
    width: 200px;
  }
```

## Paso 13

Tu marcador se vería mejor si estuviera centrado en la página. Una forma fácil de hacerlo, es con la propiedad `margin` abreviada.

En el proyecto anterior, estableciste el margen de los elementos por separado, con propiedades como `margin-top` (margen superior) y `margin-left` (margen-izquierdo). La propiedad abreviada `margin` facilita el establecer múltiples áreas del un margen al mismo tiempo.

Para centrar tu marcador en la página, dale el valor `auto` a la propiedad `margin`. Esto les da el valor `auto` a `margin-top`, `margin-right`, `margin-bottom` y `margin-left`.

```css
  .marker {
    width: 200px;
    height: 25px;
    background-color: red;
    margin: auto;
  }
```

## Paso 14

Ya que tienes un marcador centrado y con color, es hora de añadir los otros marcadores.

En él `div` con la clase `container`, añade otros dos elementos `div` y dales una clase con el valor `marker` a cada uno.

```html
  <div class="container">
    <div class="marker"></div>
    <div class="marker"></div>
    <div class="marker"></div>
  </div>
```

## Paso 15

Ahora tienes tres marcadores `div`, pero parecen un solo rectángulo grande. Deberías añadir un poco de espacio entre ellos, para que sea más fácil diferenciar cada elemento.

Cuando la propiedad `margin` tiene dos valores, el primer valor corresponde a `margin-top` y `margin-bottom` y el segundo valor corresponde a `margin-left` y `margin-right`.

En tu regla CSS `.marker` dale a la propiedad `margin` el valor `10px` `auto`.

```css
  .marker {
    width: 200px;
    height: 25px;
    background-color: red;
    margin: 10px auto;
  }
```

## Paso 16

Para dar a los marcadores diferentes colores, necesitará añadir una clase única a cada uno. Múltiples clases pueden ser añadidas a un elemento listándolas en el atributo `class` y separándolas con un espacio. Por ejemplo, lo siguiente añade las clases `animal` y `dog` a un elemento `div`.

```html
  <div class="animal dog">
```

>Si añades varias clases a un elemento HTML, los estilos de las primeras clases pueden que sean anulados por las siguientes clases.
>
>Para empezar, agrega la clase `one` al elemento `div` del primer marcador.

```html
  <div class="marker one">
  </div>
  <div class="marker">
  </div>
  <div class="marker">
  </div>
```

## Paso 17

A continuación, remover la propiedad `background-color` y su valor de la regla `.marker` CSS.

```css
  .marker {
    width: 200px;
    height: 25px;
    margin: 10px auto;
  }
```

## Paso 18

Luego, crea una nueva regla CSS que apunta a la clase `one` y establece su propiedad `background-color` a `red`.

```css
  .one {
    background-color: red;
  }
```

## Paso 19

Añade la clase two al div del segundo marcador, y la clase three al div del tercer marcador.

```html
  <div class="marker one"></div>
  <div class="marker two"></div>
  <div class="marker three"></div>
```

## Paso 20

Crea una regla CSS que apunta a la clase `two` y establece su propiedad `background-color` en `green`.

Luego, crea otra regla CSS que apunta a la clase `three` y establece su `background-color` en `blue`.

```css
  .two {
   background-color: green;
  }
  
  .three {
   background-color: blue;
  }
```

## Paso 21

Hay dos modelos principales de colores: el modelo *aditivo* RGB (rojo, verde, azul) utilizado en dispositivos electrónicos, y el modelo *sustractivo* CMYK (cian, magenta, amarillo, negro) utilizado para impresión.

En este proyecto, trabajarás con el modelo RGB. Esto significa que los colores comienzan como negros y cambian a medida que se introducen diferentes niveles de rojo, verde y azul. Una forma fácil de ver esto, es con la función CSS `rgb`.

Crea una nueva regla CSS que apunte a la clase `container` y establece su `background-color` a negro con `rgb(0, 0, 0)`.

```css
  .container {
   background-color: rgb(0, 0, 0);
  }
```

## Paso 22

Una función es una pieza de código que puede tomar una entrada y realizar una acción específica. La función CSS `rgb` acepta valores, o argumentos, para rojo, verde y azul y produce un color:

Por ejemplo:

```css
  rgb(red, green, blue);
```

Cada valor rojo, verde y azul es un número de `0` a `255`. `0` significa que hay 0% de ese color, y es negro. `255` significa que hay 100% de ese color.

En la regla CSS `.one`, reemplaza la palabra clave `red` con la función `rgb`. Para la función `rgb`, establezca el valor para rojo a `255`, el valor para verde a `0`, y el valor para azul a `0`.

```css
  .one {
    background-color: rgb(255, 0, 0);
  }
```

## Paso 23

Observa que el `background-color` (color de fondo) de tu marcador sigue siendo rojo. Esto es porque has establecido el rojo de la función `rgb` en su valor máximo de `255`, o 100% rojo, y tanto el verde como el azul con valores de `0`.

Ahora utiliza la función `rgb` para establecer los otros colores.

En la regla CSS `.two`, utiliza la función `rgb` para establecer el `background-color` al valor máximo para el verde, y a `0` para los demás valores. Y en la regla CSS `.three`, utiliza la función `rgb` para establecer el `background-color` al valor máximo para el azul y a `0` para los demás valores.

```css
  .two {
   background-color: rgb(0, 255, 0);
  }

  .three {
   background-color: rgb(0, 0, 255);
  }
```

## Paso 24

Mientras que los marcadores rojo y azul se ven iguales, el verde es mucho más claro de lo que era antes. Esto se debe a que la palabra clave del color `green` (verde) es, en realidad, una sombra más oscura, y está a medias, entre el negro y el valor máximo del verde.

En la regla CSS `.two`, establece el valor verde en la función `rgb` a `127` para reducir su intensidad.

```css
  .two {
    background-color: rgb(0, 127, 0);
  }
```

## Paso 25

Ahora, aumenta un poco más el espacio vertical entre tus marcadores y los bordes del elemento `container` en el que se encuentran.

Dentro del selector `.container` de CSS, usa la propiedad de `padding` para agregar `10px` de relleno superior e inferior y `0` de relleno a izquierda y derecha. Esta funciona de forma similar a la propiedad `margin` que usaste anteriormente.

```css
  .container {
    background-color: rgb(0, 0, 0);
    padding: 10px 0;
  }
```

## Paso 26

En el modelo de color aditivo RGB, los colores primarios son colores que, al combinarse, crean blanco puro. Pero para que esto suceda, cada color debe estar en su máxima intensidad.

Antes de combinar los colores, vuelve a colocar el marcador verde en verde puro. En la función `rgb` de la regla CSS `.two`, ajusta el verde al valor máximo de `255`.

```CSS
  .two {
   background-color: rgb(0, 255, 0);
  }
```

## Paso 27

Ahora que ya tienes los colores RGB primarios, es hora de combinarlos.

Para la función `rgb` en la regla `.container`, establece los valores de rojo, verde y azul al máximo valor de `255`.

```css
  .container {
    background-color: rgb(255, 255, 255);
    padding: 10px 0;
  }
```

## Paso 28

**Los colores secundarios** son los colores que obtienes al combinar los primarios. Puede que hayas notado algunos colores secundarios en el último paso a medida que cambiaste los valores del rojo, verde y azul.

Para crear el primer color secundario, amarillo, actualiza la función `rgb` en la regla CSS .`one` para combinar rojo puro y verde puro.

```css
  .one {
    background-color: rgb(255, 255, 0);
  }
```

## Paso 29

Para crear el siguiente color secundario, cian, actualiza la función `rgb` en la clase CSS `.two` para combinar verde puro y azul puro.

```css
  .two {
    background-color: rgb(0, 255, 255);
  }
```

## Paso 30

Para crear el **color secundario** final, magenta, actualiza la función `rgb` en la clase CSS `.three` para combinar azul puro y rojo puro.

```css
  .three {
    background-color: rgb(255, 0, 255);
  }
```

## Paso 31

Ahora que ya estás familiarizado con los colores secundarios, aprenderás cómo crear colores terciarios. Los colores terciarios se crean combinando un color primario con uno secundario cercano.

Para crear el color terciario naranja, actualiza la función `rgb` en la clase CSS `.one` para que el rojo esté en el valor máximo, y establece el verde a `127`.

```css
  .one {
    background-color: rgb(255, 127, 0);
  }
```

## Paso 32

Ten en cuenta que, para crear naranja, tuviste que aumentar la intensidad del rojo y disminuir la intensidad del verde en los valores `rgb`. Esto se debe a que el naranja es la combinación de rojo y amarillo.

Para crear el color terciario spring green (verde primavera), combina el cian con el verde. Actualiza la función `rgb` en la regla CSS `.two` para que el verde esté en el valor máximo, y establece azul a `127`.

```css
  .two {
    background-color: rgb(0, 255, 127);
  }
```

## Paso 33

Y para crear el color terciario violeta, combina magenta con azul. Actualiza la función `rgb` en la regla CSS `.three` para que el azul esté al valor máximo, y establece el rojo a `127`.

```css
.three {
  background-color: rgb(127, 0, 255);
}
```

## Paso 34

**Existen tres colores terciarios más**: verde chartreuse (**verde + amarillo**), azur (**azul + cyan**), y rosa (**rojo + magenta**).

Para crear verde chartreuse, actualiza la función `rgb` de la clase CSS `.one` de manera que el rojo esté en `127` y el verde en su máximo valor.

Para el azur, actualiza la función `rgb` de la clase CSS `.two` de manera que el verde esté en `127` y el azul en su valor máximo.

Y para el rosa, que a veces es llamado rosa brillante, actualiza la función `rgb` de la clase CSS `.three` para que el azul esté en `127` y el rojo en su valor máximo.

```css
.one {
  background-color: rgb(127, 255, 0);
}

.two {
  background-color: rgb(0, 127, 255);
}

.three {
  background-color: rgb(255, 0, 127);
}
```

## Paso 35

Una vez estudiados los colores **primarios, secundarios y terciarios** sobre un círculo cromático, será más sencillo comprender otros conceptos de teoría del color y qué impacto pueden tener en el diseño.

Primero, en las reglas CSS `.one`, `.two` y `.three`, ajusta los valores de la función `rgb` para que el color de fondo, `background-color` de cada elemento, sea completamente negro. Recuérdese que la función `rgb` utiliza el modelo aditivo, en el que los colores comienzan como negro y cambian a medida que los valores de rojo, verde y azul aumentan.

```css
.one {
  background-color: rgb(0, 0, 0);
}

.two {
  background-color: rgb(0, 0, 0);
}

.three {
  background-color: rgb(0, 0, 0);
}
```

## Paso 36

Una rueda de color es un círculo donde colores similares, o *hues*, están cerca unos de otros, y los diferentes están más separados.

Por ejemplo, el rojo puro está entre los tonos rosa y naranja.

Dos colores opuestos entre sí en la rueda de color se llaman *complementary colors*.

Si se combinan dos colores complementarios, producen gris.

Pero cuando se colocan lado a lado, estos colores producen un fuerte contraste visual y parecen más brillantes.

En la función `rgb` para la regla CSS `.one`, establezca el valor rojo al máximo de `255` para producir rojo puro. En la función `rgb` para el regla CSS `.two`, establezca para verde y azul el máximo de 255 para producir cian.

```css
.one {
  background-color: rgb(255, 0, 0);
}

.two {
  background-color: rgb(0, 255, 255);
}
```

## Paso 37

Obsérvese que los colores rojo y cian son muy brillantes uno al lado del otro. Si se hace un uso abusivo de este contraste, puede acabar distrayendo la atención, y además puede hacer un texto difícil de leer si está sobre un fondo con un color complementario.

Es mejor práctica elegir un color como dominante, y usar su complementario como énfasis para dirigir la atención sobre cierto contenido de la página.

Primero, en la regla `h1`, usa la función `rgb` para establecer el valor de `background-color` a *cyan*.

```css
h1 {
  text-align: center;
  background-color: rgb(0, 255, 255);
}
```

## Paso 38

A continuación, en la regla CSS `.one`, usa la función `rgb` para que el color de fondo, `background-color` sea negro. Y en la regla CSS `.two`, usa la función `rgb` para que el color de fondo, `background-color` sea rojo.

```css
.one {
  background-color: rgb(0, 0, 0);
}

.two {
  background-color: rgb(255, 0, 0);
}
```

## Paso 39

¿Notas cómo tus ojos se sienten naturalmente atraídos por el color rojo en el centro? Cuando diseñas un sitio, puedes usar este efecto para dirigir la atención sobre titulares importantes, botones o enlaces.

Aparte de los colores complementarios, hay otras combinaciones de colores importantes, aunque las veremos un poco más tarde.

Por ahora, usa la función `rgb` en la regla CSS `.two` para establecer el `background-color` en negro.

```css
.two {
  background-color: rgb(0, 0, 0);
}
```

## Paso 40

Y en la regla `h1`, elimina la propiedad `background-color` y su valor para volver al color blanco por defecto.

```css
h1 {
  text-align: center;
  }
```

## Paso 41

Ahora es el momento de añadir otros detalles a los marcadores, vamos con el primero.

En el elemento `div` del primer marcador, cambia la clase `one` a `red`.

```html
<div class="marker red">
</div>
<div class="marker two">
</div>
<div class="marker three">
</div>
```

## Paso 42

Actualiza la regla CSS .`one` para que apunte a la nueva clase (class) `red`.

```css
.red {
  background-color: rgb(0, 0, 0);
}

.two {
  background-color: rgb(0, 0, 0);
}

.three {
  background-color: rgb(0, 0, 0);
}
```

## Paso 43

Y actualiza la función `rgb` en la regla CSS `.red` para que el valor rojo esté al máximo.

```css
.red {
  background-color: rgb(255, 0, 0);
}

.two {
  background-color: rgb(0, 0, 0);
}

.three {
  background-color: rgb(0, 0, 0);
}
```

## Paso 44

A continuación, cambia la clase `two` a `green` en el segundo `div` de marcador, y la clase `three` a `blue` en el tercer `div` de marcador.

```HTML
<div class="marker red">
</div>
<div class="marker green">
</div>
<div class="marker blue">
</div>
```

## Paso 45

Actualiza el selector de clase CSS `.two` de manera que apunte a la nueva clase `green`. Y actualiza el selector de clase `.three` para que apunte a la nueva clase `blue`.

```css
.red {
  background-color: rgb(255, 0, 0);
}

.green {
  background-color: rgb(0, 0, 0);
}

.blue {
  background-color: rgb(0, 0, 0);
}
```

## Paso 46

Es práctica muy común aplicar color a un elemento CSS con valores hexadecimales (hex). Puede sonar complicado, pero no es más que otra forma de expresar colores RGB.

**Los valores hexadecimales** empiezan con el carácter `#`, siguiendo seis caracteres entre **0-9** y **A-F**. El primer par de caracteres representa el rojo, el segundo el verde y el tercero el azul. Pr ejemplo, `#4B5320`.

En el selector de clase `.green`, en la propiedad `background-color`, dale un valor para el color en forma de código hexadecimal, con los valores `00` para el rojo, `FF` para el verde, y `00` al azul.

```css
.green {
  background-color: #00ff00;
}
```

## Paso 47

Seguramente estés familiarizado con valores en base 10, o decimales, los cuales van de 0 a 9. Hexadecimales, o valores en base 16, van de 0 a 9 y a continuación de A a F:

- 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
- A, B, C, D, E, F

Para los colores en hexadecimal, `00` es 0% de ese color, y `FF` es 100%. De tal manera que `#00FF00` se traduce en 0% rojo, 100% verde y 0% azul, siendo equivalente a `rgb(0, 255, 0)`.

Disminuye la intensidad del verde estableciendo el valor hexadecimal del color verde a `7F`.

```css
.green {
  background-color: #007f00;
  }
```

## Paso 48

Otra forma de representar colores es el modelo *HSL*, siglas de hue, saturation y lightness (matiz, saturación y luminosidad).

La función de CSS `hsl` acepta tres valores: un número entre 0 y 360 para el matiz (hue), un porcentaje de 0 a 100 para la saturación (saturation), y otro porcentaje de 0 a 100 para la luminosidad (lightness).

Sobre un círculo cromático, el matiz (hue) rojo está en **0** grados, el verde en **120** y el azul en **240**.

La saturación (saturation) es la intensidad de un color desde 0%, o gris, hasta 100% para el color puro. Debes añadir el signo de porcentaje `%` a los valores de saturation (saturación) y lightness (luminosidad).

La luminosidad (lightness) es lo brillante que parece un color, desde **0%** o completamente negro, hasta **100%**, completamente blanco, siendo neutro el **50%**.

En la regla CSS `.blue`, utiliza la función `hsl` para cambiar la propiedad `background-color` a azul puro. Establece el tono a `240`, la saturación a `100%` y la luminosidad a `50%`.

```css
.blue {
  background-color: hsl(240, 100%, 50%);
  }
```

## Paso 49

Hemos visto unas cuantas maneras de establecer colores planos en CSS, pero también se pueden aplicar *transiciones de color*, o *gradientes*, sobre un elemento.

Se llama gradiente, o degradado, a la transición progresiva de un color a otro. La función CSS `linear-gradient` permite controlar la dirección de la transición a lo largo de una línea, y qué colores participan en el degradado.

Una cosa a tener en cuenta es que la función `linear-gradient` lo que en realidad crea es un elemento `image`, y se asocia normalmente con la propiedad `background`, la cual puede aceptar una imagen como valor.

En la regla CSS `.red`, sustituye la propiedad `background-color` por `background`.

```css
.red {
  background: linear-gradient(to right, red, yellow);
  }
```

>[!NOTE]
>
>La función `linear-gradient` acepta dos o más colores, separados por comas, y una dirección de transición, que puede ser `to top`, `to bottom`, `to left`, `to right`, `to top left`, `to top right`, `to bottom left`, `to bottom right`, o `to bottom right` (este último es el valor por defecto).

## Paso 50

La función linear-gradient es muy flexible -- aquí hay una sintaxis básica que usaras en este tutorial:

- `linear-gradient(dirección, color1, color2, ...)`: crea un gradient

`gradientDirection` es la dirección de la línea a lo largo de la cual tendrá lugar la transición. `color1` y `color2` son argumentos de color, representando los colores usados en la transición. Se pueden pasar a la función en cualquier formato, ya sea el nombre del color, `hex`, `rgb` o `hsl`.

Vamos a aplicar al primer marcador un gradiente de rojo a verde a lo largo de una línea de 90 grados.

Primero, en la regla CSS `.red`, establece la propiedad `background` a `linear-gradient()`, y al argumento gradientDirection pásale el valor `90deg`.

```css
.red {
  background: linear-gradient(90deg);
  }
```

## Paso 51

Utilizará la función `rgb` para los colores de este degradado.

En la función `linear-gradient`, use la función `rgb` para establecer el primer argumento de color en rojo puro.

```css
.red {
  background: linear-gradient(90deg, rgb(255, 0, 0));
}
```

## Paso 52

Todavía no verá el degradado porque la función `linear-gradient` necesita al menos dos argumentos de color para funcionar.

En la misma función `linear-gradient`, use la función `rgb` para establecer el segundo argumento de color en verde puro.

```css
.red {
  background: linear-gradient(90deg, rgb(255, 0, 0), rgb(0, 255, 0));
}
```

## Paso 53

Como puedes ver, la función `linear-gradient` produce un suave gradiente de rojo a verde. La función `linear-gradient` necesita un mínimo de dos colores como argumentos, pero puede aceptar bastantes más.

Usa la función `rgb` para añdir azul puro como tercer argumento de color a la función `linear-gradient`.

```css
.red {
  background: linear-gradient(90deg, rgb(255, 0, 0), rgb(0, 255, 0), rgb(0, 0, 255));
}
```

>[!NOTE]
>
>La respuesta final es: \red{background: linear-gradient(90deg, rgb(255, 0, 0), rgb(0, 255, 0), rgb(0, 0, 255));}

## Paso 54

Las paradas de color permiten afinar el emplazamiento de los colores a lo largo de la línea que sigue el gradiente. Se definen, en la función `linear-gradient`, mediante unidades de longitud, como `px` o porcentajes, a continuación del color del cual se quiere definir la parada.

Por ejemplo, en el gradiente que sigue, la transición del rojo al negro tiene lugar en el punto que representa el 90% de la línea del gradiente, de manera que el rojo ocupa la mayor parte del espacio disponible:

```css
linear-gradient(90deg, red 90%, black);
```

En la función `linear-gradient`, añade una parada de color en el `75%` después del primer argumento de color, el rojo. No añadas paradas de color en los otros argumentos de color.

```css
.red {
  background: linear-gradient(90deg, rgb(255, 0, 0) 75%, rgb(0, 255, 0), rgb(0, 0, 255));
  }
```

## Paso 55

Ahora que conoces los fundamentos de la función `linear-gradient` y de las paradas de color, vamos a hacer que nuestros marcadores parezcan más realistas.

En la función `linear-gradient`, establece `gradientDirection` a `180deg`.

```css
.red {
  background: linear-gradient(180deg, rgb(255, 0, 0) 75%, rgb(0, 255, 0), rgb(0, 0, 255));
}
```

## Paso 56

Ahora, establece la parada del color rojo en `0%`, la del verde en `50%` y la del azul en `100%`.

```css
.red {
  background: linear-gradient(180deg, rgb(255, 0, 0), rgb(0, 255, 0) 50%, rgb(0, 0, 255) 100%);
}
```

## Paso 57

Una vez establecidas las paradas de color, vamos a aplicar diferentes tonos de rojo a los argumentos de color de la función `linear-gradient`. El tono en los límites superior e inferior del marcador será más oscuro y en el centro más claro, como si estuviera iluminado perpendicularmente.

Para el primer argumento de color, que actualmente es rojo puro, actualiza la función `rgb` de manera que el valor del rojo sea `122`, el del verde `74` y el del azul `14`.

```css
.red {
  background: linear-gradient(180deg, rgb(122, 74, 14) 0%, rgb(0, 255, 0) 50%, rgb(0, 0, 255) 100%);
}
```

## Paso 58

Ahora modifica el segundo argumento de color de la función `linear-gradient`, establecido actualmente como verde puro.

Actualiza la función `rgb` de manera que el valor del rojo sea `245`, el del verde `62` y el del azul `113`.

```css
.red {
  background: linear-gradient(180deg, rgb(122, 74, 14) 0%, rgb(245, 62, 113) 50%, rgb(0, 0, 255) 100%);
}
```

## Paso 59

Por último, modifica el tercer argumento de color de la función `linear-gradient`, que ahora está como azul puro.

Actualiza la función `rgb` de forma que el valor del rojo sea `162`, el del verde `27` y el del azul `27`.

```css
.red {
  background: linear-gradient(180deg, rgb(122, 74, 14) 0%, rgb(245, 62, 113) 50%, rgb(162, 27, 27) 100%);
}
```

## Paso 60

Ahora el marcador rojo se ve mucho más realista. Haz lo mismo para el marcador verde, combinando la función `linear-gradient` y colores en hexadecimal.

En la regla CSS `.green`, cambia la propiedad `background-color` por `background`.

```css
.green {
  background: #007f00
}
```

## Paso 61

Para el gradiente de este marcador, utilizaremos colores en hexadecimal.

En la función `linear-gradient` establece `gradientDirection` a `180deg`. Y para el primer argumento de color, usa el formato hexadecimal con los valores `55` para el rojo, `68` para el verde, y `0D` para el azul.

```css
.green {
  background: linear-gradient(180deg, #55680d);
}
```

## Paso 62

Para el segundo argumento de color, utilice un código de color hexadecimal con los valores `71` para rojo, `F5` para verde y `3E` para azul.

```css
.green {
  background: linear-gradient(180deg, #55680D, #71f53e);
}
```

## Paso 63

Esto va mejorando, pero hay que oscurecer el borde inferior del marcador verde para darle un poco más de volumen.

En la función `linear-gradient` añade, como el tercer argumento de color, un código de color hexadecimal con los valores `11` para el rojo, `6C` para el verde y `31` para el azul.

```css
.green {
  background: linear-gradient(180deg, #55680D, #71F53E, #116c31);
}
```

## Paso 64

Incluso sin las paradas de color, habrás notado que los colores en el marcador verde transicionan en los mismos puntos que en el marcador rojo. El primer color está al comienzo (0%), el segundo en el centro (50%) y el último al final (100%) de la línea del gradiente.

La función `linear-gradient` calcula de forma automática estos valores, repartiendo equitativamente los colores a lo largo de la línea del gradiente.

En la regla CSS `.red`, elimina las tres paradas de color de la función `linear-gradient`, quedando el código un poco más limpio.

```css
.red {
  background: linear-gradient(180deg, rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
}
```

## Paso 65

Si en la función `linear-gradient` no se especifica el argumento `gradientDirection`, por defecto será de 180 grados, disponiendo los colores de arriba a abajo.

Limpia un poco más el código eliminando el argumento `gradientDirection` de ambas funciones `linear-gradient`.

```css
.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
}

.green {
  background: linear-gradient(#55680D, #71F53E, #116C31);
}
```

## Paso 66

Apliquemos un gradiente al marcador azul, esta vez utilizando la función `hsl` en los argumentos de color.

En la regla CSS `.blue`, sustituye la propiedad `background-color` por `background`.

```css
.blue {
  background: hsl(240, 100%, 50%);
}
```

## Paso 67

Utiliza la función `linear-gradient`, pasándole la función `hsl` con los valores `186` para el matiz (hue), `76%` para la saturación y `16%` para la luminosidad como primer argumento de color.

```css
.blue {
  background: linear-gradient(hsl(186, 76%, 16%))
  }
```

## Paso 68

Como segundo argumento de color, pasa la función `hsl` con los valores `223` para el matiz, `90%` para la saturación y `60%` para la luminosidad.

```css
.blue {
  background: linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%));
}
```

## Paso 69

Y como tercer argumento de color, pasa la función `hsl` con los valores `240` para el matiz, `56%` para la saturación y `42%` para la luminosidad.

```css
.blue {
  background: linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%), hsl(240, 56%, 42%));
}
```

## Paso 70

Ahora que los marcadores tienen los colores correctos, es hora de construir las fundas de los marcadores. Empieza con el marcador rojo.

Crea un elemento `div` dentro del elemento `div` del marcador rojo y asígnale la clase `sleeve`.

```html
<div class="marker red">
  <div class="sleeve"></div>
</div>
```

## Paso 71

Crea una nueva regla CSS que tenga como objetivo la clase `sleeve`. Establece la propiedad `width` a `110px`, y la propiedad `height` a `25px`.

```css
.sleeve {
  width: 110px;
  height: 25px;
}
```

## Paso 72

Para que el marcador se vea más realista, dale a la manga un color blanco transparente.

Primero, establezca el elemento `background-color` de la manga a `white`.

```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: white;
}
```

## Paso 73

Opacity describe cuán opaco o no transparente es algo. Por ejemplo, una pared sólida es opaca y no puede pasar la luz. Pero un vaso para beber es mucho más transparente, y puedes ver a través del vaso hacia el otro lado.

Con la propiedad CSS `opacity`, puede controlar cuán opaco o transparente es un elemento. Con el valor `0`, o 0%, el elemento será completamente transparente, y en `1.0`, o 100%, el elemento será completamente opaco como lo es por defecto.

En la regla CSS `.sleeve`, establezca la propiedad `opacity` en `0.5`.

```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: white;
  opacity: 0.5;
}
```

## Paso 74

Otra forma de establecer la opacidad de un elemento es con el canal alpha. Similar a la propiedad `opacity`, el canal alfa controla qué tan transparente u opaco es un color.

Ya has establecido la opacidad de la carátula con un color con nombre y la propiedad `opacity`, pero puedes agregar un canal alfa a las otras propiedades de color CSS.

Dentro de la regla `.sleeve`, quite la propiedad y el valor `opacity`.

```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: white;
}
```

## Paso 75

Ya está familiarizado con el uso de la función `rgb` para establecer colores. Para agregar un canal alfa a un color `rgb`, use la función `rgba` en su lugar.

La función `rgba` funciona igual que la función `rgb`, pero toma un número más de `0` a `1.0` para el canal alfa:

```css
rgba(redValue, greenValue, blueValue, alphaValue);
```

También puedes usar un canal alfa con colores hsl y hex. Más adelante verás como hacerlo.

En la regla `.sleeve`, utiliza la función `rgba` para establecer la propiedad `background-color` a blanco puro con un 50% de opacidad.

```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 50%);
}
```

## Paso 76

Su manga se ve bien, pero se vería aún mejor si se colocara más hacia el lado derecho del marcador. Una forma de hacerlo es agregar otro elemento antes de la manga para empujarla hacia la derecha.

Agregue un nuevo `div` con la clase `cap` antes del elemento de manga `div`.

```html
<div class="marker red">
  <div class="cap"></div>
  <div class="sleeve"></div>
</div>
```

## Paso 77

Cree una nueva regla CSS para apuntar a la clase `cap`. En la nueva regla, establece la propiedad `width` en `60px` y la propiedad `height` en `25px`.

```css
.cap {
  width: 60px;
  height: 25px;
}
```

## Paso 78

Parece que tu manga desapareció, pero no te preocupes, todavía está allí. Lo que ha ocurrido es que tu nuevo `div` de tapa está ocupando todo el ancho del marcador, y está empujando el mango hacia la siguiente línea.

Esto se debe a que la propiedad predeterminada `display` para los elementos `div` es `block`. Entonces, cuando dos elementos `block` están uno al lado del otro, se apilan como bloques reales. Por ejemplo, los elementos del marcador están apilados uno encima del otro.

Para colocar dos elementos `div` en la misma línea, establezca sus propiedades `display` en `inline-block`.

Cree una nueva regla para dirigirse a las clases `cap` y `sleeve` y establezca `display` en `inline-block`.

```css
.cap,
.sleeve {
 display: inline-block;
}
```

## Paso 79

En el proyecto anterior, estudiamos nociones básicas sobre bordes y la propiedad `border-color`.

Todos los elementos HTML tienen bordes, pero están establecidos a `none` por defecto. Con CSS se tiene control total sobre los bordes de un elemento, pudiendo mostrarlo en todos los lados o simplemente en uno. Para que un borde sea visible, hay que darle grosor (width) y estilo (style).

En la regla CSS `.sleeve`, añade la propiedad `border-left-width` con el valor `10px`.

```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 0.5);
  border-left-width: 10px;
}
```

## Paso 80

Los bordes tienen varios estilos para elegir. Puede ser una línea continua (solid) o discontinua (dashed), o incluso una línea punteada (dotted) si lo prefieres. Lo normal es que sean líneas continuas.

En la regla CSS `.sleeve`, añade la propiedad `border-left-style` con el valor `solid`.

```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 0.5);
  border-left-width: 10px;
 border-left-style: solid;
}
```

## Paso 81

Tu borde debe ser visible ahora. Si no se establece ningún color, el negro se utiliza por defecto.

Pero para que tu código sea más legible, es mejor establecer el color del borde explícitamente.

En la regla CSS `.sleeve`, añade la propiedad `border-left-color` con el valor `black`.

```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 0.5);
  border-left-width: 10px;
  border-left-style: solid;
 border-left-color: black;
}
```

## Paso 82

La propiedad abreviada `border-left` permite establecer el grosor, el estilo y el color del borde izquierdo de forma simultánea.

**La sintaxis sería:**

```css
border-left: ancho estilo color;
```

En la regla CSS `.sleeve`, reemplaza las propiedades `border-left-width`, `border-left-style` y `border-left-color` por la propiedad abreviada `border-left`. Los valores de grosor, estilo y color del borde izquierdo deben ser los mismos.

```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 0.5);
  border-left: 10px solid black;
}
```

## Paso 83

El marcador tiene buena pinta. Pero para hacerlo parecer aún más realista, cambia el estilo del borde a doble línea continua.

En la propiedad abreviada `border-left`, cambia el valor del estilo de `solid` a `double`.

```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 0.5);
  border-left: 10px double black;
}
```

## Paso 84

El color negro de su borde se ve bastante duro contra la manga más transparente. Puede utilizar un canal alfa para reducir la opacidad del borde negro.

Para la propiedad abreviada `border-left`, utilice la función `rgba` para establecer el valor de color en negro puro con un 75% de opacidad.

```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 0.5);
  border-left: 10px double rgba(0, 0, 0, 75%);
}
```

## Paso 85

Impresionante. Luce bien el marcador rojo. Ahora todo lo que necesita hacer es agregar las tapas y mangas a sus otros marcadores.

Agregue una gorra y una manga a los marcadores verdes y azules. Puede copiar los elementos `div` del marcador rojo y pegarlos en los otros dos marcadores.

```html
<div class="marker red">
  <div class="cap"></div>
  <div class="sleeve"></div>
</div>
<div class="marker green">
  <div class="cap"></div>
  <div class="sleeve"></div>
</div>
<div class="marker blue">
  <div class="cap"></div>
  <div class="sleeve"></div>
</div>
```

## Paso 86

La última cosa que haremos será añadir un ligero sombreado a cada marcador para hacerlos parecer aún más realistas.

La propiedad `box-shadow` permite aplicar una o más sombras alrededor de un elemento. Esta sería la sintaxis básica:

```css
box-shadow: offsetX offsetY color;
```

**Así es como los valores de `offsetX` y `offsetY` funcionan:**

- tanto `offsetX` como `offsetY` aceptan valores numéricos en `px` y otras unidades CSS
- un valor positivo de `offsetX` mueve la sombra a la derecha y un valor negativo la mueve a la izquierda
- un valor positivo de `offsetY` mueve la sombra hacia abajo y un valor negativo la sube
- si quieres un valor de cero (`0`) para `offsetX` y/o `offsetY`, no es necesario agregar una unidad. Todos los navegadores entienden que cero significa que no hay cambios.

La altura y la anchura de las sombras están determinadas por la altura y la anchura del elemento al que se aplica. También puedes usar un valor `spreadRadius` opcional para extender el alcance de la sombra. Luego veremos más sobre esto.

Comienza añadiendo una sombra simple al marcador rojo.

En la regla CSS `.red`, añade la propiedad `box-shadow` con los valores `5px` para `offsetX`, `5px` para `offsetY` y `red` para `color`.

```css
.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
  box-shadow: 5px 5px red;
}
```

## Paso 87

Como puede ver, agregó una sombra roja simple alrededor de su marcador que está 5 píxeles a la derecha y 5 píxeles hacia abajo.

Pero, ¿y si quisieras colocar tu sombra en el lado opuesto? Puede hacerlo usando valores negativos para `offsetX` y `offsetY`.

Actualice los valores de la propiedad `box-shadow` y establezca `offsetX` en `-5px` y `offsetY` en `-5px`.

```css
.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
  box-shadow: -5px -5px red;
}
```

## Paso 88

Observa que los límites de la sombra son muy bruscos. En la propiedad `box-shadow`, se encuentra el valor opcional `blurRadius`:

```css
box-shadow: offsetX offsetY blurRadius color;
```

Si no se indica un valor para `blurRadius`, será `0` por defecto, produciendo sombras con los límites bruscos. Cuanto mayor sea el valor de `blurRadius`, mayor será el efecto de difuminado de la sombra.

En la regla CSS `.green`, añade la propiedad `box-shadow` con los valores 5px para `offsetX`, `5px` para `offsetY`, `5px` para `blurRadius` y `green` para `color`.

```css
.green {
  background: linear-gradient(#55680D, #71F53E, #116C31);
  box-shadow: 5px 5px 5px green;
}
```

## Paso 89

¿Quieres expandir la sombra un poco más? Puedes hacerlo con el valor opcional `spreadRadius`:

```css
box-shadow: offsetX offsetY blurRadius spreadRadius color;
```

Como blurRadius, el valor por defecto de `spreadRadius` es `0` si no se especifica.

Practica añadiendo una sombra de 5 píxels alrededor del marcador azul.

En la regla CSS `.blue`, añade la propiedad `box-shadow` con los valores `0` para `offsetX`, `0` para `offsetY`, `0` para `blurRadius`, `5px` para `spreadRadius` y `blue` para `color`.

```css
.blue {
  background: linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%), hsl(240, 56%, 42%));
 box-shadow: 0 0 0 5px blue;
}
```

## Paso 90

Ahora que ya estás familiarizado con la propiedad `box-shadow`, es el momento de terminar de trabajar las sombras, comenzando con la del marcador rojo.

En la regla CSS `.red`, actualiza los valores de la propiedad `box-shadow` para que `offsetX` sea `0`, `offsetY` sea `0`, `blurRadius` sea `20px`, `spreadRadius` sea `0` y `color` sea `red`. Recuerda que no necesitas agregar unidades a un valor cero.

```css
.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
  box-shadow: 0 0 20px 0 red;
}
```

## Paso 91

A continuación, actualice el valor `color` de la propiedad `box-shadow` del marcador rojo.

Reemplace el color nombrado con la función `rgba`. Utilice los valores `83` para rojo, `14` para verde, `14` para azul y `0.8` para el canal alfa.

```css
.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
  box-shadow: 0 0 20px 0 rgba(83, 14, 14, 0.8);
}
```

## Paso 92

Las sombras de los marcadores verde y azul tendrán la misma posición, desenfoque y extensión. La única diferencia serán los colores.

En las reglas CSS `.green` y `.blue`, actualice los valores de las propiedades `box-shadow` para que `offsetX` sea `0`, `offsetY` sea `0`, `blurRadius` sea `20px` y `spreadRadiussea` `0`. Deje los colores como `green` y `blue` por ahora.

```css
.green {
  background: linear-gradient(#55680D, #71F53E, #116C31);
  box-shadow: 0 0 20px 0 green;
}

.blue {
  background: linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%), hsl(240, 56%, 42%));
  box-shadow: 0 0 20px 0 blue;
}
```

## Paso 93

En la propiedad `box-shadow` del marcador verde, sustituye el nombre del color por un valor hexadecimal. Utiliza los valores `3B` para el rojo, `7E` para el verde, `20` para el azul y `CC` para el canal alfa.

```css
.green {
  background: linear-gradient(#55680D, #71F53E, #116C31);
  box-shadow: 0 0 20px 0 #3b7e20cc;
}
```

## Paso 94

Por último, en la propiedad `box-shadow` del marcador azul, sustituye el nombre del color por la función `hsla`. Utiliza los valores `223` para el matiz, `59%` para la saturación, `31%` para la luminosidad y `0.8` para el canal alfa.

**¡Y con esto has concluído tu impresionante grupo de marcadores coloreados! Bien hecho.**

```css
.blue {
  background: linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%), hsl(240, 56%, 42%));
  box-shadow: 0 0 20px 0 hsla(223, 59%, 31%, 0.8);
}
```
