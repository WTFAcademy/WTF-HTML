# WTF HTML minimalist tutorial: 12. HTML and CSS


**Twitter**: [@WTFAcademy_](https://twitter.com/WTFAcademy_) | [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy Community:** [Official website wtf.academy](https://wtf.academy) | [WTF Solidity Tutorial](https://github.com/AmazingAng/WTFSolidity) | [discord](https: //discord.gg/5akcruXrsk) | [WeChat group application](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

All codes and tutorials are open source on github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

CSS (Cascading Style Sheets) is a style sheet language used to describe the appearance and format of HTML or XML documents. In this chapter, we'll cover how to insert CSS in HTML using `<style>` and `<link>`, learn about CSS selectors and properties, and how to use CSS to lay out HTML elements.

## Insert CSS using `<style>` and `<link>`

In HTML, we can insert CSS using `<style>` and `<link>` tags. Use the `<style>` tag to write CSS code inside an HTML document, while the `<link>` tag is used to link to external CSS files.

Here is an example of a `<style>` tag:

```html
<!DOCTYPE html>
<html>
<head>
   <style>
     body {
       background-color: lightblue;
     }
     h1 {
       color: white;
       text-align: center;
     }
   </style>
</head>
<body>

<h1>Insert CSS using style tag</h1>

</body>
</html>
```

Here is an example of a `<link>` tag:

```html
<!DOCTYPE html>
<html>
<head>
   <link rel="stylesheet" href="styles.css">
</head>
<body>

<h1>Use the link tag to link to external CSS files</h1>

</body>
</html>
```

In this example, "styles.css" is the path to the external CSS file.

## CSS selectors and properties

CSS selectors are used to select HTML elements that you want to style. The most common selectors are element selectors, class selectors, ID selectors, attribute selectors, etc.

CSS properties define the style of an element. Each CSS declaration always contains a property and a value, separated by a colon `:`.

Here is an example of CSS selectors and properties:

```css
body {
   background-color: lightblue;
}
h1 {
   color: white;
   text-align: center;
}
```

In this example, "body" and "h1" are selectors, "background-color", "color" and "text-align" are attributes, and "lightblue", "white" and "center" are attribute values.

## Layout HTML elements using CSS

CSS provides a variety of layout methods, including fluid layout, positioning layout, flex layout, grid layout, etc. Here, we briefly introduce flow layout and positioning layout.

Fluid layout is the basic layout method of CSS. All elements are in a flowing state by default, flowing from top to bottom, from left to right, like water. The width and height of an element can be set using the CSS "width" and "height" properties.

Positioned layout uses the CSS "position" property, which positions elements to relative or absolute positions. The value of the "position" attribute can be "static", "relative", "absolute", or "fixed".

Here is an example of using positioning layout:

```html
<!DOCTYPE html>
<html>
<style>
div.relative {
   position: relative;
   width

: 400px;
   height: 200px;
   border: 3px solid #73AD21;
}

div.absolute {
   position: absolute;
   top: 80px;
   right: 0;
   width: 200px;
   height: 100px;
   border: 3px solid #73AD21;
}
</style>
<body>

<h2>Layout HTML elements using CSS</h2>

<div class="relative">
   <div class="absolute">This div element has position: absolute;</div>
</div>

</body>
</html>
```

In this example, the inner div element is positioned relative to the outer div element.

## Summary

HTML and CSS are the cornerstones of web development. By studying this chapter, you should have learned how to insert CSS into HTML and how to use CSS selectors, properties, and layout techniques. Mastering this knowledge will help you create web pages with better style and layout.
