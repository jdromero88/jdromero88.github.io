---
layout: post
title: Functions in JavaScript
date: 2020-07-09 23:58:06.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Developer
- JavaScript
tags:
- arrow function
- function declaration
- function expression
- functions
- Javascript
- regular function
meta:
  _thumbnail_id: '142'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/functions-in-javascript/"
excerpt: 'Hola! In this post I plan on talking a bit about JavaScript functions. That
  way you''ll have some background knowledge for the future when we can dive deep
  into two types specifically: regular functions and arrow functions.'
---
<!-- wp:paragraph -->

Hola! In this post I plan on talking a bit about JavaScript functions. That way you'll have some background knowledge for the future when we can dive deep into two types specifically: regular functions and arrow functions.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions) is a JavaScript procedure—a set of statements that performs a task or calculates a value. To use a function, you must define it somewhere in the scope from which you wish to call it.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

[F_unction expression_](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function): The function keyword can be used to define a function inside an expression. Is very similar to and has almost the same syntax as a function declaration. Example:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
let sum = function(a, b){
    return a + b 
}
sum(5,10) //will return 15
```

<!-- /wp:code -->

<!-- wp:paragraph -->

[_Function declaration_:](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function) A function created with a function declaration is a Function object and has all the properties, methods and behavior of Function objects. Example:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
function sum(a,b){
   return a + b
}
sum(5,10) //will return 15
```

<!-- /wp:code -->

<!-- wp:paragraph -->

You can see both are very similar. With a function expression: you can omit the name(the function is anonymous), and allows you to use it like an _Immediately Invoked Function Expression._

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

_[Arrow function:](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)_ these are always anonymous, they are compact and cannot be used as constructor. Example:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
let sum = (a,b) => a + b
sum(5,10) // will return 15
```

<!-- /wp:code -->

<!-- wp:paragraph -->

When you first start using arrow functions the syntax may look weird but the more you use it and understand how it works the more you will end up liking them and they may become your favorite type of functions!

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Resources:

<!-- /wp:paragraph -->

<!-- wp:list -->

- [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

<!-- /wp:list -->

<!-- wp:paragraph -->

<!-- /wp:paragraph -->

