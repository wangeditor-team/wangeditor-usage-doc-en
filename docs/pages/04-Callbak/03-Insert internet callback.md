# Insert internet image callback

```jsx
const E = window.wangEditor
const editor = new E('#div1')

// callback of insert internet image
editor.config.linkImgCallback = function (src) {
    console.log('img src ', src)
}

editor.create()
```