---
layout: post
title: 'String: Manipulando ando! (bueno intentando xD)'
date: 2020-10-06 03:39:53.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Algoritmos
- Developer
- JavaScript
tags:
- algoritmos
- cadena caracteres
- Javascript
- String
meta: {}
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/string-manipulando-ando-bueno-intentando-xd/"
excerpt: |-
  Recientemente tuve una entrevista de trabajo y me dieron el siguiente algoritmo para resolver:
  Escribe un programa que convierta en mayúscula la primera letra de cada palabra en una oración.
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

Recientemente tuve una entrevista de trabajo y me dieron el siguiente algoritmo para resolver:

<!-- /wp:paragraph -->

<!-- wp:list -->

- **Escribe un programa que convierta en mayúscula la primera letra de cada palabra en una oración. Ejemplo si la oracion es 'hola mundo' el programa debe mostrar en la consola 'Hola Mundo'.** 

<!-- /wp:list -->

<!-- wp:paragraph -->

por cierto tenia 35 minutos para resolver este algoritmo.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

La primera solucion que plantee fue a la fuerza bruta.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

El primer paso fue convertir el string en un array utilizando el metodo split(). Este metodo divide el string en una lista de substrings, agregandolo a un array y devuelve ese array. La division se realiza buscando un patron, donde el patron es pasado como primer parametro al llamar al metodo.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
let oracion = 'la llama que llama'
let palabras = oracion.split(' ')
console.log(palabras)
//resultado esperado: ["la", "llama", "que", "llama"]
console.log(palabras[2])
//resultado esperado: "que"
```

<!-- /wp:code -->

<!-- wp:paragraph -->

el segundo parametro es opcionme dieron 35 minutos para resolver esto.al. Debe de ser un numero positivo que indica la cantidad de substrings a ser incluido en el array.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Continuando con el ejemplo de arriba:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
let tresPrimerasPalabras = oracion.split(' ', 3)
console.log(tresPrimerasPalabras)
//resultadoEsperado: ["la", "llama", "que"]
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Bueno continuando con la solucion del algoritmo hice lo siguiente:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
function mayusculizar(oracion){
   let palabras = oracion.split(' ')
   console.log(palabras[0].charAt(0).toUpperCase() + palabras[0].slice(1))
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Si invoco a la funcion y le paso un string de una sola palabra supongamos 'hello':

<!-- /wp:paragraph -->

<!-- wp:code -->

```
mayusculizar('hello')
//resultado esperado: "Hello"
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Si invocas de nuevo a la funcion pero le pasas un string con mas de una palabra supongamos 'hello world' todavia va a imprimir en la consola 'Hello'

<!-- /wp:paragraph -->

<!-- wp:code -->

```
mayusculizar('hello world')
//resultado esperado: "Hello"
```

<!-- /wp:code -->

<!-- wp:paragraph -->

esto pasa porque estoy resolviendo a la fuerza bruta. Si nos fijamos en el codigo solo estoy tomando el primer elemento en el array que devuelve el metodo split(). `palabras[0]`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Aqui utilize varios metodos incluidos que ya trae el objeto string:

<!-- /wp:paragraph -->

<!-- wp:list -->

- El metodo **charAt()** retorna un nuevo string que consiste en un caracter UTF-16 localizado en la posicion indicada.

<!-- /wp:list -->

<!-- wp:code -->

```
let oracion = 'Estoy aprendiendo'
console.log(oracion.charAt(3))
// resultado esperado: "o"
```

<!-- /wp:code -->

<!-- wp:list -->

- El metodo **toUpperCase()** retorna el string sobre el cual es llamado convertido a mayusculas.

<!-- /wp:list -->

<!-- wp:code -->

```
let oracion = 'Estoy aprendiendo'
console.log(oracion.charAt(3).toUpperCase())
// resultado esperado: "O"
console.log(oracion.toUpperCase())
// resultado esperado: "ESTOY APRENDIENDO"
```

<!-- /wp:code -->

<!-- wp:list -->

- y el método [slice()](/string-en-javascript-continua/) del cual ya aprendimos en el [post anterior](/string-en-javascript-continua/).

<!-- /wp:list -->

<!-- wp:paragraph -->

Continuando con la solución del algoritmo. Ahora hay que buscar una forma de recorrer el array y convertir cada primera letra de las palabras en mayusculas.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Bueno la primera idea que me vino fue crear una funcion de ayuda que sea recursiva y adentro de ella utilizar el metodo [shift()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift) para agarrar la primera palabra del array y poder mutarlo. Despues de varios intentos y no poder lograr el resultado esperado al mirar los minutos que me quedaban creo que eran como unos 10 entre en panico y dije mejor buscar otra solución. Pero igual esto fue lo que intente realizar con la funcion recursiva:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
function aMayusculas(oracion) {
  let palabras = oracion.split(' ')
  funcionAyuda(palabras)
}

function funcionAyuda(palabras) {
  let palabraEnMayuscula
  let nuevoArray = []
  
  // condicion de salida
  if(palabras.length == 0) return nuevoArray

  let palabra = palabras.shift()
  palabraEnMayuscula = palabra.charAt(0).toUpperCase() + palabra.slice(1)
  console.log(palabraEnMayuscula);
  nuevoArray.push(palabraEnMayuscula)
  return funcionAyuda(palabras)
}

console.log(aMayusculas('hola mundo'));
// resultado:
// Hola
// Mundo
// undefined
```

<!-- /wp:code -->

<!-- wp:paragraph -->

La siguiente propuesta que tuve fue y donde se me prendio la lamparita... mi momento AHAaaaaAAAAaaaAaa...

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/xT1R9IKI80368giYne" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/broadcity-season-1-episode-7-xT1R9IKI80368giYne)

<!-- /wp:html -->

<!-- wp:paragraph -->

bueno fue crear una funcion ayuda que tome un argumento string y que retorne el mismo string con el primer caracter convertido a mayusculas. Y en la funcion principal usar un map para poder mutar el array que nos devuelve el metodo split(). Bueno dentro del map en la funcion callback le pasamos nuetstra funcionAyuda() con la palabra en dicha posicion como argumento. Bueno en el codigo mas arriba ya tenemos parte de esto. Vamos a refactorizar un poco.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Codigo que ya tenemos:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
function mayusculizar(oracion){
   let palabras = oracion.split(' ')
   console.log(palabras[0].charAt(0).toUpperCase() + palabras[0].slice(1))
}
mayusculizar('hello world')
//resultado esperado: "Hello"
```

<!-- /wp:code -->

<!-- wp:paragraph -->

bueno vamos a crear la funcionAyuda() que recibe un argumento de tipo string y es la que va a convertir la primera letra de cada palabra a mayuscula y retornar esa palabra.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
function funcionAyuda(palabra){
   let enMayuscula = palabra.charAt(0).toUpperCase() + palabra.slice(1)
   return enMayuscula
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Ahora si probas esta funcion pasandole una palabra por ejemplo 'hola' va a imprimir 'Hola'

<!-- /wp:paragraph -->

<!-- wp:code -->

```
funcionAyuda('hola')
//resultado esperado: "Hola"
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Bueno ahora hay que refactorizar la funcion mayusculizar.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Aqui luego de hacer el **split(' ' )** vamos a usar el metodo [map()](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/map) que va a crear un nuevo array con el resultado de la funcion que le pasamos, en este caso funcionAyuda() .

<!-- /wp:paragraph -->

<!-- wp:code -->

```
function mayusculizar(oracion){
   let palabras = oracion.split(' ')
   let oracionConvertida = palabras.map( palabra => funcionAyuda(palabra)).join(' ')
   return oracionConvertida
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

El metodo **map()** siempre va a retornar un array con la misma cantidad de elementos. Ejemplo:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
const numeros = [1,2,3,4]
let alCuadrado = numeros.map(function(numero){
   return numero ** 2
})
```

<!-- /wp:code -->

<!-- wp:paragraph -->

en este caso numeros es un array que contiene 4 elementos y despues de ejecutar alCuadrado tambien sera un array que contiene cuatro elementos. Son el resultado de elevar al cuadrado cada numero del array numeros.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
alCuadrado
// resultado esperado: [1, 4, 9, 16]
```

<!-- /wp:code -->

<!-- wp:paragraph -->

bueno el metodo **map()** cuando comenzas a usarlo parece muy confuso pero mientras mas lo utilizas se va volviendo mas facil y tu amor por el arrow function se va a incrementar. ++ (mas adelante hago un post dedicado al metodo **map()** )

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

bueno ya ya volviendo al codigo del algoritmo ahora ya tenemos un codigo final y listo para probarlo este es:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
function funcionAyuda(palabra){
   let enMayuscula = palabra.charAt(0).toUpperCase() + palabra.slice(1)
   return enMayuscula
}

function mayusculizar(oracion){
   let palabras = oracion.split(' ')
   let oracionConvertida = palabras.map( palabra => funcionAyuda(palabra)).join(' ')
   return oracionConvertida
}

mayusculizar('hola ya estoy aqui')
// resultado esperado: "Hola Ya Estoy Aqui"
```

<!-- /wp:code -->

<!-- wp:paragraph -->

esto podemos acortarlo inclusive un poquito mas:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
function funcionAyuda(palabra){
   return palabra.charAt(0).toUpperCase() + palabra.slice(1)
}

function mayusculizar(oracion){
   let palabras = oracion.split(' ')
   return palabras.map( palabra => funcionAyuda(palabra)).join(' ')
}

mayusculizar('hola ya estoy aqui')
// resultado esperado: "Hola Ya Estoy Aqui"
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Bueno eso es todo por ahora. Hasta la proxima.

<!-- /wp:paragraph -->

