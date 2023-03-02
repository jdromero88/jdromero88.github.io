---
layout: post
title: My first time using Bulma CSS framework.
date: 2020-07-03 01:14:27.000000000 -04:00
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
- bulma
- css framework
- Developer
- html
- Jose Romero
- tutorial
- website
meta:
  _oembed_d7a86999dccbf93be61a8f5e99317a1a: "{{unknown}}"
  _thumbnail_id: '114'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/my-first-time-using-bulma-css-framework/"
excerpt: |-
  Hola! I finally decided to give a try to Bulma and so far I love it! The mainly reason is that is looks beautiful, is mobile friendly, is lightweight and was so easy to add to the project I was working on.
  I already used others CSS frameworks like Bootstrap, Semantic UI, Semantic UI is my favorite! or I should say it was?
---
<!-- wp:paragraph -->

Hola! I finally decided to give [Bulma](https://bulma.io/) a try and so far I love it! The main reason is that is looks beautiful, is mobile friendly, is lightweight and was so easy to add to the project I was working on.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

I have previously other CSS frameworks like [Bootstrap](https://getbootstrap.com/) and [Semantic UI](https://semantic-ui.com/). Semantic UI is my favorite! ... or I should say it was?!

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

So what is Bulma?

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

As they mention in their website Bulma is a CSS framework.

<!-- /wp:paragraph -->

<!-- wp:image {"id":101,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/07/bulma.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Now you may be wondering but what is a CSS Framework?

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/a5viI92PAF89q" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/reaction-a5viI92PAF89q)

<!-- /wp:html -->

<!-- wp:paragraph -->

You maybe already know what is a CSS Framework but if you don't according to Wikipedia a **[CSS framework](https://en.wikipedia.org/wiki/CSS_framework)** is a library allowing for easier, more standards-compliant web design using the Cascading Style Sheets language. Most of these frameworks contain at least a grid. More functional frameworks also come with more features and additional JavaScript based functions, but are mostly design oriented and focused around interactive UI patterns. This detail differentiates CSS frameworks from other JavaScript frameworks.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Ok now that we have and idea of what a CSS framework is and we know some of them: Bootstrap, Semantic UI, Bulma. I'm going to show you how to install Bulma into your project.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

I setup the project and I called the folder, _website-with-bulma_, and inside I have an **index.html** with this code inside:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title> Im using Bulma</title>
  </head>
  <body>
    <section class="section">
      <div class="container">
        <h1 class="title">
          Hello World
        </h1>
        <p class="subtitle">
          My first website with <strong>Bulma</strong>!
        </p>
      </div>
    </section>
  </body>
</html>
```

<!-- /wp:code -->

<!-- wp:image {"id":105,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/07/basic-code-for-bulma.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Open the index.html with your browser and it should look like this.

<!-- /wp:paragraph -->

<!-- wp:image {"id":107,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/07/basic-code-looks-like-1024x246.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

There are many ways you can add bulma to your project. You can install it via `npm install bulma`, you can add it via [CDN](https://www.jsdelivr.com/package/npm/bulma?path=css), or download it from the [repository](https://github.com/jgthms/bulma/tree/master/css). In this case we are going to do it by using the CDN because it is the fastest and easiest way.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**Step 1**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Add this code between your \<head\> \</head\>. I like to keep mine on top of the `<title></title>`

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<!-- Responsive viewport meta tag -->
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- Added Bulma by CDN -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.0/css/bulma.min.css">
```

<!-- /wp:code -->

<!-- wp:paragraph -->

That's it! Now if you refresh your **index.html** page should look like this:

<!-- /wp:paragraph -->

<!-- wp:image {"id":108,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/07/basic-code-with-bulma-1024x263.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

I know:

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/RiuMMt2r242LqRyRZn" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/Friends-friends-season-6-tv-RiuMMt2r242LqRyRZn)

<!-- /wp:html -->

<!-- wp:paragraph -->

Now going through the docs we can use their examples to add a navbar, footer, and some dummy content to have a basic template for you next project.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Lets add the navbar by adding the code right under the \<body\> tag:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<!-- Navbar -->
    <nav class="navbar is-warning" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item" href="https://bulma.io">
          <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
        </a>

        <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div id="navbarBasicExample" class="navbar-menu">
        <div class="navbar-start">
          <a class="navbar-item">
            Home
          </a>

          <a class="navbar-item">
            About
          </a>

          <div class="navbar-item has-dropdown is-hoverable">
            <a class="navbar-link">
              Services
            </a>

            <div class="navbar-dropdown">
              <a class="navbar-item">
                Repair PC/Laptops
              </a>
              <a class="navbar-item">
                Installation of OS(Operating System)
              </a>
              <hr class="navbar-divider">
              <a class="navbar-item">
                Contact
              </a>
            </div>
          </div>
        </div>

        <div class="navbar-end">
          <div class="navbar-item">
            <div class="buttons">
              <a class="button is-primary">
                <strong>Sign up</strong>
              </a>
              <a class="button is-light">
                Log in
              </a>
            </div>
          </div>
        </div>
      </div>
    </nav>
    <!-- Navbar end -->
```

<!-- /wp:code -->

<!-- wp:paragraph -->

We are using the class _is-fixed-top_ in the navbar so we would need to add this class to the \<body\> so it can add the appropiate padding to the website.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<body class="has-navbar-fixed-top">
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Refresh your website and it should look like this:

<!-- /wp:paragraph -->

<!-- wp:image {"id":109,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/07/adding-bulma-navbar-1024x654.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

If you resize your browser (make it smaller) you would see that that you now have the Navbar burger to the right of the navbar. But it is not working, yet.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":110,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/07/resize-screen-bulma.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

To make it work we need to add some Javascript code because Bulma does not include any javascript.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Lets be organized, create a folder and call it **js**. Inside that folder create a new file a and call it **bulma.js** and add the code:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
document.addEventListener('DOMContentLoaded', () => {
  // alert('holamundo')
  // Get all "navbar-burger" elements
  const $navbarBurgers = Array.prototype.slice.call(document.querySelectorAll('.navbar-burger'), 0);

  // Check if there are any navbar burgers
  if ($navbarBurgers.length > 0) {

    // Add a click event on each of them
    $navbarBurgers.forEach( el => {
      el.addEventListener('click', () => {

        // Get the target from the "data-target" attribute
        const target = el.dataset.target;
        const $target = document.getElementById(target);

        // Toggle the "is-active" class on both the "navbar-burger" and the "navbar-menu"
        el.classList.toggle('is-active');
        $target.classList.toggle('is-active');
      });
    });
  }
});
```

<!-- /wp:code -->

<!-- wp:paragraph -->

We need to link the **bulma.js** file to our **index.html** and we do that by adding this line inside our \<head\>

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<!-- Added bulma.js -->
<script src="./js/bulma.js"></script
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Now refresh and try again. Now it should be working.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":111,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/07/bulma-mobile-version.gif)

<!-- /wp:image -->

<!-- wp:paragraph -->

Next lets add some more dummy content. Why don't we add some more sections.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

You can just copy and paste a few times the section we already have. I added more text for the paragraphs using [Lorem Ipsum](https://www.lipsum.com/). And this is the code:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<section id="home" class="hero is-fullheight">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">
            Home
          </h1>
          <h2 class="subtitle">
            Medium subtitle
          </h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam orci dui, lacinia non faucibus in, posuere eget eros. In hac habitasse platea dictumst. In tortor augue, iaculis ut mi sit amet, tempus euismod elit. Nam ac eleifend enim, ac interdum enim. Nulla in purus mauris. Morbi auctor mattis mi porta scelerisque. Nullam aliquet, arcu eu eleifend finibus, ante odio tempor urna, quis congue arcu quam non purus. Morbi vel venenatis est. Aliquam tincidunt libero a quam facilisis tempus. Vestibulum bibendum orci elit, in viverra purus laoreet eget. Mauris augue diam, sagittis at leo sed, commodo dignissim neque. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Phasellus et tempor massa.</p>
          <p>Ut eu imperdiet ligula. Quisque ornare vitae risus id auctor. Curabitur dignissim id risus a hendrerit. Phasellus tempor, mauris sit amet gravida fringilla, odio lorem blandit turpis, eget pretium velit ante sit amet erat. Nulla facilisi. Praesent eleifend consequat tempus. Donec ullamcorper porttitor magna, porttitor aliquam ligula pharetra sed. Nullam nec dui nisi. Nullam vitae felis feugiat felis consequat tincidunt. Nunc bibendum nisi ornare felis vehicula efficitur.</p>
        </div>
      </div>
    </section>
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Now we only need to add the footer:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<!-- Footer -->
    <footer class="footer">
      <div class="content has-text-centered">
        <p>
          My first website using <strong>Bulma</strong> by <a href="https://josedromero.com">Jose Romero</a>.
        </p>
        <p>
          All Rights Reserved © 2020
        </p>
      </div>
    </footer>
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Refresh your website and look at what you just built. Looks good right?

<!-- /wp:paragraph -->

<!-- wp:image {"id":114,"sizeSlug":"full"} -->

![]({{ site.baseurl }}/assets/images/2020/07/final-product-bulma.gif)

<!-- /wp:image -->

<!-- wp:paragraph -->

Please go through the docs and play some more with Bulma. Later show me what you did with a screenshot in the comments. Here is the link to the repository so you can see the full project. [https://github.com/jdromero88/website-with-bulma](https://github.com/jdromero88/website-with-bulma)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Resources:

<!-- /wp:paragraph -->

<!-- wp:list -->

- [https://bulma.io/](https://bulma.io/)

<!-- /wp:list -->

<!-- wp:list -->

- [https://en.wikipedia.org/wiki/CSS\_framework](https://en.wikipedia.org/wiki/CSS_framework)

<!-- /wp:list -->

