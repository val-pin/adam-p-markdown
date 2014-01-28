Please add any tips and tricks that you come up with. For now it'll be a flat list and we'll add structure as needed.

##### Table of Contents  

[Pasting from Clipboard (without tears)](#pasting)  
[Using SVG for TeX math formulae](#svg)  
[Changing the Main Font (and other overall styles)](#mainfont)  
[Getting fancy with inline HTML](#inlinehtml)  
[Salutation Styling](#salutation)  
[Using Header Anchor Links](#header-anchors)

<a name="pasting" href="#"></a>
Pasting from Clipboard (without tears)
======================

If text is pasted from the clipboard with formatting intact, it can negatively impact the rendering of Markdown (i.e., it can make it super messed up). When pasting into an email that you plan on rendering with Markdown Here, you should try to paste as plain text.

### Windows and Linux

- **Chrome**: Context menu: "Paste as plain text". Hotkey: `Ctrl+Shift+V`.
- **Firefox**: There doesn't seem to be a menu item. Hotkey: `Ctrl+Shift+V`.
- **Thunderbird, Postbox**: _Edit_ menu and context menu: "Paste Without Formatting". Hotkey: `Ctrl+Shift+V`.

(Linux: Tested on Xubuntu.)

### Mac OS X

- **Chrome**: _Edit_ menu and context menu: "Paste and Match Style". Hotkey: ⇧⌘V (`Shift+Command+V`).
- **Firefox**: There doesn't seem to be a menu item. Hotkey: ⇧⌘V (`Shift+Command+V`).
- **Thunderbird, Postbox**: _Edit_ menu and context menu: "Paste Without Formatting". Hotkey: ⇧⌘V (`Shift+Command+V`).


<a name="svg" href="#"></a>
Using SVG for TeX math formulae
======================

The default Google Charts service that Markdown Here uses for TeX math rendering doesn't provide very crisp images. It was chosen because it was thought (by me) to be the least bad option, privacy-wise (because you're probably already using Google for your email).

However, there are other possibilities, if you're will to accept the implications. Setting this in Markdown Here's TeX math option will give you SVG images:

```no-highlight
<img src="https://latex.codecogs.com/svg.latex?{urlmathcode}" alt="{mathcode}">
```

But please note a few important things:

- You're in charge of making sure that you're not violating [CodeCogs' terms of use](http://www.codecogs.com/pages/agreements/termsofuse.php). You should also check out [their privacy policy](http://www.codecogs.com/pages/agreements/privacy_policy.php).

- Understand that CodeCogs will be able to see all of your formulae. They can also do things map your IP address to your formulae. And then they can record the IP addresses of the people that read your email and view the formulae. And so they can draw some conclusions that someone at your IP address working with people at your friends' IP addresses.

For more discussion and technical info, see [issue #144](https://github.com/adam-p/markdown-here/issues/144).


<a name="mainfont" href="#"></a>
Changing the Main Font (and other overall styles)
======================

In the "Primary Styling CSS" section of the Markdown Here options page, there is a rule for `.markdown-here-wrapper` (that's empty by default). This rule should be used for styles that you want applied to your entire email (overridden by other styles, of course). 

So, if you wanted Verdana as your default font, you could set this:

```
.markdown-here-wrapper {
  font-family: Verdana, sans;
}
```
and this (if you want to apply the new font not only to the first row of your tables):
```
table tr th, table tr td {
  font-family: Verdana, sans;
  ...
}
```

![main font example](https://f.cloud.github.com/assets/425687/588697/75922c86-c992-11e2-8071-f42f40295e3c.gif)


<a name="inlinehtml" href="#"></a>
Getting fancy with inline HTML
======================

Markdown (and Markdown Here) allows for inline HTML tags to be used when writing the Markdown, and having them preserved when rendering. This provides you with the ability to add more powerful styling than is possible with Markdown or email alone.

You probably don't want to use these tricks too often, since they involve a lot more (and less natural) typing than normal Markdown, but they can let you do very powerful things that you can't otherwise.

**PLEASE NOTE:** _Always test_ to your fancy styles and HTML tags by sending an email that uses them to yourself and then viewing the email. Some email clients strip out some styles, so it might look good when you send it, but not when you receive it.

### HTML Tags

Some HTML tags that aren't available in a normal email client can be used if typed directly. For example, you can get superscripts and subscripts like this:

```
hi<sup>1</sup> low<sub>2</sub>
```

The result will look like this: hi<sup>1</sup> low<sub>2</sub>

TODO: More examples?

### Custom CSS classes

In Markdown Here's "Primary Styling CSS" you can create custom CSS classes that apply to `<span>` elements that you use inline. 

Let's say you want to the background color of some text in your email to be a nice gradient from light blue to light pink and have a big horrible border. You could create a CSS rule like this:

```
.hi {
  background: linear-gradient(225deg, lightpink, lightblue);
  border: thick dotted purple;
} 
```

And then use it in your email something like this:

```
Happy <span class="hi">Birthday</span> my friend!
```

(The preview of it won't show properly here, but try it out yourself in your email.)

TODO: More compelling, less ridiculous examples.


<a name="salutation" href="#"></a>
Salutation Styling
==================

If you want to style the salutation of your email differently from the rest of the email, you can add a CSS rule that applies to the very first paragraph like so:

```css
.markdown-here-wrapper:first-of-type > p:first-of-type {
  color: red;
}
```

<a name="header-anchors" href="#"></a>
Using Header Anchor Links
=========================

[Stub. Someone (like me or Casey) should fill this in. Also, this section should probably not be at the bottom of the page -- it should probably be second or third.]
