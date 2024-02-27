# WTF HTML minimalist tutorial: 4. Lists and tables

WTF HTML tutorial helps newcomers get started with HTML quickly.

**Twitter**: [@WTFAcademy_](https://twitter.com/WTFAcademy_) | [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy Community:** [Official website wtf.academy](https://wtf.academy) | [WTF Solidity Tutorial](https://github.com/AmazingAng/WTFSolidity) | [discord](https: //discord.gg/5akcruXrsk) | [WeChat group application](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

All codes and tutorials are open source on github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

List and table tags in HTML are important tools for building web pages. They can help us organize and display data. Here is some basic information about lists and tables.


## List

In HTML, there are three types of lists:

1. Unordered list: Created using `<ul>` elements, and each list item must be represented by `<li>` elements.
2. Ordered list: Created using `<ol>` elements. List items are also represented by `<li>` elements. The difference is that they will automatically add serial numbers.
3. Definition list: Created using the `<dl>` element, including `<dt>` (definition title) and `<dd>` (definition description) elements.

Below we introduce the usage and characteristics of each type of list in detail.

### Unordered list

Unordered lists are the most common list type and add a small dot (also called a list symbol) before each list item. It uses `<ul>` as the container for the list, and `<li>` as the description of the specific list item. For example:

```html
<ul>
   <li>BTC</li>
   <li>ETH</li>
   <li>SHIB</li>
</ul>
```


Effect in browser:

<ul>
   <li>BTC</li>
   <li>ETH</li>
   <li>SHIB</li>
</ul>


### Ordered list

Compared to unordered lists, each list item in an ordered list is marked with a number. Ordered lists originally use `<ol>` as the container of the list, and also use `<li>` to describe specific list items. For example:

```html
<ol>
<li>BTC</li>
<li>ETH</li>
<li>SHIB</li>
</ol>
```

The browser displays the following:

<ol>
<li>BTC</li>
<li>ETH</li>
<li>SHIB</li>
</ol>

### Definition list

A definition list consists of `<dl>` (definition list), `<dt>` (definition item) and `<dd>` (definition description) elements. Definition lists are often used to present a set of terms and their definitions.

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

The browser displays the following:

<dl>
   <dt>BTC</dt>
   <dd>- desc1</dd>
   <dd>- desc2</dd>
   <dt>ETH</dt>
   <dd>- desc1</dd>
   <dd>- desc2</dd>
</dl>


## sheet

### Basic table

Tables can be used to display two-dimensional data. It uses `<table>` as the container of the table.

`<tr>`(table row) is used internally to represent a row of data

  `<tr>` internally uses `<th>` to represent the title of each column of the table, and uses `<td>` to represent each column of the row to store specific data;

Specific examples are as follows:

```html
<table>
   <tr>
     <th>Name</th>
     <th>Code</th>
     <th>Price</th>
   </tr>
   <tr>
     <td>Bitcoin</td>
     <td>BTC</td>
     <td>19969</td>
   </tr>
   <tr>
     <td>Ethereum</td>
     <td>ETH</td>
     <td>1,354</td>
   </tr>
</table>
```

The browser displays the following:

<table>
   <tr>
     <th>Name</th>
     <th>Code</th>
     <th>Price</th>
   </tr>
   <tr>
     <td>Bitcoin</td>
     <td>BTC</td>
     <td>19969</td>
   </tr>
   <tr>
     <td>Ethereum</td>
     <td>ETH</td>
     <td>1,354</td>
   </tr>
</table>

### `<thead>`, `<tbody>` and `<tfoot>`

The `<thead>`, `<tbody>` and `<tfoot>` elements are used in combination to specify the various parts of the table (header, body, footer)

Examples are as follows:

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

The browser displays the following:

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



### Merge tables

Merging tables can use the `colspan` and `rowspan` attributes of `<td>` and `<th>`, where `colspan` is used to merge multiple rows horizontally, and `rowspan` is used to merge multiple columns vertically.

Examples are as follows:

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


The browser displays the following:

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


## Summary

In this lecture we introduced lists and tables in HTML. By learning these tags, you have been able to create structured lists and tables, an important step in building high-quality web pages.
