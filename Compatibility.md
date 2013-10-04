## Other places where *Markdown Here* works

Besides Thunderbird, Gmail, Hotmail, and Yahoo.

If you find a new problem (or improvement!), or if you find a site that (almost) works, or if you have workflow suggestions, please edit this wiki page, or create a [Github issue](https://github.com/adam-p/markdown-here/issues), or post to the [MDH Google Group](https://groups.google.com/forum/#!forum/markdown-here).

### The "Works Great" Bucket

##### Google Groups

*Markdown Here* works with Google Groups posts. You can use it in the GG rich compose box, or when you're posting via email. One caveat: Digest emails strip all styling. 

##### Evernote

[A user discovered](https://github.com/adam-p/markdown-here/issues/30#issuecomment-8119861) that Markdown Here works in the [Evernote](https://www.evernote.com) web interface. 

##### Blogger

As of version 2.9.0, [earlier problems](https://github.com/adam-p/markdown-here/issues/89) are fixed and [Blogger](http://blogger.com/) is working well. Part of the fix came from changes to the default styling. If you've never customized your CSS, you should click the "Reset to Default" button for the "Primary Styling CSS". If you have customized your CSS, you can [take a look at the default CSS](https://github.com/adam-p/markdown-here/blob/master/src/common/default.css) and decide what to take.

Minor caveat: Some syntax highlighting themes with dark backgrounds don't seem to show up properly. There's an example at the bottom of [this post](http://adampersand.blogspot.ca/2013/10/mdh-test-better-blogger.html).

Thanks to [lambdaalice](https://github.com/lambdalice) for originally [reporting](https://github.com/adam-p/markdown-here/issues/89) that MDH worked with Blogger and for detailing the previous bad behaviour.

##### Wordpress

As of version 2.9.0, earlier problems are fixed and [Wordpress](http://wordpress.com/) is working well. Part of the fix came from changes to the default styling. If you've never customized your CSS, you should click the "Reset to Default" button for the "Primary Styling CSS". If you have customized your CSS, you can [take a look at the default CSS](https://github.com/adam-p/markdown-here/blob/master/src/common/default.css) and decide what to take.

Caveats and tips:
* The most annoying this is that, while editing, hitting `Enter` creates a new paragraph and hitting `Shift+Enter` creates a simple newline. The former is easier, but looks weirder while you're editing. *Markdown Here* doesn't mind which you use, but be consistent. 
* The Wordpress "Preview" button is your friend. What you see there (but not so much in the edit box) is what you get.
* In the Wordpress editor, pasting plain-text is *not* the same as typing. When pasting multi-line text, line breaks (`<br>`) are inserted; when typing, paragraphs (`<p>`) are created. MDH is fine with either, as long as their consistent within the stuff that it's trying to render.
* After rendering, inline code appears in a non-monospace font, but it is correctly monospace in the preview and in the finished post.
* Like with the Yahoo rich controls, if the paragraph type combo is clicked, focused-element finding gets busted and Markdown Toggle stops working. See [issue #16](https://github.com/adam-p/markdown-here/issues/16).

Thanks to [Sina Iravanian](https://plus.google.com/116422808039109985732/posts) for originally discovering that MDH works with Wordpress.


### Postbox

[Postbox](http://www.postbox-inc.com/) is a non-free desktop email client based on Thunderbird, and user [markgoodson](https://github.com/markgoodson) requested that *Markdown Here* [support it](https://github.com/adam-p/markdown-here/issues/30). The Mozilla extension now works with it, but with some major caveats:

* There's no options page. However, you can open the "Config Editor" from the Preferences dialog and copy/paste options from Firefox's or Thunderbird's equivalent config editor (`about:config` in Firefox, "Config Editor" in Thunderbird). *Note*: Make them all string values. 
  * I just couldn't figure out how to open a tab with the options page. This will probably require the assistance of Postbox or someone familiar with developing for it.
* Line breaks can appear mysteriously in code blocks. Postbox seems to insert unescaped newlines into the raw email when sending, which cause problems if they appear in the middle of a `<pre>` block.
* Gmail and Thunderbird reply exclusion doesn't work in Postbox. It doesn't seem to put the original email in a `<blockquote>`. You will have to use *Markdown Here's* [selection conversion](https://github.com/adam-p/markdown-here#selectionpiecemeal-conversion), like with Yahoo and Hotmail.
* Postbox won't be a first-class client for *Markdown Here*, partly because my trial license for it expires soon. If something breaks, create an issue.