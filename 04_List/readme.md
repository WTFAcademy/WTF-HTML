# WTF HTML极简教程: 4. 列表

WTF HTML教程，总结/搬运自[MDN HTML教程](https://developer.mozilla.org/zh-CN/docs/Learn/HTML)，帮助新人快速入门HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_)  ｜ [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.wtf.academy) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

在这一讲我们将介绍HTML的常用元素之一：列表。列表包含三种类型：无序列表、有序列表、定义列表。你也可以直接阅读[MDN HTML基础](https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/HTML_basics)。



## 无序列表ul（unordered lists）

无序列表常用于表示一个没有顺序关系的列表，每个列表项使用粗体圆点标记。

`<ul>` 用于作为列表的容器，而 `<li>` 用于描述具体的列表项。例如：

```html
<ul>
  <li>first item</li>
  <li>second item</li>
  <li>third item</li>
</ul>
```

* first item
* second item
* third item

## 有序列表ol（ordered lists）

相对于无序列表，有序列表的每个列表项会使用数字进行标记。

有序列表始使用 `<ol>` 作为列表的容器，同样使用 `<li>` 描述具体的列表项。例如：

```html
<ol>
<li>Coffee</li>
<li>Milk</li>
</ol>
```

浏览器中显示如下：

1. Coffee
2. Milk

## 定义列表dl（definition lists）

定义列表的每个列表项可以和具体的描述组合起来，丰富列表项的内容。

定义列表使用 `<dl>` 作为列表容器，使用 `<dt>` (definition term)作为列表项，每个列表项的定义以 `<dd>` (description detail)开始。

```html
<dl>
  <dt>Coffee</dt>
  <dd>- black coffee</dd>
  <dd>- hot coffee</dd>
  <dt>Milk</dt>
  <dd>- white milk</dd>
  <dd>- hot milk</dd>
</dl>
```

浏览器显示如下：

<dl>
  <dt>Coffee</dt>
  <dd>- black coffee</dd>
  <dd>- hot coffee</dd>
  <dt>Milk</dt>
  <dd>- white milk</dd>
  <dd>- hot milk</dd>
</dl>

## 总结

这一讲介绍了html的常用元素列表以及三种列表类型。更详细内容你可以阅读[MDN HTML基础](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals)。
