# CSS Exercises

- CAUTION: You can not simply copy and paste all the coding examples. Consider what you are doing and choose the right place for your code in your document. Three dots '...' might suggest that there is code above or below this example!

## Demo 1: CSS Essentials 1

1. Make a new html file, `index.html.`
2. Copy the following HTML code
   ```html
   <!DOCTYPE html>
    <html>
      <head>
          <meta charset="utf-8">
      </head>
      <body>
          <h1>Der Erlkönig</h1>
          <p>Johann Wolfgang von Goethe</p>
          <p>1782 - Ballade</p>
          <div id="content">
              <p class="paragraph">
                  Wer reitet so sp&auml;t durch Nacht und Wind?<br>
                  Es ist der Vater mit seinem Kind;<br>
                  Er hat den Knaben wohl in dem Arm,<br>
                  Er fa&szlig;t ihn sicher, er h&auml;lt ihn warm.<br>
              </p>
              <p class="paragraph">
                  Mein Sohn, was birgst du so bang dein Gesicht? -<br>
                  Siehst Vater, du den Erlk&ouml;nig nicht?<br>
                  Den Erlenk&ouml;nig mit Kron und Schweif? -<br>
                  Mein Sohn, es ist ein Nebelstreif. -<br>
              </p>
              <p class="paragraph">
                  &quot;Du liebes Kind, komm, geh mit mir!<br>
                  Gar sch&ouml;ne Spiele spiel ich mit dir;<br>
                  Manch bunte Blumen sind an dem Strand,<br>
                  Meine Mutter hat manch g&uuml;lden Gewand.&quot;<br>
              </p>
              <p class="paragraph">
                  Mein Vater, mein Vater, und h&ouml;rest du nicht,<br>
                  Was Erlenk&ouml;nig mir leise verspricht? -<br>
                  Sei ruhig, bleibe ruhig, mein Kind;<br>
                  In d&uuml;rren Bl&auml;ttern s&auml;uselt der Wind. -<br>
              </p>
              <p class="paragraph">
                  &quot;Willst, feiner Knabe, du mit mir gehn?<br>
                  Meine T&ouml;chter sollen dich warten sch&ouml;n;<br>
                  Meine T&ouml;chter f&uuml;hren den n&auml;chtlichen Reihn<br>
                  Und wiegen und tanzen und singen dich ein.&quot;<br>
              </p>
              <p class="paragraph">
                  Mein Vater, mein Vater, und siehst du nicht dort<br>
                  Erlk&ouml;nigs T&ouml;chter am d&uuml;stern Ort? -<br>
                  Mein Sohn, mein Sohn, ich seh es genau:<br>
                  Es scheinen die alten Weiden so grau. -<br>
              </p>
              <p class="paragraph">
                  &quot;Ich liebe dich, mich reizt deine sch&ouml;ne Gestalt;<br>
                  Und bist du nicht willig, so brauch ich Gewalt.&quot;<br>
                  Mein Vater, mein Vater, jetzt fa&szlig;t er mich an!<br>
                  Erlk&ouml;nig hat mir ein Leids getan! -<br>
              </p>
              <p class="paragraph">
                  Dem Vater grauset's, er reitet geschwind,<br>
                  Er h&auml;lt in den Armen das &auml;chzende Kind,<br>
                  Erreicht den Hof mit M&uuml;he und Not;<br>
                  In seinen Armen das Kind war tot.</p>
              </p>
          </div>
      </body>
   </html>
   ```
3. Within the head tag, create a style tag that will hold your styles for the document. You can comment in CSS starting with `/*` and ending with `*/`. Those comments can also have multiple lines.

```html
...
<style>
  /* Styles go here */
</style>
...
```

4. Create a type selector for `h1` and give it the color green

```css
h1 {
  color: green;
}
```

5. Create a class selector called `paragraph` the according attributes are already set in your HTML code.

```css
.paragraph {
  font-size: 14px;
}
```

6. Create a id selector for the content. The content should be displayed in the center of the document.

```css
#content {
  text-align: center;
}
```

7. You can give multiple paragraphs the same style by separating them with a comma `,`

```css
#content,
.paragraph {
  color: grey;
}
```

8. Let's try out the child combinator. All the paragraphs that are directed child's body should have a bigger font size. Notice that the sections within the content div will not be affected.

```css
body > p {
  font-size: 20px;
}
```

9. All the paragraphs should have a different color if your hover the mouse over a paragraph in the content section. This can be achieved by using a descendant combinator and a pseudo-class

```css
#content .paragraph:hover {
  color: red;
}
```

10. The first paragraph of the div content should have a different color. This can be achieved by using structural pseudo classes

```css
.paragraph:first-child {
  color: blue;
}
```

## Demo 2: CSS Essentials 2

1. There are a few possibilities to integrate your CSS into your HTML document. In the first example, we examined how we can use the **head element** of our document to create a document-wide valid CSS.
2. The second option is to use **inline styles**. Inline styles are valid for one element and can hold one or more style declarations. It is known to be bad practice to use inline styles.

```html
<h1 style="color: purple;">Der Erlkönig</h1>
```

3. The last option is a **separate file** to manage our CSS styles. This file represents a central place to work your styles and can be used throughout your website.
4. Create a new file called `styles.css`.
5. Copy and paste all the styles currently in your head element to your `styles.css` file.
6. Replace the style element with a link element that is pointing to your `styles.css` file.

```html
<link rel="stylesheet" href="styles.css" />
```

4. Open your document in the browser and check out if all the styles are still working

## Demo 3: cascading styles

In this demo, we want to explore which styles come first (are preferred).

1. Let's start with a fresh document. Create a new file and name it `cascading.html`.
2. Copy and paste the HTML from the first step in `Demo 1`.
3. Add the following CSS code to your document.

```html
<style>
  body {
    color: blue;
  }

  p {
    color: black;
  }

  .paragraph {
    color: gray;
  }
</style>
```

4. Open the file in the browser and find out which styles are applied.
5. Add the following inline styles

```html
...
<p style="font-size: 0.8em; color: lightgrey; ">1782 - Ballade</p>
...
<div id="content">
  <p class="paragraph" style="color: red;">
    ...
  </p>
</div>
```

6. Open the file in the browser and determine which styles are applied.
7. Add `!important to the color of the paragraph

```css
.paragraph {
  color: gray !important;
}
```

8. Open the file in the browser. What has changed?
