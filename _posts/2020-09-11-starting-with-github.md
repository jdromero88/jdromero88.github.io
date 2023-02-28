---
layout: post
title: Starting with Github.
date: 2020-09-11 19:01:07.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- Developer
- git
- Tutorial
tags:
- Developer
- Git
- Github
meta:
  _thumbnail_id: '293'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/starting-with-github/"
excerpt: Yesterday I was helping my friend to setup Github on his machine and I realized
  that I could write a blog post about this. So it can be useful to someone else or
  at least I hope so.
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

Yesterday I was helping my friend to setup Github on his machine and I realized that I could write a blog post about this. So it can be useful to someone else or at least I hope so.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

To resume very quickly the steps to setup github on you machine are: - Install Git. - Setup Git. Very easy right the second part probably is the "hardest" part.

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/idj2rnFj9tijpUERVs" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/cbc-web-exclusive-baroness-von-sketch-idj2rnFj9tijpUERVs)

<!-- /wp:html -->

<!-- wp:paragraph -->

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

To install in a Linux environment in any debian distro like Linux Mint or Ubuntu you can use:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
sudo apt-get install git
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Is going to ask for your password. Just type it and hit enter.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Next we need to configured it. First just check in case you already have a ssh key. I doubt it but just check it. To to this just type in a terminal:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
cat ~/.ssh/id_rsa.pub
```

<!-- /wp:code -->

<!-- wp:paragraph -->

If you have is going to return something like this:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
ssh-rsa Alaskdjf;lasjdf;lakjsdf;lakjsdf;lvahsd;lh;lasjdf;lakhsd;lfas;dlfkja;lsdjfaiwjo;wej;laskdjf;lasdjf;lasjdf;lkasjd;lfkja;sldfkja;lsdfj;laksjdf;lakjdsf;lasjdf;lajdf;lajdsf;lakjsdf;lakjsdf;lkajsd;fkja;lsdjfa;lsdjkf;laskdjf;la;alskdjf;alsjfoiewjao;wejfqoagagalskdjgal;sdj;lasdfjasdfjl;asdf youruser@linux-mint
```

<!-- /wp:code -->

<!-- wp:paragraph -->

If doesn't return anything you must create a key and you can do it this way:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
ssh-keygen -o
```

<!-- /wp:code -->

<!-- wp:paragraph -->

then after you create you key to see it you need to type again the command above this step.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

When you can see your key you need to select it everything and copy. from ssh-rsa............................. till you user@linux all of that. Open Github login to your account go to settings

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":287,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/09/go-to-settings.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

then go to SSH and GPG keys.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":288,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/09/go-to-SSH-and-GPG-keys.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Click on the green button New SSH key

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":289,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/09/create-new-key.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Next give it a title. Can be anything you want. I recommend you to give the name of your laptop so you can recognized easily. Paste the SSH key that was generated and click Add SSH key.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":290,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/09/add-new-key.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Now back to you terminal you need to add your email and username. Type in your terminal:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git config --global user.email "you@example.com"
```

<!-- /wp:code -->

<!-- wp:code -->

```
git config --global user.name "Your Name"
```

<!-- /wp:code -->

<!-- wp:paragraph -->

And that's it now you are ready to go. You can test it by cloning a repo from github. Try it with [this repo.](https://github.com/jdromero88/first-app)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Just click on the green button where it says code: then make sure you selected clone with SSH copy that line.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":291,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/09/clone-with-ssh.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

and in your terminal type:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
git clone git@github.com:jdromero88/first-app.git
```

<!-- /wp:code -->

<!-- wp:paragraph -->

and paste the line you copied and hit enter. This would create a copy of the repo in your laptop. now you can cd into the filder first-app and open the index.html in your browser.

<!-- /wp:paragraph -->

<!-- wp:separator -->

* * *
<!-- /wp:separator -->

<!-- wp:paragraph -->

Resources: [https://git-scm.com/book/en/v2/Getting-Started-Installing-Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

<!-- /wp:paragraph -->

