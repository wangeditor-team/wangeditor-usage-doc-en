## Set onchange callback

Set `onchange` after , when user operate (include mouse click、keyboard operate and so on.) change content , `onchange` will be auto emit.

If you need change `onchange` delay time( when no operate XXX millisecond before,  `onchange` will be emit)， can access to `onchangeTimeout` set. More info see [history setting](../02-deal\ content/07-history.md).

```jsx
const E = window.wangEditor
const editor = new E("#div1")

// set onchange callback
editor.config.onchange = function (newHtml) {
    console.log('new html when change before', newHtml)
}
// onchange emit time default value is 200ms
editor.config.onchangeTimeout = 500 // change to 500ms

editor.create()
```