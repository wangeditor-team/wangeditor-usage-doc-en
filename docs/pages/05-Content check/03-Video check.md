# Video Check
You can use `editor.config.linkVedioCheck` to customize check rules of network video.

```jsx
const E = window.wangEditor
const editor = new E('#div1')

// custom check rules of network video
editor.config.linkImgCheck = function(video) {
        // Have three case
		
		// 1. If return true,mean that check passed.
    return true
		//2. If return string, mean that check failed. this case editor will stop insert video, and alert error info(when return string).
        // return 'video have xxx error'.
		
		// If return undefined, mean that check failed. this case editor will stop insert video.
 		// In this case, you can customize error info.
}

editor.create()
```