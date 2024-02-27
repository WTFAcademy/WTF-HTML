# WTF HTML minimalist tutorial: 6. Hyperlink hyperlink

WTF HTML tutorial helps newcomers get started with HTML quickly.

**Twitter**: [@WTFAcademy_](https://twitter.com/WTFAcademy_) | [@0xAA_Science](https://twitter.com/0xAA_Science)

**WTF Academy Community:** [Official website wtf.academy](https://wtf.academy) | [WTF Solidity Tutorial](https://github.com/AmazingAng/WTFSolidity) | [discord](https: //discord.gg/5akcruXrsk) | [WeChat group application](https://docs.google.com/forms/d/e/1FAIpQLSe4KGT8Sh6sJ7hedQRuIYirOoZK_85miz3dw7vA1-YjodgJ-A/viewform?usp=sf_link)

All codes and tutorials are open source on github: [github.com/WTFAcademy/WTF-HTML](https://github.com/WTFAcademy/WTF-HTML)

---

Hyperlinks are a basic feature in HTML that link to other parts of a web page, or to other web pages, or even other websites. In this chapter, we will explain in detail how to use hyperlinks in HTML.


## Create hyperlink

Hyperlinks are primarily created in HTML through the `<a>` tag. The `<a>` tag generally contains some text or images, which will become the clickable part of the link. At the same time, we specify the target address of the link through the `href` attribute of the `<a>` tag.

```html
<a href="https://wtf.academy">Visit WTF Academy’s official website</a>
```

Browser effect:

<a href="https://wtf.academy">Visit WTF Academy’s official website</a>

## Add supporting information using the `title` attribute

Another attribute you might want to add to your links is a title; this is intended to contain supplementary information about the link, such as what information the page contains or something to note.

```html
<a href="https://wtf.academy/" title="Web3 open source academy for developers.">Visit the official website of WTF Academy</a>
```

The result is as follows (when the mouse pointer hovers over the link, the title will appear as a tooltip):

<a href="https://wtf.academy/" title="Web3 open source academy for developers.">Visit the official website of WTF Academy</a>

> **Note**
>
> The title of a link is only displayed when the mouse is hovering over it, which means that it is difficult for people using a keyboard to navigate the page to obtain the title information. If title information is important to the page, you should present it in a way that is easily accessible to all users, such as in regular text.

## Set the link opening method

Sometimes, we want to open a new browser window or tab after clicking a link instead of opening it on the current page. This can be achieved via the `target` attribute of the `<a>` tag. If we want the link to open in a new tab, we can set the `target` attribute to `_blank`.

For example:

```html
<a href="https://wtf.academy" target="_blank">Visit WTF Academy’s official website</a>
```

Browser effect:

<a href="https://wtf.academy" target="_blank">Visit WTF Academy’s official website</a>

Clicking on this hyperlink will open the official website of WTF Academy in a new browser tab.

## Anchor link

In a long web page, we may want to create links to some part within the page. This can be achieved through anchor links. First, we need to mark the target location using the `name` or `id` attribute of the `<a>` tag, and then use `#` plus the `name` or `id` value of the target in the `href` attribute of the link to create the link.

For example:

```html
<a name="section1"></a>
<!-- Some content -->
<a href="#section1">Jump to section1</a>
```

Browser effect:

<a name="section1"></a>
<a href="#section1">Jump to section1</a>


Clicking this hyperlink will jump to the `section1` part of the page.


## Email link

In addition to linking to other web pages, the `<a>` tag can also link to an email address. By adding `mailto:` before the `href` attribute value, you can create a link that when clicked launches the user's default mail client and creates a new email.

For example:

```html
<a href="mailto:example@example.com">Send email to example@example.com</a>
```

This hyperlink, when clicked, will launch the user's mail client and create a new email sent to `example@example.com`.

## Download link

```html
<a href="https://wtf.academy/img/wtflogo.png" download="wtflogo">Download WTFAcademy logo</a>
```

<a href="https://wtf.academy/img/wtflogo.png" download="wtflogo">Download WTFAcademy logo</a>


## Summary

In this chapter, we introduce how to create and use hyperlinks in HTML, including normal links, links that open in new tabs, email links, and anchor links. Understanding and mastering hyperlinks is an important step in learning HTML. It allows your web pages to connect to other web pages or other parts within the page.
