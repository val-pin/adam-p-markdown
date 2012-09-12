## Other places where *Markdown Here* works

Besides Thunderbird, Gmail, Hotmail, and Yahoo.

Please add any that you find, or more info/caveats about the existing ones!

### Google Groups

*Markdown Here* works with Google Groups posts. You can use it in the GG rich compose box, or when you're posting via email. One caveat: Digest emails strip all styling. 

### Wordpress

Discovered by user [Sina Iravanian](https://plus.google.com/116422808039109985732/posts): *Markdown Here* works in the web-based editor for [Wordpress](http://wordpress.com) posts. Caveats and tips (based on observations with default Wordpress styling):

* The Wordpress "Preview" button is your friend. What you see there (but not so much in the edit box) is what you get.
* Hitting `Enter` creates a new paragraph. When writing Markdown, this probably isn't what you want, and it causes some problems, like extra newlines in code blocks. `Shift + Enter` to the rescue -- it enters just a newline instead of a paragraph.
* When pasting text, leading spaces are lost. This seriously unfortunate, since leading spaces are significant to Markdown and to code.
  * Trailing spaces are also lost (collapsed to a single space). This is also unfortunate, since two trailing spaces are a forced newline in Markdown.
* Code blocks get an extra box around them.
* After Markdown-Toggling, fonts don't look right. Some of the syntax in a code block will be non-monospace, and all (or most?) of the normal text will appear in the default Wordpress font, rather than the font set in your *Markdown Here* options. But if you preview or post, the font will back to what's in the options (including the code blocks).
  * There are two instances (that I've found) where the font isn't right even the final post: `<h3>` and `<blockquote>`. Which is pretty weird.
* Definition lists (`<dl>`) aren't styled quite according to the options CSS.

Here's an example, using the options page sample Markdown: http://adampritch.wordpress.com/2012/09/11/4/

### Evernote

[A user discovered](https://github.com/adam-p/markdown-here/issues/30#issuecomment-8119861) that Markdown Here works in the [Evernote](https://www.evernote.com) web interface. 

Caveat: It seems that newlines are stripped out of code blocks, so they display as a single line.

### Postbox

[Postbox](http://www.postbox-inc.com/) is a non-free desktop email client based on Thunderbird, and user [markgoodson](https://github.com/markgoodson) requested that *Markdown Here* [support it](https://github.com/adam-p/markdown-here/issues/30). The Mozilla extension now works with it, but with some major caveats:

* There's no options page. However, you can open the "Config Editor" from the Preferences dialog and copy/paste options from Firefox's or Thunderbird's equivalent config editor (`about:config` in Firefox, "Config Editor" in Thunderbird). *Note*: Make them all string values. 
  * I just couldn't figure out how to open a tab with the options page. This will probably require the assistance of Postbox or someone familiar with developing for it.
* Line breaks can appear mysteriously in code blocks. Postbox seems to insert unescaped newlines into the raw email when sending, which cause problems if they appear in the middle of a `<pre>` block.
* Gmail and Thunderbird reply exclusion doesn't work in Postbox. It doesn't seem to put the original email in a `<blockquote>`. You will have to use *Markdown Here's* [selection conversion](https://github.com/adam-p/markdown-here#selectionpiecemeal-conversion), like with Yahoo and Hotmail.
* Postbox won't be a first-class client for *Markdown Here*, partly because my trial license for it expires soon. If something breaks, create an issue.