# Split toolbar and editing area

Toolbar and editing area allows to separated in wangEditor.

Because Toolbar and editing area is controlled element in wangEditor, you can customize styles such as fixed toolbar、auto add editing area height and so on.

```
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