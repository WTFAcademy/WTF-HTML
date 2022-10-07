# WTF HTML极简教程: 3. 常用文本标签

WTF HTML教程，总结/搬运自[MDN HTML教程]((https://developer.mozilla.org/zh-CN/docs/Learn/HTML))，帮助新人快速入门HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_)  ｜ [@0xAA_Science](https://twitter.com/0xAA_Science) 

**WTF Academy社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.wtf.academy) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

这一讲，我们介绍常用的文本标记 HTML 元素。你也可以直接阅读[MDN HTML基础](https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/HTML_basics)。

## `<h1>-<h6>`

标题元素可用于指定内容的标题和子标题。就像一本书的书名、每章的大标题、小标题，等。HTML 文档也是一样。HTML 包括六个级别的标题，[`<h1>–<h6>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Heading_Elements)，一般最多用到 3-4 级标题。

```html
<h1>主标题</h1>
<h2>顶层标题</h2>
<h3>子标题</h3>
<h4>次子标题</h4>
```

> **Note**
>
> 你可以看到第一级标题是有隐式的主题样式。不要使用标题元素来加大、加粗字体，因为标题对于 [无障碍访问](https://developer.mozilla.org/zh-CN/docs/Learn/Accessibility) 和 [搜索引擎优化](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals#为什么我们需要结构化？) 等问题非常有意义。要保持页面结构清晰，标题整洁，不要发生标题级别跳跃。

## `<p>`

在 HTML 中，每个段落是通过 `<p>` 元素标签进行定义的，比如下面这样：

```html
<p>我是一个段落，千真万确。</p>
```

## `<span>`

HTML `<span>` 元素是短语内容的通用行内容器，并没有任何特殊语义。可以使用它来编组元素以达到某种样式意图（通过使用类或者 Id 属性），或者这些元素有着共同的属性，比如lang。应该在没有其他合适的语义元素时才使用它。`<span>` 与 `<div>` 元素很相似，但 `<div>` 是一个 [块级元素](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Block-level_elements) 而 `<span>` 则是 [行内元素](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Inline_elements).

```html
<p><span>一些文字</span></p>
```

## `<br>`

HTML `<br>` 元素在文本中生成一个换行（回车）符号。此元素在写诗和地址时很有用，这些地方的换行都非常重要。

比如：

```html
Mozilla Foundation<br>
1981 Landings Drive<br>
Building K<br>
Mountain View, CA 94043-0801<br>
USA
```

上面的 HTML 输出为：

```plain
Mozilla Foundation
1981 Landings Drive
Building K
Mountain View, CA 94043-0801
USA
```

## `<em>` 和 `<strong>`

在口语表达中，我们有时会强调某些字，用来改变这句话的意思。同样地，在书面用语中，我们可以使用斜体字来达到同样的效果。例如，下面两个句子便有不同的意思：

I am glad you weren't late.

I am *glad* you weren't *late*. (ps: 此句中"*glad*"和"*late*"为斜体字体)

第一句话听起来真的像松了一口气因为没有迟到。相反，第二句话听起来具有讽刺性而且有隐含的攻击性，表达对一个人迟到的恼怒。

在 HTML 中我们用 `<em>` 元素来标记这样的情况。

```html
<p>I am <em>glad</em> you weren't <em>late</em>.</p>
```

为了强调重要的词，在口语方面我们往往用重音强调，在文字方面则是用粗体字来达到强调的效果。例如下面这段：

This liquid is **highly toxic**.

I am counting on you. **Do not** be late!

在 HTML 中我们用 `<strong>` 元素来标记这样的情况。

```html
<p>This liquid is <strong>highly toxic</strong>.</p>

<p>I am counting on you. <strong>Do not</strong> be late!</p>
```

## 总结

这一讲我们介绍了如何在 HTML 中标记文本，并介绍了一些最重要的元素。在这一领域还有许多语义元素，我们将在后面的文章中看到更多的语义元素。

更详细内容你可以阅读[MDN HTML基础](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals)。
