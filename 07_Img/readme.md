# WTF HTML 极简教程: 7. 图片

WTF HTML 教程，帮助新人快速入门 HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_) ｜ [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy 社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity 教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.gg/5akcruXrsk) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在 github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

在网页中，图片是一种非常重要的媒体类型，能够提升用户体验，使信息传递更为直观和生动。本章节将介绍如何在 HTML 中嵌入和处理图片。

## 插入图片

在 HTML 中，我们使用 `<img>` 标签来插入图片。`<img>` 标签是自闭合标签，也就是说它没有结束标签。图片的地址通过 `<img>` 标签的 `src`（source）属性指定。

例如：

```html
<img src="https://wtf.academy/img/wtflogo.png">
```

浏览器效果：

<img src="https://wtf.academy/img/wtflogo.png">

## 设置图片属性

`<img>` 标签还有一些其他的属性，可以用来设置图片的大小、替代文本等。

### 设置图片大小

我们可以通过 `<img>` 标签的 `width` 和 `height` 属性来设置图片的宽度和高度。这两个属性的值可以是具体的像素值，也可以是百分比。

例如：

```html
<img src="https://wtf.academy/img/wtflogo.png" width="200" height="100">
```

浏览器效果：

<img src="https://wtf.academy/img/wtflogo.png" width="200" height="100">


这将会设置图片的宽度为 200 像素，高度为 100 像素。

需要注意的是，如果同时设置了图片的宽度和高度，而这两个值的比例与图片本身的比例不一致，那么图片可能会被拉伸或压缩，造成形变。因此，在设置图片大小的时候，我们一般只设置宽度或者高度中的一个，另一个保持自动。

### 设置替代文本

替代文本（alt text）用来在图片无法加载的时候显示，也被屏幕阅读器用来读出图片的内容，帮助视力障碍者理解图片。我们通过 `<img>` 标签的 `alt` 属性来设置替代文本。

例如：

```html
<img src="https://www.example.com/path/to/image.jpg" alt="A description of the image">
```

浏览器效果：

<img src="https://www.example.com/path/to/image.jpg" alt="A description of the image">


如果图片无法加载，那么页面上将显示 "A description of the image"。


### 图片链接

图片也可以被用作超链接。我们只需要把 `<img>` 标签放在 `<a>` 标签内部，就可以创建一个图片链接。

```html
<a href="https://wtf.academy/">
  <img src="https://wtf.academy/img/wtflogo.png" alt="WTFAcademy logo" />
</a>
```

浏览器效果：

<a href="https://wtf.academy/">
  <img src="https://wtf.academy/img/wtflogo.png" alt="WTFAcademy logo" />
</a>

## 总结

在这一章节中，我们介绍了如何在 HTML 中插入图片，以及如何设置图片的属性，包括大小和替代文本。我们还讲解了如何创建图片链接。通过学习这些内容，你已经可以在你的网页中自由地使用图片了。