## Other places where *Markdown Here* works

Besides Thunderbird, Gmail, Hotmail, and Yahoo.

Please add any that you find, or more info/caveats about the existing ones!

### Google Groups

*Markdown Here* works with Google Groups posts. You can use it in the GG rich compose box, or when you're posting via email. One caveat: Digest emails strip all styling. 

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
