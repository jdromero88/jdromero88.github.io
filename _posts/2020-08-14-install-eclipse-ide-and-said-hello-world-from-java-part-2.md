---
layout: post
title: Install Eclipse IDE and said Hello World from Java (part 2)
date: 2020-08-14 17:26:26.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Java
- Tutorial
tags:
- eclipse ide
- hello world
- java
meta:
  _thumbnail_id: '231'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/install-eclipse-ide-and-said-hello-world-from-java-part-2/"
excerpt: Now is time to continue and finally use the Eclipse IDE we installed in the
  previous post. Today we will create an app to print Hello World using the Eclipse
  IDE.
---
<!-- wp:paragraph -->

Now it is time to continue and finally use the Eclipse IDE we installed in the previous [post](https://blog.josedromero.com/install-eclipse-ide-and-said-hello-world-from-java/). Today we will create an app to print Hello World using the Eclipse IDE.

<!-- /wp:paragraph -->

<!-- wp:separator -->

* * *
<!-- /wp:separator -->

<!-- wp:heading {"level":3} -->

### Step 1

<!-- /wp:heading -->

<!-- wp:paragraph -->

Open Eclipse IDE go to Menu \> Programming \> Eclipse IDE

<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->

### Step 2

<!-- /wp:heading -->

<!-- wp:paragraph -->

Then we need to create a new java project. Click File \> New \> Java Project and give it a name hello-world. Click finish.

<!-- /wp:paragraph -->

<!-- wp:image {"sizeSlug":"large"} -->

![Create new Java project]({{ site.baseurl }}/assets/images/2020/08/create-hello-world-app.gif)  

_Create new Java project_

<!-- /wp:image -->

<!-- wp:heading {"level":3} -->

### Step 3

<!-- /wp:heading -->

<!-- wp:paragraph -->

Now we need to create a package inside the folder src. Put your cursor inside the Package Explorer and right click \> New \> Package \> give it a name. Click finish.

<!-- /wp:paragraph -->

<!-- wp:image {"sizeSlug":"large"} -->

![Create a package]({{ site.baseurl }}/assets/images/2020/08/create-print-package.gif)  

_Create a package_

<!-- /wp:image -->

<!-- wp:heading {"level":3} -->

### Step 4

<!-- /wp:heading -->

<!-- wp:paragraph -->

Time to create the HelloWorld class. Again go to Package Explorer and right click \> New \> Class name it HelloWorld. \> Tick public static void main(String[] args). Click finish.

<!-- /wp:paragraph -->

<!-- wp:image {"sizeSlug":"large"} -->

![Create class HelloWorld]({{ site.baseurl }}/assets/images/2020/08/create-helloworld-class.gif)  

_Create class HelloWorld_

<!-- /wp:image -->

<!-- wp:heading {"level":3} -->

### Step 5

<!-- /wp:heading -->

<!-- wp:paragraph -->

After creating the class, the IDE will already generate some base code and it will look like this:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
package print;

public class HelloWorld {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
	}

}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

You already know how to print string in the terminal. Go ahead and type the code inside the main method. In case you don't remember how, here it is.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
package print;

public class HelloWorld {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		System.out.println("Hola Mundo desde Java!");
                System.out.println("Hello World form Java!");
	}

}
```

<!-- /wp:code -->

<!-- wp:image {"sizeSlug":"large"} -->

![print hello world]({{ site.baseurl }}/assets/images/2020/08/print-hello-world.gif)  

_print hello world_

<!-- /wp:image -->

<!-- wp:heading {"level":3} -->

### Step 6

<!-- /wp:heading -->

<!-- wp:paragraph -->

Now is time to run the project. To do this just click on the play icon or go to the menu Run \> Run. Now you should see Hello World from Java in the IDE terminal.

<!-- /wp:paragraph -->

<!-- wp:image {"sizeSlug":"large"} -->

![Run the project]({{ site.baseurl }}/assets/images/2020/08/run-the-project.gif)  

_Run the project_

<!-- /wp:image -->

<!-- wp:paragraph -->

That's all my friends. As you can see the IDE gives you many options that make it easier to develop Java application. But to learn the basics and to create a console application we just need a text editor and the terminal. See you later!

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

<!-- /wp:paragraph -->

