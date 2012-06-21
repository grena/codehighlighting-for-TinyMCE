# codehighlighting-for-TinyMCE

## What's this ?
codehighlighting-for-TinyMCE is **a plugin for tinyMCE** editor.

## What does it do ?
It allows you to put some content in your TinyMCE editor which can be colored by SyntaxHighlighter.

## What do I need ?
- This projet is a plugin for TinyMCE, so your naturally need **TinyMCE** ([here](http://www.tinymce.com/))
- This plugin prepare the code to be colored by **SyntaxHighlighter** which you can find [here](http://alexgorbatchev.com/SyntaxHighlighter/).

## How do I use it ?
Just put the **codehighlighting** folder in your TinyMCE plugins folder `tiny_mce/plugins/__here__`.  
No we need to activate the plugin. When you initialize your TinyMCE, please add :
<pre><code>
tinyMCE.init({ 
			remove_linebreaks : false, 
			plugins : "...,...,...,codehighlighting",
			theme_advanced_buttons3 : "...,...,...,codehighlighting",
			extended_valid_elements : "..., pre[class|name]",
			...
});
</code></pre>

- **remove_linebreaks** : By default TinyMCE strips out all the line breaks in your content to create a single line of HTML.
- **plugins** : Because TinyMCE have to know which plugins load.
- **theme\_advanced\_buttons3** : Just the place where TinyMCE have to put the new button.
- **extended_valid_elements** : TinyMCE controls validity of HTML elements, we now allow class and name for `<pre>` elements.

## What else ?
_SyntaxHighlighter Plug-in for Tinymce 3.X is a plugin initially developped by nawaf (see [this link](http://weblogs.asp.net/nawaf/archive/2008/04/10/syntaxhighlighter-plug-in-for-tinymce-3-x-wysiwyg-editor.aspx) ) but the problem is that it uses the `<textarea>` element which it not recognize by SyntaxHighlighter and doesn't offer a lot of option, so I rewrote the plugin to be used with `<pre>` and to be able to use more options that offer **SyntaxHighlighter**.