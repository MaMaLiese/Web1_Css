# CSS Grid Exercises

For this exercises you need to install Visual Studio Code 'https://code.visualstudio.com/' which is a free IDE.
After you installed Visual Studio Code, to make your live easier, you can go to activate 'Auto Save' at `File > Auto save`.

- CAUTION: You can not simple copy and past all of the coding examples. Think about what you are doing and choose the right place for your code in your document. Three dots '...' might suggest that there is code above or below this example!

## Demo 1: CSS Grid Essentials 1

1. Make a new html file `index.html`
2. Copy the following HTML code
   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <style>
         .container {
           display: grid;
           color: #f6f3f3;
           font-family: sans-serif;
           font-weight: 400;
           padding: 10px;
         }
         header {
           background-color: #b53d2c;
         }
         article {
           background-color: #f8ab0b;
         }
         aside {
           background-color: #57d6cc;
         }
         footer {
           background-color: #10518c;
         }
       </style>
     </head>
     <body>
       <div class="container">
         <header>Header</header>
         <article>Article</article>
         <aside>Aside</aside>
         <footer>Footer</footer>
       </div>
     </body>
   </html>
   ```
3. Activate the grid layout by adding the followin CSS

```css
...
  .container {
    display: grid;
    ...
  }
...
```

4. Make four vertical lines of grid items (grid columns) e.g.:

```css
...
  .container {
    ...
    grid-template-columns:10% 100px auto 25%;
    ...
  }
...
```

4. Try out horizontal lines of grid items grid rows e.g.:

```css
...
  .container {
    ...
    grid-template-columns: auto 25%;
    grid-template-rows:25% 100px;
    ...
  }
...
```

5. Use the `justify-content` property to align the whole grid inside the container. Try out the property `space-between` which will give the columns equal amount of space between them. Try out the property `space-around` which will give the columns equal amount of space around them. Try out the property `space-evenly` which will give the columns equal amount of space between and around them. Try out the property `center` which will align the grid in the middle of the container. Try out the property `start` which will align the grid in the beginning of the container. Try out the property `end` which will align the grid in the end of the container. E.g.:

```css
...
  .container {
    ...
    grid-template-columns: auto 25%;
    grid-template-rows:25% 100px;
    justify-content: space-evenly;
    ...
  }
...
```

6. Comment out the `justify-content` property for now

```css
...
  .container {
    ...
    /*justify-content: space-evenly;*/
    ...
  }
...
```

7. Use the `align-content` property to vertically align the whole grid inside the container. The height of the total grid height needs to be less than the container's height in order for the align-content property to work. Try out the properties `center`, `start`, `end`, `space-between`, `space-around`and `space-evenly` E.g.:

```css
...
  .container {
    ...
        grid-template-columns: 100px 100px;
        grid-template-rows: 100px 100px;
        height: 400px;
        align-items: center;
    ...
  }
...
```

8. Comment out the `align-content` property for now

```css
...
  .container {
    ...
    /*align-content: center;*/
    ...
  }
...
```

9. Define custom grid areas in the parent element

```css
  .container {
    ...
      grid-template-columns: 25% auto 25%;
      grid-template-rows: 25% 100px auto;
      grid-template-areas:
        "header  header  aside"
        "article article aside"
        ".       footer  footer";
  }
```

10. Use the defined areas for the grid items

```css
header {
  background-color: #b53d2c;
  grid-area: header;
}
article {
  background-color: #f8ab0b;
  grid-area: article;
}
aside {
  background-color: #57d6cc;
  grid-area: aside;
}
footer {
  background-color: #10518c;
  grid-area: footer;
}
```

11. Add a horizontal gap between the grid items

```css
...
  .container {
    ...
    grid-column-gap:10px;
    ...
  }
...
```

12. Add a vertical gap between the grid items

```css
...
  .container {
    ...
    grid-row-gap:10px;
    ...
  }
...
```

13. Comment out `grid-row-gap` and `grid-column-gap` and use `grid-gap`

```css
...
  .container {
    ...
     /*grid-column-gap: 10px;
        grid-row-gap: 10px;*/
     grid-gap: 10px;
    ...
  }
...
```

## Demo 2: CSS Grid Essentials 2

1. Make a new html file `index.html`
2. Copy the following HTML code
   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <style>
         .container {
           display: grid;
           color: #f6f3f3;
           font-family: sans-serif;
           font-weight: 400;
           padding: 10px;
         }
         header {
           background-color: #b53d2c;
         }
         article {
           background-color: #f8ab0b;
         }
         aside {
           background-color: #57d6cc;
         }
         footer {
           background-color: #10518c;
         }
       </style>
     </head>
     <body>
       <div class="container">
         <header>Header</header>
         <article>Article</article>
         <aside>Aside</aside>
         <footer>Footer</footer>
       </div>
     </body>
   </html>
   ```
3. Activate the grid layout by adding the followin CSS

```css
...
  .container {
    display: grid;
    min-height: 300px;
    grid-template-columns: 20% 30% 30% 20%;
    grid-template-rows: 200px 100px 200px;
    ...
  }
...
```

4. Try out start-column and end-column. E.g.:

```css
...
header {
  grid-column-start: 2;
  grid-column-end: 4;
}
article {
  grid-column-start: 1;
  grid-column-end: 2;
}
footer {
  grid-column-start: 4;
  grid-column-end: 5;
}

...
```

5. Try out `justify-self`. Vertical alignment within a grid-item. Try out properties `center`, `start`, `end`and `stretch`.

```css
...
aside {
  justify-self: center;
}
...
```

5. Try out `align-self`. Horizontal alignment within a grid-item. Try out properties `center`, `start`, `end`and `stretch`.

```css
...
aside {
  align-self:end;
}
...
```
