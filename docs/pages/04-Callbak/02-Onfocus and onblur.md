# Onfocus and Onblur
Editable area focus callback and blur callback.

```jsx
const E = window.wangEditor
const editor = new E('#div1')

editor.config.onblur = function (newHtml) {
    console.log('onblur', newHtml) // get latest html content
}
editor.config.onfocus = function (newHtml) {
    console.log('onfocus', newHtml) //  get latest html content
}

editor.create()
```