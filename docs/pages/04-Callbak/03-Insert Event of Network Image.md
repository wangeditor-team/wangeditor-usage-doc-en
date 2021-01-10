# Insert Event of Network Image

```jsx
const E = window.wangEditor
const editor = new E('#div1')

// Insert event of network image
editor.config.linkImgCallback = function (src) {
    console.log('img src ', src)
}

editor.create()
```