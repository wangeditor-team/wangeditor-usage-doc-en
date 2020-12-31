# Upload pictures by yourself

If you want to completely implement the image upload process yourself, such as uploading a picture to a cloud server, you can use the following code.

```javascript
editor.config.customUploadImg = function (resultFiles, insertImgFn) {
    // `resultFiles` is the file list selected in input.
    // insertImgFn is the function to insert into the editor after getting the picture's url

    // upload the picture, and return the result, then insert the picture into the editor
    insertImgFn(imgUrl)
}
```