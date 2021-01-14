# Content Source Code
Editor not support 'check source code' and 'edit source code', but you can implement by your self.
We can check and edit content html source code by follow steps:

- Create a `<button>`, get the content html by `editor.txt.html` when click.
- To implement 'checkout source code', then create a `<div>`, putting the content html in and hide editor temporary. If you want to format content html, you can use [highlight.js](https://highlightjs.org/) plugin.
- To implement 'edit source code', then create a `<div>`, putting the content html in and hide editor temporary. If you want to edit content code, you can use [monaco editor](https://microsoft.github.io/monaco-editor/) or [codemirror](https://codemirror.net/).

Note edit source html code may cause XSS.