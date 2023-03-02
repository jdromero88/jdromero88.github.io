---
layout: post
title: String en JavaScript. (substring)
date: 2020-11-27 15:35:33.000000000 -05:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- JavaScript
tags:
- Javascript
- String
- substring
meta: {}
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/string-en-javascript-substring/"
excerpt: El método substring() retorna una parte del string entre el inicio y el final
  de los indices pasado, or hasta el final del string.
---
<!-- wp:paragraph -->

El método substring() retorna una parte del string entre el inicio y el final de los indices pasado, or hasta el final del string.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Sintaxis:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`string.substring(indiceInicial, indiceFinal)`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Ejemplo:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
const string = "Hola Mundo"
console.log(string.substring(5,10))
//Resultado esperado "Mundo"
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Como se puede apreciar el método substring() acepta 2 parámetros, indiceInicial e indiceFinal, este ultimo parámetro es opcional. Si no se especifica el segundo parámetro va a retornar hasta el final del string.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Ejemplo:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
const string = "Hola Mundo"
console.log(string.substring(5))
//Resultado esperado "Mundo"
```

<!-- /wp:code -->

<!-- wp:paragraph -->

El indice inicial es inclusivo es decir esta el carácter en esa posición sera incluido en el substring. Mientras que el indice final señala el carácter donde el método comenzara a excluir.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Ejemplo:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
const string = "Hola Mundo"
console.log(string.substring(0,4))
// resultado esperado: Hola
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Referencias:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

[MDN String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substring)

<!-- /wp:paragraph -->

