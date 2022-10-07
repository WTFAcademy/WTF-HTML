# WTF HTML极简教程: 4. 列表

WTF HTML教程，总结/搬运自[MDN HTML教程](https://developer.mozilla.org/zh-CN/docs/Learn/HTML)，帮助新人快速入门HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_)  ｜ [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.wtf.academy) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

在这一讲我们将介绍HTML的常用元素：列表和[表格](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/table)。你也可以直接阅读[MDN HTML基础](https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/HTML_basics)。

## 列表


## 无序列表ul（unordered lists）
列表包含三种类型：[无序列表](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ul)、[有序列表](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ol)、[定义列表](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/dl)。

### 无序列表ul（unordered lists）

无序列表常用于表示一个没有顺序关系的列表，每个列表项使用粗体圆点标记。

`<ul>` 用于作为列表的容器，而 `<li>` 用于描述具体的列表项。例如：

```html
<ul>
  <li>BTC</li>
  <li>ETH</li>
  <li>SHIB</li>
</ul>
```


浏览器中显示如下：

<ul>
  <li>BTC</li>
  <li>ETH</li>
  <li>SHIB</li>
</ul>


### 有序列表ol（ordered lists）

相对于无序列表，有序列表的每个列表项会使用数字进行标记。

有序列表始使用 `<ol>` 作为列表的容器，同样使用 `<li>` 描述具体的列表项。例如：

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


### 定义列表dl（definition lists）

定义列表的每个列表项可以和具体的描述组合起来，丰富列表项的内容。

定义列表使用 `<dl>` 作为列表容器，使用 `<dt>` (definition term)作为列表项，每个列表项的定义以 `<dd>` (description detail)开始。

示例如下：

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


## 表格table

### 基础使用 `<table>`、`<tr>`、`<th>`和 `<td>`

表格可以用于展示二维的数据，使用 `<table>`作为表格的容器

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



### 合并表格：colspan和rowspan

合并表格可以使用 `<td>`和`<th>`的colspan和rowspan属性，其中colspan用于水平合并多行，rowspan用于垂直合并多列。

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

这一讲介绍了html的常用元素列表以及三种列表类型，还有表格的基本使用和合并表格的方式。更详细内容你可以阅读[MDN HTML基础](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals)。
