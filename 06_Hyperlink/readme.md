# WTF HTML极简教程: 6. Hyperlink 超链接

WTF HTML教程，帮助新人快速入门HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_)  ｜ [@0xAA_Science](https://twitter.com/0xAA_Science) 

**WTF Academy社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.gg/5akcruXrsk) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

超链接是 HTML 中的一项基本功能，它可以链接到网页的其他部分，或者链接到其他网页，甚至是其他网站。在这一章节，我们将详细介绍如何在 HTML 中使用超链接。


## 创建超链接

超链接在 HTML 中主要通过 `<a>` 标签来创建。`<a>`标签内部一般包含一些文本或者图片，这些内容将成为链接的可点击部分。同时，我们通过`<a>`标签的 `href` 属性指定链接的目标地址。

```html
<a href="https://wtf.academy">访问 WTF Academy 的官网</a>
```

浏览器效果：

<a href="https://wtf.academy">访问 WTF Academy 的官网</a>

## 使用 `title` 属性添加支持信息

你可能要添加到你的链接的另一个属性是 title（标题）；这旨在包含关于链接的补充信息，例如页面包含什么样的信息或需要注意的事情。

```html
<a href="https://wtf.academy/" title="面向开发者的Web3开源学院。">访问 WTF Academy 的官网</a>
```

结果如下（当鼠标指针悬停在链接上时，标题将作为提示信息出现）：

<a href="https://wtf.academy/" title="面向开发者的Web3开源学院。">访问 WTF Academy 的官网</a>

> **Note**
>
> 链接的标题仅当鼠标悬停在其上时才会显示，这意味着使用键盘来导航网页的人很难获取到标题信息。如果标题信息对于页面非常重要，你应该使用所有用户能都方便获取的方式来呈现，例如放在常规文本中。

## 设置链接打开方式

有时，我们希望点击链接后在新的浏览器窗口或者标签页中打开，而不是在当前页面打开。这可以通过 `<a>` 标签的 `target` 属性来实现。如果我们希望链接在新的标签页打开，可以将 `target` 属性设置为 `_blank`。

例如：

```html
<a href="https://wtf.academy" target="_blank">访问 WTF Academy 的官网</a>
```

浏览器效果：

<a href="https://wtf.academy" target="_blank">访问 WTF Academy 的官网</a>

这个超链接点击后将在新的浏览器标签页中打开 WTF Academy 的官网。

## 锚点链接

在一个长的网页中，我们可能希望创建链接到页面内部某个部分的链接。这可以通过锚点链接来实现。首先，我们需要使用 `<a>` 标签的 `name` 或 `id` 属性来标记目标位置，然后在链接的 `href` 属性中使用 `#` 加上目标的 `name` 或 `id` 值来创建链接。

例如：

```html
<a name="section1"></a>
<!-- 一些内容 -->
<a href="#section1">跳转到 section1</a>
```

浏览器效果：

<a name="section1"></a>
<a href="#section1">跳转到 section1</a>


这个超链接点击后将会跳转到页面的 `section1` 部分。


## 邮箱链接

除了链接到其他网页，`<a>` 标签还可以链接到电子邮件地址。通过在 `href` 属性值前面添加 `mailto:`，可以创建一个点击后会启动用户默认的邮件客户端，并创建一封新邮件的链接。

例如：

```html
<a href="mailto:example@example.com">发送邮件到 example@example.com</a>
```

这个超链接点击后将启动用户的邮件客户端，并创建一封发送到 `example@example.com` 的新邮件。

## 下载链接

```html
<a href="https://wtf.academy/img/wtflogo.png" download="wtflogo">下载 WTFAcademy logo</a>
```

<a href="https://wtf.academy/img/wtflogo.png" download="wtflogo">下载 WTFAcademy logo</a>


## 总结

在这一章节中，我们介绍了如何在 HTML 中创建和使用超链接，包括普通链接、在新标签页打开的链接、邮箱链接和锚点链接。理解和掌握超链接是学习 HTML 的一个重要步骤，它能使你的网页和其他网页或者页面内部的其他部分相互连接。