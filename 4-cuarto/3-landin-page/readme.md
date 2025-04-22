# Landing Page del producto

Este es uno de los proyectos necesarios para obtener su crtificacion.

Para este proyecto, ustede construira una pagina de inicio de producto para comercalizar un producto de su eleccion

- **Objetivo**: construye una aplicación que sea funcionalmente similar a `https://product-landing-page.freecodecamp.rocks`. **No copies este proyecto de demostración**

## Instrucciones

- 1 Tu página de inicio de producto debe tener un `elemento header` con un correspondiente `id="header"`

- 2 Puedes ver una imagen dentro del elemento `header` con el correspondiente `id="header-img"` (Un logotipo sería una buena imagen aquí)

- 3 Dentro del elemento `#header` puedes ver un elemento `nav` con el correspondiente `id="nav-bar"`

- 4 Puedes ver al menos tres elementos que se puede hacer clic dentro del elemento nav, cada uno con la clase `nav-link`

- 5 Cuando haces clic en un botón `.nav-link` en el elemento `nav` se te llevará a la sección correspondiente de la página de inicio

- 6 Puedes ver un vídeo del producto incrustado con `id="video"`

- 7 Tu página de inicio tiene un elemento `form` con un `id="form"` correspondiente

- 8 Dentro del formulario, hay un campo `input` con `id="email"`, donde puedes ingresar tu correo electrónico

- 9 El campo de entrada `#email` debe tener un marcador de texto para que los usuarios sepan para qué sirve este campo

- 10 El campo de entrada `#email` usa validación HTML5 para confirmar que el texto ingresado sea una dirección de email

- 11 Dentro del formulario, hay un `input` de tipo submit (enviar) con su correspondiente `id="submit"`

- 12 Cuando haces clic en el elemento `#submit`, el email es enviado a una página web (Utiliza esta URL de pruebas: `https://www.freecodecamp.com/email-submit`)

- 13 La barra de navegación siempre debe estar en la parte superior del viewport

- 14 Tu página de inicio de tu producto debe tener al menos una consulta de medios

- 15 Tu página de inicio de producto debe utillizar el flexbox CSS al menos una vez

Completa las intrucciones y pasa los tests de abajo para completar este projecto. Dale tu estilo personal. ¡Que tengas una feliz programación!

>[!NOTE]
>
>Asegúrese de adicionar `link rel="stylesheet" href="styles.css"` en su HTML para enlazar su hoja de estilos y aplicarla a su CSS

## SOLUCION

### EL html

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Producto</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header id="header">
        <img id="header-img" src="logo.png" alt="Logotipo">
        <nav id="nav-bar">
            <a href="#section1" class="nav-link">Sección 1</a>
            <a href="#section2" class="nav-link">Sección 2</a>
            <a href="#section3" class="nav-link">Sección 3</a>
        </nav>
    </header>

    <section id="section1">
        <h2>Sección 1</h2>
        <p>Contenido de la sección 1.</p>
    </section>

    <section id="section2">
        <h2>Sección 2</h2>
        <p>Contenido de la sección 2.</p>
        <video id="video" controls>
            <source src="producto-video.mp4" type="video/mp4">
            Tu navegador no soporta el elemento de video.
        </video>
    </section>

    <section id="section3">
        <h2>Sección 3</h2>
        <p>Contenido de la sección 3.</p>
    </section>

    <form id="form" action="https://www.freecodecamp.com/email-submit" method="POST">
        <label for="email">Correo electrónico:</label>
        <input id="email" type="email" name="email" placeholder="Ingrese su correo electrónico" required>
        <input id="submit" type="submit" value="Enviar">
    </form>

    <footer>
        <p>&copy; 2025 Producto</p>
    </footer>
</body>
</html>
```

### CSS

```css
/* Estilos generales */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #333;
    color: white;
    padding: 20px;
    position: sticky;
    top: 0;
    z-index: 1000;
}

#header-img {
    max-height: 50px;
}

#nav-bar {
    display: flex;
}

.nav-link {
    color: white;
    text-decoration: none;
    margin: 0 15px;
}

.nav-link:hover {
    text-decoration: underline;
}

section {
    padding: 50px 20px;
}

form {
    margin-top: 20px;
}

#email {
    padding: 10px;
    margin-right: 10px;
}

#submit {
    padding: 10px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
}

#submit:hover {
    background-color: #45a049;
}

/* Consultas de medios */
@media (max-width: 768px) {
    header {
        flex-direction: column;
        align-items: flex-start;
    }

    #nav-bar {
        flex-direction: column;
    }

    .nav-link {
        margin: 10px 0;
    }
}

@media (max-width: 480px) {
    #header-img {
        max-height: 40px;
    }

    #email, #submit {
        width: 100%;
        margin-bottom: 10px;
    }
}

```
