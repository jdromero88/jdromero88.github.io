---
layout: post
title: Hola Mundo con Python
date: 2020-12-04 17:03:51.000000000 -05:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- python
tags:
- begginers
- hola mundo
- Python
meta: {}
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/hola-mundo-con-python/"
excerpt: Recientemente me contactaron reclutadores para ofrecerme oportunidades laborales
  como Full Stack developer, un requisito es que debes se fluido con Python. Así que
  ahora estoy dando mis primeros pasos con Python.
---
<!-- wp:paragraph -->

Recientemente me contactaron reclutadores para ofrecerme oportunidades laborales como Full Stack developer, un requisito es que debes se fluido con [Python](https://www.python.org/). Así que ahora estoy dando mis primeros pasos con Python.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Si necesitas instalar python podes seguir este [enlace](https://wiki.python.org/moin/BeginnersGuide/Download) esta en ingles.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Segun Wikipedia **[Python](https://es.wikipedia.org/wiki/Python)** es un lenguaje de programación interpretado cuya filosofía hace hincapié en la legibilidad de su código.​ Se trata de un lenguaje de programación multiparadigma, ya que soporta orientación a objetos, programación imperativa y, en menor medida, programación funcional. Es un lenguaje interpretado, dinámico y multiplataforma.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Y bueno la tradición de todo programador es siempre imprimir el famoso " **Hello World!**"

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Asumiendo que tenes instalado python podes abrir el terminal y escribir:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
$ python3
```

<!-- /wp:code -->

<!-- wp:paragraph -->

muestra lo siguiente:

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":353,"sizeSlug":"large"} -->

![python]({{ site.baseurl }}/assets/images/2020/12/python.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

ahora escribo esta linea de código:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`print("Hello World!")`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Y va a imprimir Hello World!

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":354,"sizeSlug":"large"} -->

![python Hello World!]({{ site.baseurl }}/assets/images/2020/12/python-hello-world.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

OK eso es lo mas básico.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Ahora voy a crear un nuevo archivo y lo voy a llamar `hola-mundo.py` dentro de este archivo voy a crear una funcion que se llama **diHolaMundo()** que como el nombre ya lo dice va a imprimir "Hola Mundo!"

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":355,"sizeSlug":"large"} -->

![Hola Mundo desde un archivo de texto]({{ site.baseurl }}/assets/images/2020/12/python-hola-mundo-from-file.png)

<!-- /wp:image -->

<!-- wp:code -->

```
# declaro o defino la función
def diHolaMundo():
    print("Hola Mundo") # imprime Hola Mundo

# Invoca la función 
diHolaMundo()
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Para ejecutar este archivo basta con ir a la terminal y escribir

<!-- /wp:paragraph -->

<!-- wp:code -->

```
python hola-mundo.py
```

<!-- /wp:code -->

<!-- wp:paragraph -->

apretas enter y ya va a imprimir Hola Mundo.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":356,"sizeSlug":"large"} -->

![Python ejecutar desde archivo.]({{ site.baseurl }}/assets/images/2020/12/python-ejecutar-desde-archivo.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

bueno lo siguiente seria cambiar un poco la función para que pueda recibir un argumento, para esto le agrego el parámetro **oración** a la función.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
# declaro o defino la funcion con un parametro
def diHolaMundo(oracion):
    print(oracion) # imprime el parametro

# Invoca la funcion y le pasamos un argumento como string.
diHolaMundo("Hola Mundo estoy aprendiendo Python")
```

<!-- /wp:code -->

<!-- wp:paragraph -->

ejecuto de nuevo el programa en la terminal y nos muestra:

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":358,"sizeSlug":"large"} -->

![función con parametro.]({{ site.baseurl }}/assets/images/2020/12/python-function-con-parametro.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Esto es todo por ahora. Si por ahí tienen algún tutorial o curso que recomiendan me dicen en los comentarios.

<!-- /wp:paragraph -->

