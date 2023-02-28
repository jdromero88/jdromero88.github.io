---
layout: post
title: MySQL Double datatype with Rails Migration.
date: 2020-09-04 15:07:09.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- Developer
- mysql
- rails
tags:
- decimal
- double
- mysql
- rails
meta:
  _thumbnail_id: '283'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/mysql-double-datatype-with-rails-migration/"
excerpt: I was creating a MySQL database using Ruby on Rails. Everything was going
  fine until was the moment to create a table that has the data type double.
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

I was creating a MySQL database using Ruby on Rails. Everything was going fine until was the moment to create a table that has the data type double.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

My version of: `Rails 6.0.3.2` to check your version just type `rails --version`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

To recreate the problem I'm going to create a new rails app with a mysql database. My database is going to have one table. Would looks like this:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
Database Name: mysql_double_datatype_development
Table Name: test
id(int) name(string) quantity(double(6,3)) price(decimal(7,2)) 
1 product1 60.123 111.50
```

<!-- /wp:code -->

<!-- wp:paragraph -->

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

To create a new rails app. Run in your terminal:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`rails new mysql-double-datatype -d mysql`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

cd into your new app folder

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`cd mysql-double-datatype/`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

I'm going to use the rails generator so to create a new resource type:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`rails g resource Test name:string quantity:double price:decimal{7,2}`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

This returned this:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
jodarove@linux-mint:~/development/code/blog/mysql-double-datatype$ rails g resource Test name:string quantity:double price:decimal{7,2}
The dependency tzinfo-data (>= 0) will be unused by any of the platforms Bundler is installing for. Bundler is installing for ruby but the dependency is only for x86-mingw32, x86-mswin32, x64-mingw32, java. To add those platforms to the bundle, run `bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java`.
Running via Spring preloader in process 11761
      invoke active_record
      create db/migrate/20200904174157_create_tests.rb
      create app/models/test.rb
      invoke test_unit
      create test/models/test_test.rb
      create test/fixtures/tests.yml
      invoke controller
      create app/controllers/tests_controller.rb
      invoke erb
      create app/views/tests
      invoke test_unit
      create test/controllers/tests_controller_test.rb
      invoke helper
      create app/helpers/tests_helper.rb
      invoke test_unit
      invoke assets
      invoke scss
      create app/assets/stylesheets/tests.scss
      invoke resource_route
       route resources :tests
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Everything looks fine. The migration created looks like this:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
class CreateTests < ActiveRecord::Migration[6.0]
  def change
    create_table :tests do |t|
      t.string :name
      t.double :quantity
      t.decimal7 :price
      t.decimal2 :price

      t.timestamps
    end
  end
end
```

<!-- /wp:code -->

<!-- wp:paragraph -->

time to create the database. Run `rails db:create`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

you may get this error:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
Access denied for user 'root'@'localhost'
Couldn't create 'mysql_double_datatype_development' database. Please check your configuration.
rails aborted!
```

<!-- /wp:code -->

<!-- wp:paragraph -->

to fix this just open the file **database.yml** this is located in the config **folder**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

is look like this:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
default: &default
  adapter: mysql2
  encoding: utf8mb4
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  username: root
  password:
  socket: /var/run/mysqld/mysqld.sock
```

<!-- /wp:code -->

<!-- wp:paragraph -->

and update username and password with your mysql credentials.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Time to run again `rails db:create`

<!-- /wp:paragraph -->

<!-- wp:code -->

```
jodarove@linux-mint:~/development/code/blog/mysql-double-datatype$ rails db:create
The dependency tzinfo-data (>= 0) will be unused by any of the platforms Bundler is installing for. Bundler is installing for ruby but the dependency is only for x86-mingw32, x86-mswin32, x64-mingw32, java. To add those platforms to the bundle, run `bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java`.
Created database 'mysql_double_datatype_development'
Created database 'mysql_double_datatype_test'
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Now the database is created!

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/k39w535jFPYrK" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/how-i-met-your-mother-thumbs-up-neil-patrick-harris-k39w535jFPYrK)

<!-- /wp:html -->

<!-- wp:paragraph -->

Now is time to run `rails db:migrate`

<!-- /wp:paragraph -->

<!-- wp:code -->

```
jodarove@linux-mint:~/development/code/blog/mysql-double-datatype$ rails db:migrate
The dependency tzinfo-data (>= 0) will be unused by any of the platforms Bundler is installing for. Bundler is installing for ruby but the dependency is only for x86-mingw32, x86-mswin32, x64-mingw32, java. To add those platforms to the bundle, run `bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java`.
== 20200904174157 CreateTests: migrating ======================================
-- create_table(:tests)
rails aborted!
StandardError: An error has occurred, all later migrations canceled:

undefined method `double' for #<ActiveRecord::ConnectionAdapters::MySQL::TableDefinition:0x000055ea3c76d9b0>
/home/jodarove/development/code/blog/mysql-double-datatype/db/migrate/20200904174157_create_tests.rb:5:in `block in change'
```

<!-- /wp:code -->

<!-- wp:paragraph -->

we got an error.

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/54PaD9dWT0go" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/eye-roll-ryan-reynolds-ugh-54PaD9dWT0go)

<!-- /wp:html -->

<!-- wp:paragraph -->

reading the error we now that the problem is the double and is in line 5 in the file `20200904174157_create_tests.rb`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Here is where I start researching how to fix this. I went to the [rails docs](https://guides.rubyonrails.org/v3.2/migrations.html#supported-types) but it wasn't very helpful they don't even mention the double just float. Keep browsing through stackoverflow I came across this [post](https://stackoverflow.com/questions/3099785/what-is-rails-migration-equivalent-to-mysqls-double-datatype/48813142#48813142) and specificaly this answer help me to fix my error. I just added the precision I wanted within the parenthesis.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
t.column :field, "double(6,3)"
```

<!-- /wp:code -->

<!-- wp:paragraph -->

I'm going to update manually the migration

<!-- /wp:paragraph -->

<!-- wp:code -->

```
class CreateTests < ActiveRecord::Migration[6.0]
  def change
    create_table :tests do |t|
      t.string :name
      t.column :quantity, "double(6,3)"
      t.decimal7 :price
      t.decimal2 :price

      t.timestamps
    end
  end
end
```

<!-- /wp:code -->

<!-- wp:paragraph -->

save it and run `rails db:drop && rails db:create && rails db:migrate`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

What happens now? Another error.

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/p8Uw3hzdAE2dO" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/angry-frustrated-annoyed-p8Uw3hzdAE2dO)

<!-- /wp:html -->

<!-- wp:code -->

```
== 20200904174157 CreateTests: migrating ======================================
-- create_table(:tests)
rails aborted!
StandardError: An error has occurred, all later migrations canceled:

undefined method `decimal7' for #<ActiveRecord::ConnectionAdapters::MySQL::TableDefinition:0x000055c78ff82170>
Did you mean? decimal
/home/jodarove/development/code/blog/mysql-double-datatype/db/migrate/20200904174157_create_tests.rb:6:in
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Now is the decimal we know that is on the migration file in line 6. We need to updated to this `t.decimal :price, precision: 7, scale: 2`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

now the migration file looks like this.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
class CreateTests < ActiveRecord::Migration[6.0]
  def change
    create_table :tests do |t|
      t.string :name
      t.column :quantity, "double(6,3)"
      t.decimal :price, precision: 7, scale: 2
      t.timestamps
    end
  end
end
```

<!-- /wp:code -->

<!-- wp:paragraph -->

save it and run ` rails db:drop && rails db:create && rails db:migrate`

<!-- /wp:paragraph -->

<!-- wp:code -->

```
jodarove@linux-mint:~/development/code/blog/mysql-double-datatype$ rails db:drop && rails db:create && rails db:migrate
The dependency tzinfo-data (>= 0) will be unused by any of the platforms Bundler is installing for. Bundler is installing for ruby but the dependency is only for x86-mingw32, x86-mswin32, x64-mingw32, java. To add those platforms to the bundle, run `bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java`.
Dropped database 'mysql_double_datatype_development'
Dropped database 'mysql_double_datatype_test'
The dependency tzinfo-data (>= 0) will be unused by any of the platforms Bundler is installing for. Bundler is installing for ruby but the dependency is only for x86-mingw32, x86-mswin32, x64-mingw32, java. To add those platforms to the bundle, run `bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java`.
Created database 'mysql_double_datatype_development'
Created database 'mysql_double_datatype_test'
The dependency tzinfo-data (>= 0) will be unused by any of the platforms Bundler is installing for. Bundler is installing for ruby but the dependency is only for x86-mingw32, x86-mswin32, x64-mingw32, java. To add those platforms to the bundle, run `bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java`.
== 20200904174157 CreateTests: migrating ======================================
-- create_table(:tests)
   -> 0.0071s
== 20200904174157 CreateTests: migrated (0.0072s) =============================
```

<!-- /wp:code -->

<!-- wp:paragraph -->

wohoo! finally. Now if you take a look at your logs: `log>development.log` you would see that the migration create this SQL statement

<!-- /wp:paragraph -->

<!-- wp:code -->

```
CREATE TABLE `tests` (`id` bigint NOT NULL AUTO_INCREMENT PRIMARY KEY, `name` varchar(255), `quantity` double(6,3), `price` decimal(7,2), `created_at` datetime(6) NOT NULL, `updated_at` datetime(6) NOT NULL)
```

<!-- /wp:code -->

<!-- wp:paragraph -->

That's is for now! Hope you find this useful.

<!-- /wp:paragraph -->

