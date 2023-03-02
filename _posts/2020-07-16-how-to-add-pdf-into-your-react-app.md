---
layout: post
title: How to add PDF into your React app.
date: 2020-07-16 14:52:21.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- REACT
- Tutorial
tags:
- embed
- pdf
- REACT
- render
meta:
  _thumbnail_id: '161'
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/how-to-add-pdf-into-your-react-app/"
excerpt: Hola! So as you know or maybe not I graduated from Flatiron School Software
  Engineer program. That means that I am applying to a lot of jobs, I would like to
  say that I'm sending at least 5 resumes per day (some days even more and others
  days less. We are in 2020 and we still need to send our resume in PDF format (most
  likely).
---
<!-- wp:paragraph -->

Hola! So as you know ~~or maybe not~~ that I graduated from the Flatiron School Software Engineering program. That means that I am applying to a lot of jobs, I would like to say that I'm sending at least 5 resumes per day (some days even more ~~and others days less~~ ). We are in 2020 but we still need to send our resume in PDF format (most likely).

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/l0EwYNj4E0dEe1sD6" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/new-girl-fox-new-girl-l0EwYNj4E0dEe1sD6)

<!-- /wp:html -->

<!-- wp:paragraph -->

That made me think that...

<!-- /wp:paragraph -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/DfSXiR60W9MVq" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/alan-DfSXiR60W9MVq)

<!-- /wp:html -->

<!-- wp:paragraph -->

...most likely someone already had this problem before. So I started looking for a way how to embed my resume into my [personal website](https://josedromero.com), (FYI: I made my website with REACT and \<3 )

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

After typing the words <q>embed pdf to react</q> into google literally the first result that came was [React-PDF](https://projects.wojtekmaj.pl/react-pdf/)

<!-- /wp:paragraph -->

<!-- wp:image {"id":145,"sizeSlug":"large"} -->

![Tutorial install react-pdf by José Romero]({{ site.baseurl }}/assets/images/2020/07/react-pdf.png "Google result of "embed pdf to react"")

<!-- /wp:image -->

<!-- wp:paragraph -->

So when is time to "send" my resume to any recruiter I just would need to add a link to my resume on my site. This way I'm directing them to my website where they are just a click away to see my portfolio, skill set, and most important they are seeing my work already live.

<!-- /wp:paragraph -->

<!-- wp:separator -->

* * *
<!-- /wp:separator -->

<!-- wp:paragraph -->

Now here is how to install React-PDF. (I'm assuming that you already a React app to work on)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**Step 1**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

To install just type this in your terminal: `npm install react-pdf`

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

**Step 2**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

I created a new component Resume where I want to embed my resume. As you can see in the gif my resume component only has the word Resume.

<!-- /wp:paragraph -->

<!-- wp:image {"id":147,"sizeSlug":"full"} -->

![José Romero website, San Ignacio Paraguay]({{ site.baseurl }}/assets/images/2020/07/Jose-Romero-website-react-app.gif)

<!-- /wp:image -->

<!-- wp:paragraph -->

This is my starting code:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import React from 'react'
import {Container, Header, Grid,} from 'semantic-ui-react'

const Resume = () => {
  return(
    <Container fluid>
      <Grid stackable>
        <Grid.Row>
          <Grid.Column width={16}>
            <Header className='header' as='h1'>Résumé</Header>
          </Grid.Column>
        </Grid.Row>
      </Grid>
    </Container>

  )
}
 export default Resume
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Now to be able to render the PDF, react-pdf we need to import the components Document and Page from react-pdf

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import { Document, Page } from 'react-pdf'
```

<!-- /wp:code -->

<!-- wp:paragraph -->

**Step 3**

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Importing our pdf file. In my case my file is located inside the assets folder as you can see in the image.

<!-- /wp:paragraph -->

<!-- wp:image {"id":154,"sizeSlug":"large"} -->

![José Romero Résumé]({{ site.baseurl }}/assets/images/2020/07/Jose-Romero-resume-location.png)

<!-- /wp:image -->

<!-- wp:code -->

```
import JRResume from '../assets/Jose Romero - Resume.pdf'
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Now we need to show our Document component. To do that we need to add the code:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
<Document file={JRResume}> //Document has a prop file and we pass our document in this case JRResume
   <Page pageNumber={1} />
</Document>
```

<!-- /wp:code -->

<!-- wp:paragraph -->

This way does not work. It is going to show you this message instead of the pdf.

<!-- /wp:paragraph -->

<!-- wp:image {"id":155,"sizeSlug":"large"} -->

![Failed to load resume - react-pdf]({{ site.baseurl }}/assets/images/2020/07/Failed-to-load-resume-1024x284.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

This is because we need to enable the PDF.js worker. We need to import the Document from a different path as you can see next:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import { Document } from 'react-pdf/dist/entry.webpack';
import { Page } from 'react-pdf'
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Using PDF.js worker is the key for performance. This allows it to render the pdf file in a different thread so our app can keep rendering without any issues.

<!-- /wp:paragraph -->

<!-- wp:image {"id":156,"sizeSlug":"large"} -->

![José Romero, San Ignacio Paraguay - Résumé.]({{ site.baseurl }}/assets/images/2020/07/Jose-Romero-resume-react-pdf-1024x829.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Final code:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
import React from 'react'
import {Container, Header, Grid,} from 'semantic-ui-react'
import { Document } from 'react-pdf/dist/entry.webpack';
import { Page } from 'react-pdf'
import JRResume from '../assets/Jose Romero - Resume.pdf'

const Resume = () => {
  return(
    <Container fluid>
      <Grid stackable>
        <Grid.Row>
          <Grid.Column width={4}>
          </Grid.Column>
          <Grid.Column width={8}>
            <Header className='header' as='h1'>Résumé</Header>
            <Document file={JRResume}>
              <Page pageNumber={1} />
            </Document>
          </Grid.Column>
          <Grid.Column width={4}>
          </Grid.Column>            
        </Grid.Row>
      </Grid>
    </Container>

  )
}
 export default Resume
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Please let me know in the comments if you had any problems or if you make it work!

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Link to the repository: [https://github.com/jdromero88/personal-website](https://github.com/jdromero88/personal-website).

<!-- /wp:paragraph -->

<!-- wp:separator -->

* * *
<!-- /wp:separator -->

<!-- wp:paragraph -->

Resources:

<!-- /wp:paragraph -->

<!-- wp:list -->

- [https://react-pdf.org/](https://projects.wojtekmaj.pl/react-pdf/)

<!-- /wp:list -->

<!-- wp:paragraph -->

<!-- /wp:paragraph -->

