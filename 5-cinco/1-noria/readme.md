# Aprende a animar con CSS construyendo una noria

Puedes utilizar la animación CSS para llamar la atención sobre secciones específicas de tu página web y hacerla más atractiva.

En este curso, construirás una noria. Aprenderás a utilizar CSS para animar elementos, transformarlos y ajustar su velocidad.

## Paso 1

Comience con la codigo de repetición estándar. Añada su declaración de `DOCTYPE`, su elemento `html` con el idioma establecido en Inglés, con los elementos `head` y `body`.

Añade tu elemento `meta`, `charset` para el conjunto de caracteres correcto, tu elemento `title`, y un elemento `link` para el archivo `./styles.css`.

Establece el `title` a `Ferris Wheel`.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ferris Wheel</title>
  <link rel="stylesheet" href="styles.css">
</head>

<body>

</body>

</html>
```

## Paso 2

Agrega un `div` dentro de tu elemento `body` y asígnale una `class` de `wheel`.

Dentro de tu nueva etiqueta `div`, agrega seis elementos `span` con la `class` de `line`, ahora agrega otros seis elementos `div` con la `class` de `cabin`.

```css
<body>
  <div class="wheel">
    <span class="line"></span>
    <span class="line"></span>
    <span class="line"></span>
    <span class="line"></span>
    <span class="line"></span>
    <span class="line"></span>

    <div class="cabin"></div>
    <div class="cabin"></div>
    <div class="cabin"></div>
    <div class="cabin"></div>
    <div class="cabin"></div>
    <div class="cabin"></div>
  </div>
</body>
```

## Paso 3

Crea un selector para el elemento `wheel`. Comienza estableciendo el `border` a `2px solid black`, el `border-radius` a `50%`, y el `margin-left` a `50px`.

```css
.wheel {
 border: 2px solid black;
 border-radius: 50%;
 margin-left: 50px;
}
```

## Paso 4

Define la propiedad `position` del selector `.wheel` con el valor `absolute`. Establece el `height` y el `width` ambos a `55vw`.

```css
.wheel {
  border: 2px solid black;
  border-radius: 50%;
  margin-left: 50px;
  position: absolute;
  height: 55vw;
  width: 55vw;
}
```

## Paso 5

Dale a tu selector `.wheel` las propiedades `max-height` y `max-width`, ambas establecidas en `500px`.

```css
.wheel {
  border: 2px solid black;
  border-radius: 50%;
  margin-left: 50px;
  position: absolute;
  height: 55vw;
  width: 55vw;
  max-height: 500px;
  max-width: 500px;
}
```

## Paso 6

Crea un selector para el elemento `.line`. Comienza estableciendo el `background-color` a `black`, el `width` a `50%`, y el `height` a `2px`.

```css
.line {
 background-color: black;
 width: 50%;
 height: 2px;
}
```

## Paso 7

Establece la propiedad `position` del selector `.line` en `absolute`, la propiedad `left` en `50%`, y la propiedad `top` en `50%`.

```css
.line {
  background-color: black;
  width: 50%;
  height: 2px;
  position: absolute;
  left: 50%;
  top: 50%;
}
```

## Paso 8

La propiedad `transform-origin` se usa para establecer el punto alrededor del cual se aplica la transformación CSS. Por ejemplo, al utilizar `rotate` (lo cual harás más adelate en este proyecto), el `transform-origin` determina alrededor de qué punto el elemento es rotado.

Dale al selector `.line` la propiedad `transform-origin` establecida en `0% 0%`. Esto desplazará el punto de origen en `0%` desde la izquierda y en `0%` desde el borde superior, colocándolo en la esquina superior izquierda del elemento.

```css
.line {
  background-color: black;
  width: 50%;
  height: 2px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform-origin: 0% 0%;
}
```

## Paso 9

Crea un selector que apunte a tu segundo elemento `.line`. Establece la propiedad `transform` en `rotate(60deg)`.

Recuerda que la propiedad `transform` te permite manipular la figura de un elemento. En este caso, usar el valor `rotate(60deg)` hara que el elemento rote alrededor de `transform-origin` en 60 grados en el sentido de las agujas del reloj.

```css
.line:nth-of-type(2)  {
 transform: rotate(60deg);
}
```

## Paso 10

Usando el mismo patrón, crea un nuevo selector para el tercer `.line`, el cuarto `.line`, el quinto `.line`, y el sexto `.line`.

Establece la propiedad `transform` para el tercer `.line` a `rotate(120deg)`, para el cuarto a `rotate(180deg)`, para el quinto a `rotate(240deg)`, y para el sexto a `rotate(300deg)`.

```css
.line:nth-of-type(3)  {
  transform: rotate(120deg);
}

.line:nth-of-type(4)  {
  transform: rotate(180deg);
}

.line:nth-of-type(5)  {
  transform: rotate(240deg);
}

.line:nth-of-type(6)  {
  transform: rotate(300deg);
}
```

## Paso 11

Crea un selector `.cabin`. Establece el `background-color` en `red`, el `width` en `20%`, y el `height` en `20%`.

```css
.cabin {
 background-color: red;
 width: 20%;
 height: 20%;
}
```

## Paso 12

Asigna al `.cabin` una `position` de `absolute` y un `border` de `2px solid`.

```css
.cabin {
  background-color: red;
  width: 20%;
  height: 20%;
  position: absolute;
  border: 2px solid;
}
```

## Paso 13

Establece el `.cabin` para que tenga una propiedad `transform-origin` con un valor `50% 0%`. Esto establecerá que el punto esté desplazado un `50%` desde la izquierda y un `0%` desde el borde superior, colocándolo en el centro del borde superior del elemento.

```css
.cabin {
  background-color: red;
  width: 20%;
  height: 20%;
  position: absolute;
  border: 2px solid;
  transform-origin: 50% 0%;
}
```

## Paso 14

Es hora de posicionar las cabinas alrededor de la rueda. Selecciona el primer elemento de `.cabin`. Establece la propiedad `right` en `-8.5%` y la propiedad `top` en `50%`.

```css
.cabin:nth-of-type(1) {
  right: -8.5%;
  top: 50%;
}
```

## Paso 15

Siguiendo con el patrón, selecciona los siguientes elementos de `.cabin` y aplícales estas reglas:

- La segunda `.cabin` debe tener la propiedad `right` establecida en `17%` y la propiedad `top` establecida en `93.5%`.
  
- El tercer `.cabin` debería tener la propiedad `right` establecida en `67%` y la propiedad `top` establecida en `93.5%`.

- El cuarto `.cabin` debería tener la propiedad `left` establecida en `-8.5%` y la propiedad `top` establecida en `50%`.

- El quinto `.cabin` debería tener la propiedad `left` establecida en `17%` y la propiedad `top` establecida en `7%`.

- El sexto `.cabin` debería tener la propiedad `right` establecida en `17%` y la propiedad `top` establecida en `7%`.

```css
.cabin:nth-of-type(2) {
 right: 17%;
 top: 93.5%;
}

.cabin:nth-of-type(3) {
 right: 67%;
 top: 93.5%;
}

.cabin:nth-of-type(4) {
 left: -8.5%;
 top: 50%;
}

.cabin:nth-of-type(5) {
 left: 17%;
 top: 7%;
}

.cabin:nth-of-type(6) {
 right: 17%;
 top: 7%;
}
```

## Paso 16

La regla `@keyframes` es usada para definir el flujo de una animación CSS. Dentro de la regla `@keyframes` puedes crear selectores para puntos específicos en la secuencia de animación, tales como `0%` o `25%`, o usar `from` y `to` para definir donde empieza y termina una secuencia.

Las reglas `@keyframes` requieren que se les asigne un nombre, que se utiliza en otras reglas para hacer referencia. Por ejemplo, la regla `@keyframes freeCodeCamp { }` se llamaría `freeCodeCamp`.

Hora de empezar a animar. Crea una regla `@keyframes` llamada `wheel`.

```css
@keyframes wheel {
  
}
```

## Paso 17

Ahora tienes que definir como debe empezar tu animación. Para esto, tienes que definir una regla `0%` dento de tu regla `@keyframes wheel`. Las propiedades que establezcas en este selector anidado se aplicarán al inicio de tu animación.

Como ejemplo, ésta sería una regla `12%`:

- **Código de ejemplo**

  ```css
  @keyframes freecodecamp {
    12% {
      color: green;
    }
  }
  ```

```css
@keyframes wheel {
  0% {}
}
```

## Paso 18

Dale a la regla `0%` la propiedad `transform` establecida en `rotate(0deg)`. Esto iniciará la animación sin ninguna rotación.

```css
@keyframes wheel {
   0% {
    transform: rotate(0deg);
   }
}
```

## Paso 19

Ahora dale a la regla `@keyframes wheel` un selector `100%`. Dentro de éste, establece `transform` a `rotate(360deg)`. Al hacer esto tu animación hará una rotación entera.

```css
@keyframes wheel {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

## Paso 20

La propiedad `animation-name` se usa para vincular la regla `@keyframes` a un selector CSS. El valor de la propiedad debe coincidir con el nombre de la regla `@keyframes`. Dale al selector `.wheel` la propiedad `animation-name` establecida en `wheel`.

La propiedad `animation-duration` se usa para establecer cuánto tiempo tarda la animación en completarse. El tiempo debe ser especificado en segundos (`s`) o en milisegundos (`ms`). Establece tu selector `.wheel` para que tenga una propiedad `animation-duration` establecida en `10s`.

```CSS
.wheel {
  border: 2px solid black;
  border-radius: 50%;
  margin-left: 50px;
  position: absolute;
  height: 55vw;
  width: 55vw;
  max-width: 500px;
  max-height: 500px;
  animation-name: wheel;
  animation-duration: 10s
}
```

## Paso 21

La propiedad `animation-iteration-count` establece cuántas veces se repetirá tu animación. Puede ser establecido a un número, o a `infinite`, lo cual repetirá indefinidamente la animación. Tu noria no debe detenerse, así que establece el selector `.wheel` para que tenga un `animation-iteration-count` establecido en `infinite`.

La propiedad `animation-timing-function` establece cómo debería progresar la animación con el tiempo. Hay distintos valores para esta propiedad, pero queremos que la animación de la noria se reproduzca al mismo ritmo de principio a fin. Establece `animation-timing-function` en `linear` en tu selector `.wheel`.

```css
.wheel {
  border: 2px solid black;
  border-radius: 50%;
  margin-left: 50px;
  position: absolute;
  height: 55vw;
  width: 55vw;
  max-width: 500px;
  max-height: 500px;
  animation-name: wheel;
  animation-duration: 10s;
  animation-iteration-count: infinite;
  animation-timing-function: linear
}
```

## Paso 22

Crea otra regla `@keyframes` con el nombre `cabins`. Usa las mismas propiedad que tu `@keyframes wheel`, copiando las reglas `0%` y `100%`, pero estableciendo la propiedad `transform` del selector `100%` en `rotate(-360deg)`.

```css
@keyframes cabins {
 0% {
  transform: rotate(0deg);
 }
 100% {
  transform: rotate(-360deg);
 }
}
```

## Paso 23

Con tu selector `.wheel`, creaste cuatro propiedades diferentes para controlar tu animación. Para tu selector `.cabin` puedes usar la propiedad `animation` para establecerlos todos a la vez.

Establece la propiedad `animation` de la regla `.cabin` en `cabins 10s linear infinite`. Esto establecerá las propiedades `animation-name`, `animation-duration`, `animation-timing-function`, y `animation-iteration-count` en ese orden.

```css
.cabin {
  background-color: red;
  width: 20%;
  height: 20%;
  position: absolute;
  border: 2px solid;
  transform-origin: 50% 0%;
  animation: cabins 10s linear infinite;
}
```

## Paso 24

Para que la animación de tu cabina se vea más como un movimiento balanceante, puedes usar la función de temporización `ease-in-out`. Este ajuste le dirá a la animación que empiece y termine a un ritmo más lento, pero que se mueva mas rápido a mitad del ciclo.

Reemplaza `linear` a `ease-in-out` en el selector `.cabin`.

```css
.cabin {
  background-color: red;
  width: 20%;
  height: 20%;
  position: absolute;
  border: 2px solid;
  transform-origin: 50% 0%;
  animation: cabins 10s ease-in-out infinite;
}
```

## Paso 25

Puedes utilizar reglas `@keyframes` para controlar algo más que la transformación de un elemento. En el selector `0%` de tu `@keyframes cabins`, establece el `background-color` en `yellow`.

```css
@keyframes cabins {
  0% {
    transform: rotate(0deg);
  background-color: yellow;
  }
  100% {
    transform: rotate(-360deg);
  }
}
```

## Paso 26

Entre los selectores `0%` y `100%`, añade un selector `50%`. Esto se aplicará en el medio del ciclo de animación. Establece `background-color` en `purple`.

```css
@keyframes cabins {
  0% {
    transform: rotate(0deg);
    background-color: yellow;
  }
  50% {
  background-color: purple;
 }
  100% {
    transform: rotate(-360deg);
  }
}
```

## Paso 27

Debido a que la animación está en un bucle infinito y los colores del inicio y del final no son los mismos, la transición cuando cambia de amarillo a rojo es repentina.

Para empezar a arreglar esto, elimina el `background-color` de tu selector `0%`.

```css
@keyframes cabins {
  0% {
    transform: rotate(0deg);
  }
  50% {
    background-color: purple;
  }
  100% {
    transform: rotate(-360deg);
  }
}
```

## Paso 28

Crea un nuevo selector `25%` entre tus selectores `0%` y `50%`. Dale a este nuevo selector la propiedad `background-color` establecida en `yellow`.

```css
@keyframes cabins {
  0% {
    transform: rotate(0deg);
  }
  25% {
    background-color: yellow;
 }
  50% {
    background-color: purple;
  }
  100% {
    transform: rotate(-360deg);
  }
}
```

## Paso 29

Finalmente, crea un nuevo selector `75%` entre tus selectores `50%` y `100%`. Dale a tu nuevo selector la propiedad `background-color` establecida en `yellow`.

**Con esto, la animación se verá mucho más suave y tu noria estará terminada.**

```css
@keyframes cabins {
  0% {
    transform: rotate(0deg);
  }
  25% {
    background-color: yellow;
  }
  50% {
    background-color: purple;
  }
  75% {
  background-color: yellow;
 }
  100% {
    transform: rotate(-360deg);
  }
}
```
