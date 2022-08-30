
# Portfolio project 1

## Code institute: HTML and CSS
![Responsive design for the live site](assets/images/readme_images/responsive_design.png)
[Live website address](https://james-glennon.github.io/portfolio-project-one/)

*author: James Glennon*

## About

The function of the site is to be a consise summary of the history of the RMS Titanic, from construction to its rediscovery.

## Features

![Titanic seen through background](assets/images/readme_images/background.png)

The site includes a background image which covers the entire web page, which can be seen through the transparent elements of the page.

The page also has a fallback background colour similar to the image, to ensure the same colour contrast should the image fail to load.

![Navigation bar by default](assets/images/readme_images/nav-default.png)
![Navigation bar reacting to hover](assets/images/readme_images/nav-hover.png)

A navigation bar that links to the appropriate sections of the page/website.
The links respond to hover by changing colour and growing while hovered.

![Reference link superscript default appearence](assets/images/readme_images/ref-default.png)
![Reference link supercript hover response](assets/images/readme_images/ref-hover.png)

Superscript links that connect to media references relevent to that section of content.
These links respond to hover by swapping text and background colour.

![External references for media and images](assets/images/readme_images/footer-ref.png)

A list of references for text and image content used to create this page, including links to the external sites.
The links include aria labels and open in a new tab.

![Main page image at 1200px page width](assets/images/readme_images/hero-image1200px.png)
![Main page image at 600px page width](assets/images/readme_images/hero-image600px.png)

A hero image that responds to browser size by cropping the image, rather that stretching or compressing it.

![Google maps in an iframe embedded in the page](assets/images/readme_images/google-map.png)


A functional google maps page displaying the location of the Titanic Belfast museum.

## Testing

### Links

All internal links were tested and confirmed to focus on the correct parts of the page.

All external links were tested and confirmed to open in a new tab.

### Browsers

The live web address included in this read me file was tested on google chrome, microsoft edge, mozilla firefox and opera.

#### Google Chrome

The website was coded using chrome and chrome dev tools, including lighthouse. 

![Chrome lighthouse results for the website](assets/images/readme_images/chrome-lighthouse.png)

No known issues exclusive to Chrome (see bugs)

#### Microsoft Edge

![Edge scrolling past the "edges" of the page](assets/images/readme_images/edge-scroll.png)

The vertical scrolling of the page allows user to scroll "beyond" the page, revealing the fallback background colour.

#### Mozilla Firefox

![Navigation links appearing green in firefox](assets/images/readme_images/firefox_nav.png)

Links in the navigation bar appear to have a green font colour despite no CSS colour rule.

![Reference links having an unusual underline effect](assets/images/readme_images/firefox_ref.png)

Reference superscript appears with an unexpected underline effect much lower than expected.

#### Opera

No known issues exclusive to Opera.

### Bugs

#### Unexpected gap in background colour

A margin between the last paragraph element of the learn more section created a gap between the background colours of the main section and the footer, resulting in an uncovered line. After attempts to target this paragraph as a 'child of the h4 header with a paragraph sibling' proved unsuccessful,
```
    h4 > p ~ p
```
the footer was given a top margin of minus 2.0 rem to cover the gap.

#### Footer background colour

In order to split the footer into two horizontal divs, one for text references and the other for images, the divs were set to float. Doing this caused the background colour to no longer apply. To remedy this, a hidden paragraph was placed at the end of the footer with the property 'Clear'. The paragraph was given the id of 'signoff'
```
    <p id="signoff">

    #signoff {
    clear: both;
    text-align: center;
    visibility: hidden;
    }
```

#### Side by side image

In the voyage section are two images side by side in the same container div. The images would not fit flush with one another at 50% width, dispite all padding and margins reduced to zero and box-sizing set to border-box.
To remedy this, the images were given negative horizontal margins and greater width as to cover the whole width of the container.
```
    #menu, #astor {
    width: 51%;
    height: 88%;
    margin: 0 -1%;
    box-sizing: border-box;
    display: inline-block;
    border: #1288c2 4px solid;
    border-top: none ;
}
```
#### Footer Divs

The side by side footer divs acted unexpectedly, at less than 1200px width, after adding media queries for responsive design.

both divs would float to the right of the footer.

To remedy this, the width of the divs were increased and positioned vertically.

#### Resposive design beyond 1600px width

It was my desire to have the main element be a fixed 1495px width for screens larger than 1600px wide, and centered in the page.

```
    @media screen and (min-width: 1600px) {

    h1,
    h2,
    main,
    footer {
        width: 1495px;
        margin-left: auto;
    }
```

The above code proved ineffective, and so instead, the margin adjusted for breakpoint screen widths, rather than responding dynamically.

### Known unresolved bugs

#### Text escaping footer

![Reference text extending beyond footer border](assets/images/readme_images/footer-error.png)

At narrow screen sizes (~450px wide or less), text for image reference #11 extends beyond the sides of the footer.

I am uncertain how to address this, as image reference #13 remains in the footer, dispite having more text.

#### Incorrect aspect ratio of Map image

![Map image resulting in poor lighthouse score](assets/images/readme_images/map-error.png)

One of the factors contributing to the low "Best practices score" on google's lighthouse tool is an improperly proportioned map.

to fit an image into a container div, I used the object-fit attribute. 

I found the cover value hid important parts of the image, while contain revealed the background colour in an unattractive way.

I instead used the fill value, which results in the image stretching and squashing with no background exposed.

I would have liked to created a container div that would shrink/grow with page width while keeping aspect ratio, but I do not know how.


### Validator Testing

![W3C HTML validator result](assets/images/readme_images/html-val.png)

HTML validated using the [W3C_HTML_Validator](https://validator.w3.org/#validate_by_input)

![W3C CSS validator result](assets/images/readme_images/css-val.png)

CSS validated using the [W3C_CSS_Validator(Jigsaw)](https://jigsaw.w3.org/css-validator/#validate_by_input)

## Deployment

Code was written in [gitpod](https://www.gitpod.io/) and was incrementally saved and pushed to [github](https://github.com/) for version control.

The site was then hosted on [github pages](https://pages.github.com/)

## Credits

### Media

The information was sourced from [Britannica](https://www.britannica.com/), [History](https://www.history.co.uk/), [Ultimate Titanic](https://ultimatetitanic.com/), and [Wikipedia](https://en.wikipedia.org/wiki/John_Jacob_Astor_IV).

An additional image was sourced from [All that's interesting](https://allthatsinteresting.com/)

Referenced content is cited in the footer of the website.

The website background image was sourced from [Britannica](https://www.britannica.com/topic/Titanic#/media/1/597128/163712)

Fonts were sourced from [google fonts](https://fonts.google.com/)

### Coding

This read me document was structured based on the example provided in the code institute module for portfolio project one.

[Markdown Guide](https://www.markdownguide.org/) was used for markdown synthax for this readme file.

[The World Wide Web Consortium (W3C)](https://www.w3.org/) was used several times for html and css synthax.

[FreeConvert](https://www.freeconvert.com/image-converter) was used to convert images from .jpg to .webp format.

![embed link for google maps](assets/images/readme_images/gmap-embed.png)

The code for the iframe containing the map was provided by the [Google Maps](https://www.google.ie/maps/) website.

Google dev tools within the chrome browser where used during development to identify errors/issues.