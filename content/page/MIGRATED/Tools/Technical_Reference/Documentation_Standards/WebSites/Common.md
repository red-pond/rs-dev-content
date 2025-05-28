---
title: Common Content
weight: 4
---

## Some Common Components of Pages

These days, there are many websites that allow you to create content (e.g. videos, tweets, spreadsheet, etc.) and embed it in your website. The git hosted web pages we use are written in markdown, but can recognize blocks of html like `<iframe>`, which are the most standard way to embed something. 

------
### Embedding a Video
#### With iframe
Since Jekyll sites support html, you can actually use html `<iframe>` to embed videos easily. The video I want to [embed](http://riverscapes.northarrowresearch.com/Technical_Reference/jekyll_toolbox.html#youtube-videos) is [https://www.youtube.com/watch?v=JFzYE_Cnjjw&feature=youtu.be](https://www.youtube.com/watch?v=JFzYE_Cnjjw&feature=youtu.be). 

Watch this [video](https://youtu.be/4UKe5BkzJEY) for how to embed a video.

<div class="responsive-embed">
	<iframe width="560" height="315" src="https://www.youtube.com/embed/4UKe5BkzJEY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>

Note using the `<div class="responsive-embed"> </div>` tags around your `<iframe>` will help center the iframe and adaptively scale it for differen screen sizes and devices:

Use:
``` html
<div class="responsive-embed">
	<iframe width="560" height="315" src="https://www.youtube.com/embed/4UKe5BkzJEY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>
```
Instead of:
``` html
	<iframe width="560" height="315" src="https://www.youtube.com/embed/4UKe5BkzJEY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
```
#### Markdown Alternative
However, for regular markdown there is still an option that includes a preview of the site (this is supported, for example in GitHub issue forums, whereas the iframe is not). It relies on the thumbnails that YouTube automatically generates for every youtube vide on its image server (`https://img.youtube.com/`; see [here](https://www.sitepoint.com/youtube-video-thumbnail-urls/) for more information on how YouTube does this). Thus, if you use the image markdown syntax (`![alt-text](imagepath)`) inside a regular markdown hyperlink (`[text](url)`) you can produce the illusion of an embedded youtube video (it is actually just an image that links to YouTube).

Use the following syntax and substitute in your YouTube video ID for `YTID`:
``` markdown
[![Alt-text](https://img.youtube.com/vi/YTID/0.jpg)](https://www.youtu.be/watch?v=YTID)
```
For example, using the above id of `4UKe5BkzJEY` for `YTID` would show up as: <br>
[![Alt-text](https://img.youtube.com/vi/4UKe5BkzJEY/0.jpg)](https://www.youtu.be/watch?v=4UKe5BkzJEY)

Note subsituting `1.jpg` for `0.jpg` switches to a thumbnail size. <br>
[![Alt-text](https://img.youtube.com/vi/4UKe5BkzJEY/1.jpg)](https://www.youtu.be/watch?v=4UKe5BkzJEY)

Finally, if you want to make the hyperlink open in a new tab, use:
``` markdown
[![Alt-text](https://img.youtube.com/vi/YTID/0.jpg)](https://www.youtu.be/watch?v=YTID){:target="_blank"}
```

------
### Embedding an Image
Of all the things to do in these markdown Git-hosted webpages, embedding an image is actually the most annoying and difficult (compared with WYSWYG web platforms like Weebly or Google Sites).  The reasons are it is not a drag and drop operation and you kind of need to know what you are doing. The steps are:
1. Get your image prepared.
2. Resize your image to desired size that it will appear on page (e.g. width of 300 pixels would be half width, 600 pixels would be fuller). You can use Photoshop or [Faststone Capture](http://www.faststone.org/FSCaptureDetail.htm) (for example).
3. It is best practice to then tinify (make smaller) your image using something like [TinyPng](https://tinypng.com/). These typically achieve 20 to 50% compression and help your images and whole page load faster.
4. Copy your image to the appropriate folder path (for BRAT, that is [`\docs\assets\images\`](https://github.com/Riverscapes/pyBRAT/tree/master/docs/assets/images) or subfolder and will be referred to by path as `"/images/"`)
5. Reference the image in your markdown page. This is done with following syntax for the [`BRAT_Logo-wGrayTxt.png`](https://github.com/Riverscapes/pyBRAT/blob/master/docs/assets/images/BRAT_Logo-wGrayTxt.png):

``` markdown
![BRAT_Logo-wGrayTxt](\assets\images\BRAT_Logo-wGrayTxt.png)
```

And will look like:

![BRAT_Logo-wGrayTxt](\assets\images\BRAT_Logo-wGrayTxt.png)

To make that image hyperlinkable (clickable), you enclose it in square brackets `[]` and then put hyperlink in `()` parentheses.  For example, to make image above clickable and linking to  [http://google.com](http://google.com)

``` markdown
[![BRAT_Logo-wGrayTxt](\assets\images\BRAT_Logo-wGrayTxt.png)](http://google.com)
```
In this video, I illustrate how to do steps 2-5 of this with a screen shot taken in Faststone Capture:

<div class="responsive-embed">
	<iframe width="560" height="315" src="https://www.youtube.com/embed/CucZ7tU0Amo" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>

------
### Adding a Button

The best places to look for examples of buttons is on the [styleguide template](https://riverscapes.github.io/TemplateDocs/styleguide.html) - and [corresponding markdown](https://github.com/Riverscapes/TemplateDocs/edit/master/styleguide.md) or to copy a button you like from an existing page. Buttons can be:
- Just text: <a class="hollow button" href="/">  Back to BRAT Home </a>
- Image and Text: <a class="hollow button" href="/"><img src="/images/favicons/favicon-16x16.png">  Back to BRAT Home </a>
- or Icon and Text: <a class="hollow button" href="/Documentation/Standards"><i class = "fa fa-check-square-o"></i> Back to ETAL Standards</a>

See [Icon Library](https://fontawesome.com/v4.7.0/icons/) for a list of icons that our Riverscapes recognize and you can use.  

The basic syntax for a button goes something like:
``` markdown
<a class="hollow button" href="/Documentation/Standards"><i class = "fa fa-check-square-o"></i> Back to ETAL Standards</a>
```

In the video below, we walk you through how to make your own button to navigate to a specific page on the website <a class="hollow button" href="/Documentation/Standards"><i class = "fa fa-check-square-o"></i> Back to ETAL Standards</a>  and an external URL (http://google.com) <a class="hollow button" href="/Documentation/Standards"><i class = "fa fa-google"></i> Take me Away to Google</a>. 

<div class="responsive-embed">
	<iframe width="560" height="315" src="https://www.youtube.com/embed/4kAN1dA819c" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>
------
### Embed a Slideshow

Its nice to be able to embed slideshows on a page:

<div class="responsive-embed">
	<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRQPbDbYvEaL9GXhS4QfhEBe0fwOq0XBZmBBSXZ5EJFOknRxkG1tdO2OVhuUC4TkSqQwMUF2aOQWSBs/embed?start=false&loop=false&delayms=3000" frameborder="0" width="550" height="450" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
</div>

This video walks you through how to:

<div class="responsive-embed">
	<iframe width="560" height="315" src="https://www.youtube.com/embed/oZHBn5DrY0k" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>

------
### Linking to a PDF

#### Providing a useful citation with links

There are many ways to provide a citation. This is the _least useful_:

- Macfarlane WW, Gilbert JT, Gilbert JD, Saunders WC, Hough-Snee N, Hafen C, Wheaton JM and Bennett SN. 2018. What are the Conditions of Riparian Ecosystems? Identifying Impaired Floodplain Ecosystems across the Western U.S. Using the Riparian Condition Assessment (RCA) Tool. Environmental Management. DOI: 10.1007/s00267-018-1061-2.

This is _better_ because it provides a link from the title to the Research Gate entry (which tracks statistics on reads and downlaods), and link from the DOI to the stable, pemenant URL:

- Macfarlane WW, Gilbert JT, Gilbert JD, Saunders WC, Hough-Snee N, Hafen C, Wheaton JM and Bennett SN. 2018. [What are the Conditions of Riparian Ecosystems? Identifying Impaired Floodplain Ecosystems across the Western U.S. Using the Riparian Condition Assessment (RCA) Tool](https://www.researchgate.net/publication/325098563_What_are_the_Conditions_of_Riparian_Ecosystems_Identifying_Impaired_Floodplain_Ecosystems_across_the_Western_US_Using_the_Riparian_Condition_Assessment_RCA_Tool). Environmental Management. DOI: [10.1007/s00267-018-1061-2](http://dx.doi.org/10.1007/s00267-018-1061-2).   

** This is our lab standard for citations ** -_link to ResearchGate through title, link to DOI through DOI._

If you need some help on how to upload your content to ResearchGate, see here:

<div class="responsive-embed">
	<iframe width="560" height="315" src="https://www.youtube.com/embed/PsTJfCI09SY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>




#### Hosting a PDF on AWS instead of ResearchGate

There are situations where its nice to provide a direct link to the PDF (e.g. slides in workshop or handout), that we don't want to post on ResearchGate. If we want to provide a link to a PDF that we hosted on AWS, here's an example:

- [PDF of my paper](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Workshops/BRAT/2018/Burnt/Macfarlane_et_al-2018-Environmental_Management.pdf)

The syntax for above is: `[PDF of my paper](https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Workshops/BRAT/2018/Burnt/Macfarlane_et_al-2018-Environmental_Management.pdf)`

The video (scroll down) shows how to upload to [AWS](http://aws.amazon.com) (easy). 

If I want to show a PDF icon next to above citation, to indicate there is a pdf, I can use my <i class="fa fa-file-pdf-o" aria-hidden="true"></i> pdf [icon](https://fontawesome.com/v4.7.0/icon/file-pdf-o) with `<i class="fa fa-file-pdf-o" aria-hidden="true"></i>`:

- <i class="fa fa-file-pdf-o" aria-hidden="true"></i> Macfarlane WW, Gilbert JT, Gilbert JD, Saunders WC, Hough-Snee N, Hafen C, Wheaton JM and Bennett SN. 2018.  [What are the Conditions of Riparian Ecosystems? Identifying Impaired Floodplain Ecosystems across the Western U.S. Using the Riparian Condition Assessment (RCA) Tool](https://www.researchgate.net/publication/325098563_What_are_the_Conditions_of_Riparian_Ecosystems_Identifying_Impaired_Floodplain_Ecosystems_across_the_Western_US_Using_the_Riparian_Condition_Assessment_RCA_Tool). Environmental Management. DOI: [10.1007/s00267-018-1061-2](http://dx.doi.org/10.1007/s00267-018-1061-2).

But, that doesn't allow me to click on PDF icon and get to it. To do this, I need to have a html `<a href="">` tag:

- <a href="https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Workshops/BRAT/2018/Burnt/Macfarlane_et_al-2018-Environmental_Management.pdf" ><i class="fa fa-file-pdf-o" aria-hidden="true"></i></a> Macfarlane WW, Gilbert JT, Gilbert JD, Saunders WC, Hough-Snee N, Hafen C, Wheaton JM and Bennett SN. 2018.  [What are the Conditions of Riparian Ecosystems? Identifying Impaired Floodplain Ecosystems across the Western U.S. Using the Riparian Condition Assessment (RCA) Tool](https://www.researchgate.net/publication/325098563_What_are_the_Conditions_of_Riparian_Ecosystems_Identifying_Impaired_Floodplain_Ecosystems_across_the_Western_US_Using_the_Riparian_Condition_Assessment_RCA_Tool). Environmental Management. DOI: [10.1007/s00267-018-1061-2](http://dx.doi.org/10.1007/s00267-018-1061-2).

This was done with `<a href="https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Workshops/BRAT/2018/Burnt/Macfarlane_et_al-2018-Environmental_Management.pdf" ><i class="fa fa-file-pdf-o" aria-hidden="true"></i></a>` and collapsing the PDF icon inside the hyperlink `<a>` tag.

##### Or a Button...

Finally, a button can be nice for the paper.

<a class="hollow button" href="https://s3-us-west-2.amazonaws.com/etalweb.joewheaton.org/Workshops/BRAT/2018/Burnt/Macfarlane_et_al-2018-Environmental_Management.pdf"><i class = "fa fa-file-pdf-o" ></i>  Download my PDF please!</a>


A long-winded video showing how you do all the above, plus the upload to AWS.

<div class="responsive-embed">
	<iframe width="560" height="315" src="https://www.youtube.com/embed/uRFkxY2d_ow" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>

-------

## Embed a Gist

If I have a GIST (e.g. [this one](https://gist.github.com/joewheaton/002acd9ea725f6d4a1bac38ee9a0dd50)), you can simply copy the embed code and paste it in. For example, this produces:
`<script src="https://gist.github.com/joewheaton/002acd9ea725f6d4a1bac38ee9a0dd50.js"></script>` this:


<script src="https://gist.github.com/joewheaton/002acd9ea725f6d4a1bac38ee9a0dd50.js"></script>

-----

## Add a Google Search Bar for your Site

If you want a Google Search Bar for your site, use Google's [Programmable Search Engine](https://programmablesearchengine.google.com/controlpanel/all). You have to Add your search engine, and in it tell it `what site() to search?` (e.g. for GCD it might be `gcd/riverscapes.net/*`) 

It then gives you some code (e.g.):
```
<script async src="https://cse.google.com/cse.js?cx=31c6cfa7b5dba45da">
</script>
<div class="gcse-search"></div>
```
that correspondes to a search bar:
<script async src="https://cse.google.com/cse.js?cx=31c6cfa7b5dba45da">
</script>
<div class="gcse-search"></div>

You can customize the look and feel as well. 

-----
## Add a DOI with Zenodo for your Website or Tool

[Zedondo](https://zenodo.org/) provides an easy way to make your website citeable, trackable and indexed. You can even make your contribution part of the [Riverscape Consortium Zeondo Community]()

1. Create a Zenodo account (preferably linked you your [ORCID](https://orcid.org))
2. Link your GitHub account in your profile.
3. Click on GitHub in your settings. You will have access to all your repositories. 
4. Flip the switch to enable Zenodo tracking of your repository. Do this before creating a release.
5. Create a release (once tracking, Zenodo will automatically download a .zip-ball of each new release and register a DOI.)
6. Get your badge!

For example, for the [Low-Tech PBR website](http://lowtechpbr.restoration.usu.edu), it generated this badge: [![DOI](https://zenodo.org/badge/156031626.svg)](https://zenodo.org/badge/latestdoi/156031626) and provided the following markdown:

```
[![DOI](https://zenodo.org/badge/156031626.svg)](https://zenodo.org/badge/latestdoi/156031626)
```

The Zeondo Entry also then provides a suggested citation!  We've been adding these to our site `footer.html`. For example for GCD we used:

```
<div class="float-left">
        To cite content from this site use:<br>  <a href="https://doi.org/10.5281/zenodo.7248344"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.7248344.svg" alt="DOI"></a>

</div>

<div class="float-right">
    The <a href="https://github.com/Riverscapes/GCD">GCD</a> <i class="fa fa-github" aria-hidden="true"></i> site is licensed under a <a href="https://github.com/Riverscapes/gcd/blob/master/LICENSE">GNU General Public License v3.0</a>,<br> and some specific content is licensed with
      <a href="http://creativecommons.org/licenses/by/4.0/" target="_blank">
        <img src="{{site.baseurl}}/assets/images/cc-watermarks-riverscapes_orig.png" alt="Picture">
    </a>
    <br>&nbsp;
</div>
```
<div class="float-left">
        To cite content from this site use:<br>  <a href="https://doi.org/10.5281/zenodo.7248344"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.7248344.svg" alt="DOI"></a>

</div>

<div class="float-right">
    The <a href="https://github.com/Riverscapes/GCD">GCD</a> <i class="fa fa-github" aria-hidden="true"></i> site is licensed under a <a href="https://github.com/Riverscapes/gcd/blob/master/LICENSE">GNU General Public License v3.0</a>,<br> and some specific content is licensed with
      <a href="http://creativecommons.org/licenses/by/4.0/" target="_blank">
        <img src="{{site.baseurl}}/assets/images/cc-watermarks-riverscapes_orig.png" alt="Picture">
    </a>
    <br>&nbsp;
</div>