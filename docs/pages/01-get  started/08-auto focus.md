# Auto focus

By default, the editing area will be focused when initializing. If you want to cancel auto focus that using `editor.config.focus`.

You can use `editor.config.focus` to cancel auto focus. For example: 

```jsx
const editor = new E('#div1')

// cancel auto focus
editor.config.focus = false

editor.create()
```