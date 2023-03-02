---
layout: post
title: Comandos básicos de Git.
date: 2020-09-17 16:03:19.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- Developer
- git
tags:
- command
- Git
- Github
meta:
  _thumbnail_id: '297'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/comandos-basicos-de-git/"
excerpt: En el post anterior hable de como configurar git. Bueno ahora toca hablar  de
  los comandos básicos que todos debemos saber. Los comandos que yo uso todos los
  dias son ```add, commit, push, merge, checkout, status```
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

En el post [anterior](/starting-with-github/) hable de como configurar git. Bueno ahora toca hablar de los comandos básicos que todos debemos saber. Los comandos que yo uso todos los dias son `add, commit, push, merge, checkout, status`

<!-- /wp:paragraph -->

<!-- wp:separator -->

* * *
<!-- /wp:separator -->

<!-- wp:heading -->

## git init

<!-- /wp:heading -->

<!-- wp:paragraph -->

se encarga de inicializar un directorio como un repositorio Git.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Sintaxis:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`git init`

<!-- /wp:paragraph -->

<!-- wp:heading -->

## git clone

<!-- /wp:heading -->

<!-- wp:paragraph -->

como el nombre lo dice clona (realiza una copia) todo el repositorio indicado en la url.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Sintaxis:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git clone <url>
git clone git@github.com:jdromero88/first-app.git
```

<!-- /wp:code -->

<!-- wp:heading -->

## git status

<!-- /wp:heading -->

<!-- wp:paragraph -->

muestra los archivos que fueron modificados en el directorio, listos o no para el proximo commit.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":297,"sizeSlug":"large"} -->

![git status]({{ site.baseurl }}/assets/images/2020/09/git-status-1024x340.png)  

_git status_

<!-- /wp:image -->

<!-- wp:heading -->

## git add

<!-- /wp:heading -->

<!-- wp:paragraph -->

agrega un archivo para el commit.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

sintaxis:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git add nombre-del-archivo
git add prueba.txt
```

<!-- /wp:code -->

<!-- wp:paragraph -->

vamos a suponer que tenes 4 archivos: index.html, contacto.html, servicios.html y nosotros.html

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Y modificaste 3 de ellos: index.html, contacto.html y servicios.html  
para agregar a la etapa de commit tendrias que hacer:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git add index.html
git add contacto.html
git add servicios.html
```

<!-- /wp:code -->

<!-- wp:paragraph -->

podes ahorrarte tiempo escribiendo simplemente

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git add .
```

<!-- /wp:code -->

<!-- wp:paragraph -->

esto pondría todos los archivos modificados en la etapa lista para el commit.

<!-- /wp:paragraph -->

<!-- wp:heading -->

## git commit

<!-- /wp:heading -->

<!-- wp:paragraph -->

confirma el contenido (tus archivos) organizado como una nueva captura (snapshot).

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Sintaxis:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git commit -m 'mensaje'
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Un ejemplo: es poner un mensaje descriptivo:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git commit -m 'Actualize el div en el index'
```

<!-- /wp:code -->

<!-- wp:heading -->

## git push

<!-- /wp:heading -->

<!-- wp:paragraph -->

Transmitir el contenido local confirmado (commit) al repositorio remoto.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Sintaxis:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git push
```

<!-- /wp:code -->

<!-- wp:heading -->

## git branch

<!-- /wp:heading -->

<!-- wp:paragraph -->

Lista todas las ramas (branches) del repositorio. Un \* aparece al lado de la rama activa.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git branch
```

<!-- /wp:code -->

<!-- wp:paragraph -->

para crear una nueva rama basta con poner el nombre de la rama despues de branch

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git branch nueva-rama
```

<!-- /wp:code -->

<!-- wp:heading -->

## git checkout

<!-- /wp:heading -->

<!-- wp:paragraph -->

este comando es el encargado de cambiar de ramas. Si el repositorio tiene 3 ramas: master, nueva-rama, cargar-foto. Y tu rama activa es master para cambiar a la rama cargar-foto tenes que usar el comando:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git checkout cargar-foto
```

<!-- /wp:code -->

<!-- wp:heading -->

## git merge

<!-- /wp:heading -->

<!-- wp:paragraph -->

este comando une o fusiona dos ramas. La rama actual con la rama especificada con el comando.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Sintanxis:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git merge branch
```

<!-- /wp:code -->

<!-- wp:paragraph -->

por ejemplo estas en la rama master y queres hacer merge con la rama cargar-foto

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`git merge cargar-foto`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

OK esto es todo por ahora. Espero que te sirva de ayuda.

<!-- /wp:paragraph -->

