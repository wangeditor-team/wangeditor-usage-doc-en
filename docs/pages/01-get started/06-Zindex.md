# ZIndex

You can use `editor.config.zIndex` to change editor `z-index` . By default, the editor `z-index` is 1000.

<span style="color: red;">Note：</span> `z-index` Need ` >= 0`

```jsx
const editor = new E('#div1')

editor.config.zIndex = 500

editor.create()
```