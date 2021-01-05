# Content API
If want to know common use about content, you can reference following docs: [content](../02-deal%20content/01-setContent.md).

## editor.cmd.do(name: string, value: string)
Inserting text at cursor position.

`editor.cmd.do(name, value)` API is equal to invoke browser native API: `document.execCommand(name, false, value)`, you can leran more about it to visit following link: [docs](https://developer.mozilla.org/zh-CN/docs/Web/API/Document/execCommand).