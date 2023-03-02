---
layout: post
title: Create sitemap for your REACT app.
date: 2020-06-27 01:07:36.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Developer
- REACT
- Tutorial
tags:
- Developer
- Javascript
- REACT
- router
- sitemap
meta:
  _thumbnail_id: '96'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/create-sitemap-for-your-react-app/"
excerpt: 'Hey there!  I had to create a sitemap for my website (which I made with
  REACT) to have better SEO (Search Engine Optimization). I went to google and searched
  for: create sitemap and I opened the first link https://www.xml-sitemaps.com and
  I put my website address and generate the sitemap.'
---
<!-- wp:paragraph -->

Hey there! I had to create a sitemap for my website (which I made with REACT) to have better SEO (Search Engine Optimization). I went to google and searched for: `create sitemap` and I opened the first link [https://www.xml-sitemaps.com](https://www.xml-sitemaps.com/) and I put my website address and generate the sitemap.

<!-- /wp:paragraph -->

<!-- wp:image {"id":79,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/06/Jose-Romero-Sitemap.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Everything went smoothly... until I saw that the sitemap generator only found the home route (as you can see in the pic above) `https://josedromero.com`. But it didn't find any of the other routes that I currently have e.g.: [https://josedromero.com/portfolio](https://josedromero.com/portfolio), [https://josedromero.com/about](https://josedromero.com/about). So, that made me wonder if that was because I made my website with REACT; because I had never had this problem using a sitemap generator on a website made it with pure HTML.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

I went back to google( ~~what a surprise right?~~ Thanks google) to see if I could find a sitemap generator for REACT app and I came across [react-router-sitemap](https://www.npmjs.com/package/react-router-sitemap) which is a module for generating sitemaps using React Router configuration.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

I wanted to write about my experience with installing the module, in case someone else needed in the future (which would probably would be me again jajaja)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Here is how you do it from scratch:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**Step 1**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

In your terminal type: `npx create-react-app create-sitemap`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

where `create-sitemap` is the name of the app. You can change that to whatever you want to name your react app.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**Step 2**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Go inside the directory of your app, in this case `cd create-sitemap`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**Step 3**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Install react-router-dom `npm install react-router-dom`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Make sure everything is working and run `npm start`. If everything is working you should see something like this in your browser.

<!-- /wp:paragraph -->

<!-- wp:image {"id":81,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/06/react-app-jose-romero.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

**Step 4**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Go to **index.js** file and add this: `import { BrowserRouter } from 'react-router-dom'` and wrap the `<App />` component with `<BrowserRouter>`. It should look like this

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
import * as serviceWorker from './serviceWorker';
import { BrowserRouter } from 'react-router-dom'

ReactDOM.render(
  <React.StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </React.StrictMode>,
  document.getElementById('root')
);

// If you want your app to work offline and load faster, you can change
// unregister() to register() below. Note this comes with some pitfalls.
// Learn more about service workers: https://bit.ly/CRA-PWA
serviceWorker.unregister();
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**Step 5**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Create a file called **Routes.js** and add this code:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import React from 'react';
import { Switch, Route } from 'react-router';
import About from './About'
import Projects from './Projects'
import Contact from './Contact'
const Routes = () => {
  return (
    <Switch>
      <Route path='/about' component = { About } />
      <Route path='/projects' component = { Projects } />
      <Route path='/contact' component = { Contact }/>
      <Route path='/' />
    </Switch>

  )
}
export default Routes
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**Step 6**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Now we need to create the files About.js, Projects.js, Contact.js

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**About.js** paste this:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import React from 'react'

export default function About(){
  return(
    <div>
      <h1>this is the About Page</h1>
    </div>
  )
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**Projects.js** paste this:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import React from 'react'

export default function Projects(){
  return(
    <div>
      <h1>this is the Projects Page</h1>
    </div>
  )
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**Contact.js** paste this:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import React from 'react'

export default function Contact(){
  return(
    <div>
      <h1>this is the Contact Page</h1>
    </div>
  )
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**Step 7**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Create a file called **Navbar.js** and paste this code:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import React from 'react'

export default function Navbar() {
  return (
    <>
      <nav>
        <a href="/">Home</a> |
        <a href="/about">About</a> |
        <a href="/projects">Projects</a> |
        <a href="/contact">Contact</a>
      </nav>
    </>
  )
}
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**Step 8**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Now we need to update the **App.js** file by importing the files

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import Routes from './Routes'
import Navbar from './Navbar'
```

<!-- /wp:code -->

<!-- wp:paragraph -->

and then adding the components Navbar and Routes. I put them between the header and the img.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<header className="App-header">
   <Navbar />
   <Routes />
   <img src={logo} className="App-logo" alt="logo" />
```

<!-- /wp:code -->

<!-- wp:paragraph -->

The file **App.js** should look like this now.

<!-- /wp:paragraph -->

<!-- wp:image {"id":82,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/06/create-react-sitemap.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

**Step 9**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Now we are finally going to install react-router-sitemap in the terminal run `npm i --save react-router-sitemap`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**Step 10**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Create a new file called **sitemap-builder.js** and add this code:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
require("babel-register")({
  presets: ["es2015", "react"]
});

const router = require('./Routes').default;
const Sitemap = require('react-router-sitemap').default;

(
    new Sitemap(router)
        .build('https://mi-awesome-website.com')
        .save('./public/sitemap.xml')
);
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**Step 11**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

We need to install babel-register

<!-- /wp:paragraph -->

<!-- wp:code -->

```
npm install --save-dev babel-cli
npm install --save-dev babel-preset-es2015
npm install --save-dev babel-preset-react
npm install --save-dev babel-register
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**Step 12**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Time to add our script to the **package.json**

<!-- /wp:paragraph -->

<!-- wp:code -->

```
"scripts": {
    ...,
    "sitemap": "babel-node ./sitemap-builder.js"
  }
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**Step 13**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Now we can run the script `npm run sitemap`

<!-- /wp:paragraph -->

<!-- wp:image {"id":83,"sizeSlug":"full"} -->

![]({{ site.baseurl }}/assets/images/2020/06/sitemap-script.gif)

<!-- /wp:image -->

<!-- wp:paragraph -->

and the file **sitemap.xml** is createed as you can see in the gif above.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

I hope you find this useful. If you have any problems please let me know.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**UPDATE**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

I totally forgot to show the **sitemap.xml** and now that I was looking into it I realized that the sitemap just generate the main address. I'm currently looking how to fix this to show all the routes from the **Routes.js** that we setup in our SPA.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<!-- sitemap.xml -->
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9" xmlns:news="http://www.google.com/schemas/sitemap-news/0.9" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:mobile="http://www.google.com/schemas/sitemap-mobile/1.0" xmlns:image="http://www.google.com/schemas/sitemap-image/1.1" xmlns:video="http://www.google.com/schemas/sitemap-video/1.1">
<url> <loc>https://mi-awesome-website.com/</loc> </url>
</urlset>
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**UPDATE 2**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

I found a work around to fix this problem. We need to create a file **router.js** and just copy and paste the code from the **Routes.js** and make sure you update the file. You can see the difference in the next picture.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**router.js** file:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import React from 'react';
import { Switch, Route } from 'react-router';

export default (
  <Switch>
    <Route path='/about' />
    <Route path='/projects' />
    <Route path='/contact' />
    <Route path='/' />
  </Switch>
)
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Make sure you also update the **sitemap-builder.js** to pull the new file you create.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
require("babel-register")({
  presets: ["es2015", "react"]
});
const router = require('./router').default;
const Sitemap = require('react-router-sitemap').default;
(
   new Sitemap(router)
      .build("https://mi-awesome-website.com")
      .save('./public/sitemap.xml')
);
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Now you run again `npm run sitemap` and should generate your **sitemap.xml** and should looks like this.

<!-- /wp:paragraph -->

<!-- wp:image {"id":97,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/06/sitemap.xml_-1024x482.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

**Resources:**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

1- [https://www.npmjs.com/package/react-router-sitemap](https://www.npmjs.com/package/react-router-sitemap)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

2- [https://github.com/kuflash/react-router-sitemap/blob/master/api.md](https://github.com/kuflash/react-router-sitemap/blob/master/api.md)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Repository:

<!-- /wp:paragraph -->

<!-- wp:list -->

- [https://github.com/jdromero88/](https://github.com/jdromero88/create-sitemap-react-app)[create](https://github.com/jdromero88/create-sitemap-react-app)[-sitemap-react-app](https://github.com/jdromero88/create-sitemap-react-app)

<!-- /wp:list -->

