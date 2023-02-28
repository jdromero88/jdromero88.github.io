---
layout: post
title: Connect Ruby to mysql database.
date: 2020-08-28 21:22:16.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Developer
- mysql
- ruby
- Tutorial
tags:
- Linux
- mysql
- ruby
meta:
  _thumbnail_id: '249'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/connect-ruby-to-mysql-database/"
excerpt: Today I'm going to show how to connect Ruby with your Mysql Database.
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

Today I'm going to show how to connect your Ruby with your Mysql Database.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

I'm running Linux mint 19.3 Tricia x64.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":246,"sizeSlug":"large"} -->

![Linux Mint version]({{ site.baseurl }}/assets/images/2020/08/mint-version.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

This is my ruby version:

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":248,"width":580,"height":91,"sizeSlug":"large"} -->

![ruby version]({{ site.baseurl }}/assets/images/2020/08/ruby-version.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

When I tried to install the mysql gem was throwing me this error:

<!-- /wp:paragraph -->

<!-- wp:image {"id":249,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/08/gem-install-mysql-error-1024x269.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

after trying different solutions from stack overflow neither of them were working for me \</3 ='(.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Here is the full error:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
jodarove@linux-mint:~$ gem install mysql
Building native extensions. This could take a while...
ERROR: Error installing mysql:
	ERROR: Failed to build gem native extension.

    current directory: /home/jodarove/.rvm/gems/ruby-2.6.1/gems/mysql-2.9.1/ext/mysql_api
/home/jodarove/.rvm/rubies/ruby-2.6.1/bin/ruby -I /home/jodarove/.rvm/rubies/ruby-2.6.1/lib/ruby/site_ruby/2.6.0 -r ./siteconf20200828-14870-1qfbjzk.rb extconf.rb
checking for mysql_query() in -lmysqlclient... no
checking for -lm... yes
checking for mysql_query() in -lmysqlclient... no
checking for -lz... yes
checking for mysql_query() in -lmysqlclient... no
checking for -lsocket... no
checking for mysql_query() in -lmysqlclient... no
checking for -lnsl... yes
checking for mysql_query() in -lmysqlclient... no
checking for -lmygcc... no
checking for mysql_query() in -lmysqlclient... no
***extconf.rb failed***
Could not create Makefile due to some reason, probably lack of necessary
libraries and/or headers. Check the mkmf.log file for more details. You may
need configuration options.

Provided configuration options:
	--with-opt-dir
	--without-opt-dir
	--with-opt-include
	--without-opt-include=${opt-dir}/include
	--with-opt-lib
	--without-opt-lib=${opt-dir}/lib
	--with-make-prog
	--without-make-prog
	--srcdir=.
	--curdir
	--ruby=/home/jodarove/.rvm/rubies/ruby-2.6.1/bin/$(RUBY_BASE_NAME)
	--with-mysql-config
	--without-mysql-config
	--with-mysql-dir
	--without-mysql-dir
	--with-mysql-include
	--without-mysql-include=${mysql-dir}/include
	--with-mysql-lib
	--without-mysql-lib=${mysql-dir}/lib
	--with-mysqlclientlib
	--without-mysqlclientlib
	--with-mlib
	--without-mlib
	--with-mysqlclientlib
	--without-mysqlclientlib
	--with-zlib
	--without-zlib
	--with-mysqlclientlib
	--without-mysqlclientlib
	--with-socketlib
	--without-socketlib
	--with-mysqlclientlib
	--without-mysqlclientlib
	--with-nsllib
	--without-nsllib
	--with-mysqlclientlib
	--without-mysqlclientlib
	--with-mygcclib
	--without-mygcclib
	--with-mysqlclientlib
	--without-mysqlclientlib

To see why this extension failed to compile, please check the mkmf.log which can be found here:

  /home/jodarove/.rvm/gems/ruby-2.6.1/extensions/x86_64-linux/2.6.0/mysql-2.9.1/mkmf.log

extconf failed, exit code 1

Gem files will remain installed in /home/jodarove/.rvm/gems/ruby-2.6.1/gems/mysql-2.9.1 for inspection.
Results logged to /home/jodarove/.rvm/gems/ruby-2.6.1/extensions/x86_64-linux/2.6.0/mysql-2.9.1/gem_make.out
```

<!-- /wp:code -->

<!-- wp:paragraph -->

I also tried to install mysql2 gem but I still was getting an error. Anyways after more google-ing I finally found this [answer](https://stackoverflow.com/a/9759324) in Stack overflow. To be honest I wasn't sure that it was going to work because it was useful only 2 times but I tried anyways.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
sudo gem install ruby-mysql
```

<!-- /wp:code -->

<!-- wp:paragraph -->

But this actually went through the installation and I started to smile =)

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/3osxYy31LMEZJEn864" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/new-girl-fox-new-girl-newgirl-3osxYy31LMEZJEn864)

<!-- /wp:html -->

<!-- wp:paragraph -->

Now I just need it to test it to see if was actually is going to work.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Time to create a database! You can do it by running these commands:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
mysql -u yourUsername -p 
//is going to ask for your password
CREATE DATABASE connectRuby;
USE connectRuby;
CREATE TABLE user(id smallint unsigned not null auto_increment, name varchar(20) not null, constraint pk_example primary key (id) );
```

<!-- /wp:code -->

<!-- wp:paragraph -->

it is going to look like this:

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":252,"width":580,"height":309,"sizeSlug":"large"} -->

![Create mysql database]({{ site.baseurl }}/assets/images/2020/08/create-database-1024x547.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Paste this in your ruby file:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
require "mysql"

db_host = "127.0.0.1" #Using localhost wasn't working for me
db_user = "TypeYourUsername"
db_pass = "PutYourPassword"
db_name = "connectRuby"

@db = Mysql.connect(db_host, db_user, db_pass, db_name)
puts "Server version: " + @db.get_server_info

def insertUsers
  x = 1
  while x < 5
    @db.query("INSERT INTO user (name) VALUES ('user-#{x}');")
    x += 1
  end
  puts "Number of rows inserted: #{@db.affected_rows}"
end

# Invoking the method to create the users.
insertUsers
```

<!-- /wp:code -->

<!-- wp:paragraph -->

in your terminal run your ruby file by typing:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
ruby filename.rb
```

<!-- /wp:code -->

<!-- wp:image {"id":256,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/08/test-mysql-connection-1024x510.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

if you did everything right you should see: `Number of rows inserted: 1`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Now you can paste this part:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
def printUsers
  res = @db.query("SELECT * FROM user")
  while row = res.fetch_row do
    printf "%s, %s\n", row[0], row[1]
  end
  puts "Number of rows returned: #{res.num_rows}"

  res.free
end

# This is invoking the method to print the rows
printUsers
```

<!-- /wp:code -->

<!-- wp:paragraph -->

and run your ruby file again:

<!-- /wp:paragraph -->

<!-- wp:image {"id":258,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/08/get-all-users.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

voila all the users printed.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Here is the full code:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
require "mysql"

db_host = "127.0.0.1"
db_user = "youUsername"
db_pass = "yourPassword"
db_name = "connectRuby"

@db = Mysql.connect(db_host, db_user, db_pass, db_name)
puts "Server version: " + @db.get_server_info

def insertUsers
  x = 1
  while x < 5
    @db.query("INSERT INTO user (name) VALUES ('user-#{x}');")
    x += 1
  end
  puts "Number of rows inserted: #{@db.affected_rows}"
end

def printUsers
  res = @db.query("SELECT * FROM user")
  while row = res.fetch_row do
    printf "%s, %s\n", row[0], row[1]
  end
  puts "Number of rows returned: #{res.num_rows}"
  res.free
end

# Invoking the method to create the users.
insertUsers

# This is invoking the method to print the rows
printUsers
```

<!-- /wp:code -->

<!-- wp:separator -->

* * *
<!-- /wp:separator -->

<!-- wp:paragraph -->

Resources:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

[http://www.kitebird.com/articles/ruby-mysql.html](http://www.kitebird.com/articles/ruby-mysql.html)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

<!-- /wp:paragraph -->

