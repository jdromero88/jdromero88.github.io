---
layout: post
title: Open PDF in your react app
date: 2020-08-21 15:55:34.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- Developer
- REACT
- Tutorial
tags:
- pdf
- REACT
meta:
  _thumbnail_id: '238'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/open-pdf-in-your-react-app/"
excerpt: I just "re-model" my portfolio website and I decided to change the way I
  was showing my resume. A few posts ago I talked about how to render a pdf into your
  react app using  React-PDF. This time I decided that instead of rendering inside
  the app I actually wanted to open it in the browser.
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

I just "remodeled" my portfolio website and I decided to change the way I was displaying my resume. A [few posts](https://blog.josedromero.com/how-to-add-pdf-into-your-react-app/) ago I talked about how to render a pdf into your react app using React-PDF. This time I decided that instead of rendering inside the app I actually wanted to open it in the browser.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Now my problem was that when I was hitting the route where I put my pdf file, `https://myawesomewebsite.com/pdf/resume.pdf` instead of opening my resume it just showed my home page again.

<!-- /wp:paragraph -->

<!-- wp:image {"id":237,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/08/resume-path.png)  

_I uploaded my resume.pdf to my hosting as you can see in the picture above._

<!-- /wp:image -->

<!-- wp:paragraph -->

These are the routes that I have in my app.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<Switch>
   <Route exact path='/portfolio' component={Portfolio} />
   <Route exact path='/about' component={About} />
   <Route path='/' component={Home} />
</Switch>
```

<!-- /wp:code -->

<!-- wp:paragraph -->

So every time I hit the route `https://josedromero.com/pdf/resume.pdf` to open my resume, the app went and checked if any routes matched the route that was requested and the only one that matched was the `/ ` and it took me back to my home page.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Now to fix this annoying problem I had to add my resume.pdf to my assets folder `src > assets > resume.pdf`. If you don't have one just create a assets folder.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Ok now we have our pdf file inside our react app and we are ready open it. Now to import it I'm doing so in my component `Navbar.jsx`

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import React from 'react'
import ResumePDF from '../assets/resume.pdf'
class Navbar extends React.Component{
  render(){
     .
     .
     .
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Then in the anchor tag href instead of putting the route of the pdf file I just put the file that we imported `href={ResumePDF} `

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<a className="navbar-item" target="_blank" rel="noopener noreferrer" href={ResumePDF}>
   Resume
</a>
```

<!-- /wp:code -->

<!-- wp:paragraph -->

And that is it! Now when you click in the link to the pdf file it should open the pdf!

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

<!-- /wp:paragraph -->

