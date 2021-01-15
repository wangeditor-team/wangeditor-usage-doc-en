# Upload Images by Yourself

If you want to completely implement the image upload process yourself, such as uploading a image to a cloud server, you can use the following code.

```javascript
editor.config.customUploadImg = function (resultFiles, insertImgFn) {
    // `resultFiles` is the file list selected in input.
    // insertImgFn is the function to insert into the editor after getting the images's url

    // upload the image, and return the result, then insert the image into the editor
    insertImgFn(imgUrl)
}
```