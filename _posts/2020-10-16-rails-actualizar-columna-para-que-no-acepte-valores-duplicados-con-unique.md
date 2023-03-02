---
layout: post
title: 'Rails: actualizar columna para que NO acepte valores duplicados con UNIQUE.'
date: 2020-10-16 22:29:21.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- rails
tags:
- migrations
- rails
meta: {}
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/rails-actualizar-columna-para-que-no-acepte-valores-duplicados-con-unique/"
excerpt: 'Recientemente se me presento el siguiente problema: Tengo una tabla personas
  con los campos: nombres, apellidos, email, fecha_nacimiento. Cuando cree la migracion
  se me olvido de hacer que el email sea unico (unique) que no se permita crear dos
  registros con el mismo email.'
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

Recientemente se me presento el siguiente problema: Tengo una tabla personas con los campos: nombres, apellidos, email, fecha\_nacimiento. Cuando cree la migracion se me olvido de hacer que el email sea unico (unique) que no se permita crear dos registros con el mismo email.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Estoy usando Rails 6.0.3.2 y la forma de arreglar esto fue crear una migracion nueva: `rails g migration AddUniquenessConstraintToPersonas`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

esto me creo el siguiente archivo:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
class AddUniquenessConstraintToPersonas < ActiveRecord::Migration[6.0]
  def change
  end
end
```

<!-- /wp:code -->

<!-- wp:paragraph -->

a lo cual tengo que agregarle: `add_index :personas, :email, unique: true`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

la sintaxis es:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`add_index :nombre_tabla, :nombre_columna, unique: true`.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Bueno nuestra nueva migracion quedaria asi:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
class AddUniquenessConstraintToPersonas < ActiveRecord::Migration[6.0]
  def change
     add_index :personas, :email, unique: true
  end
end
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Ahora solo queda por ejecutar: `rails db:migrate` para actualizar nuestro schema.rb

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Despues de ejecutar podes verificar tu schema.rb y deberia estar actualizado con esta linea.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`t.index ["email"], name: "index_personas_on_email", unique: true`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Y bueno eso es todo. Espero que te sirva y que ya no tengas datos duplicados en tu tabla. Saludos.

<!-- /wp:paragraph -->

