---
layout: post
title: Operador condicional (ternario) en JavaScript
date: 2020-11-12 17:03:45.000000000 -05:00
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
- js
- operador ternario
- ternary operator
meta: {}
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/operador-condicional-ternario-en-javascript/"
excerpt: 'Es el único operador que toma 3 operandos: Una condición seguido de un signo
  de interrogación "?", luego una expresión que se ejecutará si la condición es verdadera(truthy)
  y le sigue los dos puntos ":" y finalmente la expresión que se ejecutará si la condición
  es falsa(falsy).'
---
<!-- wp:paragraph -->

Es el único operador que toma 3 operandos: Una condición seguido de un signo de interrogación "?", luego una expresión que se ejecutará si la condición es verdadera(truthy) y le sigue los dos puntos ":" y finalmente la expresión que se ejecutará si la condición es falsa(falsy).

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Este operador se usa frecuentemente para acortar la instrucción if. Aparte de que facilita la lectura de código.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**Sintaxis** :

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`condicion ? expresionSiEsVerdadera : expresionSiEsFalsa`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**Ejemplos** :

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Usando if { } else { }

<!-- /wp:paragraph -->

<!-- wp:code -->

```
let billetera = 500;
let trabajar = 15;
let nuevaLaptop = 700;

function comprarRegalo(){
   if (billetera > nuevaLaptop){
      return comprarLaptop()
   } else {
      return hayQueTrabajar()
   }
}

function comprarLaptop(){
      billetera = billetera - nuevaLaptop
      return `Tenes una nueva laptop! Hurra! Dinero en tu billetera: ${billetera}`
}

function hayQueTrabajar(){
   billetera = billetera + trabajar
   return `Tu billetera: ${billetera}`
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Usando el operador ternario:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
let billetera = 500;
let trabajar = 15;
let nuevaLaptop = 700;

function comprarRegalo(){
   return (billetera > nuevaLaptop) ? comprarLaptop() : hayQueTrabajar()
}

function comprarLaptop(){
      billetera = billetera - nuevaLaptop
      return `Tenes una nueva laptop! Hurra! Dinero en tu billetera: ${billetera}`
}

function hayQueTrabajar(){
   billetera = billetera + trabajar
   return `Tu billetera: ${billetera}`
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

usando el operador ternario nos ahorra unas líneas de código y también facilita la lectura.

<!-- /wp:paragraph -->

