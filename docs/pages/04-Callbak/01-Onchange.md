# onchange

## Set Onchange Callback

When the `onchange` function set, it will be executed automatically after the content change due to user's actions, such as mouse click, keyboard typing and so on.

In the default case , `onchange` will executed automatically when the use does not operate for 200ms. If you want change delay time of `onchange`, you can use `editor.config.onchangeTimeout` property. More info about it, you can see `set history config`.

```jsx
const E = window.wangEditor
const editor = new E("#div1")

// set onchange callback
editor.config.onchange = function (newHtml) {
    console.log('new html when change before', newHtml)
}
// set the execution frequency of onchange, it's initialized to 200 milliseconds.
editor.config.onchangeTimeout = 500 // 修改为 500ms

editor.create()
```