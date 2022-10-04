# WTF HTML极简教程: 1. Hello HTML （9行代码）

WTF HTML教程，总结/搬运自[MDN HTML教程]((https://developer.mozilla.org/zh-CN/docs/Learn/HTML))，帮助新人快速入门HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_)  ｜ [@0xAA_Science](https://twitter.com/0xAA_Science) 

**WTF Academy社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.wtf.academy) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

这一讲，我们介绍HTML基础，并写第一个HTML程序：Hello HTML（9行代码）。你也可以直接阅读[MDN HTML基础](https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/HTML_basics)。


## 什么是 HTML ？

超文本标记语言 (英语：**H**yper**t**ext **M**arkup **L**anguage，简称：HTML ) 是一种用来结构化 Web 网页及其内容的标记语言。网页内容可以是：一组段落、一个重点信息列表、也可以含有图片和数据表。

HTML 不是一门编程语言，而是一种用于定义内容结构的*标记语言*。HTML 由一系列的**元素**（`element`）组成，这些元素可以用来包围不同部分的内容，使其以某种方式呈现或者工作。一对标签（`tag`）可以为一段文字或者一张图片添加超链接，将文字设置为斜体，改变字号，等等。例如下面内容：

```plain
My cat is very grumpy
```

可以将这行文字封装成一个段落（**p**aragraph）元素来使其在单独一行呈现：

```html
<p>My cat is very grumpy</p>
```

## HTML 元素详解

让我们深入探索一下这个段落元素。

![HTML 元素](./img/1-1.png)

这个元素的主要部分有：

1. **开始标签**（Opening tag）：包含元素的名称（本例为 p），被大于号、小于号所包围。表示元素从这里开始或者开始起作用 —— 在本例中即段落由此开始。
2. **结束标签**（Closing tag）：与开始标签相似，只是其在元素名之前包含了一个斜杠。这表示着元素的结尾 —— 在本例中即段落在此结束。初学者常常会犯忘记包含结束标签的错误，这可能会产生一些奇怪的结果。
3. **内容**（Content）：元素的内容，本例中就是所输入的文本本身。
4. **元素**（Element）：开始标签、结束标签与内容相结合，便是一个完整的元素。

元素也可以有属性（Attribute）：

![HTML 属性](./img/1-2.png)

属性包含了关于元素的一些额外信息，这些信息本身不应显现在内容中。本例中，`class` 是属性名称，`editor-note` 是属性的值。`class` 属性可为元素提供一个标识名称，以便进一步为元素指定样式或进行其他操作时使用。

属性应该包含：

1. 在属性与元素名称（或上一个属性，如果有超过一个属性的话）之间的空格符。
2. 属性的名称，并接上一个等号。
3. 由引号所包围的属性值。

> **备注：** 不包含 ASCII 空格（以及 `"` `'` `` ` `` `=` `<` `>` ）的简单属性值可以不使用引号，但是建议将所有属性值用引号括起来，这样的代码一致性更佳，更易于阅读。

### 嵌套元素

也可以将一个元素置于其他元素之中 —— 称作**嵌套**。要表明猫咪非常暴躁，可以将“very”用 `strong` 元素包围，从而突出显示：

```html
<p>My cat is <strong>very</strong> grumpy.</p>
```

必须保证元素嵌套次序正确：本例首先使用 `p` 标签，然后是 `strong` 标签，因此要先结束 `strong` 标签，最后再结束 `p` 标签。这样是不对的：

```html example-bad
<p>My cat is <strong>very grumpy.</p></strong>
```

元素必须正确地开始和结束，才能清楚地显示出正确的嵌套层次。否则浏览器就得自己猜测，虽然它会竭尽全力，但很大程度不会给你期望的结果。所以一定要避免！

### 空元素

不包含任何内容的元素称为空元素。比如 `img` 元素：

```html
<img src="images/firefox-icon.png" alt="My test image">
```

本元素包含两个属性，但是并没有 `</img>` 结束标签，元素里也没有内容。这是因为图像元素不需要通过内容来产生效果，它的作用是向其所在的位置嵌入一个图像。

## 开发工具

我们建议大家使用 [VSCode](https://code.visualstudio.com/download) 开发 HTML，并用浏览器（Chrome）打开`.html`文件进行浏览。

## Hello HTML

现在来看看单个元素如何彼此协同构成一个完整的 HTML 页面，我们将写第一个 HTML 程序：Hello HTML（9行代码）

```html
<!DOCTYPE html>
<html>
  <head>
    <title>This is the head</title>
  </head>
  <body>
    <p>Hello <strong>HTML</strong>.</p>
  </body>
</html>
```

![Hello HTML](./img/1-3.png)

Hello HTML中包括以下元素：

- `<!DOCTYPE html>` — 文档类型。混沌初分，HTML 尚在襁褓（大约是 1991/92 年）之时，`DOCTYPE` 用来链接一些 HTML 编写守则，比如自动查错之类。`DOCTYPE` 在当今作用有限，仅用于保证文档正常读取。现在知道这些就足够了。
- `<html></html>` — `html` 元素。该元素包含整个页面的内容，也称作根元素。
- `<head></head>` — `head` 元素。该元素的内容对用户不可见，其中包含例如面向搜索引擎的搜索关键字（keyword）、页面描述、CSS 样式表和字符编码声明等。
- `<title></title>` — `title` 元素。该元素设置页面的标题，显示在浏览器标签页上，也作为收藏网页的描述文字。
- `<body></body>` — `body` 元素。该元素包含期望让用户在访问页面时看到的内容，包括文本、图像、视频、游戏、可播放的音轨或其他内容。
- `<p></p>` - 段落元素，表示文本的一个段落，通常表现为一整块与相邻文本分离的文本，或以垂直的空白隔离或以首行缩进。

## 总结

这一讲我们介绍了什么是HTML，HTML的元素和开发工具，并且写了第一个HTML程序：Hello HTML。