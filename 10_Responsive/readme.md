# WTF HTML极简教程: 10. 响应式设计和移动HTML

WTF HTML 教程，帮助新人快速入门 HTML。

**推特**：[@WTFAcademy_](https://twitter.com/WTFAcademy_) ｜ [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy 社群：** [官网 wtf.academy](https://wtf.academy) | [WTF Solidity 教程](https://github.com/AmazingAng/WTFSolidity) | [discord](https://discord.wtf.academy) | [微信群申请](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

所有代码和教程开源在 github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

响应式设计是一种让网站设计能够对不同设备和屏幕大小进行优化的方法，使得网站在任何设备上都能提供良好的用户体验。这种设计方法的核心包括视图窗口(viewport)，设备独立像素，媒体查询，以及对图片和表格的响应式设计。

## 视图窗口(viewport)和设备独立像素

视图窗口是用户在浏览器中可以看到的网页的区域。在移动设备上，视图窗口的宽度通常等于设备的物理屏幕宽度。

为了在所有设备上创建统一的布局，我们需要使用设备独立像素。设备独立像素是一个虚拟像素单位，用于在不同的设备上提供一致的布局，而不是依赖于设备的实际物理像素。

在HTML中，可以使用`<meta>`标签设置视图窗口的宽度和初始缩放级别：

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

## 媒体查询

媒体查询是CSS3的一部分，它允许内容对不同的设备或视窗条件进行响应。例如，你可以使用媒体查询在小屏幕和大屏幕设备上应用不同的样式：

```css
/* 在宽度小于 600px 的设备上应用的样式 */
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

## 图片和表格的响应式设计

对于图片，可以使用 CSS 的 `max-width` 属性来确保图片不会超过其容器的宽度：

```css
img {
  max-width: 100%;
  height: auto;
}
```

对于表格，响应式设计的方法各异，一种常见的方法是在小屏幕设备上将表格转换为一个键值对列表：

```css
@media only screen and (max-width: 600px) {
  td:before {
    content: attr(data-label);
    float: left;
    text-transform: uppercase;
    font-weight: bold;
  }
}
```

在上述 CSS 中，`attr(data-label)` 会把每个 `td` 元素前面的内容替换为它的 `data-label` 属性的值。

## 总结

响应式设计和移动HTML是现代web开发的重要组成部分。通过理解和运用视图窗口，设备独立像素，媒体查询，以及对图片和表格的响应式设计，你可以创建在任何设备和屏幕大小上都能提供优良用户体验的网站。