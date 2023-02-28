---
layout: post
title: Starting your first project.
date: 2020-06-05 23:08:57.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- Developer
- Tutorial
tags:
- css
- html
- linux mint
- tutorial
- website
meta:
  _thumbnail_id: '59'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/starting-your-first-project/"
excerpt: |-
  You have just finished setting up your developer environment. Now we can start working on your first project!
  To do that you need to decide where you would like to keep your projects or apps.  I have mine in a directory called /development/code as you can see in the next picture.
---
<!-- wp:paragraph -->

You have just finished setting up your [developer environment](https://blog.josedromero.com/setting-up-your-linux-mint-developer-environment/). Now we can start working on your first project!

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

To do that you need to decide where you would like to keep your projects or apps. I have mine in a directory called /development/code as you can see in the next picture.

<!-- /wp:paragraph -->

<!-- wp:image {"id":45,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/06/working-directory-1024x130.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

There are many ways to create a directory (folder) . I'm going to show you 2 of those ways.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

1- In a terminal just type **`mkdir`** NameOfFolder. For this example I'm calling it devs.

<!-- /wp:paragraph -->

<!-- wp:image {"id":47,"sizeSlug":"full"} -->

![]({{ site.baseurl }}/assets/images/2020/06/create-dir.gif)

<!-- /wp:image -->

<!-- wp:paragraph -->

**`mkdir`** is the command to make a directory. **`cd`** is the command to change directory. **`ls`** is the command to list information about files and directories. **`pwd`** is the command to print working directory.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

2- Open your home folder then right click and created folder.

<!-- /wp:paragraph -->

<!-- wp:image {"id":50,"sizeSlug":"full"} -->

![]({{ site.baseurl }}/assets/images/2020/06/folder-way.gif)

<!-- /wp:image -->

<!-- wp:paragraph -->

Ok now that you have decided where to keep your apps (projects) you can begin.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

I'm creating a directory called firstApp and inside the folder I need to create a file index.html ( to create a file you can use the command `touch` nameOfFile.extension)

<!-- /wp:paragraph -->

<!-- wp:image {"id":53,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/06/firstApp.gif)

<!-- /wp:image -->

<!-- wp:paragraph -->

With the command `atom .` we are opening the project folder with atom text editor. Once atom is opened you can see the project folder with the index.html. Then after you open that file in your browser you will see that it is empty, just a blank page.

<!-- /wp:paragraph -->

<!-- wp:image {"id":55,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/06/atom-text-editor.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Now lets type some html

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>..:: My first Website ::..</title>
  </head>
  <body>
    <h1>Hello World - Hola Mundo</h1>
    <h2>this is my first website</h2>
  </body>
</html>
```

<!-- /wp:code -->

<!-- wp:image {"id":56,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/06/writing-html.gif)

<!-- /wp:image -->

<!-- wp:paragraph -->

You can save pressing `ctrl + s` or go to file \> save and now you can open the index.html in your browser.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

If you click on the bottom where it says index.html it's going to copy the path and you can just go to your browser and paste it and hit enter. (Watch the next gif)

<!-- /wp:paragraph -->

<!-- wp:image {"id":59,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/06/open-in-browser.gif)

<!-- /wp:image -->

<!-- wp:paragraph -->

That is it for now! You can play around adding more html.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

On the [next post](https://blog.josedromero.com/starting-your-first-project-part-2/) I'm going to show you how to use github with your project and making this website prettier. [Part 2](https://blog.josedromero.com/starting-your-first-project-part-2/)

<!-- /wp:paragraph -->

