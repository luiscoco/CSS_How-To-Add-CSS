# CSS: How to add CSS

When a browser reads a style sheet, it will format the HTML document according to the information in the style sheet.

Three Ways to Insert CSS

There are three ways of inserting a style sheet:

- **1. External CSS**

- **2. Internal CSS**

- **3. Inline CSS**

## 1. External CSS

With an external style sheet, you can change the look of an entire website by changing just one file!

Each HTML page must include a reference to the external style sheet file inside the <link> element, inside the head section.

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="mystyle.css">
  </head>
  <body>
    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

**style.css**

```css
body {
  background-color: lightblue;
}

h1 {
  color: navy;
  margin-left: 20px;
}
```

## 2. Internal CSS

An internal style sheet may be used if one single HTML page has a unique style.

The internal style is defined inside the <style> element, inside the head section.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
    body {
      background-color: linen;
    }
    
    h1 {
      color: maroon;
      margin-left: 40px;
    } 
    </style>
  </head>
  <body>
    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

## 3. Inline CSS

An inline style may be used to apply a unique style for a single element.

To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.

```html
<!DOCTYPE html>
<html>
  <body>
    <h1 style="color:blue;text-align:center;">This is a heading</h1>
    <p style="color:red;">This is a paragraph.</p>
  </body>
</html>
```

## 4. Multiple Style Sheets

If some properties have been defined for the same selector (element) in different style sheets, the **value from the last read style sheet will be used**. 

If the internal style is defined after the link to the external style sheet, the ```<h1>``` elements will be "orange":

```html
<!DOCTYPE html>
<html>
  <head>
  <link rel="stylesheet" type="text/css" href="mystyle.css">
    <style>
    h1 {
      color: orange;
    }
    </style>
  </head>
  <body>
    <h1>This is a heading</h1>
    <p>The style of this document is a combination of an external stylesheet, and internal style</p>
  </body>
</html>
```

## 5. Cascading Order

What style will be used when there is more than one style specified for an HTML element?

All the styles in a page will "cascade" into a new "virtual" style sheet by the following rules, where number one has the highest priority:

**Inline style (inside an HTML element)** MAYOR PRIORITY

**External and internal style sheets (in the head section)**

**Browser default**

So, an **inline style has the highest priority**, and will override external and internal styles and browser defaults.





