# WTF HTML极简教程: 8. 语义元素

WTF HTML教程，帮助新人快速入门HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_)  ｜ [@0xAA_Science](https://twitter.com/0xAA_Science) 

**WTF Academy社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.gg/5akcruXrsk) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

语义化的 HTML 是指通过使用恰当的标签来传达内容的含义和结构，这样可以使得你的代码更易读易懂，同时也有助于搜索引擎优化 (SEO)。在 HTML5 中，引入了一系列新的语义标签，这些标签可以更清晰地描述你的内容和页面结构。在这一章节中，我们会介绍一些常见的语义标签。

## 常见的语义元素：

### 文本类：

一个页面结构通常包含：页眉、页脚、标题、导航、内容、侧边栏等等。

我们可以这样来编写页面，如下图所示。

![非语言化布局图](./img/8-1.png)

如上图所示，只需要使用 `<div>` 元素就可以完成一个页面的布局。甚至文本内容，例如标题、段落等等，也可以使用 `<div>` 来编写。

但是这样会产生两个很明显问题：
1. 不利于开发人员编写代码，当你面对满屏幕的 `<div>` 元素时，你很难快速分清楚他们所代表的含义。
2. 不利于搜索引擎优化（SEO），浏览器只知道你用了 `<div>` 元素，而 `div` 元素本身不具有任何含义，它只是一个容器。

这时候我们可以通过使用语义元素来解决这两个问题，如下图所示。

![语言化布局图](./img/8-2.png)

我们分别使用了 `<header>`  `<nav>`  `<main>`  `<aside>`  `<footer>` 来分别表示页面中不同的区域。

使用这些标签让页面具有良好的语义和结构，从而方便开发人员和浏览器都能快速理解网页内容。

这并不表示你不可以使用 `<div>` 元素 来编写页面，只是我们可以在页面特定的内容上，可以使用一些语义元素来替代 `<div>` 元素。这就是开头所说的让正确的元素做正确的事情。

下面我们来简单介绍一下这些标签。

- `<header>` 用于展示介绍性内容，通常包含一组介绍性的或是辅助导航的实用元素。它可能包含一些标题元素，但也可能包含其他元素，比如 Logo、搜索框、作者名称，等等。

- `<nav>` 表示页面的一部分，其目的是在当前文档或其他文档中提供导航链接。导航部分的常见示例是菜单，目录和索引。

- `<main>` 呈现了文档的 body 或应用的主体部分。主体部分由与文档直接相关，或者扩展于文档的中心主题、应用的主要功能部分的内容组成。

- `<aside>` 表示一个和其余页面内容几乎无关的部分，被认为是独立于该内容的一部分并且可以被单独的拆分出来而不会使整体受影响。其通常表现为侧边栏或者标注框。

- `<footer>` 通常用来表示页脚。一个页脚通常包含该章节作者、版权数据或者与文档相关的链接等信息。

- `<address>` 表示其中的 HTML 提供了某个人或某个组织（等等）的联系信息。

- `<article>` 表示文档、页面、应用或网站中的独立结构，其意在成为可独立分配的或可复用的结构，如在发布中，它可能是论坛帖子、杂志或新闻文章、博客、用户提交的评论、交互式组件，或者其他独立的内容项目。​​

- `<section>` 表示 HTML 文档中一个通用独立章节，它没有更具体的语义元素来表示。一般来说会包含一个标题。

例如：

```html
<header>
  <h1>Site Name</h1>
  <nav>
    <ul>
      <li><a href="/">Home</a></li>
      <li><a href="/about">About</a></li>
      <li><a href="/contact">Contact</a></li>
    </ul>
  </nav>
</header>

<main>
  <article>
    <h2>Blog Post Title</h2>
    <p>Blog post content...</p>
  </article>

  <aside>
    <h3>About the author</h3>
    <p>Author information...</p>
  </aside>
</main>

<footer>
  <p>&copy; 2023 Site Name</p>
</footer>
```

## 为什么需要语义元素？
1. 更便于开发。如上所述，你所编写的 HTML 代码更易于理解，可读性更高。
2. 方便其他设备解析（如屏幕阅读器、盲人阅读器、移动设备）以语义的方式来渲染网页。
3. 更便于 SEO 优化。比起使用非语义化的 `<div>` 标签，使用语义化可使网页更容易被用户搜索到。


## 总结

在这一章节中，我们介绍了语义化的 HTML 以及一些常见的语义标签。通过使用语义标签，你可以创建出更具可读性、易于维护，并且对搜索引擎友好的代码。