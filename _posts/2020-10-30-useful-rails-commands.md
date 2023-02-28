---
layout: post
title: Useful rails commands
date: 2020-10-30 20:00:46.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- rails
tags:
- commands
- rails
meta: {}
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/useful-rails-commands/"
excerpt: Here we are again with another post. Today I’m going to talk to you about
  rails commands; specifically about db:prepare & rails db:reset. I picked this topic
  to help you save a few seconds while setting up the rails app.
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

Here we are again with another post. Today I’m going to talk to you about rails commands; specifically about **db:prepare** & **rails db:rese** t. I picked this topic to help you save a few seconds while setting up the rails app.  
I know I know we all feel like Regina Phalange.

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/XWZi4377aAp7a" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/friends-tv-phoebe-XWZi4377aAp7a)

<!-- /wp:html -->

<!-- wp:paragraph -->

After you create your app (here is a reminder just in case)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`rails new visit-dc`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

and create the resources (another reminder just in case)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

rails g resource Place name description

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

here comes the “magic”, when you run

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`rails db:prepare`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

It is running “under&nbsp;the hood”&nbsp; **rails db:create** &nbsp;and&nbsp; **rails** &nbsp; **db:migrate**. That means that it is creating the schema and creating the database. Yes you are right “all of this” is running with just one command. I know this information is saving you 1000 milliseconds

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":334,"sizeSlug":"large"} -->

![rails db:prepare]({{ site.baseurl }}/assets/images/2020/10/rails-db-prepare.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

To get some extra help (cough&nbsp;_NOT REALLY_&nbsp;cough) you can run rails **db:prepare -h**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Ok now lets move on to the next trick that will save you another 1000 milliseconds.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**WARNING** : Use at your own risk. Hahaha just kidding. It is very important to make sure you are&nbsp; **NOT** &nbsp;working in your production database.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

`rails db:reset`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

This command will drop the current database and create it again. After that it will run the command&nbsp; **rails db:seed**. So if you have any dummy data in your seed file this will populate your brand new database.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":335,"sizeSlug":"large"} -->

![rails db:reset]({{ site.baseurl }}/assets/images/2020/10/rails-db-reset.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

_Bonus command:_&nbsp;using&nbsp; **rails db:setup** &nbsp;will create the database and run the command&nbsp; **rails db:seed**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Thanks for your attention!

<!-- /wp:paragraph -->

