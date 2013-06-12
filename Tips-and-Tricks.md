Please add any tips and tricks that you come up with. For now it'll be a flat list and we'll add structure as needed.

##### Table of Contents  

[Pasting from Clipboard (without tears)](#pasting)  
[Changing the Main Font (and other overall styles)](#mainfont)  
[Getting fancy with inline HTML](#inlinehtml)  
[Salutation Styling](#salutation)  

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