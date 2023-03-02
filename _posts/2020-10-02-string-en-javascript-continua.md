---
layout: post
title: String en JavaScript.(continúa)
date: 2020-10-02 23:42:09.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- Developer
- JavaScript
tags:
- Javascript
- slice
- String
meta: {}
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/string-en-javascript-continua/"
excerpt: En el post anterior hable del objeto String. Ahora voy a continuar con otros  de
  los objectos incorporados (built-in objects) que trae JavaScript para manipular
  Strings.
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

En el [post anterior](/string-en-javascript/) hable del objeto String. Ahora voy a continuar con otros de los objectos incorporados (built-in objects) que trae JavaScript para manipular Strings.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

El método **slice()** extrae una seccion del string y retorna como un nuevo string sin modificar el string original.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
let stringEjemplo = 'Una noche tibia nos conocimos.'
console.log(stringEjemplo.slice(4))
//resultado esperado: noche tibia nos conocimos
console.log(stringEjemplo.slice(4,9))
//resultado esperado: noche
console.log(stringEjemplo.slice(-9))
//resultado esperado: conocimos
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Los parámetros que acepta el método **slice()** son:

<!-- /wp:paragraph -->

<!-- wp:list -->

- **Posición inicial:** indica el inicio de la extracción. Debe ser un número entero ya sea positivo o negativo. Si recibe un numero igual o mayor a la longitud del string, este retornara un string vacío. Si recibe un numero negativo lo que JS realiza el stringEjemplo.length - 9.
- **Posición final:** indica el final de la extracción. Debe de ser un número entero positivo o negativo. Si este parámetro es omitido, es indefinido o es mayor a la longitud del string el método slice() extraera hasta el final del string. Si la posición inicial es negativa la posición final tambien debe de ser negativa en caso contrario devolvera un string vacío.

<!-- /wp:list -->

<!-- wp:paragraph -->

<!-- /wp:paragraph -->

