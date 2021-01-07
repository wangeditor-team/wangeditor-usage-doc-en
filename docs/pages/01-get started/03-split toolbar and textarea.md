# Split Toolbar and Editable Area

Toolbar and editable area allows to separated in wangEditor.

Because Toolbar and editable area is controlled element in wangEditor, you can customize styles such as fixed toolbar、auto add editing area height and so on.

```html
<head>
    <style>
        .toolbar {
            border: 1px solid #ccc;
        }
        .text {
            border: 1px solid #ccc;
            min-height: 400px;
        }
    </style>
</head>
<body>
    <p>
        container and toolbar split
    </p>
    <div>
        <div id="toolbar-container" class="toolbar"></div>
        <p>------ split line ------</p>
        <div id="text-container" class="text"></div>
    </div>

    <script src="//unpkg.com/wangeditor/dist/wangEditor.min.js"></script>
    <script>
        const E = window.wangEditor
        const editor = new E('#toolbar-container', '#text-container') // transfer two element
        editor.create()
    </script>
</body>
```
From upper code , you can knows that toolbar and editable area is two `div` , that means you can set any style you want.