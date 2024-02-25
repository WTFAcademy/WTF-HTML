# WTF HTML minimalist tutorial: 2. Element

WTF HTML tutorial helps newcomers get started with HTML quickly.

**Twitter**: [@WTFAcademy_](https://twitter.com/WTFAcademy_) | [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy Community:** [Official website wtf.academy](https://wtf.academy) | [WTF Solidity Tutorial](https://github.com/AmazingAng/WTFSolidity) | [discord](https: //discord.gg/5akcruXrsk) | [WeChat group application](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

All codes and tutorials are open source on github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

After we understand the basic concepts of HTML, we will discuss the elements of HTML in depth.


## Attributes of elements

HTML elements can have attributes, which provide more information about the element or define certain behaviors of the element. Properties are always defined in the start tag, often using the form "property name = property value". For example, a link (`a`) element can use the `href` attribute to specify the target address of the link:

```html
<a href="https://www.example.com">Visit our website</a>
```

Effect in browser:

<a href="https://www.example.com">Visit our website</a>


In the above code, the value of the `href` attribute of the `a` element is `"https://www.example.com"`, which means that when the link is clicked, the browser will navigate to that URL.

Properties should contain:

1. A space between the attribute and the element name (or the previous attribute if there is more than one attribute).
2. The name of the attribute, followed by an equal sign.
3. The attribute value surrounded by quotation marks.

Commonly used properties:

1. `id`: Provide a unique identifier for the element.
2. `class`: Provide one or more class names for the element. Different elements can add the same class name.
3. `style`: Provides inline styles for elements.


## Nested elements

HTML elements can be nested within other elements. This means you can place another element or elements inside one element to create more complex content structures. For example, you might include one or more link elements inside a paragraph element:

```html
<p>My cat is <strong>very</strong> grumpy.</p>
```
Effect in browser:

<p>My cat is <strong>very</strong> grumpy.</p>

It is necessary to ensure that the nesting order of elements is correct: in this example, the `<p>` tag is used first, and then the `<strong>` tag, so the `<strong>` tag must be ended first, and then the `<p>` tag. This is not right:

```html
<p>My cat is <strong>very grumpy.</p></strong>
```

Effect in browser:

<p>My cat is <strong>very grumpy.</p></strong>

Therefore elements must start and end correctly to clearly show the correct nesting level. Otherwise the browser will have to guess on its own, and although it will try its best, it will most likely not give you the results you expect. So be sure to avoid it!

## Empty element

There are some elements in HTML that have no content and do not require closing tags. These are called empty elements. For example, the `<br>` tag inserts a line break, and the `<img>` tag is used to insert an image.

```html
<br>
<img src="image.jpg" alt="My Image">
```

## Block level elements

Block-level elements (Block-level Elements) are displayed in the form of blocks on the page and are often used as structural elements. Common block-level elements include: `<div>`, `<p>`, `<h1>`-`<h6>` and `<ul>`, etc. The characteristics of block-level elements are:

1. Own a line
2. The width and height of the element can be set
3. The default width is 100% of its parent container
4. Stacked with other block-level elements

```html
<div>I am div</div>
<div>I am also div</div>
```

Effect in browser:
<div>I am div</div>
<div>I am also div</div>


## Inline elements

Inline Elements do not start a new line; they flow within the text, taking up only the width required by the content they contain. Common inline elements include: `<span>`, `<a>` and `<img>`, etc. The characteristics of inline elements are:

1. Can be arranged on the same line as adjacent inline elements
2. The width and height of the element cannot be set.
3. The width of the element will be stretched by the content

```html
<span>I am span</span>
<span>I am also span</span>
```

Effect in browser:

<span>I am span</span>
<span>I am also span</span>


## Summary

In this lecture, we specifically analyzed the elements in HTML, including element attributes, nested elements, empty elements, block-level elements and inline elements.
