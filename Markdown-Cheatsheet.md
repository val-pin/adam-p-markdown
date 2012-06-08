This is intended as a very quick reference and showcase. For more complete info, see [John Gruber's original spec](http://daringfireball.net/projects/markdown/) and the [Github-flavored Markdown info page](http://github.github.com/github-flavored-markdown/).

This is specifically **Github-flavored Markdown**.

Note that the styling *Markdown Here* uses might vary from what Github uses (so, what you see below). But it should be pretty close.

## Header Text

```no-highlight
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

# H1
## H2
### H3
#### H4
##### H5
###### H6

## Emphasis

```no-highlight
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.
```

Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

## Lists

```no-highlight
1. Ordered list
2. Another item
  * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
  1. Ordered sub-list
4. And another item.  
   
   Some text that should be intended to be aligned with the above item.

* Unordered list can use asterisks
- Or minuses
+ Or pluses
```

1. Ordered list
2. Another item
  * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
  1. Ordered sub-list
4. And another item.  
   
   Some text that should be intended to be aligned with the above item.

* Unordered list can use asterisks
- Or minuses
+ Or pluses

## Links

There are two ways to do links.

```no-highlight
[I'm an inline-style link](https://www.google.com)

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself][]

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com
```

[I'm an inline-style link](https://www.google.com)

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself][]

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com

## Images

```no-highlight
Here's our logo:

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Title text")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Title text"
```

Here's our logo:

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Title text")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Title text"

## Code and Syntax Highlighting

```no-highlight
Inline `code` has `back-ticks around` it.
```

Inline `code` has `back-ticks around` it.

Blocks of code are either fenced by lines with three back-ticks <code>```</code>, or are indented with four spaces. I recommend only using the fenced code blocks -- they're easier and only they support syntax highlighting.

```no-highlight
 ```javascript
 var s = "JavaScript syntax highlighting";
 alert(s);
 ```
 
 ```python
 s = "Python syntax highlighting"
 print s
 ```
 
 ```
 No language indicated, so no syntax highlighting. But let's throw in a <b>tag</b>.
 ```
```

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

```python
s = "Python syntax highlighting"
print s
```

```
No language indicated, so no syntax highlighting in Markdown Here (varies on Github). But let's throw in a <b>tag</b>.
```

To see what languages are available for highlighting, and how to write those language names, see the [highlight.js demo page](http://softwaremaniacs.org/media/soft/highlight/test.html).

## Blockquotes

```no-highlight
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 
```

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 

## HTML

You can also use raw HTML in your Markdown, and it'll mostly work pretty well. Here are a couple of common examples:

```no-highlight
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>

<table>
  <tr>
    <th></th>
    <th>Tables</th>
    <th>Are</th>
    <th>Cool</th>
  </tr>
  <tr>
    <th>Zebra</th>
    <td>Stripes</td>
    <td>Are</td>
    <td>Pretty</td>
  </tr>
  <tr>
    <th>Here</th>
    <td>Is</td>
    <td>Another</td>
    <td>Row</td>
  </tr>
</table>
```

<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>

<table>
  <tr>
    <th></th>
    <th>Tables</th>
    <th>Are</th>
    <th>Cool</th>
  </tr>
  <tr>
    <th>Zebra</th>
    <td>Stripes</td>
    <td>Are</td>
    <td>Pretty</td>
  </tr>
  <tr>
    <th>Here</th>
    <td>Is</td>
    <td>Another</td>
    <td>Row</td>
  </tr>
</table>

Github-flavored Markdown supports a special table syntax, but *Markdown Here* does not support it yet. [There's an issue for it.](https://github.com/adam-p/markdown-here/issues/13)


## Horizontal Rule

```
Three or more...

---

Hyphens

***

Asterisks

___

Underscores
```

Three or more...

---

Hyphens

***

Asterisks

___

Underscores