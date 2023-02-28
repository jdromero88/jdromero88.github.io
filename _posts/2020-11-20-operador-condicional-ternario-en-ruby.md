---
layout: post
title: Operador condicional (ternario) en Ruby
date: 2020-11-20 12:57:39.000000000 -05:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- Developer
- ruby
tags:
- condicional
- operador
- ruby
- ternario
meta: {}
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/operador-condicional-ternario-en-ruby/"
excerpt: En el post anterior hable del operador ternario en JavaScript ahora es el
  turno de Ruby. También consta de 3 partes. La primera parte seria la condición y
  el resto los 2 posibles resultados.
---
<!-- wp:paragraph -->

En el post anterior hable del [operador ternario en JavaScript](https://blog.josedromero.com/operador-condicional-ternario-en-javascript/) ahora es el turno de Ruby.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

También consta de 3 partes. La primera parte seria la condición y el resto los 2 posibles resultados.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**Sintaxis** : `condición ? verdadero : falso`

<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->

1. **Condición** : `edad >= 18`
2. **Verdadero** : `"Podes gestionar tu licencia de conducir."`
3. **Falso** : `"Podes gestionar tu licencia de conducir."`

<!-- /wp:list -->

<!-- wp:paragraph -->

Ejemplo usando if...else:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
# definimos edad = 21
edad = 21
if edad >= 18
   puts "Podes gestionar tu licencia de conducir."
else
   puts "Debes cumplir 18 años para obtener la licencia de conducir."
end
```

<!-- /wp:code -->

<!-- wp:paragraph -->

con el operador ternario podemos simplificarlo:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
edad >= 18 ? "Podes gestionar tu licencia de conducir." : "Podes gestionar tu licencia de conducir."
```

<!-- /wp:code -->

<!-- wp:paragraph -->

La idea de usar un operador ternario es el de facilitar la lectura de código. Así que por favor no vengas con ideas descabelladas para complicar algo que nació para ser simple.

<!-- /wp:paragraph -->

