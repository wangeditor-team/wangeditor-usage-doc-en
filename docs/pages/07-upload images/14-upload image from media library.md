# upload image from media library

if you want to upload images from the media library, you can use the following code.

<span style="color: red;">Note:</span> if you set the setting with upload images from the media library and upload images from the local at the same time, <span style="color: red;">upload images from the local will be a failure.</span>

``` javascript
editor.config.uploadImgFromMedia = function () {
  // 1. Call your own media library and display the UI page methods
  // ...
  // 2.Insert the image address returned by the media library into the editor, assuming imgUrl is the image address variable returned by the media

  editor.cmd.do( 'insertHTML', `<img src="${imgUrl}" style="max-width:100%;"/>` )
}
```

## Example
``` html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>wangEditor</title>
    <style>
    </style>
</head>

<body>
    <p>
        wangEditor demo
    </p>
    <div id="div1">
        <p>Welcome to use <b>wangEditor</b> editor</p>
        <p>
            <img src="http://www.wangeditor.com/imgs/logo.jpeg" />
        </p>
    </div>

    <script src="../dist/wangEditor.js"></script>
    <script>
        var E = window.wangEditor
        var editor = new E('#div1')

        editor.config.uploadImgFromMedia = function () {
          // Call your own media library and display the UI page methods
          // Suppose you use the confirm method to simulate calling the media library
          const img = confirm('Call media library ')
          if (img) {
            const imgUrl = 'https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png'
            // Insert the link to the media library callback into the editor using the editor.cmd.do method
            editor.cmd.do(
              'insertHTML',
              `<img src="${imgUrl}" style="max-width:100%;"/>`
            )
          } else {
            console.log('cancel')
          }
        }
        editor.create()
    </script>
</body>

</html>
```