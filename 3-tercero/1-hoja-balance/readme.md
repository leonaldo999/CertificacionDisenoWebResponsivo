# Aprende mas sobre los pseudo-selectores de CSS costruyendo una hoja de balance

Puede utilizar **pseudoselectores** CSS para cambiar elementos HTML específicos.

En este curso, construirás un balance usando pseudo selectores. Aprenderás a cambiar el estilo de un elemento al pasar el ratón por encima y a activar otros eventos en tu página web.

## Paso 1

Configura tu HTML con los elementos `DOCTYPE`, `html` indicando que este documento está en inglés, `head` y `body`.

Dale a tu elemento `head` los elementos `meta` apropiados para el `charset` y el `viewport`, un elemento `title` con un título apropiado y un elemento `link` para la hoja de estilos.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hoja de Balance</title>
  <link rel="stylesheet" href="styles.css">
</head>

<body>
</body>

</html>
```

## Paso 2

Dentro de tu elemento `body`, anida un elemento `section` dentro de un elemento `main`.

```html
<body>
  <main>
    <section></section>
  </main>
</body>
```

## Paso 3

Dentro de tu elemento `section`, agrega un elemento `h1` con un elemento `span` anidado.

```html
<section>
  <h1><span></span></h1>
</section>
```

## Paso 4

Los lectores de pantalla anuncian los elementos HTML basándose en el flujo del documento. Eventualmente, queremos que el balance financiero tenga un título de "Balance Sheet" y un subtítulo de "AcmeWidgetCorp". Sin embargo, este orden no tiene sentido si es anunciado por un lector de pantalla.

Dale a tu `span` existente el atributo `class` establecido en `flex`, y agrega dos elementos `span` dentro de él. Dale al primero el texto `AcmeWidgetCorp`. Dale al segundo el texto `Balance Sheet`. Utilizarás CSS para invertir el orden del texto de la página, pero el orden del HTML tendrá más sentido para los lectores de pantalla.

```html
<span class="flex">
  <span>AcmeWidgetCorp</span>
  <span>Balance Sheet</span>
</span>
```

## Paso 5

Debajo de tu elemento `h1`, crea un elemento `div`. Dale un atributo `id` establecido en `years`. Tú quieres que este elemento en particular este oculto para los lectores de pantalla, así que dale el atributo `aria-hidden` establecido en `true`.

```html
<div id="years" aria-hidden="true">
</div>
```

## Paso 6

Dentro de tu elemento `div`, agrega tres elementos `span`. Give each of them a `class` attribute set to `year`, and add the following text (in order): `2019`, `2020`, and `2021`.

```html
  <div id="years" aria-hidden="true">
    <span class="year">2019</span>
    <span class="year">2020</span>
    <span class="year">2021</span>
  </div>
```

## Paso 7

Debajo de tu elemento `div` existente, agrega un nuevo elemento `div` con un `class` establecido en `table-wrap`. Este será el contenedor para tus tablas.

Dentro de eso, agrega tres elementos `table`. Tú usarás CSS para estilizarlas en una sola tabla, pero usando tablas separadas ayudarás a los lectores de pantalla a entender el flujo del documento.

```html
  <div class="table-wrap">
    <table></table>
    <table></table>
    <table></table>
  </div>
```

## Paso 8

Las tablas HTML usan el elemento `caption` para describir de que trata la tabla. El elemento `caption` siempre debe ser el primer hijo de un `table`, pero se puede posicionar con la propiedad CSS `caption-side`.

Agrega un elemento `caption` para tu primer `table` y dale el texto `Assets`.

```html
  <table>
    <caption>Assets</caption>
  </table>
```

## Paso 9

Los elementos `thead` y `tbody` son usados para indicar que parte de tu tabla es la cabecera, y que parte contiene los datos principales o el contenido.

Agrega un `thead` y un `tbody` a tu primer `table`, debajo del elemento `caption`.

```html
  <table>
    <caption>Assets</caption>
    <thead></thead>
    <tbody></tbody>
  </table>
```

## Paso 10

El elemento `tr` se utiliza para indicar una fila de la tabla. Agrega un elemento `tr` dentro de tu elemento `thead`. En tu nuevo elemento `tr`, agrega un elemento `td`, seguido de tres elementos `th`.

El elemento `td` indica una celda de datos, mientras que el elemento `th` indica una celda de cabecera.

```html
  <thead>
    <tr>
      <td></td>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
```

## Paso 11

Dentro de cada uno de tus nuevos elementos `th`, anida un elemento `span` con el `class` establecido en `sr-only year`. Dales el siguiente texto (en ese orden): `2019`, `2020` y `2021`.

Dale a tu tercer elemento `th` el atributo `class` establecido en `current`.

Deja tu elemento `td` vacío. Este elemento solo existe para asegurar que tu tabla tiene un diseño de cuatro columnas y asociar las cabeceras con las columnas correctas.

```html
  <thead>
    <tr>
      <td></td>
      <th>
        <span class="sr-only year">2019</span>
      </th>
      <th>
        <span class="sr-only year">2020</span>
      </th>
      <th class="current">
        <span class="sr-only year">2021</span>
      </th>
    </tr>
  </thead>
```

## Step 12

Paso 12
Dentro de tu elemento `tbody`, agrega cuatro elementos `tr`. Dale a los primeros tres un atributo `class` establecido en `data` y al cuarto un atributo `class` establecido en `total`.

```html
  <tbody>
    <tr class="data"></tr>
    <tr class="data"></tr>
    <tr class="data"></tr>
    <tr class="total"></tr>
  </tbody>
```

## Paso 13

En tu primer `tr`, agrega un elemento `th` con el texto `Cash This is the cash we currently have on hand..` Wrap all of that text except `Cash` in a `span` element with the `class` set to `description`.

Siguiendo eso, agrega tres elementos `td` con el siguiente texto (en ese orden): `$25`, `$30`, `$28`. Dale al tercer elemento `td` un atributo `class` establecido en `current`.

```html
<tr class="data">
  <th>
    Cash 
    <span class="description">This is the cash we currently have on hand.</span>
  </th>
  <td>$25</td>
  <td>$30</td>
  <td class="current">$28</td>
</tr>
```

## Paso 14

En tu segundo elemento `tr`, agrega un elemento `th` con el texto `Checking Our primary transactional account.`. Wrap that text, except for `Checking`, in a `span` element with the `class` attribute set to `description`.

Siguiendo eso, agrega tres elementos `td` con el siguiente texto (en ese orden): `$54`, `$56`, `$53`. Dale al tercer elemento `td` un atributo `class` establecido en `current`.

```html
  <tr class="data">
    <th>
      Checking <span class="description">Our primary transactional account.</span>
    </th>
    <td>$54</td>
    <td>$56</td>
    <td class="current">$53</td>
  </tr>
```

## Paso 15

En tu tercer elemento `tr`, agrega un elemento `th` con el texto `Savings Funds set aside for emergencies.`. Wrap that text, except for `Savings`, in a `span` element with the `class` attribute set to `description`.

Siguiendo eso, agrega tres elementos `td` con el siguiente texto (en ese orden): `$500`, `$650`, `$728`. Dale al tercer elemento `td` un atributo `class` establecido en `current`.

```html
  <tr class="data">
    <th>Savings <span class="description">Funds set aside for emergencies.</span></th>
    <td>$500</td>
    <td>$650</td>
    <td class="current">$728</td>
  </tr>
```

## Paso 16

En tu cuarto elemento `tr`, agrega un elemento `th` con el texto `Total Assets`. Wrap the text `Assets` in a `span` element with the `class` attribute set to `sr-only`.

Siguiendo eso, agrega tres elementos `td` con el siguiente texto (en ese order): `$579`, `$736`, `$809`. Dale al tercer elemento `td` un atributo `class` establecido en `current`.

```html
  <tr class="total">
    <th>Total <span class="sr-only">Assets</span></th>
    <td>$579</td>
    <td>$736</td>
    <td class="current">$809</td>
  </tr>
```

## Paso 17

Es hora de movernos a tu segunda tabla. Empieza dándole un elemento `caption` establecido en `Liabilities`. Then add your `thead` and `tbody`.

```html
  <table>
    <caption>Liabilities</caption>
    <thead></thead>
    <tbody></tbody>
  </table>
```

## Paso 18

Within your `thead`, add a `tr`. Dentro de eso, agrega un elemento `td` y tres elementos `th`.

```html
  <table>
    <caption>Liabilities</caption>
    <thead>
      <tr>
        <td></td>
        <th></th>
        <th></th>
        <th></th>
      </tr>
    </thead>
    <tbody>
    </tbody>
  </table>
```

## Paso 19

Give each `th` element a `span` element with the `class` set to `sr-only` and the following text, in order: `2019`, `2020`, and `2021`.

```html
  <table>
    <caption>Liabilities</caption>
    <thead>
      <tr>
        <td></td>
        <th><span class="sr-only">2019</span></th>
        <th><span class="sr-only">2020</span></th>
        <th><span class="sr-only">2021</span></th>
      </tr>
    </thead>
    <tbody>
    </tbody>
  </table>
```

## Paso 20

Dentro del elemento `tbody`, agrega cuatro elementos `tr`. Dale al primero de los tres el atributo `class` establecido en `data` y al cuarto el atributo `class` establecido en `total`.

```html
  <table>
    <caption>Liabilities</caption>
    <thead>
      <tr>
        <td></td>
        <th><span class="sr-only">2019</span></th>
        <th><span class="sr-only">2020</span></th>
        <th><span class="sr-only">2021</span></th>
      </tr>
    </thead>
    <tbody>
      <tr class="data"></tr>
      <tr class="data"></tr>
      <tr class="data"></tr>
      <tr class="total"></tr>
    </tbody>
  </table>
```

## Paso 21

Dentro del primer `tr`, agrega un elemento `th` con el texto `Loans The outstanding balance on our startup loan.`. Wrap that text, except for `Loans`, within a `span` element with the `class` set to `description`.

Agrega tres elementos `td` debajo de eso y dales el siguiente texto, en ese orden: `$500`, `$250` y `$0`. Dale al tercer elemento `td` un `class` establecido en `current`.

```html
  <tr class="data">
    <th>
      Loans <span class="description">The outstanding balance on our startup loan.</span>
    </th>
    <td>$500</td>
    <td>$250</td>
    <td class="current">$0</td>
  </tr>
  <tr class="data">
  </tr>
  <tr class="data">
  </tr>
  <tr class="total">
  </tr>
```

## Paso 22

Dentro del segundo `tr`, agrega un elemento `th` con el texto `Expenses Annual anticipated expenses, such as payroll.`. Wrap that text, except for `Expenses`, within a `span` element with the `class` set to `description`.

Agrega tres elementos `td` debajo de eso y dales el siguiente texto, en ese orden: `$200`, `$300` y `$400`. Dale al tercer elemento `td` un `class` establecido en `current`.

```html
  <tr class="data">
    <th>Loans <span class="description">The outstanding balance on our startup loan.</span></th>
    <td>$500</td>
    <td>$250</td>
    <td class="current">$0</td>
  </tr>
  <tr class="data">
    <th>Expenses <span class="description">Annual anticipated expenses, such as payroll.</span></th>
    <td>$200</td>
    <td>$300</td>
    <td class="current">$400</td>
  </tr>
  <tr class="data">
  </tr>
  <tr class="total">
  </tr>
```

## Paso 23

Dentro del tercer `tr`, agrega un elemento `th` con el texto `Credit The outstanding balance on our credit card.`. Wrap that text, except for `Credit`, within a `span` element with the `class` set to `description`.

Agrega tres elementos `td` debajo de eso, y dales el siguiente texto, en ese orden: `$50`, `$50` y `$75`. Dale al tercer elemento `td` un `class` establecido en `current`.

```html
  <tr class="data">
    <th>Loans <span class="description">The outstanding balance on our startup loan.</span></th>
    <td>$500</td>
    <td>$250</td>
    <td class="current">$0</td>
  </tr>
  <tr class="data">
    <th>Expenses <span class="description">Annual anticipated expenses, such as payroll.</span></th>
    <td>$200</td>
    <td>$300</td>
    <td class="current">$400</td>
  </tr>
  <tr class="data">
    <th>Credit <span class="description">The outstanding balance on our credit card.</span></th>
    <td>$50</td>
    <td>$50</td>
    <td class="current">$75</td>
  </tr>
  <tr class="total">
  </tr>
```

## Paso 24

En tu cuarto elemento `tr`, agrega un elemento `th` con el texto `Total Liabilities`. Wrap the text `Liabilities` in a `span` element with the `class` attribute set to `sr-only`.

Siguiendo eso, agrega tres elementos `td` con el siguiente texto (en ese orden): `$750`, `$600`, `$475`. Dale al tercer elemento `td` un atributo `class` establecido en `current`.

```html
  <tr class="data">
    <th>Loans <span class="description">The outstanding balance on our startup loan.</span></th>
    <td>$500</td>
    <td>$250</td>
    <td class="current">$0</td>
  </tr>
  <tr class="data">
    <th>Expenses <span class="description">Annual anticipated expenses, such as payroll.</span></th>
    <td>$200</td>
    <td>$300</td>
    <td class="current">$400</td>
  </tr>
  <tr class="data">
    <th>Credit <span class="description">The outstanding balance on our credit card.</span></th>
    <td>$50</td>
    <td>$50</td>
    <td class="current">$75</td>
  </tr>
  <tr class="total">
    <th>Total <span class="sr-only">Liabilities</span></th>
    <td>$750</td>
    <td>$600</td>
    <td class="current">$475</td>
  </tr>
```

## Paso 25

Para tu tercera tabla, agrega un `caption` con el texto `Net Worth` y configura la cabecera y el cuerpo de la tabla.

```html
  <table>
    <caption>Net Worth</caption>
    <thead></thead>
    <tbody></tbody>
  </table>
```

## Paso 26

Dentro de tu `thead`, crea un elemento `tr`. Dentro de eso, agrega un elemento `td` y tres elementos `th`. Within each of the `th` elements, add a span element with the `class` set to `sr-only` and the following text, in order: `2019`, `2020`, and `2021`.

```html
  <table>
    <caption>Net Worth</caption>
    <thead>
      <tr>
        <td></td>
        <th><span class="sr-only">2019</span></th>
        <th><span class="sr-only">2020</span></th>
        <th><span class="sr-only">2021</span></th>
      </tr>
    </thead>
    <tbody>
    </tbody>
  </table>
```

## Paso 27

Within the `tbody`, add a `tr` with the `class` set to `total`. In that, add a `th` with the text `Total Net Worth`, and wrap `Net Worth` in a `span` with the `class` set to `sr-only`.

Luego agrega tres elementos `td`, dando al tercero un `class` establecido en `current`, y dando a cada uno el siguiente texto: `$-171`, `$136`, `$334`.

```html
  <table>
    <caption>Net Worth</caption>
    <thead>
      <tr>
        <td></td>
        <th><span class="sr-only">2019</span></th>
        <th><span class="sr-only">2020</span></th>
        <th><span class="sr-only">2021</span></th>
      </tr>
    </thead>
    <tbody>
      <tr class="total">
        <th>Total <span class="sr-only">Net Worth</span></th>
        <td>$-171</td>
        <td>$136</td>
        <td class="current">$334</td>
      </tr>
    </tbody>
  </table>
```

## Paso 28

Es momento de estilizar tu tabla. Empieza restableciendo el modelo de caja. Crea un selector `html` y dale una propiedad `box-sizing` establecida en `border-box`.

```css
html {
  box-sizing: border-box;
}
```

## Paso 29

Crea un selector `body` con una propiedad `font-family` de `sans-serif` y un color de `#0a0a23`.

```css
body {
 font-family: sans-serif;
 color: #0a0a23;
}
```

## Paso 30

Ante de ir demasiado lejos en tu estilización, deberías hacer uso la clase `sr-only`. Puedes usar CSS para hacer que los elementos con esta clase estén completamente ocultos de la página visual, pero que sigan siendo anunciados por los lectores de pantalla.

El CSS que está a punto de escribir es un conjunto común de propiedades utilizadas para asegurar que los elementos estén completamente ocultos visualmente.

El selector `span[class~="sr-only"]` seleccionará cualquier elemento `span` cuyo `class` incluya `sr-only`. Crea ese selector, y dale una propiedad `border` establecida en `0`.

```css
span[class~="sr-only"]{
  border: 0;
}
```

## Paso 31

La propiedad CSS `clip` se utiliza para definir la visibilidad de las partes de un elemento. Configure el selector `span[class~="sr-only"]` para tener una propiedad `clip` con el valor `rect(1px, 1px, 1px, 1px)`.

La propiedad `clip-path` determina la forma que la propiedad `clip` debe tomar. Ajusta la propiedad `clip-path` al valor de `inset(50%)`, formando la región de recorte en un rectángulo dentro del elemento.

```css
span[class~="sr-only"] {
  border: 0;
  clip: rect(1px, 1px, 1px, 1px);
 clip-path: inset(50%);
}
```

## Paso 32

Ahora hay que reducir el tamaño de estos elementos. Dale a tu selector `span[class~="sr-only"]` la propiedad `width` y `height`, establecidas en `1px`.

```css
span[class~="sr-only"] {
  border: 0;
  clip: rect(1px, 1px, 1px, 1px);
  clip-path: inset(50%);
  width: 1px;
 height: 1px;
}
```

## Paso 33

Para evitar que el contenido del texto se desborde, dale a tu selector `span[class~="sr-only"]` una propiedad overflow establecida en `hidden` y una propiedad `white-space` establecida en `nowrap`.

```css
span[class~="sr-only"] {
  border: 0;
  clip: rect(1px, 1px, 1px, 1px);
  clip-path: inset(50%);
  height: 1px;
  width: 1px;
  overflow: hidden;
 white-space: nowrap;
}
```

## Paso 34

Por último, necesitas sacar estos elementos ocultos del flujo del documento. Dale al selector `span[class~="sr-only"]` una propiedad `position` establecida en `absolute`, una propiedad `padding` establecida en `0` y una propiedad `margin` establecida en `-1px`. Esto asegurará que no solo no sean visibles, sino que ni siquiera estén dentro de la vista de la página.

```css
span[class~="sr-only"] {
  border: 0;
  clip: rect(1px, 1px, 1px, 1px);
  clip-path: inset(50%);
  height: 1px;
  width: 1px;
  position: absolute;
  overflow: hidden;
  white-space: nowrap;
  padding: 0;
  margin: -1px;
}
```

## Paso 35

Es el momento de dar estilo a la cabecera de tu tabla. Crea un selector `h1`. Dale una propiedad `max-width` establecida en `37.25rem`, una propiedad `margin` establecida en `0 auto` y una propiedad `padding` establecida en `1.5rem 1.25rem`.

```css
h1 {
  max-width: 37.25rem;
  margin: 0 auto;
  padding: 1.5rem 1.25rem;
}
```

## Paso 36

Apunta a tu contenedor flex con un selector `h1 .flex`. Dale una propiedad `display` establecida en `flex` para habilitar el diseño flexbox. Luego establece la propiedad `flex-direction` a `column-reverse` - esto mostrara los elementos anidados del fondo en la parte superior. Por último, establece la propiedad `gap` en `1rem` para crear algo de espacio entre los elementos.

```css
h1 .flex {
  display: flex;
  flex-direction: column-reverse;
  gap: 1rem;
}
```

## Paso 37

El pseudo-selector `:first-of-type` se utiliza para apuntar al primer elemento que coincida con el selector. Crea un selector `h1 .flex` `span:first-of-type` para apuntar al primer elemento `span` en tu contenedor `.flex`. Recuerda que tus elementos `span` están invertidos, visualmente, por lo que este aparecerá como el segundo elemento en la página.

Dale a tu nuevo selector una propiedad `font-size` de `0.7em` para que se parezca más a un subtítulo.

```css
h1 .flex span:first-of-type {
  font-size: 0.7em;
}
```

## Paso 38

El pseudo-selector `:last-of-type` hace exactamente lo contrario - apunta al último elemento que coincida con el selector. Crea un selector `h1 .flex span:last-of-type` para apuntar al último `span` en tu contenedor flex, y dale una propiedad `font-size` establecida en `1.2em` para que se vea como un encabezado.

```css
h1 .flex span:last-of-type{
  font-size: 1.2em;
}
```

## Paso 39

Has envuelto tu tabla en un elemento de sección - ahora puedes estilizarla para darle un borde a tu tabla. Crea un selector `section`, y dale una propiedad `max-width` establecida en `40rem` para un diseño adaptativo. Establece la propiedad `margin` a `0 auto` para centrarlo, y establece la propiedad `border` a `2px solid #d0d0d5`.

```css
section {
 max-width: 40rem;
 margin: 0 auto;
 border: 2px solid #d0d0d5;
}
```

## Paso 40

La última parte del encabezamiento de la tabla son los años. Crea un selector `#years` y habilita el flexbox. Alinea el contenido hasta el final de la dirección flex, y haz que el elemento este posicionado fijamente. Fíjalo en la parte superior de su contenedor con `top: 0`.

```css
#years {
  display: flex;
  justify-content: flex-end;
  position: sticky;
 top: 0;
}
```

## Paso 41

Ahora aplica un poco de color a tu `#years`. Dale al texto el color `#fff` y al fondo el color `#0a0a23`.

```css
#years {
  display: flex;
  justify-content: flex-end;
  position: sticky;
  top: 0;
  color: #fff;
  background-color: #0a0a23;
}
```

## Paso 42

La función `calc()` es una función CSS que te permite calcular un valor basado en otros valores. Por ejemplo, lo puedes usar para calcular el ancho del viewport menos el margen de un elemento:

- **Código de ejemplo**:
  
  ```css
  .example {
    margin: 10px;
    width: calc(100% - 20px);
  }
  ```

Dale a #years un `margin` de `0 -2px`, y un `padding` establecido en `0.5rem calc(1.25rem + 2px) 0.5rem 0`.

```css
#years {
  display: flex;
  justify-content: flex-end;
  position: sticky;
  top: 0;
  background: #0a0a23;
  color: #fff;
  margin: 0 -2px;
  padding: 0.5rem calc(1.25rem + 2px) 0.5rem 0;
}
```

## Paso 43

Añadir la posición `sticky` movió el elemento a su propio grupo. Para asegurarse de que tu elemento `#years` no sea ocultado por diferentes grupos, añade una propiedad `z-index` establecida en `999` en la regla `#years`.

```css
#years {
  display: flex;
  justify-content: flex-end;
  position: sticky;
  top: 0;
  background: #0a0a23;
  color: #fff;
  padding: 0.5rem calc(1.25rem + 2px) 0.5rem 0;
  margin: 0 -2px;
  z-index: 999;
}
```

## Paso 44

Estiliza tu texto dentro de tu elemento `#years` creando un selector `#years span[class]`. La sintaxis `span[class]` apuntará a cualquier elemento `span` que tenga un atributo `class`, independientemente del valor del atributo.

Dale a tu nuevo selector una fuente `bold` (en negrita), un ancho de `4.5rem` y un texto alineado a la derecha.

```css
#years span[class] {
  font-weight: bold;
  width: 4.5rem;
  text-align: right;
}
```

## Paso 45

Envolviste tus tablas en un contenedor con la clase `table-wrap`. Crea un selector para esa clase y dale un `padding` establecido en `0 0.75rem 1.5rem 0.75rem`.

```css
.table-wrap {
  padding: 0 0.75rem 1.5rem 0.75rem;
}
```

## Paso 46

Antes de que empieces a sumergirte en la tabla misma, tus elementos `span` están actualmente en negrita. Crea un selector `span:not(.sr-only)` y dale una propiedad `font-weight` establecida en `normal`.

El pseudo-selector `:not()` se utiliza para apuntar a todos los elementos que no coinciden con el selector - en este caso, cualquiera de tus elementos `span` que no tengan la clase `sr-only`. Esto asegura que tus reglas anteriores para el selector `span[class~="sr-only"]` no se sobreescriban.

```css
span:not(.sr-only) {
  font-weight: normal;
}
```

## Paso 47

En lugar de tener que revisar constantemente que no sobrescribas tus propiedades, puedes usar la palabra clave `!important` para asegurar que esas propiedades siempre serán aplicadas, sin importar el orden o la especificidad.

Dale a cada propiedad en tu selector `span[class~="sr-only"]` una palabra clave `!important`. No cambies ninguno de los valores.

```css
span[class~="sr-only"] {
  border: 0 !important;
  clip: rect(1px, 1px, 1px, 1px) !important;
  clip-path: inset(50%) !important;
  width: 1px !important;
  height: 1px !important;
  position: absolute !important;
  overflow: hidden !important;
  white-space: nowrap !important;
  padding: 0 !important;
  margin: -1px !important;
}
```

## Paso 48

Ahora que tienes agregada la palabra clave `!important`, puedes eliminar el `:not(.sr-only)` de tu selector `span`.

```css
span {
  font-weight: normal;
}
```

## Paso 49

Crea un selector `table` para apuntar a tus tablas. Establece la propiedad `border-collapse` en `collapse`, lo que permitirá que los bordes de las celdas se contraigan en un solo borde, en lugar de un borde alrededor de cada celda. También establece la propiedad `border` en `0` para ocultar los bordes.

```css
table {
  border-collapse: collapse;
  border: 0;
}
```

## Paso 50

Asegúrate de que tu tabla llene su contenedor con una propiedad `width` establecida en `100%`, luego posiciónalo relativamente y dale un margen superior de `3rem`.

```css
table {
  border-collapse: collapse;
  border: 0;
  width: 100%;
  position: relative;
  margin-top: 3rem;
}
```

## Paso 51

A continuación, necesitas estilizar tus elementos `caption` para que se parezcan más a encabezados. Crea un selector `table caption`. Configura el texto para que tenga un color de `#356eaf`, un tamaño de `1.3em` y un grosor normal.

```css
table caption {
  font-weight: normal;
  color: #356eaf;
  font-size: 1.3em;
}
```

## Paso 52

Ahora dale a los subtítulos una posición absoluta, y muévelos `-2.25rem` desde arriba y `0.5rem` desde la izquierda.

```css
table caption {
  color: #356eaf;
  font-size: 1.3em;
  font-weight: normal;
  position: absolute;
  top: -2.25rem;
  left: 0.5rem;
}
```

## Paso 53

Crea un selector que apunte a tus elementos `td` dentro del cuerpo de tu tabla. Dales un ancho para rellenar el viewport, con un mínimo y máximo de `4rem`. Este enfoque asegura que el ancho sea fijo, mientras que ajustando `width` específicamente permitiría que los elementos se encojan dentro del contenedor.

```css
tbody td {
  width: 100vw;
  min-width: 4rem;
  max-width: 4rem;
}
```

## Paso 54

Ahora apunta a los elementos `th` dentro del cuerpo de tu tabla, y dales un ancho de todo el contenedor, menos `12rem`.

```css
tbody th {
  width: calc(100% - 12rem);
}
```

## Paso 55

El selector `[attribute="value"]` apunta a cualquier elemento que tenga un atributo con un valor específico. Crea un selector `tr[class="total"]` para apuntar específicamente a tus elementos `tr` con la clase `total`. Dale un borde inferior de `4px double #0a0a23` y haz la fuente negrita.

```css
tr[class="total"] {
  border-bottom: 4px double #0a0a23;
  font-weight: bold;
}
```

## Paso 56

Usando la misma sintaxis del selector anterior y apunta a los elementos `th` dentro de las filas de tu tabla, donde el `class` es `total`. Alinea el texto a la izquierda, y dales un relleno de `0.5rem 0 0.25rem 0.5rem`.

```css
tr[class="total"] th {
  text-align: left;
  padding: 0.5rem 0 0.25rem 0.5rem;
}
```

## Paso 57

La diferencia clave entre `tr[class="total"]` y `tr.total` es que el primero seleccionara los elementos `tr` donde la única clase sea `total`. The second will select `tr` elements where the class *includes* `total`.

En tu caso, `tr.total` funcionará. Puedes usar este selector para apuntar a todos los elementos `td` dentro de tus filas `.total`. Alinea el texto a la derecha, y dales un relleno de `0 0.25rem`.

```css
tr.total td {
  text-align: right;
  padding: 0 0.25rem;
}
```

## Paso 58

El pseudo-selector `:nth-of-type()` se utiliza para apuntar a elementos específicos en función de su orden entre los hermanos del mismo tipo. Utiliza este pseudo-selector para apuntar al tercer elemento `td` dentro de las filas `total` de tu tabla. Dale un relleno derecho de `0.5rem`.

```css
tr.total td:nth-of-type(3) {
  padding-right: 0.5rem;
}
```

## Paso 59

Dale a tus elementos `tr.total` un efecto hover que cambie el fondo a `#99c9ff`.

```css
tr.total:hover {
  background-color: #99c9ff;
}
```

## Paso 60

Selecciona tus elementos `td` con el valor del `class` establecido en `current`, y haz la fuente cursiva.

```css
td.current {
  font-style: italic;
}
```

## Paso 61

Select the `tr` elements with the `class` set to `data`. Dales una imagen de fondo de `linear-gradient(to bottom, #dfdfe2 1.845rem, white 1.845rem)`.

```css
tr.data {
  background-image: linear-gradient(to bottom, #dfdfe2 1.845rem, white 1.845rem);
}
```

## Paso 62

Selecciona los elementos `th` dentro de tus elementos `tr.data`. Alinea el texto a la izquierda, y dales un margen superior de `0.3rem` y un relleno izquierdo de `0.5rem`.

```css
tr.data th {
  text-align: left;
  padding-top: 0.3rem;
  padding-left: 0.5rem;
}
```

## Paso 63

Crea un selector `tr.data th .description` que apunte a los elementos con el `class` establecido en `description` que estén dentro de tus elementos `th` en las filas de tu tabla `.data`. Dales una visualización de bloque, haz el texto en cursiva con un grosor normal, y colócalos con un padding establecido en `1rem 0 0.75rem` y un margen derecho de `-13.5rem`.

```css
tr.data th .description {
  display: block;
  font-style: italic;
  font-weight: normal;
  padding: 1rem 0 0.75rem;
  margin-right: -13.5rem;
}
```

## Paso 64

Ahora todos tus elementos `span` tienen un estilo más específico, lo que significa que puedes remover tu regla `span`.

```css
/* 
Se elimina span

span {
  font-weight: normal;
}
*/
```

## Paso 65

Tu importe en dólares está actualmente desalineado. Crea un selector que apunte a los elementos `td` dentro de tus elementos `tr.data`. Alinea el texto verticalmente en la parte superior, horizontalmente alinea el texto a la derecha, y establece el relleno en `0.3rem 0.25rem 0`.

```css
tr.data td {
  vertical-align: top;
  text-align: right;
  padding: 0.3rem 0.25rem 0;
}
```

## Paso 66

Crea otro selector para los elementos td dentro de tu elemento tr.data, pero selecciona específicamente el último. Dale un relleno derecho de 0.5rem.

```css
tr.data td:last-of-type {
  padding-right: 0.5rem;
} 
```

>[!NOTE]
>
>**¡Felicidades! ¡Tu balance financiero está completo!**
