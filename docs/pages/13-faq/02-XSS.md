# XSS

Rich text editor is easily attacted by attackers.

We recommand use [xss](https://www.npmjs.com/package/xss) tool.

```javascript
const html = editor.txt.html()
const safeHtml = xss(html)
console.log('filtered html', safeHtml)
```

