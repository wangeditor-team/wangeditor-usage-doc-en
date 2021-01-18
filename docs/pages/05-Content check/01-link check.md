# Link Check
You can use `editor.config.linkCheck` to customize check rules of link.

```jsx
const E = window.wangEditor
const editor = new E('#div1')

// Custom check rule of link
editor.config.linkCheck = function(text, link) {
        // have three case
		
		// 1. If return true,mean that check passed.
    	return true
		//2. If return string, mean that check failed. this case editor will stop insert link, and alert error info(when return string)
        // return 'link have xxx error'
		 
		// If return undefined, mean that check failed. this case editor will stop insert link.
 		// In this case, you can custom error info.
}

editor.create()
```