# WTF HTML minimalist tutorial: 5. Form

WTF HTML tutorial helps newcomers get started with HTML quickly.

**Twitter**: [@WTFAcademy_](https://twitter.com/WTFAcademy_) | [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy Community:** [Official website wtf.academy](https://wtf.academy) | [WTF Solidity Tutorial](https://github.com/AmazingAng/WTFSolidity) | [discord](https: //discord.gg/5akcruXrsk) | [WeChat group application](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

All codes and tutorials are open source on github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

Forms are a very important part of HTML that allow users to enter information on a web page and submit the information to the server. In this chapter, we will introduce in detail how to use tags such as `<form>`, `<input>`, `<textarea>` to create forms.

## Form creation

In HTML, form creation is mainly done by the `<form>` element. The `<form>` element defines the area where users enter data, and can contain different types of input elements, such as text fields, selection boxes, check boxes, radio buttons, and buttons.

A basic form structure is as follows:

```html
<form>
   <!-- Form elements are placed here -->
</form>
```

In the `<form>` element, you can add the attributes `action` and `method`. The `action` attribute defines the URL of the file to be processed after the form data is submitted to the server. The `method` attribute defines how data is sent to the server. Commonly used values ​​are "get" and "post".

## Text input

In forms, we often need users to enter text. This can be done via an `<input>` element with its `type` attribute set to "text".

For example:

```html
<form>
First name: <input type="text" name="firstname"><br>
Last name: <input type="text" name="lastname">
</form>
```

Browser effect:

<form>
First name: <input type="text" name="firstname"><br>
Last name: <input type="text" name="lastname">
</form>

## password

If you require the user to enter a password, you can set the `type` attribute of the `<input>` element to "password" and the input content will be hidden.

For example:

```html
<form>
Password: <input type="password" name="pwd">
</form>
```

Browser effect:

<form>
Password: <input type="password" name="pwd">
</form>

## Radio Buttons

Radio buttons and checkboxes allow users to select one or more from multiple options. The radio button's `type` attribute value is "radio".

```html
<form action="">
ACCOUNT:
<input type="radio" name="address" value="addr1">0x5B38Da6a701c568545dCfcB03FcB875f56beddC4<br>
<input type="radio" name="address" value="addr2">0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2
</form>
```

Browser effect:

<form action="">
ACCOUNT:

<input type="radio" name="address" value="addr1">0x5B38Da6a701c568545dCfcB03FcB875f56beddC4<br>
<input type="radio" name="address" value="addr2">0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2
</form>

### Checkboxes

A checkbox can select one or more options, defined using **`<input type="checkbox">`**

Examples are as follows:

```html
<form>
   Token value <br>
   <input type="checkbox" name="token_value" value="Wei">Wei<br>
   <input type="checkbox" name="token_value" value="GWei">GWei<br>
   <input type="checkbox" name="token_value" value="Ether">Ether<br>
</form>
```

Browser effect:

<form>
   Token value <br>
   <input type="checkbox" name="token_value" value="Wei">Wei<br>
   <input type="checkbox" name="token_value" value="GWei">GWei<br>
   <input type="checkbox" name="token_value" value="Ether">Ether<br>
</form>


### Drop-down list (select)

A drop-down list allows the user to select one from multiple options. It is created from the `<select>` element and uses the `<option>` element to define options.

Examples are as follows:

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

Browser effect:

<form action="">
   Contract
   <select>
     <option>Facucet.sol</option>
     <option>ERC20.sol</option>
     <option>ERC721.sol</option>
   </select>
</form>

### Submit button (Submit)

Forms usually require a submit button to submit user input. This can be done by setting the `type` attribute of the `<input>` element to "submit".

Examples are as follows:

```html
<form name="input" action="action.php" method="get">
   <input type="submit" value="Deploy">
   <input type="text" name="user" placeholder='address'>
</form>
```

Browser effect:

<form name="input" action="action.php" method="get">
   <input type="submit" value="Deploy">
   <input type="text" name="user" placeholder='address'>
</form>

## Other elements of the form

There are also some common element attributes of table forms:

- **name**: The name of the form. The value cannot be an empty string and needs to be unique within the form collection it is in

- **action**: Specify the delivery address of the form content to process the input data

- **method**: Define the submission method of form data, which can be the following values:

   - **post**: HTTP POST method, the form data will be included in the form body and sent to the server. It can be used to submit sensitive data, such as username and password, etc.
   - **get**: Default value, HTTP GET method, form data will be appended to the URL of the **action** attribute, and **?** is used as the delimiter. It is generally used for insensitive information, such as paging, etc. . For example: https://www.wtfacademy.com/?currentPage=1, where currentPage=1 is the data submitted by the get method


## Summary

The above is the basic usage of HTML forms. By learning these tags and attributes, you should be able to create basic HTML forms.
