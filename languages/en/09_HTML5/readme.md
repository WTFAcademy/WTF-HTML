# WTF HTML minimalist tutorial: 9. HTML5 new features

WTF HTML tutorial to help newcomers get started with HTML quickly.

**Twitter**: [@WTFAcademy_](https://twitter.com/WTFAcademy_) | [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy Community:** [Official website wtf.academy](https://wtf.academy) | [WTF Solidity Tutorial](https://github.com/AmazingAng/WTFSolidity) | [discord](https: //discord.gg/5akcruXrsk) | [WeChat group application](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

All codes and tutorials are open source on github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

HTML5 is the latest version of HTML, which introduces many new tags, attributes and functions that greatly enhance the functionality and interactivity of the web. In this chapter, we'll introduce some of the new features of HTML5, including new tags and attributes, as well as new form types and attributes.

## New tags and attributes

HTML5 introduces a series of new tags and attributes to provide richer content presentation and more powerful functionality.

### `<video>` and `<audio>`

The `<video>` and `<audio>` tags make it easier to embed video and audio on web pages. You can specify multiple audio or video sources using the `<source>` tag, and the browser will choose the first one it supports.

Here is an example of a `<video>` tag:

```html
<video controls width="500">
   <source src="movie.mp4" type="video/mp4">
   <source src="movie.ogg" type="video/ogg">
   Your browser does not support the video tag.
</video>
```
Browser effect:

<video controls width="500">
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>


Here is an example of an `<audio>` tag:

```html
<audio controls>
   <source src="audio.mp3" type="audio/mpeg">
   <source src="audio.ogg" type="audio/ogg">
   Your browser does not support the audio tag.
</audio>
```

Browser effect:

<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  <source src="audio.ogg" type="audio/ogg">
  Your browser does not support the audio tag.
</audio>


### `<canvas>`

The `<canvas>` tag is used to draw graphics on web pages. It provides a programmable environment for images. Unlike the `<img>` tag, `<canvas>` allows you to dynamically generate images via JavaScript.

Here is an example of using `<canvas>` to draw a rectangle:

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

## New form types and properties

HTML5 introduces several new input types and attributes to enhance the functionality and ease of use of forms.

### New input type

HTML5 provides some new input types, such as `email`, `number`, `date`, etc. These new input types provide better input control and validation.

Here are some examples of the new input types:

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

Browser effect:
<form>
   <label for="email">Email:</label>
   <input type="email" id="email" name="email">

   <label for="quantity">Quantity (between 1 and 5):</label>
   <input type="number" id="quantity" name="quantity" min="1" max="5">

   <label for="birthday">Birthday:</label>
   <input type="date" id="birthday" name="birthday">
</form>


### New input properties

HTML5 also introduces some new input attributes, such as `placeholder`, `required`, etc.

The `placeholder` attribute can provide a hint for an input field, while the `required` attribute can make an input field required.

Here are some examples of the new input properties:

```html
<form>
   <label for="fname">First name:</label>
   <input type="text" id="fname" name="fname" placeholder="Your first name" required>

   <label for="lname">Last name:</label>
   <input type="text" id="lname" name="lname" placeholder="Your last name">
</form>
```

Browser effect:

<form>
   <label for="fname">First name:</label>
   <input type="text" id="fname" name="fname" placeholder="Your first name" required>

   <label for="lname">Last name:</label>
   <input type="text" id="lname" name="lname" placeholder="Your last name">
</form>


## Summary

In this chapter, we introduce some of the new features of HTML5, including new tags and attributes, as well as new form types and attributes. By learning and using these new features, you can create richer, more powerful web pages.
