# WTF HTML极简教程: 2. Element

WTF HTML教程，帮助新人快速入门HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_)  ｜ [@0xAA_Science](https://twitter.com/0xAA_Science) 

**WTF Academy社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.wtf.academy) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

在我们了解了HTML的基础概念后，我们将深入讨论HTML的元素。


## 元素的属性

HTML 元素可以拥有属性（Attribute），它们提供了有关元素的更多信息，或者定义了元素的某些行为。属性总是在开始标签中定义，常常使用 "属性名=属性值" 的形式出现。例如，链接（`a`）元素可以使用 `href` 属性指定链接的目标地址：

```html
<a href="https://www.example.com">Visit our website</a>
```

浏览器中效果：

<a href="https://www.example.com">Visit our website</a>


在上述代码中，`a` 元素的 `href` 属性的值为 `"https://www.example.com"`，这意味着当点击该链接时，浏览器将导航到该 URL。

属性应该包含：

1. 在属性与元素名称（或上一个属性，如果有超过一个属性的话）之间的空格符。
2. 属性的名称，并接上一个等号。
3. 由引号所包围的属性值。

常用的属性：

1. `id`:为元素提供一个唯一标识符。
2. `class`：为元素提供一个或多个类名，不同的元素可以添加相同的类名。
3. `style`:为元素提供内联样式。


## 嵌套元素

HTML 元素可以嵌套在其他元素中。这意味着你可以在一个元素内部放置另一个或多个元素，以创建更复杂的内容结构。例如，你可能会在一个段落元素内部包含一个或多个链接元素：

```html
<p>My cat is <strong>very</strong> grumpy.</p>
```
浏览器中效果:

<p>My cat is <strong>very</strong> grumpy.</p>

必须保证元素嵌套次序正确：本例首先使用`<p>`标签，然后是`<strong>`标签，因此要先结束`<strong>`标签，最后再结束`<p>`标签。这样是不对的：

```html
<p>My cat is <strong>very grumpy.</p></strong>
```

浏览器中效果:

<p>My cat is <strong>very grumpy.</p></strong>

因此元素必须正确地开始和结束，才能清楚地显示出正确的嵌套层次。否则浏览器就得自己猜测，虽然它会竭尽全力，但很大程度不会给你期望的结果。所以一定要避免！

## 空元素

HTML 中有一些元素没有内容，也不需要结束标签，这些被称为空元素（Empty Elements）。比如 `<br>` 标签插入一个换行，`<img>` 标签用来插入图片。

```html
<br>
<img src="image.jpg" alt="My Image">
```

## 块级元素

块级元素（Block-level Elements）在页面中以块的形式显示，常常用作结构元素。常见的块级元素有：`<div>`、`<p>`、`<h1>`-`<h6>` 和 `<ul>` 等。块级元素的特点是：

1. 独占一行
2. 元素的宽高可以设置
3. 默认宽度是它父容器的100%
4. 与其他块级元素上下堆叠

```html
<div>我是div</div>
<div>我也是div</div>
```

浏览器中效果:
<div>我是div</div>
<div>我也是div</div>


## 行内元素

行内元素（Inline Elements）不会开始新的一行，它们在文本中流动，仅占据它们包含的内容所需要的宽度。常见的行内元素有：`<span>`、`<a>` 和 `<img>` 等。行内元素的特点是：

1. 可以与相邻的行内元素排列在同一行
2. 元素的宽高不可设置
3. 元素宽度会被内容撑开

```html
<span>我是span</span>
<span>我也是span</span>
```

浏览器中效果:

<span>我是span</span>
<span>我也是span</span>


## 总结

这一讲我们具体分析了HTML中的元素，包括元素的属性、嵌套元素、空元素、块级元素和行内元素。
