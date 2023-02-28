---
layout: post
title: Install Eclipse IDE and said Hello World from Java
date: 2020-08-06 23:58:26.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- Developer
- Java
- Tutorial
tags:
- eclipse ide
- hello world
- Install
- java
- linux mint
meta:
  _thumbnail_id: '217'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/install-eclipse-ide-and-said-hello-world-from-java/"
excerpt: 'Today is time to dust off my java skills that I learn way back during my
  time in college. So I''m going to show how to install Eclipse IDE for Java developers
  in Linux Mint and create the famous Hello World application using a text editor
  vs Eclipse IDE. '
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

Today it's time to dust off my java skills that I learned way back during my time in college. I'm going to show how to install Eclipse IDE for Java developers and create the famous **Hello World** application using a text editor vs Eclipse IDE.

<!-- /wp:paragraph -->

<!-- wp:separator -->

* * *
<!-- /wp:separator -->

<!-- wp:paragraph -->

For this tutorial I'm assuming that you already have JDK (Java Development Kit) installed in your system. To check, type in a terminal:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
javac -version
```

<!-- /wp:code -->

<!-- wp:image {"align":"center","id":212,"sizeSlug":"full"} -->

![Linux Mint | javac -version]({{ site.baseurl }}/assets/images/2020/08/javac-version-linux-mint.png)  

_Linux Mint | javac -version_

<!-- /wp:image -->

<!-- wp:paragraph -->

If no version is printed in your terminal, you will need to install it before continuing with the step 1.

<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->

#### **Step 1**

<!-- /wp:heading -->

<!-- wp:paragraph -->

Download&nbsp;[Eclipse-IDE](https://www.eclipse.org/downloads/)

<!-- /wp:paragraph -->

<!-- wp:image {"sizeSlug":"large"} -->

![Download Eclipse IDE]({{ site.baseurl }}/assets/images/2020/08/download-eclipse.gif)  

_Download Eclipse IDE_

<!-- /wp:image -->

<!-- wp:heading {"level":4} -->

#### Step 2

<!-- /wp:heading -->

<!-- wp:paragraph -->

Create a folder where you want to install Eclipse. I'm going to name mine eclipse-ide-2020‑06, but you can name it whatever you want. To do this we need to open a Terminal. You can do this by pressing Ctrl + Alt + t and typing:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
mkdir /home/your-user/eclipse-ide-2020‑06
```

<!-- /wp:code -->

<!-- wp:list -->

- _make sure you replace 'your-user' with your username._

<!-- /wp:list -->

<!-- wp:image {"sizeSlug":"large"} -->

![Create directory where we want to extract the Eclipse IDE installer]({{ site.baseurl }}/assets/images/2020/08/create-eclipse-folder.gif)  

_Create directory where we want to extract the Eclipse IDE installer_

<!-- /wp:image -->

<!-- wp:heading {"level":4} -->

#### Step 3

<!-- /wp:heading -->

<!-- wp:paragraph -->

We need to extract eclipse into the directory that was created: now in your terminal type this:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
tar -zxvf /home/your-user/Downloads/eclipse-inst-linux64.tar.gz -C /home/your-user/eclipse-ide-2020-06/
```

<!-- /wp:code -->

<!-- wp:list -->

- _make sure your paths are correct and replace 'your-user' with your username._

<!-- /wp:list -->

<!-- wp:image {"sizeSlug":"large"} -->

![Extract Eclipse IDE installer]({{ site.baseurl }}/assets/images/2020/08/extract-eclipse.gif)  

_Extract Eclipse IDE installer_

<!-- /wp:image -->

<!-- wp:heading {"level":4} -->

#### Step 4

<!-- /wp:heading -->

<!-- wp:paragraph -->

Now it is finally time to install it. To run the installer type this in your terminal:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
sudo /home/your-user/eclipse-ide-2020-06/eclipse-installer/eclipse-inst
```

<!-- /wp:code -->

<!-- wp:list -->

- it is going to ask you for your password.&nbsp;_Make sure you replace 'your-user' with your username._

<!-- /wp:list -->

<!-- wp:image {"sizeSlug":"large"} -->

![Run Eclipse IDE installer]({{ site.baseurl }}/assets/images/2020/08/run-eclipse-installer.gif)  

_Run Eclipse IDE installer_

<!-- /wp:image -->

<!-- wp:heading {"level":4} -->

#### Step 5

<!-- /wp:heading -->

<!-- wp:paragraph -->

Click on the option you want to install; in this case click on Eclipse IDE for Java Developer. Pick the directory you want to install it in, in my case I want to install it in this directory

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","sizeSlug":"large"} -->

![directory to install Eclipse]({{ site.baseurl }}/assets/images/2020/08/directory-to-install.png)  

_directory to install Eclipse_

<!-- /wp:image -->

<!-- wp:list -->

- _So I'm going to change root for opt_

<!-- /wp:list -->

<!-- wp:image {"sizeSlug":"large"} -->

![Eclipse IDE for java developers]({{ site.baseurl }}/assets/images/2020/08/installing-eclipse-ide-java-developer.gif)  

_Eclipse IDE installer_

<!-- /wp:image -->

<!-- wp:list -->

- _Accept the license. When it is done installing just click on launch_

<!-- /wp:list -->

<!-- wp:heading {"level":4} -->

#### Step 6

<!-- /wp:heading -->

<!-- wp:paragraph -->

After launching, it is going to ask you to create a workspace (A workspace is where Eclipse is going to keep all the eclipse projects by default)

<!-- /wp:paragraph -->

<!-- wp:image {"sizeSlug":"large"} -->

![eclipse ide create workspace]({{ site.baseurl }}/assets/images/2020/08/create-workspace.gif)  

_create workspace_

<!-- /wp:image -->

<!-- wp:image {"sizeSlug":"large"} -->

![eclipse ide create workspace]({{ site.baseurl }}/assets/images/2020/08/create-workspace-2.gif)  

_create workspace_

<!-- /wp:image -->

<!-- wp:image {"sizeSlug":"large"} -->

![Eclipse IDE for Java Developers]({{ site.baseurl }}/assets/images/2020/08/eclipse-for-linux-mint.gif)  

_Eclipse IDE for Java Developers_

<!-- /wp:image -->

<!-- wp:heading {"level":4} -->

#### Step 7

<!-- /wp:heading -->

<!-- wp:paragraph -->

To create a launcher (desktop icon) run the next command in your terminal:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
sudo xed .local/share/applications/eclipse.desktop
```

<!-- /wp:code -->

<!-- wp:paragraph -->

It is going to open a text editor, you should then paste this inside and save it.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
[Desktop Entry]
Encoding=UTF-8
Name=Eclipse IDE
Comment=Eclipse Integrated Development Environment
Exec=/opt/eclipse/java-2020-06/eclipse/eclipse
Icon=/opt/eclipse/java-2020-06/eclipse/icon.xpm
Categories=Application;Development;Java;IDE
Version=1.0
Type=Application
```

<!-- /wp:code -->

<!-- wp:paragraph -->

To use the new launcher outside the dash we need to change the permission:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
sudo chmod +x ~/.local/share/applications/eclipse.desktop
```

<!-- /wp:code -->

<!-- wp:image {"sizeSlug":"large"} -->

![create Eclipse IDE Launcher]({{ site.baseurl }}/assets/images/2020/08/create-desktop-icon.gif)  

_create Eclipse IDE Launcher_

<!-- /wp:image -->

<!-- wp:heading {"level":4} -->

#### Step 8

<!-- /wp:heading -->

<!-- wp:paragraph -->

Now it is time to test the launcher. Open the folder where it is located:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
xdg-open .local/share/applications/
```

<!-- /wp:code -->

<!-- wp:image {"sizeSlug":"large"} -->

![Open Eclipse IDE launcher directory]({{ site.baseurl }}/assets/images/2020/08/open-launcher-folder.gif)  

_Open Eclipse IDE launcher directory_

<!-- /wp:image -->

<!-- wp:list -->

- _You may have this problem: 'the eclipse executable launcher was unable to locate its companion shared library'_.&nbsp;To fix this run:

<!-- /wp:list -->

<!-- wp:code -->

```
sudo chmod 775 -R /root/
```

<!-- /wp:code -->

<!-- wp:image {"sizeSlug":"large"} -->

![Fix 'the eclipse executable launcher was unable to locate its companion shared library' | Linux Mint]({{ site.baseurl }}/assets/images/2020/08/fix-shared-library.gif)  

_Fix 'the eclipse executable launcher was unable to locate its companion shared library'_

<!-- /wp:image -->

<!-- wp:paragraph -->

Then execute the launcher again. You can also find the launcher under: Menu \> Programming

<!-- /wp:paragraph -->

<!-- wp:image {"sizeSlug":"large"} -->

![Eclipse IDE in Menu > Programming]({{ site.baseurl }}/assets/images/2020/08/new-launcher.gif)  

_Eclipse IDE in Menu > Programming_

<!-- /wp:image -->

<!-- wp:separator -->

* * *
<!-- /wp:separator -->

<!-- wp:paragraph -->

This is getting to long! Very quickly I'm going to show you how to create a 'Hello World' with java in a text editor.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

To do this create a new directory. You can name it whatever you want. Inside create a file named **hello-world.java** and paste this:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
// Create the class HelloWorld
class HelloWorld{
  // Call the main() method to start our application
  public static void main(String args[]){
    // Print Hello World in terminal
    System.out.println("Hola Mundo desde Java!");
    System.out.println("Hello World form Java!");
  }
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Now we need to compile our application. To do this in your terminal type the following:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
javac hello-world.java
```

<!-- /wp:code -->

<!-- wp:paragraph -->

This will create a new file called HelloWorld.class. Now we need to run our app. In the terminal run:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
java HelloWorld
```

<!-- /wp:code -->

<!-- wp:paragraph -->

That is! You should now see Hola Mundo desde Java! and Hello World from Java! in your terminal.

<!-- /wp:paragraph -->

<!-- wp:image {"id":217,"sizeSlug":"large"} -->

![Hello World with Java]({{ site.baseurl }}/assets/images/2020/08/hello-world-java.png)  

_Hello World with Java_

<!-- /wp:image -->

<!-- wp:paragraph -->

Congrats! This is your first java app! For the 2nd part of this post I will make the same but with the Eclipse IDE.

<!-- /wp:paragraph -->

