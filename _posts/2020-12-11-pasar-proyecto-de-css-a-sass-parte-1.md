---
layout: post
title: Pasar proyecto de CSS a SASS (parte 1)
date: 2020-12-11 22:59:14.000000000 -05:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- Developer
- sass
tags:
- css
- html
- sass
- scss
meta:
  _edit_last: '1'
  _wp_old_slug: pasar-proyecto-de-css-a-sass
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/pasar-proyecto-de-css-a-sass-parte-1/"
excerpt: |-
  Bueno como ya sabemos CSS es el maquillaje del HTML.
  En Wikipedia dice que CSS (siglas en inglés de Cascading Style Sheets), en español «Hojas de estilo en cascada», es un lenguaje de diseño gráfico para definir y crear la presentación de un documento estructurado escrito en un lenguaje de marcado.
---
<!-- wp:paragraph -->

Bueno como ya sabemos **CSS** es el maquillaje del **HTML**.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

En [Wikipedia](https://es.wikipedia.org/wiki/Hoja_de_estilos_en_cascada) encontramos que **CSS** (siglas en inglés de Cascading Style Sheets), en español «Hojas de estilo en cascada», es un lenguaje de diseño gráfico para definir y crear la presentación de un documento estructurado escrito en un lenguaje de marcado.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Pero que es **SASS**?

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

[Sass](https://es.wikipedia.org/wiki/Sass) (Syntactically Awesome Stylesheets) es un metalenguaje de Hojas de Estilo en Cascada (CSS). Es un lenguaje de script que es traducido a CSS.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Bueno ahora tenemos una idea básica. Lo que hare sera primero hay que tener SASS instalado para eso voy a asumir que estas corriendo un linux ya sea ubuntu o una distro debian. En este caso Linux Mint 19.3.

<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->

1. Instalar [Homebrew](https://brew.sh/) :

<!-- /wp:list -->

<!-- wp:list -->

- Abris una terminal pegas esto y le das enter

<!-- /wp:list -->

<!-- wp:code -->

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

<!-- /wp:code -->

<!-- wp:list -->

- ahora pegas esto y enter de nuevo

<!-- /wp:list -->

<!-- wp:code -->

```
test -d ~/.linuxbrew && eval $(~/.linuxbrew/bin/brew shellenv)
```

<!-- /wp:code -->

<!-- wp:list -->

- seguimos con esto:

<!-- /wp:list -->

<!-- wp:code -->

```
test -d /home/linuxbrew/.linuxbrew && eval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)
```

<!-- /wp:code -->

<!-- wp:list -->

- ahora:

<!-- /wp:list -->

<!-- wp:code -->

```
test -r ~/.bash_profile && echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.bash_profile
```

<!-- /wp:code -->

<!-- wp:list -->

- por ultimo:

<!-- /wp:list -->

<!-- wp:code -->

```
echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.profile
```

<!-- /wp:code -->

<!-- wp:paragraph -->

bueno cerras y volves abrir el terminal ahora ejecutas:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
sudo apt-get update
```

<!-- /wp:code -->

<!-- wp:paragraph -->

ahora en la terminal ejecutas `brew` y te mostrara algo similar

<!-- /wp:paragraph -->

<!-- wp:code -->

```
jodarove@linux-mint:~$ brew
Example usage:
  brew search [TEXT|/REGEX/]
  brew info [FORMULA...]
  brew install FORMULA...
  brew update
  brew upgrade [FORMULA...]
  brew uninstall FORMULA...
  brew list [FORMULA...]

Troubleshooting:
  brew config
  brew doctor
  brew install --verbose --debug FORMULA

Contributing:
  brew create [URL [--no-fetch]]
  brew edit [FORMULA...]

Further help:
  brew commands
  brew help [COMMAND]
  man brew
  https://docs.brew.sh
```

<!-- /wp:code -->

<!-- wp:paragraph -->

si ves eso genial! estas en la dirección correcta.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

2. Instalar [SASS](https://sass-lang.com/install)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Para eso en una terminal ejecutas

<!-- /wp:paragraph -->

<!-- wp:code -->

```
brew install sass/sass/sass
```

<!-- /wp:code -->

<!-- wp:paragraph -->

y listo ahora para probar si estas en el camino correcto basta con ejecutar `sass` en la terminal y te mostrara algo similar

<!-- /wp:paragraph -->

<!-- wp:code -->

```
jodarove@linux-mint:~$ sass
Compile Sass to CSS.

Usage: sass <input.scss> [output.css]
       sass <input.scss>:<output.css> <input/>:<output/> <dir/>

━━━ Input and Output ━━━━━━━━━━━━━━━━━━━
    --[no-]stdin Read the stylesheet from stdin.
    --[no-]indented Use the indented syntax for input from stdin.
-I, --load-path=<PATH> A path to use when resolving imports.
                               May be passed multiple times.
-s, --style=<NAME> Output style.
                               [expanded (default), compressed]
    --[no-]charset Emit a @charset or BOM for CSS with non-ASCII characters.
                               (defaults to on)
    --[no-]error-css When an error occurs, emit a stylesheet describing it.
                               Defaults to true when compiling to a file.
    --update Only compile out-of-date stylesheets.

━━━ Source Maps ━━━━━━━━━━━━━━━━━━━━━━━━
    --[no-]source-map Whether to generate source maps.
                               (defaults to on)
    --source-map-urls How to link from source maps to source files.
                               [relative (default), absolute]
    --[no-]embed-sources Embed source file contents in source maps.
    --[no-]embed-source-map Embed source map contents in CSS.

━━━ Other ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
    --watch Watch stylesheets and recompile when they change.
    --[no-]poll Manually check for changes rather than using a native watcher.
                               Only valid with --watch.
    --[no-]stop-on-error Don't compile more files once an error is encountered.
-i, --interactive Run an interactive SassScript shell.
-c, --[no-]color Whether to use terminal colors for messages.
    --[no-]unicode Whether to use Unicode characters for messages.
-q, --[no-]quiet Don't print warnings.
    --[no-]trace Print full Dart stack traces for exceptions.
-h, --help Print this usage information.
    --version Print the version of Dart Sass.
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Bueno ya que esto se volvió un poco largo voy a dividir este post en dos. Quédate atento por la segunda parte de este post para saber como convertir el archivo . **css** a . **scss** y ver en primera mano la diferencias y las ventajas de usar **SASS**.

<!-- /wp:paragraph -->

