# WTF HTML极简教程: 12. HTML和CSS


**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_) ｜ [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy 社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity 教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.wtf.academy) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在 github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

CSS (Cascading Style Sheets) 是一种样式表语言，用于描述 HTML 或 XML 文档的外观和格式。在本章中，我们将介绍如何在 HTML 中使用 `<style>` 和 `<link>` 插入 CSS，了解 CSS 的选择器和特性，以及如何使用 CSS 布局 HTML 元素。

## 使用 `<style>` 和 `<link>` 插入 CSS

在 HTML 中，我们可以使用 `<style>` 和 `<link>` 标签来插入 CSS。使用 `<style>` 标签，可以在 HTML 文档内部书写 CSS 代码，而 `<link>` 标签则用于链接到外部的 CSS 文件。

这是一个 `<style>` 标签的例子：

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

<h1>使用style标签插入CSS</h1>

</body>
</html>
```

这是一个 `<link>` 标签的例子：

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

<h1>使用link标签链接到外部CSS文件</h1>

</body>
</html>
```

在这个例子中，"styles.css" 是外部 CSS 文件的路径。

## CSS选择器和特性

CSS 选择器是用于选择想要给样式的 HTML 元素。最常见的选择器有元素选择器、类选择器、ID选择器、属性选择器等。

CSS 属性定义了元素的样式。每个 CSS 声明总是包含一个属性和一个值，属性和值之间用冒号 `:` 分隔。

这是一个 CSS 选择器和属性的例子：

```css
body {
  background-color: lightblue;
}
h1 {
  color: white;
  text-align: center;
}
```

在这个例子中，"body" 和 "h1" 是选择器，"background-color", "color" 和 "text-align" 是属性，"lightblue", "white" 和 "center" 是属性的值。

## 使用CSS布局HTML元素

CSS 提供了多种布局方式，包括流式布局、定位布局、flex布局、网格布局等。在这里，我们简单介绍一下流式布局和定位布局。

流式布局是 CSS 的基础布局方式，所有的元素默认都在一个流的状态中，从上至下，从左至右，像水一样流动。元素的宽度和高度可以通过 CSS 的 "width" 和 "height" 属性来设置。

定位布局使用 CSS 的 "position" 属性，它可以将元素定位到相对或绝对的位置。"position" 属性的值可以是 "static"、"relative"、"absolute" 或 "fixed"。

以下是一个使用定位布局的例子：

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

<h2>使用CSS布局HTML元素</h2>

<div class="relative">
  <div class="absolute">This div element has position: absolute;</div>
</div>

</body>
</html> 
```

在这个例子中，内部的 div 元素是相对于外部 div 元素进行定位的。

## 总结

HTML 和 CSS 是网页开发的基石。通过学习本章内容，你应该已经了解了如何在 HTML 中插入 CSS，以及如何使用 CSS 选择器、特性和布局技术。掌握这些知识，将有助于你创建更具样式和布局的网页。