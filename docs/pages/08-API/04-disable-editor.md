# Disable Editor

**Note it is supported from v4.1.0.**

If you disabled editor, you only can read content, and do not edit it. You can edit content after canceling disabled.

```js
// create editor
const E = window.wangEditor
const editor = new E('#div1')
editor.create()

// Disabled editor by disable API
$btn1.click(() => {
  editor.disable()
})

// Cancel disabled by enable API
$btn2.click(() => {
  editor.enable()
})
```