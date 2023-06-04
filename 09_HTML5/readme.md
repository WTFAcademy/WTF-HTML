# WTF HTML极简教程: 9. HTML5新特性

WTF HTML 教程，帮助新人快速入门 HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_) ｜ [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy 社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity 教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.wtf.academy) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在 github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

HTML5 是 HTML 的最新版本，它引入了许多新的标签、属性和功能，大大增强了 web 的功能和互动性。在这一章节中，我们将介绍一些 HTML5 的新特性，包括新的标签和属性，以及新的表单类型和属性。

## 新的标签和属性

HTML5 引入了一系列新的标签和属性，以提供更丰富的内容展示和更强大的功能。

### `<video>` 和 `<audio>`

`<video>` 和 `<audio>` 标签使得在网页上嵌入视频和音频变得更加简单。你可以使用 `<source>` 标签指定多个音频或视频源，浏览器将会选择第一个它支持的源。

以下是一个 `<video>` 标签的示例：

```html
<video controls width="500">
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>
```
浏览器效果：

<video controls width="500">
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>


以下是一个 `<audio>` 标签的示例：

```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  <source src="audio.ogg" type="audio/ogg">
  Your browser does not support the audio tag.
</audio>
```

浏览器效果：

<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  <source src="audio.ogg" type="audio/ogg">
  Your browser does not support the audio tag.
</audio>


### `<canvas>`

`<canvas>` 标签用于在网页上绘制图形，它为图像提供了一个可编程的环境。与 `<img>` 标签不同，`<canvas>` 允许你通过 JavaScript 动态生成图像。

以下是一个使用 `<canvas>` 绘制矩形的示例：

```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000;">
Your browser does not support the HTML5 canvas tag.
</canvas>

<script>
var canvas = document.getElementById("myCanvas");
var ctx = canvas.getContext("2d");
ctx.fillStyle = "#000000";
ctx.fillRect(0, 0, 80, 80);
</script>
```

## 新的表单类型和属性

HTML5 引入了一些新的输入类型和属性，以增强表单的功能和易用性。

### 新的输入类型

HTML5 提供了一些新的输入类型，如 `email`、`number`、`date` 等。这些新的输入类型可以提供更好的输入控制和验证。

以下是一些新的输入类型的示例：

```html
<form>
  <label for="email">Email:</label>
  <input type="email" id="email" name="email">

  <label for="quantity">Quantity (between 1 and 5):</label>
  <input type="number" id="quantity" name="quantity" min="1" max="5">

  <label for="birthday">Birthday:</label>
  <input type="date" id="birthday" name="birthday">
</form>
```

浏览器效果：
<form>
  <label for="email">Email:</label>
  <input type="email" id="email" name="email">

  <label for="quantity">Quantity (between 1 and 5):</label>
  <input type="number" id="quantity" name="quantity" min="1" max="5">

  <label for="birthday">Birthday:</label>
  <input type="date" id="birthday" name="birthday">
</form>


### 新的输入属性

HTML5 还引入了一些新的输入属性，如 `placeholder`、`required` 等。

`placeholder` 属性可以为输入字段提供一个提示，而 `required` 属性可以使输入字段变得必需。

以下是一些新的输入属性的示例：

```html
<form>
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname" placeholder="Your first name" required>

  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname" placeholder="Your last name">
</form>
```

浏览器效果：

<form>
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname" placeholder="Your first name" required>

  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname" placeholder="Your last name">
</form>


## 总结

在这一章节中，我们介绍了一些 HTML5 的新特性，包括新的标签和属性，以及新的表单类型和属性。通过学习和使用这些新特性，你可以创建出更丰富、更强大的 web 页面。