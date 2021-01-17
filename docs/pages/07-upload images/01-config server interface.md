# Config Server Interface
**Note: If you have trouble in uploading images, please open the browser developer tools and check the error message output by console.error. **

# Config Interface

```javascript
const E = window.wangEditor
const editor = new E('#div1')

// config the address of the interface
editor.config.uploadImgServer = '/upload-img'

editor.create()
```

The image menu of the editor will display the tab and icon of the uploaded image, after the configuration is complete, as shown in the figure below.

![](../../images/upload-img.png)

**It is important that the format of the server's return is!!!**

The interface should return `application/json` format, the format requirements are as follows.

```javascript
{
    // The `error` is an error flag, 0 means no error, other values mean there is an error, it can be obtained through the following monitoring function `fail`, and handle it.
    "errno": 0,

    // This `data`, which returns an address online, is a array.
    "data": [
        "图片1地址",
        "图片2地址",
        "……"
    ]
}
```