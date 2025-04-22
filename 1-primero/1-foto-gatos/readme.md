# Aprenda HTML constuyendo una aplicacion de fotos de gatos

- Las etiquetas HTML dan la pagina su estructura. Puedes usar etiquetas HTML para anadir fotos, botones, y otros elementos en tu pagina.
- En este curso, aprenderás las etiquetas HTML más comunes por medio de la construcción de tu propia aplicación para fotos de gatos.

## Paso 1

Todas las páginas deben comenzar con `<!DOCTYPE html>`. Esta cadena especial es conocida como una declaración y se asegura de que el navegador intente cumplir las especificaciones de la industria.

`<!DOCTYPE html>` le dice a los navegadores que el documento es un documento HTML5 la cual es la última versión de HTML.

```html
<!DOCTYPE html>
```

## Paso 2

Puedes ver que todo el contenido de la página está anidado dentro de un elemento `html`. El elemento `html` es elemento esencial de una página HTML y envuelve todo el contenido en la página.

Tu también puedes especificar el lenguaje de tu página agregando el atributo `lang` a el elemento `html`.

```html
<html lang="en">
  </html>
```

## Paso 3

Sin embargo, otro tipo información que también es importante va dentro del elemento `head`.

El elemento `head` se utiliza para contener metadatos sobre el documento, como su título, enlaces a hojas de estilo y scripts. Los metadatos son información sobre la página que no se muestra directamente en la página.

```html
<head>
</head>
```

## Paso 4

Dentro del elemento `head`, anida un elemento `meta` con un atributo `charset`. Con el valor `utf-8` que le dirá al navegador cómo codificar los caracteres en la página.
Ten en cuenta que el elemento `meta` es un elemento vacío. `<meta attribute="value">`

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

## Paso 5

El elemento `title` (título) determina lo que los navegadores muestran en la barra de título o en las pestañas del navegador.

```html
  <title>APP foto de gatos</title>
```

## Paso 6

En el paso anterior, has colocado los elementos `h1`, `h2`, `comentario` y `p` dentro del elemento `main`. This is called nesting. Los elementos anidados deben colocarse dos espacios más a la derecha del elemento en el que están anidados. `Este espacio se llama sangría (indentación en programación)` y se utiliza para facilitar la lectura de HTML.

```css
```
