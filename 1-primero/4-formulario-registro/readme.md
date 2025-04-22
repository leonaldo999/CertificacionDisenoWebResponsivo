# Aprende formularios HTML construyendo un formulario de registro

- Puedes hacer uso de formularios HTML para recopilar información de las personas que visitan tu página web.

- En este curso, aprenderás formularios de HTML construyendo una página de registro. Aprenderás cómo controlar qué tipo de datos pueden colocarse en tu formulario, y herramientas nuevas de CSS para cambiar el diseño de tu página.

## Paso 1

¡Bienvenido al proyecto de formulario de registro! Para iniciar, añada la declaración `!DOCTYPE` html en la parte superior del documento para que el navegador sepa qué tipo de documento está utilizando.

```html
<!DOCTYPE html>
```

## Paso 2

Abajo del DOCTYPE, añade un elemento html con un atributo lang establecido a en, para que tengas espacio para comenzar a poner código.

```html
<!DOCTYPE html>
<html lang="en">
</html>
```

## Paso 3

A continuación, añadir etiquetas `head` y `body` dentro del elemento `html`.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
  </head>
  <body>
  </body>
</html>
```

## Paso 4

Añade un `title` y un elemento `meta` dentro del elemento `head`. Dale a tu proyecto el título de `Registration Form` y añade el atributo `charset` con el valor `utf-8` a tu elemento `meta`.

```html
<head>
  <meta charset="UTF-8">
  <title>Registration Form</title>
</head>
```

## Paso 5

Anida un elemento `link` dentro del elemento `head`. Dale un atributo `rel` con el valor de `stylesheet` y un atributo `href` con un valor de `styles.css`.

```html
<head>
  <meta charset="UTF-8">
  <title>Registration Form</title>
  <link rel="stylesheet" href="styles.css">
</head>
```

## Paso 6

Dentro del `body`, proporciona un contexto de encabezado para el contenido, agregando un `h1` con el texto `Registration Form`.

```html
<body>
  <h1>Registration Form</h1>
</body>
```

## Paso 7

Debajo del encabezado, utilice el siguiente texto dentro de un elemento de párrafo para animar a los usuarios a registrarse:

```html
<body>
  <h1>Registration Form</h1>
  <p>Please fill out this form with the required information</p>
</body>
```

## Paso 8

La unidad `vh` significa viewport height (altura de la pantalla) y es relativa al 1% de la altura `(height`) de la pantalla. Esto la hace relativa a la altura de la pantalla/ventana gráfica.

Es hora de engalanar el proyecto con un poco de CSS. Comienza estableciendo para `body` la propiedad `width` a `100%`, y la propiedad `height` a `100vh`.

```css
body {
 width: 100%;
 height: 100vh;
}

```

## Paso 9

Ahora, deshazte de la barra de desplazamiento horizontal, estableciendo el `margin` por defecto del `body` añadido por algunos navegadores a `0`.

```css
body {
  width: 100%;
  height: 100vh;
  margin: 0
}
```

## Paso 10

Eso es mejor. Ahora, haz que el fondo sea fácil de ver, cambiando el `body` `background-color` a `#1b1b32`. Luego, para ver el texto, cambia el `color` a `#f5f6f7`.

```css
body {
  width: 100%;
  height: 100vh;
  margin: 0;
  background-color: #1b1b32;
 color: #f5f6f7;
}
```

## Paso 11

Como sugiere el título, estás creando un formulario. Por lo tanto, después del elemento `p` inserta un `form` con un atributo de `action` apuntando a `<https://register-demo.freecodecamp.org>`.

```html
<body>
  <h1>Registration Form</h1>
  <p>Please fill out this form with the required information</p>
  <form action="https://register-demo.freecodecamp.org"></form>
</body>
```

## Paso 12

El atributo `method` especifica cómo enviar datos de formulario a la dirección URL especificada en el atributo `action`. Los datos del formulario se pueden enviar a través de una solicitud `GET` como parámetros de URL (con `method="get"`) o mediante una solicitud POST como datos en el cuerpo de la solicitud (con method="post").

Establezca el atributo `method` para enviar los datos del formulario a través de una solicitud `POST`.

```html
<form action='https://register-demo.freecodecamp.org' method="post"></form>
```

## Paso 13

Como el formulario tiene tres secciones distintas, agrega tres elementos `fieldset` dentro del elemento `form`.

```html
<body>
  <h1>Registration Form</h1>
  <p>Please fill out this form with the required information</p>
  <form method="post" action='https://register-demo.freecodecamp.org'>
  <fieldset></fieldset>
  <fieldset></fieldset>
  <fieldset></fieldset>
  </form>
</body>
```

## Paso 14

El primer `fieldset` contendrá los campos de nombre, email y contraseña. Empieza agregando cuatro elementos `label` al primer `fieldset`.

```html
<form method="post" action='https://register-demo.freecodecamp.org'>
  <fieldset>
  <label></label>
  <label></label>
  <label></label>
  <label></label>
  </fieldset>
  <fieldset></fieldset>
  <fieldset></fieldset>
</form>
```

## Paso 15

Agrega el siguiente texto a los elementos `label`:

- `Enter Your First Name:`
- `Enter Your Last Name:`
- `Enter Your Email:`
- `Create a New Password:`

```html
<fieldset>
  <label>Enter Your First Name:</label>
  <label>Enter Your Last Name:</label>
  <label>Enter Your Email:</label>
  <label>Create a New Password:</label>
</fieldset>
```

## Paso 16

La unidad `rem` significa root (raíz) `em`, y es relativa al tamaño de fuente del elemento `html`.

Como los elementos `label` por defecto son inline, se muestran todos juntos en la misma línea, haciendo difícil su lectura. Para mostrarlos en diferentes líneas, añade `display: block` al elemento `label`, y dale a la propiedad `margin` un valor de `0.5rem 0`, para darles un poco de separación.

```css
label {
 display: block;
 margin: 0.5rem 0;
}
```

## Paso 17

Anida un elemento `input` dentro de cada `label`. Asegúrate de agregar cada `input` después del texto del `label`, e incluye un espacio después de los dos puntos.

```html
<fieldset>
  <label>Enter Your First Name: <input type="text"></label>
  <label>Enter Your Last Name: <input type="text"></label>
  <label>Enter Your Email: <input type="text"></label>
  <label>Create a New Password: <input type="text"></label>
</fieldset>
```

## Paso 18

Siguiendo las mejores prácticas de accesibilidad, vincule los elementos `input` y los elementos `label` utilizando el atributo `for`.

Utiliza `first-name`, `last-name`, `email` y `new-password` como valores para los respectivos atributos `id`.

```html
<fieldset>
  <label for="first-name">Enter Your First Name: <input id="first-name" type="text"></label>
  <label for="last-name">Enter Your Last Name: <input id="last-name" type="text"></label>
  <label for="email">Enter Your Email: <input id="email" type="text"></label>
  <label for="new-password">Create a New Password: <input id="new-password" type="text"></label>
</fieldset>
```

## Paso 19

Especificar el atributo `type` de un elemento de formulario es importante para que el navegador sepa qué tipo de datos debe esperar. Si el `type` no está especificado, el navegador utilizará por defecto `text`.

Da a los dos primeros elementos `input` un atributo `type` de `text`, al tercero un atributo `type` de `email` y al cuarto un atributo `type` de `password`.

El type `email` solo permite correos electrónicos con un `@` y un `.` en el dominio. El type password oculta la entrada, y advierte si el sitio no utiliza HTTPS.

```html
<fieldset>
  <label for="first-name">Enter Your First Name: <input id="first-name" type="text"></label>
  <label for="last-name">Enter Your Last Name: <input id="last-name" type="text"></label>
  <label for="email">Enter Your Email: <input id="email" type="email"></label>
  <label for="new-password">Create a New Password: <input id="new-password" type="password"></label>
</fieldset>
```

## Paso 20

El primer elemento `input` con un `type` de `submit` se establece automáticamente para enviar a su elemento `form` padre más cercano.

Para manejar el envío del formulario, después del último elemento `fieldset` agrega un elemento `input` con el atributo `type` establecido en `submit` y el atributo `value` establecido en `Submit`.

```html
<fieldset>
    <label for="first-name">Enter Your First Name: <input id="first-name" type="text" /></label>
    <label for="last-name">Enter Your Last Name: <input id="last-name" type="text" /></label>
    <label for="email">Enter Your Email: <input id="email" type="email" /></label>
    <label for="new-password">Create a New Password: <input id="new-password" type="password" /></label>
  </fieldset>
  <fieldset></fieldset>
  <fieldset></fieldset>
<input type="submit" value="Submit">
```

## Paso 21

En este punto, deberías poder enviar el formulario. Sin embargo, puede notar que no pasa casi nada.

Para hacer el formulario más interactivo, agrega el atributo `required` a los elementos `input` en el primer `fieldset`.

Ahora, si intentas enviar el formulario sin rellenar los campos requeridos, verá un mensaje de error.

```html
<fieldset>
  <label for="first-name">Enter Your First Name: <input id="first-name" type="text" required></label>
  <label for="last-name">Enter Your Last Name: <input id="last-name" type="text" required></label>
  <label for="email">Enter Your Email: <input id="email" type="email" required></label>
  <label for="new-password">Create a New Password: <input id="new-password" type="password" required></label>
</fieldset>
<fieldset></fieldset>
<fieldset></fieldset>
<input type="submit" value="Submit" />
```

## Paso 22

Algunos valores del atributo `type` vienen con una validación de formulario incorporada. Por ejemplo, `type="email"` requiere que el valor sea una dirección de correo electrónico válida.

Agrega validación personalizada al elemento `input` de contraseña, agregando un atributo `minlength` con un valor de `8`. De este modo se evita que se envíen entradas de menos de 8 caracteres.

```html
<fieldset>
  <label for="first-name">Enter Your First Name: <input id="first-name" type="text" required /></label>
  <label for="last-name">Enter Your Last Name: <input id="last-name" type="text" required /></label>
  <label for="email">Enter Your Email: <input id="email" type="email" required /></label>
  <label for="new-password">Create a New Password: <input id="new-password" type="password" required required minlength="8"/></label>
</fieldset>
```

## Paso 23

Con el `type="password"` puedes usar el atributo `pattern` para definir una expresión regular que la contraseña debe coincidir para ser considerada válida.

Agrega un atributo `pattern` al elemento `input` de contraseña para requerir que la entrada coincida con: `[a-z0-5]{8,}`

Lo anterior es una expresión regular que coincide con ocho o más letras minúsculas o los dígitos del `0` al `5`. Luego, elimina el atributo `minlength`, y pruébalo.

```html
<fieldset>
  <label for="first-name">Enter Your First Name: <input id="first-name" type="text" required /></label>
  <label for="last-name">Enter Your Last Name: <input id="last-name" type="text" required /></label>
  <label for="email">Enter Your Email: <input id="email" type="email" required /></label>
  <label for="new-password">Create a New Password: <input id="new-password" type="password" pattern="[a-z0-5]{8,}" required /></label>
</fieldset>
```

## Paso 24

Pasemos a la siguiente parte del formulario de registro. Esta sección pedirá el tipo de cuenta que el usuario está creando.

Empieza agregando dos elementos `label` al segundo `fieldset`.

```html
<fieldset>
  <label></label>
  <label></label>
</fieldset>
```

## Paso 25

Los usuarios podrán elegir entre `Personal` o `Business`.

Para ello, dentro de cada uno de los dos primeros elementos `label`, agrega un elemento `input` con el `type="radio"`.

```html
<fieldset>
  <label><input type="radio"></label>
  <label><input type="radio"></label>
</fieldset>
```

## Paso 26

Dentro de cada elemento `label` correspondiente, e inmediatamente después del elemento `input`, agrega un espacio y agregar el siguiente texto:

`Personal` y `Business` respectivamente.

```html
<label><input type="radio" /> Personal</label>
<label><input type="radio" /> Business</label>
```

## Paso 27

Solo quieres que se pueda seleccionar un input de radio a la vez. Sin embargo, el formulario no sabe que los inputs de radio están relacionadas.

Para relacionar los inputs de radio, dales el mismo atributo `name` con un valor de `account-type`. Ahora, no es posible seleccionar ambos inputs de radio al mismo tiempo.

```html
<fieldset>
  <label><input type="radio" name="account-type"/> Personal</label>
  <label><input type="radio" name="account-type"/> Business</label>
</fieldset>
```

## Paso 28

Por ahora, los usuarios pueden enviar el formulario sin seleccionar los inputs de tipo radio. Aunque anteriormente usaste el atributo `required` para indicar que un input es obligatorio, en este caso, añadir `required` a ambos inputs no funcionará, ya que transmitirá información incorrecta a los usuarios.

Para resolver esto, puedes proporcionar contexto de lo que se necesita, añadiendo un elemento `legend` (leyenda) con el texto `Account type (required)` antes de los elementos `label` dentro del segundo `fieldset`. Después añade un atributo `checked` al input con el texto `Personal` para asegurarse de que el formulario se envía con los datos requeridos.

```html
<fieldset>
  <legend>Account type (required)</legend>
  <label><input type="radio" name="account-type" checked/> Personal</label>
  <label><input type="radio" name="account-type" /> Business</label>
</fieldset>
```

## Paso 29

Siga las mejores prácticas de accesibilidad vinculando los elementos `input` y los elementos `label` en el segundo `fieldset`.

Utiliza `personal-account` y `business-account` como valores para los respectivos atributos `id`.

```html
<fieldset>
  <legend>Account type (required)</legend>
  <label for="personal-account"><input id="personal-account" type="radio" name="account-type" checked/> Personal</label>
  <label for="business-account"><input id="business-account" type="radio" name="account-type"/> Business</label>
</fieldset>
```

## Paso 30

Debe confirmar que el usuario ha leído los términos y condiciones (terms and conditions).

Añade un elemento `label`. Dentro del nuevo elemento `label`, agrega un elemento `input` con un atributo `type` con el valor `checkbox`. Haz que este elemento `input` sea requerido (`required`) para que los usuarios no puedan registrarse sin leer los términos y condiciones.

Añade un atributo `id` y un atributo `for` y dales el valor `terms-and-conditions` para la accesibilidad.

```html
    <label for="terms-and-conditions">
      <input id="terms-and-conditions" type="checkbox" required> 
    </label>
```

## Paso 31

Añade el texto `I accept the terms and conditions` inmediatamente después del elemento de `input` en la `label` recién añadida. Después, vincula el texto `terms and conditions` al siguiente enlace:
`https://www.freecodecamp.org/news/terms-of-service/
`

```html
    <label for="terms-and-conditions">
      <input id="terms-and-conditions" type="checkbox" required> I accept the <a
        href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
    </label>
```

## Paso 32

Pasando al final `fieldset`. ¿Qué pasa si quisieras permitir que un usuario suba una foto de perfil?

Bueno, el `input` con tipo `file` permite eso. Agrega un `label` con el texto `Upload a profile picture:` y anida un `input` aceptando la carga de un archivo.

```html
    <fieldset>
      <label for="">
        Upload a profile picture: 
        <input type="file" accept="image/*" required>
      </label>
    </fieldset>
```

## Paso 33

Añade otro `label` después del primero, con el texto `Input your age (years):`. Then, nest an `input` with the `type` of `number`.

A continuación, añade un atributo `min` al `input` con un valor de `13` porque los usuarios menores de 13 años no deben registrarse. Además, los usuarios probablemente no superen la edad de 120; agregue un atributo `max` con un valor de `120`.

Ahora, si alguien intenta enviar el formulario con valores fuera del rango, aparecerá una advertencia, y el formulario no enviará. Pruébalo.

```html
      <label for="">
        Input your age (years):
        <input type="number" min="13" max="120">
      </label>
```

## Paso 34

Añadir un menú desplegable al formulario es fácil con el elemento `select`. El elemento `select` es un contenedor para un grupo de elementos `option`, y el elemento `option` actúa como una etiqueta para cada opción desplegable. Ambos elementos requieren etiquetas de cierre.

Comienza añadiendo un elemento `select` debajo de los dos elementos `label`. Luego, anida 5 elementos `option` dentro del elemento `select`.

```html
    <fieldset>
      <label>Upload a profile picture: <input type="file" /></label>
      <label>Input your age (years): <input type="number" min="13" max="120" /></label>
      <select>
        <option></option>
        <option></option>
        <option></option>
        <option></option>
        <option></option>
      </select>
    </fieldset>
```

## Paso 35

Nida el elemento `select` (con sus elementos `option`) dentro de `label` con el texto `How did you hear about us?.` El texto debe venir antes del elemento `select`.

```html
    <fieldset>
      <label>Upload a profile picture: <input type="file" /></label>
      <label>Input your age (years): <input type="number" min="13" max="120" /></label>
      <label>
        How did you hear about us?
        <select>
          <option></option>
          <option></option>
          <option></option>
          <option></option>
          <option></option>
        </select>
      </label>
    </fieldset>
```

## Paso 36

Las opciones desplegables están actualmente vacías. Para darles contenido, agregue el siguiente texto a cada elemento subsecuente de `option`:

- (select one)
- freeCodeCamp News
- freeCodeCamp YouTube Channel
- freeCodeCamp Forum
- Other

```html
      <fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" /></label>
        <label>How did you hear about us?
          <select>
            <option>(select one)</option>
            <option>freeCodeCamp News</option>
            <option>freeCodeCamp YouTube Channel</option>
            <option>freeCodeCamp Forum</option>
            <option>Other</option>
          </select>
        </label>
      </fieldset>
```

## Paso 37

Enviar el formulario con una opción seleccionada no enviaría un valor útil al servidor. Por lo tanto, cada elemento `option` necesita que se le dé un atributo `value`. Sin el cual, el contenido de texto del `option` será enviado al servidor.

Dale al primer `option` un `value` de `""`, y a los elementos `option` subsecuentes atributos `value` del `1` al `4`.

```html
    <fieldset>
      <label for="">
        Upload a profile picture:
        <input type="file" accept="image/*" required>
      </label>
      <label for="">
        Input your age (years):
        <input type="number" min="13" max="120">
      </label>
      <label>
        How did you hear about us?
        <select>
          <option value="">(select one)</option>
          <option value="1">freeCodeCamp News</option>
          <option value="2">freeCodeCamp YouTube Channel</option>
          <option value="3">freeCodeCamp Forum</option>
          <option value="4">Other</option>
        </select>
      </label>
    </fieldset>
```

## Paso 38

El elemento `textarea` actúa como un elemento `input` de tipo `text`, pero viene con la ventaja añadida de poder recibir texto de varias líneas, y un número inicial de filas y columnas.

Los usuarios podrán registrarse con una biografía. Agregar un `label` con el texto `Provide a bio:` al final del `fieldset`. Agrega un elemento `textarea` dentro del elemento `label`. Tenga en cuenta que el elemento `textarea` requiere una etiqueta de cierre.

```html
    <fieldset>
      <label>Upload a profile picture: <input type="file" /></label>
      <label>Input your age (years): <input type="number" min="13" max="120" /></label>
      <label>How did you hear about us?
          <select>
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
      <label>
        Provide a bio:
        <textarea></textarea>
      </label>
    </fieldset>
```

## Paso 39

Vincule los elementos de formulario aplicables y con sus elementos `label`.

Utiliza `profile-picture`, `age`, `referrer` y `bio` como valores para los respectivos atributos `id`.

```html
    <fieldset>
      <label for="profile-picture">
        Upload a profile picture:
        <input id="profile-picture" type="file" accept="image/*" required>
      </label>
      <label for="age">
        Input your age (years):
        <input id="age" type="number" min="13" max="120">
      </label>
      <label for="referrer">
        How did you hear about us?
        <select id="referrer">
          <option value="">(select one)</option>
          <option value="1">freeCodeCamp News</option>
          <option value="2">freeCodeCamp YouTube Channel</option>
          <option value="3">freeCodeCamp Forum</option>
          <option value="4">Other</option>
        </select>
      </label>
      <label for="bio">
        Provide a bio:
        <textarea id="bio"></textarea>
      </label>
    </fieldset>
```

## Paso 40

El `textarea` aparece demasiado pequeño. Para darle un tamaño inicial, puedes agregar los atributos `rows` y `cols`.

Agrega un tamaño inicial de `3` filas (rows) y `30` columnas (columns).

```html
      <fieldset>
        <label for="profile-picture">Upload a profile picture: <input id="profile-picture" type="file" /></label>
        <label for="age">Input your age (years): <input id="age" type="number" min="13" max="120" /></label>
        <label for="referrer">How did you hear about us?
          <select id="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
        <label for="bio">Provide a bio:
          <textarea id="bio" rows="3" cols="30"></textarea>
        </label>
      </fieldset>
```

## Paso 41

Para dar a los campistas una idea de lo que deben poner en su biografía, se utiliza el atributo `placeholder`. El `placeholder` acepta un valor de texto, que se muestra hasta que el usuario empieza a escribir.

Dale al `textarea` un `placeholder` de `I like coding on the beach...`.

```html
    <fieldset>
      <label for="profile-picture">Upload a profile picture: <input id="profile-picture" type="file" /></label>
      <label for="age">Input your age (years): <input id="age" type="number" min="13" max="120" /></label>
      <label for="referrer">How did you hear about us?
          <select id="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
      <label for="bio">Provide a bio:
        <textarea id="bio" rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>
        </label>
    </fieldset>
```

## Paso 42

Con envíos de formularios, es útil y buena práctica proporcionar a cada elemento de la tabla de envío un atributo `name`. Este atributo se utiliza para identificar el elemento en el envío del formulario.

Exceptuando a las dos entradas `radio` (las cuales ya has nombrado), dale a cada elemento enviable un único atributo `name` de tu preferencia.

```html
    <fieldset>
      <label for="first-name">Enter Your First Name: <input id="first-name" name="first-name" type="text" required></label>
      <label for="last-name">Enter Your Last Name: <input id="last-name" name="last-name" type="text" required></label>
      <label for="email">Enter Your Email: <input id="email" name="email" type="email" required></label>
      <label for="new-password">Create a New Password: <input id="new-password" name="new-password" type="password" required
          pattern="[a-z0-5]{8,}"></label>
    </fieldset>
    <fieldset>
      <legend>Account type (required)</legend>
      <label for="personal-account"><input id="personal-account" type="radio" name="account-type" checked />
        Personal</label>
      <label for="business-account"><input id="business-account" type="radio" name="account-type" /> Business</label>
    </fieldset>
    <fieldset>
      <label for="profile-picture">
        Upload a profile picture:
        <input id="profile-picture" name="profile-picture" type="file" accept="image/*" required>
      </label>
      <label for="age">
        Input your age (years):
        <input id="age" name="age" type="number" min="13" max="120">
      </label>
      <label for="referrer">
        How did you hear about us?
        <select id="referrer" name="referrer">
          <option value="">(select one)</option>
          <option value="1">freeCodeCamp News</option>
          <option value="2">freeCodeCamp YouTube Channel</option>
          <option value="3">freeCodeCamp Forum</option>
          <option value="4">Other</option>
        </select>
      </label>
      <label for="bio">
        Provide a bio:
        <textarea id="bio" name="bio" rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>
      </label>
    </fieldset>
    <label for="terms-and-conditions">
      <input id="terms-and-conditions" name="terms-and-conditions" type="checkbox" required> I accept the <a
        href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
    </label>
```

## Paso 43

El HTML para el formulario de registro está terminado. Ahora, puedes mejorar su apariencia.

Empieza cambiando la fuente a `Tahoma`, y el tamaño de fuente a `16px` en el `body`.

```css
body {
 width: 100%;
 height: 100vh;
 margin: 0;
 background-color: #1b1b32;
 color: #f5f6f7;
 font-family: Tahoma, Geneva, Verdana, sans-serif;
 font-size: 16px;
}
```

## Paso 44

Center the `h1` and `p` elements by giving them a `margin` of `1em auto`. Luego, alinea su texto en el `center` (centro) también.

```css
h1,
p {
 margin: 1em auto;
 text-align: center;
}
```

## Paso 45

Centra el elemento `form`, dándole un `margin` de `0 auto`. Luego, fija su tamaño a un ancho máximo de `500px`, y un ancho mínimo de `300px`. En medio de ese rango, permite que tenga un `width` de `60vw`.

```css
form {
 margin: 0 auto;
 max-width: 500px;
 min-width: 300px;
 width: 60vw;
}
```

## Paso 46

Durante el desarrollo, es útil ver los bordes por defecto del `fieldset`. Sin embargo, hacen que el contenido aparezca demasiado separado.

Elimina el `border`, y agrega un relleno de `2rem` solo en la parte superior e inferior de cada `fieldset`. Asegúrate de eliminar el `padding` izquierdo y derecho.

```css
fieldset {
 border: none;
 padding: 2rem 0;
}
```

## Paso 47

Para dar a los elementos `fieldset` un poco de separación, selecciónalos y dales un `border-bottom` de `3px solid #3b3b4f`.

```css
fieldset {
  border: none;
  padding: 2rem 0;
 border-bottom: 3px solid #3b3b4f;
}
```

## Paso 48

El borde del último elemento `fieldset` se ve un poco fuera de lugar. Puedes seleccionar el último elemento de un tipo específico utilizando la pseudo-clase CSS `last-of-type`, de esta manera:

```css
p:last-of-type { }
```

Esto seleccionará el último elemento `p`. Cree un nuevo selector que apunte al último elemento `fieldset` y establezca su `border-bottom` a `none`.

```css
fieldset:last-of-type {
 border-bottom: none;
}
```

## Paso 49

Sería más estético que el texto del `label` apareciera encima de los elementos del formulario.

Selecciona todos los elementos `input`, `textarea` y `select`, y haz que ocupen todo el ancho de sus elementos padre.

Además, agrega `10px` de `margin` a la parte superior de los elementos seleccionados. Establece los otros márgenes a `0`.

```css
input, textarea, select {
 width: 100%;
 margin: 10px 0 0 0;
}
```

## Paso 50

Para el segundo `fieldset`, quieres que el texto del `input` y el `label` aparezcan en la misma línea.

Empieza por dar a los elementos `input` en el segundo `fieldset` una clase `inline`.

```html
    <fieldset>
      <legend>Account type (required)</legend>
      <label for="personal-account">
        <input id="personal-account" type="radio" name="account-type" checked class="inline" />
        Personal
      </label>
      <label for="business-account">
        <input id="business-account" type="radio" name="account-type" class="inline" />
        Business
      </label>
    </fieldset>
```

## Paso 51

Selecciona solos los elementos `.inline`, y dales un `width` de `unset`. Esto eliminará la regla anterior que establece que todos los `input` tengan un `width: 100%`.

```css
.inline {
 width: unset;
}
```

## Paso 52

Agrega un poco de espacio entre los elementos `.inline` y el texto del `label`, dando un `margin` derecho de `0.5em`. Además, establece todos los demás márgenes a `0`.

```css
.inline {
  width: unset;
 margin: 0 0.5em 0 0;
}
```

## Paso 53

Si te fijas bien, te darás cuenta de que los elementos `.inline` están demasiado arriba en la línea.

Para combatir esto, establezca la propiedad `vertical-align` a `middle`.

```css
.inline {
 width: unset;
 margin: 0 0.5em 0 0;
 vertical-align: middle;
}
```

## Paso 54

Para hacer que los elementos `input` y `textarea` se mezclen con el tema de fondo, establece su `background-color` a `#0a0a23`. Luego, dales un borde de un `1px`, que sea de estilo `solid` y sea de un color `#0a0a23`.

```css
input, textarea {
 background-color: #0a0a23;
 border: 1px solid #0a0a23;
}
```

## Paso 55

Actualmente, si escribes en los elementos `input` o `textarea`, no podrás ver el texto. Además, su altura es demasiado pequeña para ser fácil de usar.

Arregla esto, estableciendo el `color` a `#ffffff`, y estableciendo su `min-height` a `2em`.

```css
input, textarea {
  background-color: #0a0a23;
  border: 1px solid #0a0a23;
  color: #ffffff;
 min-height: 2em;
}
```

## Paso 56

Quieres que el elemento `select` siga teniendo un fondo blanco, pero ahora no tiene el mismo `min-height` que los elementos `input` y `textarea`.

Mueve la propiedad `min-height` y el valor para que los tres tipos de elementos tengan el mismo valor `min-height`, y el `select` siga teniendo un fondo blanco.

```css
body {
  width: 100%;
  height: 100vh;
  margin: 0;
  background-color: #1b1b32;
  color: #f5f6f7;
  font-family: Tahoma;
  font-size: 16px;
}

h1, p {
  margin: 1em auto;
  text-align: center;
}

form {
  width: 60vw;
  max-width: 500px;
  min-width: 300px;
  margin: 0 auto;
}

fieldset {
  border: none;
  padding: 2rem 0;
  border-bottom: 3px solid #3b3b4f;
}

fieldset:last-of-type {
  border-bottom: none;
}

label {
  display: block;
  margin: 0.5rem 0;
}

input,
textarea,
select {
  margin: 10px 0 0 0;
  width: 100%;
  min-height: 2em;

}

input, textarea {
  background-color: #0a0a23;
  border: 1px solid #0a0a23;
  color: #ffffff;
}

.inline {
  width: unset;
  margin: 0 0.5em 0 0;
  vertical-align: middle;
}
```

## Paso 57

Para dar estilo al botón de envío, puede utilizar un selector de atributos (attribute), que selecciona un elemento basado en el valor del atributo dado. Aquí hay un ejemplo:

```css
input[name="password"]
```

Lo anterior selecciona los elementos `input` con un atributo `name` con el valor `password`.

Ahora, utiliza el selector de atributos para dar estilo al botón de envío con un `display` de `block`, y un `width` de `60%`.

```css
input[type="submit"] {
 display: block;
 width: 60%;
}
```

## Paso 58

Con un `display` de `block` el botón de envío se sitúa al ras del borde izquierdo de su padre.

Utiliza la misma técnica utilizada para centrar el `form` para centrar el botón de envío.

```css
input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto;
}
```

## Paso 59

Para que el botón de envío se vea más en línea con el resto del formulario, dale el mimo `height` que los otros campos (`2em`). Además, aumente el `font-size` a `1.1rem`.

```css
input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto;
  height: 2em;
 font-size: 1.1rem;
}
```

## Paso 60

Para hacer que el botón de envío aparezca de forma más distintiva, dale un `background-color` de `#3b3b4f`, y un `border-color` de `white`.

```css
input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto;
  height: 2em;
  font-size: 1.1rem;
  background-color: #3b3b4f;
 border-color: white;
}
```

## Paso 61

Por último, para el botón de envío, quieres separarlo del `fieldset` anterior, y ajustar su ancho para que nunca sea inferior a `300px`.

Cambia la propiedad `margin` para incluir `1em` en la parte superior e inferior, dejando los márgenes derecho e izquierdo en `auto`. A continuación ajuste la anchura como se ha descrito anteriormente.

```css
input[type="submit"] {
  display: block;
  width: 60%;
  margin: 1em auto;
  height: 2em;
  font-size: 1.1rem;
  background-color: #3b3b4f;
  border-color: white;
 min-width: 300px;
}
```

## Paso 62

La mayoría de los navegadores inyectan sus propias propiedades y valores CSS por defecto para los diferentes elementos. Si te fijas bien, podrás notar que el `input` de archivo es más pequeño que los otros elementos `input` de texto. Por defecto, se da un `padding` de `1px 2px` a los elementos `input` en los que puedes escribir.

Usando otro selector de atributos, estiliza el `input` con un `type` de `file` para que tenga el mismo relleno que los otros elementos `input`.

```css
input[type="file"] {
 padding: 1px 2px;
}
```

## Paso 63

Hablando de `padding`, el botón de envío se encuentra en la parte inferior del elemento `form`. Agrega `2em` de `padding` solo a la parte inferior del `form`.

```css
form {
  width: 60vw;
  max-width: 500px;
  min-width: 300px;
  margin: 0 auto;
 padding-bottom: 2em;
}
```

## Paso 64

Haz que el `input` del texto terms and conditions sea de tipo `inline` (en línea) añadiendo la clase apropiada en el HTML.

```html
      <label for="terms-and-conditions">
        <input class="inline" id="terms-and-conditions" type="checkbox" required name="terms-and-conditions" /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
      </label>
```

## Paso 65

Por último, cambia el color del texto del enlace `terms and conditions` a `#dfdfe2` añadiendo un nuevo selector en el código CSS.

¡Bien hecho! Ha completado la parte final del proyecto de práctica del *Registration Form*.

```css
a {
 color: #dfdfe2;
 text-decoration: none;
}
```
