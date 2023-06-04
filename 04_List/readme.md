# WTF HTML极简教程: 4. 列表和表格

WTF HTML教程，帮助新人快速入门HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_)  ｜ [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.wtf.academy) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---


HTML 中的列表和表格标签是构建网页的重要工具，它们可以帮助我们组织和显示数据。以下是关于列表和表格的一些基本信息。


## 列表

在HTML中，有三种类型的列表：

1. 无序列表（Unordered list）：使用`<ul>`元素来创建，每个列表项都要用`<li>`元素来表示。
2. 有序列表（Ordered list）：使用`<ol>`元素来创建，列表项同样用`<li>`元素来表示，不同的是它们会自动添加序号。
3. 定义列表（Definition list）：使用`<dl>`元素创建，包含`<dt>`（定义标题）和`<dd>`（定义描述）元素。

下面我们详细介绍每种列表的用法和特点。

### 无序列表

无序列表是最常见的列表类型，它在每个列表项前添加一个小圆点（也叫做列表符号）。它使用 `<ul>` 作为列表的容器，而 `<li>` 作为描述具体的列表项。例如：

```html
<ul>
  <li>BTC</li>
  <li>ETH</li>
  <li>SHIB</li>
</ul>
```


浏览器中效果：

<ul>
  <li>BTC</li>
  <li>ETH</li>
  <li>SHIB</li>
</ul>


### 有序列表

相对于无序列表，有序列表的每个列表项会使用数字进行标记。有序列表始使用 `<ol>` 作为列表的容器，同样使用 `<li>` 描述具体的列表项。例如：

```html
<ol>
<li>BTC</li>
<li>ETH</li>
<li>SHIB</li>
</ol>
```

浏览器中显示如下：

<ol>
<li>BTC</li>
<li>ETH</li>
<li>SHIB</li>
</ol>


### 定义列表

定义列表由`<dl>`（定义列表）、`<dt>`（定义项）和`<dd>`（定义描述）元素组成。定义列表通常用来展示一组术语和它们的定义。

```html
<dl>
  <dt>BTC</dt>
  <dd>- desc1</dd>
  <dd>- desc2</dd>
  <dt>ETH</dt>
  <dd>- desc1</dd>
  <dd>- desc2</dd>
</dl>
```

浏览器显示如下：

<dl>
  <dt>BTC</dt>
  <dd>- desc1</dd>
  <dd>- desc2</dd>
  <dt>ETH</dt>
  <dd>- desc1</dd>
  <dd>- desc2</dd>
</dl>


## 表格

### 基础表格

表格可以用于展示二维的数据，它使用 `<table>`作为表格的容器

内部使用 `<tr>`(table row)表示一行的数据

 `<tr>`内部使用 `<th>`表示表格每列的标题，使用 `<td>`表示该行每列，存放具体的数据；

具体示例如下：

```html
<table>
  <tr>
    <th>Name</th>
    <th>Code</th>
    <th>Price</th>
  </tr>
  <tr>
    <td>比特币</td>
    <td>BTC</td>
    <td>19969</td>
  </tr>
  <tr>
    <td>以太币</td>
    <td>ETH</td>
    <td>1,354</td>
  </tr>
</table>
```

浏览器显示如下：

<table>
  <tr>
    <th>Name</th>
    <th>Code</th>
    <th>Price</th>
  </tr>
  <tr>
    <td>比特币</td>
    <td>BTC</td>
    <td>19969</td>
  </tr>
  <tr>
    <td>以太币</td>
    <td>ETH</td>
    <td>1,354</td>
  </tr>
</table>


### `<thead>`、`<tbody>`和 `<tfoot>`

`<thead>`、`<tbody>`和 `<tfoot>`元素结合起来使用，用来规定表格的各个部分（表头、主体、页脚）

示例如下：

```html
<table>
  <thead>
    <tr>
      <th>Token</th>
      <th>Cost</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Total</td>
      <td>180</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>BTC</td>
      <td>100</td>
    </tr>
    <tr>
      <td>ETH</td>
      <td>80</td>
    </tr>
  </tbody>
</table>
```

浏览器显示如下：

<table>
  <thead>
    <tr>
      <th>Token</th>
      <th>Cost</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Total</td>
      <td>180</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>BTC</td>
      <td>100</td>
    </tr>
    <tr>
      <td>ETH</td>
      <td>80</td>
    </tr>
  </tbody>
</table>



### 合并表格

合并表格可以使用 `<td>`和`<th>`的`colspan`和`rowspan`属性，其中`colspan`用于水平合并多行，`rowspan`用于垂直合并多列。

示例如下：

```html
<table>
  <tr>
    <th>Token</th>
    <th>Price</th>
    <th>Total</th>
  </tr>
  <tr>
    <td>BTC</td>
    <td>100</td>
    <td rowspan="2">300</td>
  </tr>
  <tr>
    <td>ETH</td>
    <td>200</td>
  </tr>
</table>
```


浏览器显示如下：

<table>
  <tr>
    <th>Token</th>
    <th>Price</th>
    <th>Total</th>
  </tr>
  <tr>
    <td>BTC</td>
    <td>100</td>
    <td rowspan="2">300</td>
  </tr>
  <tr>
    <td>ETH</td>
    <td>200</td>
  </tr>
</table>


## 总结

这一讲我们介绍了 HTML 中的列表和表格。通过学习这些标签，你已经能够创建结构化的列表和表格，这是构建高质量网页的重要步骤。