
# Portfolio project 1

## Code institute: HTML and CSS

*author: James Glennon*

## About

The function of the site is to be a consise summary of the history of the RMS Titanic, from construction to its rediscovery.

## Features

The site includes a background image which covers the entire web page, which can be seen through the transparent elements of the page.

A navigation bar that links to the appropriate sections of the page/website.

A hero image that responds to browser size by cropping the image, rather that stretching or compressing it.

## Testing

HTML validated using the [W3C_HTML_Validator](https://validator.w3.org/#validate_by_input)

CSS validated using the [W3C_CSS_Validator(Jigsaw)](https://jigsaw.w3.org/css-validator/#validate_by_input)

### Browsers

### Bugs

#### Unexpected gap in background colour

A margin between the last paragraph element of the learn more section created a gap between the background colours of the main section and the footer, resulting in an uncovered line. After attempts to target this paragraph as a 'child of the h4 header with a paragraph sibling' proved unsuccessful,

    h4 > p ~ p

the footer was given a top margin of minus 2.0 rem to cover the gap.

#### Footer background colour

In order to split the footer into two horizontal divs, one for text references and the other for images, the divs were set to float. Doing this caused the background colour to no longer apply. To remedy this, a hidden paragraph was placed at the end of the footer with the property 'Clear'. The paragraph was given the id of 'signoff'

    <p id="signoff">

    #signoff {
    clear: both;
    text-align: center;
    visibility: hidden;
    }

#### Redundant CSS

After achieving the desired page layout/style, lines of CSS were commented out one at a time to confirm if they were necessary.

### Validator Testing

## Deployment

## Credits

### Media

The information was sourced from [Brittanica](https://www.britannica.com/), [History](https://www.history.co.uk/), and [Ultimate_Titanic](https://ultimatetitanic.com/).  
Referenced content is cited in the footer of the website.

The website background image was sourced from [Brittanica](https://www.britannica.com/topic/Titanic#/media/1/597128/163712)

Fonts were sourced from [google fonts](https://fonts.google.com/)

### Coding