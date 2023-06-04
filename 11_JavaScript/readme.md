# WTF HTML极简教程: 11. HTML和JavaScript

WTF HTML 教程，帮助新人快速入门 HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_) ｜ [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy 社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity 教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.wtf.academy) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在 github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

JavaScript 是一种轻量级的编程语言，经常与 HTML 和 CSS 一起使用，用于创建交互式的网站。在本章，我们将介绍如何使用 `<script>` 标签在 HTML 中插入 JavaScript，HTML DOM模型，以及如何使用 JavaScript 操作 HTML 元素。

## 使用 `<script>` 标签插入 JavaScript

在 HTML 中，我们可以使用 `<script>` 标签插入 JavaScript 代码。`<script>` 标签可以放在 HTML 文档的 `<head>` 或 `<body>` 部分。通常，为了避免阻塞页面的渲染，我们会将 `<script>` 标签放在 `<body>` 标签的末尾。

下面是一个简单的示例：

```html
<!DOCTYPE html>
<html>
<body>

<h2>HTML 和 JavaScript 示例</h2>

<button onclick="displayDate()">显示日期</button>

<script>
function displayDate() {
  document.getElementById("demo").innerHTML = Date();
}
</script>

</body>
</html>
```

在这个示例中，当用户点击按钮时，JavaScript 函数 `displayDate()` 会被执行，显示当前的日期和时间。

## HTML DOM模型

DOM (Document Object Model) 是一个跨平台和语言独立的接口，允许程序和脚本动态访问和更新文档的内容、结构和样式。

HTML DOM 是一个标准对象模型和编程接口。它将 HTML 文档转化为一个树形结构，其中每个节点都是一个对象，代表了 HTML 文档的一部分。

## 使用JavaScript操作HTML元素

JavaScript 可以通过 HTML DOM 来访问和更改 HTML 元素。下面是一些常用的 DOM 方法：

- `document.getElementById(id)`：返回对拥有指定 id 的第一个对象的引用。
- `document.getElementsByClassName(name)`：返回一个包含所有带有指定类名的元素的 NodeList。
- `document.getElementsByTagName(name)`：返回一个包含所有带有指定标签名的元素的 NodeList。
- `document.querySelector(cssQuery)`：返回文档中匹配指定 CSS 选择器的第一个元素。
- `document.querySelectorAll(cssQuery)`：返回文档中匹配指定 CSS 选择器的所有元素的 NodeList。

这些方法可以用来获取 HTML 元素，然后可以使用 DOM 属性和方法修改这些元素，比如改变元素的文本内容、属性值或样式。

例如，下面的 JavaScript 代码使用 `getElementById` 方法获取了一个元素，并修改了该元素的文本内容：

```html
<!DOCTYPE html>
<html>
<body>

<h1 id="myHeading">Hello World!</h1>

<button onclick="changeText()">点击改变文本</button>

<script>
function changeText() {
  var heading = document.getElementById("myHeading");
  heading.innerHTML = "Hello WTF!";
}
</script>

</body>
</html>
```

当用户点击按钮时，页面上的标题会从 "Hello World!" 变为 "Hello WTF!"。

## 总结

HTML和JavaScript是紧密配合的两个技术，JavaScript提供了操作HTML元素的能力，而HTML DOM模型则为我们提供了一种标准的方式来表示和操作HTML文档。掌握这两个技术，可以帮助你创建更加动态和交互式的网站。