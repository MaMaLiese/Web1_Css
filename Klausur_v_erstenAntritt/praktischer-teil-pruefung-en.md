# Exam Web Basics

Download the zip-file from Moodle and unpack it. In the zip-file you will find a given HTML files, CSS files, pictures and a screenshot. For this exam take a look at the screenshot. Your final website should look like the website on the screenshots. The following instructions should help you to get to the final result systematically. 

**Keep in Mind**: You can at HTML Elements and Attributes but can not reassemble or delete already given HTML Elements or delete text or uncomment text or add text. CSS should only be added to the given CSS File. Don't use JavaScript.

**Upload:**

Take the folder and make a zip encoded package and upload it to Moodle.

**Name of zip file:** WEB-Lastname-Firstname.zip

## Semantic Elements

1. Open `index.html` and take a look at all the div Elements and exchange them if possible with block elements which also have semantic meaning e.g.

```html
<!--Before -->
<div id="header"></div>
<!--After -->
<header id="header"></header>
```

## Navigation

1. Open `index.html` and take a look at the section with the list of links:

```html
<ul>
  <li><a href="\">Home</a></li>
  <li><a href="">Pictures</a></li>
</ul>
```

2. Create a Link for `Pictures` which links to the
   html file `cats.html` which is located in the folder contents

## Styles

1. Open `index.html` and create a link element in the header to the extern styles file `styles.css`

2. Open `cats.html` and create a link element in the header to the extern styles file `styles.css`

3. Open `styles.css` and apply following styles:
   Heading Elements, Paragraphs, Citations:

- Colors needed:
  - grey (Heading 3 and Paragraph)
  - lightslategray (Heading 2)
  - darkslategrey (Heading 1)
  - darkgrey (Citation)
- Font-family (please apply only to Heading Elements, Paragraphs and  Citations):
  - Helvetica
  - sans-serif

4. Apply the styles for the header. 
- (Tipps: `background: aquamarine` [Think about CSS-Box related styles, and `2px` wide `border` on the bottom of the element]).
5. Apply styles for navigation.
   - (Tipps: `background: grey`, List elements color: `white`, font size: `20px`, List Style: `none` )
6. List elements should change color when hovered to `aquamarine`.
7. Apply styles for the footer. 
   - (Tipps: `background: cornflowerblue`, text should be centered, [Think about CSS-Box related styles: `padding` of `1rem` applied only to top and bottom] )
8. Apply styles for comments. 
   - (Tipps: `background: aliceblue`, [Think about CSS-Box related styles (`border` - `2px`, `padding` - `.25rem`)])
9. Apply styles for boxes.
   - (Tipps: `background: lightgrey;`, [Think about CSS-Box related styles (`padding` - only on the left and the right side of the element - `1rem`)])

Tipps: 

<div class="page"/>

## Positioning

1. The navigation and main content should be displayed in a row. Use Flexbox or CSS-Grid to achieve this.

2. The articles and comments should be on top of each other. Use Flexbox or CSS-Grid to achieve this.

3. The three boxes should be in a row if there is enough space. If there is not enough space they should start a new row. Please use only Flexbox to achieve this.
   - Tipp: spacing (the gap) between the elements is `1rem`

4. Within a box the contents should be in a column. Align the picture in the center. (Tipp: Use the `align-self` property on the image element). Please use only Flexbox to achieve this.


## Javascript

Take a look at the following section:

```html
<section id="cookieblock">By using this website, you automatically accept that we use cookies.<button>Understood</button></section>
```

1. When the button "Understood" is clicked, a cookie with the name "CookieBlock" should be set to "Understood". The cookie should expire in 3 months.
    - (Tipp: you can use `onclick` attribute of the button element)
    - (Tipp: For setting the cookie, you can take a look here: https://www.w3schools.com/js/js_cookies.asp)
