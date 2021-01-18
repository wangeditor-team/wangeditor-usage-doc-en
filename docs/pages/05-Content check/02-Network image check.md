# Network Image Check
You can use `editor.config.linkImgCheck` to customize check rules of network image.

```jsx
const E = window.wangEditor
const editor = new E('#div1')

// Custom check rules of network image
editor.config.linkImgCheck = function(imgSrc) {
    	// Have three case
		
		// 1. If return true,mean that check passed.
    	return true
		//2. If return string, mean that check failed. this case editor will stop insert image, and alert error info(when return string)
    	// return 'image have xxx error'
		
		// If return undefined, mean that check failed. this case editor will stop insert image.
 		// In this case, you can customize error info.
}

editor.create()
```