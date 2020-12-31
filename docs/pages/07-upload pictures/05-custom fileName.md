# Custom fileName
You can customize the value of the `fileName` while uploading pictures, that means When using `formData.append(name, file)` to add a picture, the first parameter can be set by yourself.

```javascript
editor.config.uploadFileName = 'your-custom-fileName'
```