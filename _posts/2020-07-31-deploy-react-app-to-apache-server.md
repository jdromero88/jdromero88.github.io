---
layout: post
title: Deploy React app to apache server.
date: 2020-07-31 01:31:56.000000000 -04:00
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
- apache
- Deploy
- Developer
- Javascript
- REACT
- server
- website
meta:
  _thumbnail_id: '193'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/deploy-react-app-to-apache-server/"
excerpt: |-
  This post is dedicated to the people like me who went through a headaches went it was time to deploy a React website into an apache server.

  First thing I did was buy domain and hosting (I got them from bluehost.) and them jump straight into my text editor Atom to start building my personal website with React and Semantic-UI.
---
<!-- wp:heading {"align":"center"} -->

## Hola! 

<!-- /wp:heading -->

<!-- wp:paragraph -->

This post is dedicated to the people like me who went through so many headaches when it was time to deploy a React website into an apache server.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

First thing I did was buy domain and hosting (I got both of them from [bluehost.](https://www.bluehost.com/)) and them jumped straight into my text editor [Atom](https://atom.io/) to start building my [personal website](https://josedromero.com/) with [React](https://reactjs.org/) and [Semantic-UI](https://semantic-ui.com/).

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

When I felt that my website was ready to put it live and show it to the world I realized that...

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/4Hx5nJBfi8FzFWxztb" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/tv4-problem-tom-hanks-houston-we-have-a-4Hx5nJBfi8FzFWxztb)

<!-- /wp:html -->

<!-- wp:paragraph -->

Ok normally to put your website live you need to upload to your hosting to your index.html and other files you used. Normally it looks like this for a [static website](https://blog.josedromero.com/starting-your-first-project/)

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":183,"sizeSlug":"large"} -->

![Static website files example]({{ site.baseurl }}/assets/images/2020/07/files-to-upload.png "Static website files example")

<!-- /wp:image -->

<!-- wp:paragraph -->

But when you are developing with React your amount of files increases substantially. Keep in mind that this is just a very simple React app with only 4 components.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":184,"sizeSlug":"large"} -->

![React files]({{ site.baseurl }}/assets/images/2020/07/react-files.png "React files")  

_React files_

<!-- /wp:image -->

<!-- wp:paragraph -->

So the question was: Do I need to upload all these files? or how the heck do I do that? So after spending some time with my friend [google](https://www.google.com/) I finally found a solution. Here it is, so you guys don't need to go through all the same headaches I went through.

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/26uflTE3n9Tom1ipi" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/new-girl-new-girl-jess-ng-26uflTE3n9Tom1ipi)

<!-- /wp:html -->

<!-- wp:paragraph -->

The website that I'm going to deploy is the one I made in this [blog post](https://blog.josedromero.com/create-sitemap-for-your-react-app/).

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":193,"sizeSlug":"large"} -->

![react sitemap app]({{ site.baseurl }}/assets/images/2020/07/react-sitemap-app-1024x576.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

In **package.json** make sure you add homepage with the root of your website.

<!-- /wp:paragraph -->

<!-- wp:code -->

```
"name": "create-sitemap",
  "homepage": "https://josedromero.com/deployreactapp",
  "version": "0.1.0",
  .
  .
  .
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**Step 1**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Log into your cpanel normally `www.yourwebsite.com/cpanel` or in my case I need to do it through [bluehost](https://www.bluehost.com/web-hosting/cplogin?_ga=2.162882292.978560099.1595995215-457930475.1583097743). When you are logged go to cpanel and click on File Manager

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":187,"sizeSlug":"large"} -->

![cpanel]({{ site.baseurl }}/assets/images/2020/07/cpanel.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

**Step 2**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Click on public\_html and here is where you need to upload the files you are going to deploy with our React website. In your case maybe you already have 2 folders and 1 file:

<!-- /wp:paragraph -->

<!-- wp:list -->

- .well-known
- cgi-bin 
- .htaccess
- If you do, just leave them there.

<!-- /wp:list -->

<!-- wp:image {"align":"center","id":189,"sizeSlug":"large"} -->

![cpanel public_html directory.]({{ site.baseurl }}/assets/images/2020/07/directory-to-upload-react-app-1024x420.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

**Step 3**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

When you run it in your terminal `npm start ` you should see something like this:

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":191,"sizeSlug":"large"} -->

![run npm start]({{ site.baseurl }}/assets/images/2020/07/npm-start.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

As you can see it is tellling us that we are not running an optimized version.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**Step 4**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

In a terminal run `npm run build` and when it is done you should see that it created a new folder **build**

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":194,"sizeSlug":"large"} -->

![]({{ site.baseurl }}/assets/images/2020/07/build-directory-1024x764.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

**Step 5**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Finally we need to upload all the files in the **build** floder into our **public\_html**. In the cpanel make sure you are inside the folder **public\_html** and then click upload and select all the files inside your build folder.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":195,"sizeSlug":"large"} -->

![upload all the files inside the folder build.]({{ site.baseurl }}/assets/images/2020/07/upload-build-files-1024x561.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

When you finish uploading all the files, you can go to the browser and type your domain https://myamazingwebsite.com and you should see your React website.

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

<!-- /wp:paragraph -->

