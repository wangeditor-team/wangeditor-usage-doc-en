# Insert event of network video

After inserting network video, you can customize check rule of video use `editor.config.onlineVideoCallback`.

```jsx
const E = window.wangEditor
const editor = new E('#div1')

// 自定义检查插入视频的回调
editor.config.onlineVideoCallback = function (video) {
// you can customize content of callback after inserting a video successfully.
  console.log('video content', video)
}

editor.create()
```