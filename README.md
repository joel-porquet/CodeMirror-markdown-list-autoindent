# CodeMirror-markdown-list-autoindent

This package is essentially a patch to
[CodeMirror](https://github.com/codemirror/CodeMirror) that adds support for
list auto-indentation in Markdown.

When continuing a list in Markdown, type `<Tab>` to indent the next bullet or
`<Shift-Tab>` to unindent it.

Example:

![Screencast](https://raw.githubusercontent.com/joel-porquet/CodeMirror-markdown-list-autoindent/master/screencast.gif)

## NPM

The package is on
[NPM](https://www.npmjs.com/package/codemirror-markdown-list-autoindent):

```console
$ npm install codemirror-markdown-list-autoindent
```

## Usage

When including CodeMirror in your JS client, add the new `indentlist.js` file:

```HTML
<link rel="stylesheet" href="(path_to_code_mirror)/lib/codemirror.css">
<script src="(path_to_code_mirror)/lib/codemirror.js"></script>
<script src="(path_to_code_mirror)/addon/edit/continuelist.js"></script>
<script src="(path_to_code_mirror)/addon/edit/indentlist.js"></script>
<script src="(path_to_code_mirror)/mode/markdown.js"></script>
```

Then bind the `<Tab>` and `<Shift-Tab>` keys to the right events:

```Javascript
extraKeys: {"Enter": "newlineAndIndentContinueMarkdownList",
            "Tab": "autoIndentMarkdownList",
            "Shift-Tab": "autoUnindentMarkdownList"}
```
