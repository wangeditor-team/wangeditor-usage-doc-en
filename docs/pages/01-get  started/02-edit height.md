# Editable area height

You can use `editor.config.height` property to change editable area height in wangEditor. By default, the editable area height is `300px`.

```jsx
const editor = new E('#div1')

// set editing area height to 500px
editor.config.height = 500

// notice，you sholud set height before using create()
editor.create()
```