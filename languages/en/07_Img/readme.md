# WTF HTML Minimalist Tutorial: 7. Pictures

WTF HTML tutorial to help newcomers get started with HTML quickly.

**Twitter**: [@WTFAcademy_](https://twitter.com/WTFAcademy_) | [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy Community:** [Official website wtf.academy](https://wtf.academy) | [WTF Solidity Tutorial](https://github.com/AmazingAng/WTFSolidity) | [discord](https: //discord.gg/5akcruXrsk) | [WeChat group application](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

All codes and tutorials are open source on github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

In web pages, pictures are a very important media type that can improve user experience and make information delivery more intuitive and vivid. This chapter explains how to embed and manipulate images in HTML.

## Insert picture

In HTML, we use the `<img>` tag to insert images. The `<img>` tag is a self-closing tag, which means it has no closing tag. The address of the image is specified through the `src` (source) attribute of the `<img>` tag.

For example:

```html
<img src="https://wtf.academy/img/wtflogo.png">
```

Browser effect:

<img src="https://wtf.academy/img/wtflogo.png">

## Set image properties

The `<img>` tag also has some other attributes that can be used to set the size of the image, alternative text, etc.

### Set image size

We can set the width and height of the image through the `width` and `height` attributes of the `<img>` tag. The values ​​of these two properties can be specific pixel values ​​or percentages.

For example:

```html
<img src="https://wtf.academy/img/wtflogo.png" width="200" height="100">
```

Browser effect:

<img src="https://wtf.academy/img/wtflogo.png" width="200" height="100">


This will set the image's width to 200 pixels and its height to 100 pixels.

It should be noted that if the width and height of the image are set at the same time, and the ratio of these two values ​​​​is inconsistent with the ratio of the image itself, the image may be stretched or compressed, causing deformation. Therefore, when setting the image size, we generally only set one of the width or height, and keep the other automatic.

### Set alternative text

Alt text is used to display when an image cannot be loaded. It is also used by screen readers to read the content of the image to help the visually impaired understand the image. We set the alternative text through the `alt` attribute of the `<img>` tag.

For example:

```html
<img src="https://www.example.com/path/to/image.jpg" alt="A description of the image">
```

Browser effect:

<img src="https://www.example.com/path/to/image.jpg" alt="A description of the image">


If the image fails to load, "A description of the image" will appear on the page.


### image link

Images can also be used as hyperlinks. We only need to put the `<img>` tag inside the `<a>` tag to create an image link.

```html
<a href="https://wtf.academy/">
   <img src="https://wtf.academy/img/wtflogo.png" alt="WTFAcademy logo" />
</a>
```

Browser effect:

<a href="https://wtf.academy/">
   <img src="https://wtf.academy/img/wtflogo.png" alt="WTFAcademy logo" />
</a>

## Summary

In this chapter, we introduced how to insert images in HTML and how to set the image's properties, including size and alt text. We also covered how to create image links. By learning these things, you can now freely use images in your web pages.
