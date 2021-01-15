# Custom FileName
You can customize the value of the `fileName` while uploading images, that means When using `formData.append(name, file)` to add a image, the first parameter can be set by yourself.

```javascript
editor.config.uploadFileName = 'your-custom-fileName'
```