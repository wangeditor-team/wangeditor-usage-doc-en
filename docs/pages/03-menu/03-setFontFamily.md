# Set Font Size

You can set font family to use `editor.config.fontNames`:

```js
const E = window.wangEditor
const editor = new E('#div1')

editor.config.fontNames = [
    // object type
     {name:"Custom font name",value:"Arial"},
    // string type
    'Arial'
    'Tahoma',
    'Verdana',
    'Times New Roman',
    'Courier New',
]

editor.create()
```
