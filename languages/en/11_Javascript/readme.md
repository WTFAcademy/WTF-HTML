# WTF HTML minimalist tutorial: 11. HTML and JavaScript

WTF HTML tutorial to help newcomers get started with HTML quickly.

**Twitter**: [@WTFAcademy_](https://twitter.com/WTFAcademy_) | [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy Community:** [Official website wtf.academy](https://wtf.academy) | [WTF Solidity Tutorial](https://github.com/AmazingAng/WTFSolidity) | [discord](https: //discord.gg/5akcruXrsk) | [WeChat group application](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

All codes and tutorials are open source on github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

JavaScript is a lightweight programming language often used along with HTML and CSS to create interactive websites. In this chapter, we will introduce how to use the `<script>` tag to insert JavaScript in HTML, the HTML DOM model, and how to use JavaScript to manipulate HTML elements.

## Insert JavaScript using the `<script>` tag

In HTML, we can insert JavaScript code using the `<script>` tag. The `<script>` tag can be placed in the `<head>` or `<body>` section of an HTML document. Usually, to avoid blocking the rendering of the page, we place the `<script>` tag at the end of the `<body>` tag.

Here's a simple example:

```html
<!DOCTYPE html>
<html>
<body>

<h2>HTML and JavaScript examples</h2>

<button onclick="displayDate()">Display date</button>

<script>
function displayDate() {
   document.getElementById("demo").innerHTML = Date();
}
</script>

</body>
</html>
```
In this example, when the user clicks the button, the JavaScript function `displayDate()` is executed, displaying the current date and time.

## HTML DOM model

DOM (Document Object Model) is a cross-platform and language-independent interface that allows programs and scripts to dynamically access and update the content, structure, and style of documents.

The HTML DOM is a standard object model and programming interface. It converts the HTML document into a tree structure, where each node is an object representing a part of the HTML document.

## Use JavaScript to manipulate HTML elements

JavaScript can access and change HTML elements through the HTML DOM. Here are some commonly used DOM methods:

- `document.getElementById(id)`: Returns a reference to the first object with the specified id.
- `document.getElementsByClassName(name)`: Returns a NodeList containing all elements with the specified class name.
- `document.getElementsByTagName(name)`: Returns a NodeList containing all elements with the specified tag name.
- `document.querySelector(cssQuery)`: Returns the first element in the document that matches the specified CSS selector.
- `document.querySelectorAll(cssQuery)`: Returns a NodeList of all elements in the document that match the specified CSS selector.

- These methods can be used to obtain HTML elements, which can then be modified using DOM properties and methods, such as changing the element's text content, attribute values, or styles.

For example, the following JavaScript code uses the `getElementById` method to obtain an element and modify the text content of the element:

```html
<!DOCTYPE html>
<html>
<body>

<h1 id="myHeading">Hello World!</h1>

<button onclick="changeText()">Click to change text</button>

<script>
function changeText() {
   var heading = document.getElementById("myHeading");
   heading.innerHTML = "Hello WTF!";
}
</script>

</body>
</html>
```

When the user clicks the button, the title on the page changes from "Hello World!" to "Hello WTF!".

## Summary

HTML and JavaScript are two technologies that work closely together. JavaScript provides the ability to operate HTML elements, while the HTML DOM model provides us with a standard way to represent and operate HTML documents. Mastering these two techniques can help you create more dynamic and interactive websites.
