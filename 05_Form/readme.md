# WTF HTML极简教程: 5. 表单

WTF HTML教程，帮助新人快速入门HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_)  ｜ [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.gg/5akcruXrsk) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

表单是 HTML 中非常重要的一部分，它能让用户在网页上输入信息，并将信息提交到服务器。在这一章节中，我们将详细介绍如何使用`<form>`、`<input>`、`<textarea>`等标签来创建表单。

## 表单的创建

在 HTML 中，表单的创建主要由`<form>`元素完成。`<form>`元素定义了用户输入数据的区域，并且可以包含不同类型的输入元素，如文本字段、选择框、复选框、单选框和按钮等。

一个基本的表单结构如下：

```html
<form>
  <!-- 表单元素放在这里 -->
</form>
```

在`<form>`元素中，你可以添加属性`action`和`method`。`action`属性定义表单数据提交到服务器后的处理文件的 URL。`method`属性定义数据如何发送到服务器，常用的值有 "get" 和 "post"。

## 文本输入

在表单中，我们经常需要用户输入文本。这可以通过`<input>`元素完成，其`type`属性设置为 "text"。

例如：

```html
<form>
First name: <input type="text" name="firstname"><br>
Last name: <input type="text" name="lastname">
</form>
```

浏览器效果：

<form>
First name: <input type="text" name="firstname"><br>
Last name: <input type="text" name="lastname">
</form>

## 密码

如果你需要用户输入密码，可以将`<input>`元素的`type`属性设置为 "password"，输入的内容会被隐藏起来。

例如：

```html
<form>
Password: <input type="password" name="pwd">
</form>
```

浏览器效果：

<form>
Password: <input type="password" name="pwd">
</form>

## 单选按钮（Radio Buttons）

单选按钮和复选框可以让用户在多个选项中选择一个或多个。单选按钮的`type`属性值为 "radio"。

```html
<form action="">
ACCOUNT:
<input type="radio" name="address" value="addr1">0x5B38Da6a701c568545dCfcB03FcB875f56beddC4<br>
<input type="radio" name="address" value="addr2">0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2
</form>
```

浏览器效果：

<form action="">
ACCOUNT:

<input type="radio" name="address" value="addr1">0x5B38Da6a701c568545dCfcB03FcB875f56beddC4<br>
<input type="radio" name="address" value="addr2">0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2
</form>

### 复选框（Checkboxes）

复选框可以选取一个或多个选项，使用 **`<input type="checkbox">`** 定义

示例如下：

```html
<form>
  Token value <br>
  <input type="checkbox" name="token_value" value="Wei">Wei<br>
  <input type="checkbox" name="token_value" value="GWei">GWei<br>
  <input type="checkbox" name="token_value" value="Ether">Ether<br>
</form>
```

浏览器效果：

<form>
  Token value <br>
  <input type="checkbox" name="token_value" value="Wei">Wei<br>
  <input type="checkbox" name="token_value" value="GWei">GWei<br>
  <input type="checkbox" name="token_value" value="Ether">Ether<br>
</form>


### 下拉列表（select）

下拉列表可以让用户从多个选项中选择一个。它由`<select>`元素创建，并使用`<option>`元素来定义选项。

示例如下：

```html
<form action="">
  Contract
  <select>
    <option>Facucet.sol</option>
    <option>ERC20.sol</option>
    <option>ERC721.sol</option>
  </select>
</form>
```

浏览器效果：

<form action="">
  Contract
  <select>
    <option>Facucet.sol</option>
    <option>ERC20.sol</option>
    <option>ERC721.sol</option>
  </select>
</form>

### 提交按钮（Submit）

表单通常需要一个提交按钮来提交用户的输入。这可以通过设置`<input>`元素的`type`属性为 "submit" 来完成。

示例如下：

```html
<form name="input" action="action.php" method="get">
  <input type="submit" value="Deploy">
  <input type="text" name="user" placeholder='address'>
</form>
```

浏览器效果：

<form name="input" action="action.php" method="get">
  <input type="submit" value="Deploy">
  <input type="text" name="user" placeholder='address'>
</form>

## 表单其他元素

还有一些表表单常见的元素属性：

- **name**：表单的名称。该值不能是空字符串，并且在它所在的表单集合中需要是唯一的

- **action** ：指定表单内容的送达地址，实现对输入数据的处理

- **method**：定义表单数据的提交方式，可以是以下值：

  - **post**：HTTP POST 方法，表单数据会包含在表单体内发送给服务器，可以用于提交敏感数据，如用户名与密码等
  - **get**：默认值， HTTP GET 方法，表单数据会附加在 **action** 属性的 URL 中，并以 **?** 作为分隔符，一般用于不敏感信息，如分页等。例如：https://www.wtfacademy.com/?currentPage=1，这里的 currentPage=1 就是 get 方法提交的数据


## 总结

以上就是 HTML 表单的基本用法。通过学习这些标签和属性，你应该已经能够创建基本的 HTML 表单了。