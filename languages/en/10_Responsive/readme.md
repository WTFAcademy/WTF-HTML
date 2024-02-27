# WTF HTML minimalist tutorial: 10. Responsive design and mobile HTML

WTF HTML tutorial to help newcomers get started with HTML quickly.

**Twitter**: [@WTFAcademy_](https://twitter.com/WTFAcademy_) | [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy Community:** [Official website wtf.academy](https://wtf.academy) | [WTF Solidity Tutorial](https://github.com/AmazingAng/WTFSolidity) | [discord](https: //discord.gg/5akcruXrsk) | [WeChat group application](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

All codes and tutorials are open source on github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

Responsive design is a method for website design to be optimized for different devices and screen sizes so that the website can provide a good user experience on any device. The core of this design approach includes viewports, device-independent pixels, media queries, and responsive design for images and tables.

## Viewport and device-independent pixels

The view window is the area of ​​a web page that users can see in the browser. On mobile devices, the width of the view window is usually equal to the physical screen width of the device.

To create a consistent layout across all devices, we need to use device-independent pixels. A device-independent pixel is a virtual pixel unit used to provide a consistent layout across different devices, rather than relying on the actual physical pixels of the device.

In HTML, you can set the width and initial zoom level of the view window using the `<meta>` tag:

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

## Media Inquiries

Media queries are a part of CSS3 that allow content to respond to different device or viewport conditions. For example, you can use media queries to apply different styles on small and large screen devices:

```css
/* Styles to apply on devices with width less than 600px */
@media only screen and (max-width: 600px) {
   body {
     background-color: lightblue;
  }
}
```

## Responsive design for images and tables

For images, you can use the CSS `max-width` property to ensure that the image does not exceed the width of its container:

```css
img {
   max-width: 100%;
   height: auto;
}
```

For tables, approaches to responsive design vary. A common approach is to convert the table into a list of key-value pairs on small screen devices:

```css
@media only screen and (max-width: 600px) {
  td:before {
    content: attr(data-label);
    float: left;
    text-transform: uppercase;
    font-weight: bold;
  }
}
```

In the CSS above, `attr(data-label)` will replace the content before each `td` element with the value of its `data-label` attribute.

## Summary

Responsive design and mobile HTML are important parts of modern web development. By understanding and using view windows, device-independent pixels, media queries, and responsive design for images and tables, you can create websites that provide a great user experience on any device and screen size.
