---
layout: post
title: Pasar proyecto de CSS a SASS (parte 2)
date: 2020-12-18 23:18:54.000000000 -05:00
categories:
- Beginner
- sass
tags:
- css
- html
- sass
- scss
permalink: "/pasar-proyecto-de-css-a-sass-parte-2/"
excerpt: Continuando con el post anterior. Ahora hay que convertir el archivo css
  a scss. Una foto para ver como esta la estructura de mi proyecto.
---
<!-- wp:paragraph -->

Continuando con el [post anterior](/pasar-proyecto-de-css-a-sass-parte-1/). Ahora hay que convertir el archivo **css** a **scss**. Una foto para ver como esta la estructura de mi proyecto.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":368,"sizeSlug":"large","linkDestination":"none"} -->

![]({{ site.baseurl }}/assets/images/2020/12/proyecto-estructura.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

ahora mismo el mi index.html se ve así

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="./css/style.css">
    <title>CSS a SASS</title>
  </head>
  <body>
    <h1>hola mundo</h1>
    <h2>Este es solo un ejemplo de un sitio web</h2>
    <ul>
      <li>uno</li>
      <li>dos</li>
      <li>tres</li>
    </ul>
  </body>
</html>
```

<!-- /wp:code -->

<!-- wp:paragraph -->

aquí se nota que esta utilizando la hoja de estilo de este directorio `./css/style.css` y tiene esto adentro:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
h1 {
  color:#317ccf;
}

h2 {
  color:#db691d
}

li {
  color: #8c74d1
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

bueno sass te ofrece 2 tipos de sintaxis **.sass** y **.scss** para este ejemplo utilizo **.scss**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

[Sintaxis](https://sass-lang.com/guide) **.sass**

<!-- /wp:paragraph -->

<!-- wp:code -->

```
body
  font: 100% $font-stack
  color: $primary-color
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Sintaxis **.scss**

<!-- /wp:paragraph -->

<!-- wp:code -->

```
body {
  font: 100% $font-stack;
  color: $primary-color;
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

como se observa la sintaxis **.css** y la **.scss** con iguales. Bueno ahora hay que que compilar la hoja de estilo `./css/style.css` a **.scss** para lograr esto:

<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->

1. creas un archivo nuevo en mi caso lo llame **main.css** y lo deje en la carpeta principal.
2. actualizamos la extension de este archivo `./css/style.css` a **.scss** quedaría así: `./css/style.scss`

<!-- /wp:list -->

<!-- wp:image {"id":375,"sizeSlug":"large","linkDestination":"none"} -->

![antes de compilar .scss]({{ site.baseurl }}/assets/images/2020/12/antes-de-compilar-scss-1.png)  

_antes de compilar .scss_

<!-- /wp:image -->

<!-- wp:paragraph -->

3. ahora debemos compilar el archivo **style.scss** para eso se ejecuta en la terminal: `sass css/style.scss main.css`

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":376,"sizeSlug":"large","linkDestination":"none"} -->

![sass --watch css/style.scss main.css]({{ site.baseurl }}/assets/images/2020/12/despues-de-compilar-scss-1024x550.png)  

_sass css/style.scss main.css_

<!-- /wp:image -->

<!-- wp:paragraph -->

y listo ya esta el archivo **main.css** con el css adentro. Ahora queda por actualizar el archivo **index.html** para que este apuntando al **main.css** y queda así:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="main.css">
    <title>CSS a SASS</title>
  </head>
  <body>
    <h1>hola mundo</h1>
    <h2>Este es solo un ejemplo de un sitio web</h2>
    <ul>
      <li>uno</li>
      <li>dos</li>
      <li>tres</li>
    </ul>
  </body>
</html>
```

<!-- /wp:code -->

<!-- wp:paragraph -->

ok ahora cada vez que haces haces un cambio en el archivo **style.scss** tenes que ejecutar el comando sass para que compile a css esto es medio tedioso así que sass tiene una opción para que este mirando cualquier cambio que se haga en el archivo esta opcion es `--watch`. Queda ejecutar así: `sass --watch css/style.scss main.css` ahora cada vez que realizas un cambio y lo guardas va a compilar automaticamente.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":381,"sizeSlug":"full","linkDestination":"none"} -->

![sass --watch css/style.scss main.css]({{ site.baseurl }}/assets/images/2020/12/opcion-watch.gif)  

_sass --watch css/style.scss main.css_

<!-- /wp:image -->

<!-- wp:paragraph -->

Y bueno otra vez esto se alargo, así que una tercera parte vendrá mas adelante para comentar sobre los beneficios de usar SASS.

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/f9jwBVzohvX7LSRqWU" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/BritanniaOnEpix-britannia-britanniaonepix-britanniaepix-f9jwBVzohvX7LSRqWU)

<!-- /wp:html -->

