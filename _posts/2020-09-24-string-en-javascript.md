---
layout: post
title: String en JavaScript.
date: 2020-09-24 22:59:55.000000000 -04:00
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
- String
- tolowercase
- touppercase
meta: {}
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/string-en-javascript/"
excerpt: |-
  Hoy voy a hablar un poco de los objectos incorporados (built-in objects)que trae JavaScript para manipular Strings.

  El objeto String es usado para representar y manipular una secuencia de caracteres.
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

Hoy voy a hablar un poco de los objectos incorporados (built-in objects)que trae JavaScript para manipular Strings.

<!-- /wp:paragraph -->

<!-- wp:quote -->

> El objeto String es usado para representar y manipular una secuencia de caracteres.
> 
> <cite><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String" target="_blank" rel="noreferrer noopener">https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String</a></cite>

<!-- /wp:quote -->

<!-- wp:quote -->

> Strings (Cadenas de caracteres) son útiles para almacenar datos que se pueden representar en forma de texto. Una de las operaciones mas usadas con Strings son para chequear su longitud.
> 
> <cite><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String" target="_blank" rel="noreferrer noopener">https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String</a></cite>

<!-- /wp:quote -->

<!-- wp:paragraph -->

Podemos crear un String de la siguiente manera:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`let string = "Soy una string"`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`let stringDos = 'Soy string dos'`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`let stringTres = `Soy string tres``

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`let stringCuatro = new String("Soy string cuatro")`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Uno de los metodos que yo utilizo casi todos los dias es **toLowerCase()**, **toUpperCase()**, y **slice()**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

El metodo **toLowerCase()** retorna el mismo string convertido a minusculas.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
let oracion = 'La llama que llama.'
console.log(oracion.toLowerCase())
// resultado esperado: "la llama que llama."
```

<!-- /wp:code -->

<!-- wp:paragraph -->

El metodo **toUpperCase()** retorna el mismo string convertido a mayusculas.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
let oracion = 'La llama que llama.'
console.log(oracion.toLowerCase())
// resultado esperado: "LA LLAMA QUE LLAMA."
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Bueno eso es todo por ahora en el siguiente post voy a hablar de metodo **slice()** y otros metodos mas.

<!-- /wp:paragraph -->

<!-- wp:separator -->

* * *
<!-- /wp:separator -->

<!-- wp:paragraph -->

Recursos:

<!-- /wp:paragraph -->

<!-- wp:list -->

- [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
- [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String/toLowerCase](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase)
- [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String/toUpperCase](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase)

<!-- /wp:list -->

