# Insert internet video callback

When insert internet video after, you can custom check video callback use `editor.config.onlineVideoCallback`.

```jsx
const E = window.wangEditor
const editor = new E('#div1')

// custom insert video callback
editor.config.onlineVideoCallback = function (video) {
 	// emit this callback when insert video success
    // you can custom this callback content.
  console.log('insert video content', video)
}

editor.create()
```