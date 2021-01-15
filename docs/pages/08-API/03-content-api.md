# Content API
If you want to know common usage of content, you can reference following docs: [content](../02-deal%20content/01-setContent.md).

## editor.cmd.do(name: string, value: string)
Inserting text at cursor position.

`editor.cmd.do(name, value)` API is equal to browser native API: `document.execCommand(name, false, value)`, you can learn more about it to visit following link: [docs](https://developer.mozilla.org/zh-CN/docs/Web/API/Document/execCommand).