# Encuesta

Este es uno de los proyectos necesarios para obtener su certificacion.
Para este proyecto, construira un formulario de encuesta para recopilar datos de usuario

- **Objetivo**: Construye una aplicación que sea funcionalmente similar a `https://survey-form.freecodecamp.rocks`. **No copies este proyecto de demostración**.

## Instrucciones

- 1 Debe tener un título de página en in elemento `h1` con un `id` de `title`

- 2 Debes tener una pequeña explicación en un elemento p con un id de `description`

- 3 Debe tener un elemento `form` con un `id` de `survey-form`

- 4 Dentro del elemento form, debes ser obligatorio (required) ingresar tu nombre en un campo de `input` que tenga un `id` de `name` y un `type` de `text`

- 5 Dentro del elemento form debe ser obligatorio (required) ingresar tu nombre en un campo de `input` que tenga un `id` de `email`

- 6 Si introduces un correo electrónico que no tiene el formato correcto, tú debes ver una alerta de validación en THML5

- 7 Dentro de tu form, tu puedes introducir un número en un campo input que tenga un `id` de `number`

- 8 La entrada de números no debe aceptar caracteres no numéricos, ya sea impidiendo que los escribas o mostrando un error de validación HTML5 (dependiendo del navegador).

- 9 Si ingresas un número que esté fuera del rango de números permitido, que es definido por los atributos `min` y `max`, verás un error de validación de HTML5

- 10 Para los campos de entrada de nombre, email y número, puedes ver los correspondientes elementos `label` en el formulario, que describen el propósito de cada campo con los siguientes id: `id="name-label"`, `id="email-label"` y `id="number-label"`

- 11 Para los campos de entrada de nombre, correo electrónico y número, podrás ver un texto provisional que da una descripción o instrucciones para cada campo

- 12 Dentro del elemento de formulario, debes tener un elemento desplegable `select` con un `id` de `dropdown` con al menos dos opciones para elegir

- 13 Dentro del elemento de formulario, puedes seleccionar una opción de un grupo de al menos dos botones de radio que son agrupados utilizando el atributo `name`

- 14 Dentro del elemento de formulario, puedes seleccionar varios campos en una serie de casillas de verificación, cada una debe tener un atributo value

- 15 Dentro del elemento de formulario, se te presenta un textarea para comentarios adicionales

- 16 Dentro del elemento form, se te presenta un botón con un id de submit para enviar todas las entradas

Completa las intrucciones y pasa los tests de abajo para completar este projecto. Dale tu estilo personal. ¡Que tengas una feliz programación!

>[!NOTE]
>
>Asegúrese de adicionar `<link rel="stylesheet" href="styles.css">` en su HTML para enlazar su hoja de estilos y aplicarla a su CSS

## SOLUCION

### EL html

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Encuesta</title>
  <link rel="stylesheet" href="styles.css">
</head>

<body>
  <div class="container">
    <header class="header">
      <h1 id="title" class="text-center">Formulario de encuesta de freeCodeCamp</h1>
      <p id="description" class="description text-center">
        Gracias por tomarte el tiempo para ayudarnos a mejorar la plataforma.
      </p>
    </header>
    <form id="survey-form">
      <div class="form-group">
        <label id="name-label" for="name">Name</label>
        <input type="text" name="name" id="name" class="form-control" placeholder="Enter your name" required="">
      </div>
      <div class="form-group">
        <label id="email-label" for="email">Email</label>
        <input type="email" name="email" id="email" class="form-control" placeholder="Enter your Email" required="">
      </div>
      <div class="form-group">
        <label id="number-label" for="number">Age<span class="clue">(optional)</span></label>
        <input type="number" name="age" id="number" min="10" max="99" class="form-control" placeholder="Age">
      </div>
      <div class="form-group">
        <p>Which option best describes your current role?</p>
        <select id="dropdown" name="role" class="form-control" required="">
          <option disabled="" selected="" value="">Select current role</option>
          <option value="student">Student</option>
          <option value="job">Full Time Job</option>
          <option value="learner">Full Time Learner</option>
          <option value="preferNo">Prefer not to say</option>
          <option value="other">Other</option>
        </select>
      </div>

      <div class="form-group">
        <p>Would you recommend freeCodeCamp to a friend?</p>
        <label>
          <input name="user-recommend" value="definitely" type="radio" class="input-radio" checked="">Definitely</label>
        <label>
          <input name="user-recommend" value="maybe" type="radio" class="input-radio">Maybe</label>

        <label><input name="user-recommend" value="not-sure" type="radio" class="input-radio">Not sure</label>
      </div>

      <div class="form-group">
        <p>What is your favorite feature of freeCodeCamp?</p>
        <select id="most-like" name="mostLike" class="form-control" required="">
          <option disabled="" selected="" value="">Select an option</option>
          <option value="challenges">Challenges</option>
          <option value="projects">Projects</option>
          <option value="community">Community</option>
          <option value="openSource">Open Source</option>
        </select>
      </div>

      <div class="form-group">
        <p>
          What would you like to see improved?
          <span class="clue">(Check all that apply)</span>
        </p>

        <label><input name="prefer" value="front-end-projects" type="checkbox" class="input-checkbox">Front-end
          Projects</label>
        <label>
          <input name="prefer" value="back-end-projects" type="checkbox" class="input-checkbox">Back-end
          Projects</label>
        <label><input name="prefer" value="data-visualization" type="checkbox" class="input-checkbox">Data
          Visualization</label>
        <label><input name="prefer" value="challenges" type="checkbox" class="input-checkbox">Challenges</label>
        <label><input name="prefer" value="open-source-community" type="checkbox" class="input-checkbox">Open Source
          Community</label>
        <label><input name="prefer" value="gitter-help-rooms" type="checkbox" class="input-checkbox">Gitter help
          rooms</label>
        <label><input name="prefer" value="videos" type="checkbox" class="input-checkbox">Videos</label>
        <label><input name="prefer" value="city-meetups" type="checkbox" class="input-checkbox">City Meetups</label>
        <label><input name="prefer" value="wiki" type="checkbox" class="input-checkbox">Wiki</label>
        <label><input name="prefer" value="forum" type="checkbox" class="input-checkbox">Forum</label>
        <label><input name="prefer" value="additional-courses" type="checkbox" class="input-checkbox">Additional
          Courses</label>
      </div>

      <div class="form-group">
        <p>Any comments or suggestions?</p>
        <textarea id="comments" class="input-textarea" name="comment"
          placeholder="Enter your comment here..."></textarea>
      </div>

      <div class="form-group">
        <button type="submit" id="submit" class="submit-button">
          Submit
        </button>
      </div>
    </form>
  </div>
</body>

</html>
```

### EL css

```css
body {
  font-family: 'Roboto', sans-serif;
  background-color: #e9ecef;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 600px;
  margin: 50px auto;
  background: #fff;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.header {
  text-align: center;
  margin-bottom: 30px;
}

.text-center {
  text-align: center;
}

.description {
  font-size: 1.1em;
  color: #6c757d;
}

.form-group {
  margin-bottom: 25px;
}

label {
  display: block;
  margin-bottom: 8px;
  font-weight: 500;
  color: #495057;
}

input[type="text"],
input[type="email"],
input[type="number"],
select,
textarea {
  width: 100%;
  padding: 12px;
  margin-top: 5px;
  border: 1px solid #ced4da;
  border-radius: 5px;
  box-sizing: border-box;
  font-size: 1em;
  color: #495057;
}

input[type="text"]:focus,
input[type="email"]:focus,
input[type="number"]:focus,
select:focus,
textarea:focus {
  border-color: #80bdff;
  outline: none;
  box-shadow: 0 0 5px rgba(0, 123, 255, 0.25);
}

.input-radio,
.input-checkbox {
  margin-right: 10px;
}

textarea {
  height: 120px;
}

.submit-button {
  background-color: #007bff;
  color: white;
  padding: 15px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 1em;
  transition: background-color 0.3s ease;
}

.submit-button:hover {
  background-color: #0056b3;
}

```
