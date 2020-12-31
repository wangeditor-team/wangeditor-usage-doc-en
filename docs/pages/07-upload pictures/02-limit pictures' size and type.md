# Limit pictures' size and type

# Limit pictures' size
The default picture size is 5M, you can modify it yourself.
```javascript
editor.config.uploadImgMaxSize = 2 * 1024 * 1024 // 2M
```

# Limit pictures' type
You can push types in `uploadImgAccept` array.
```javascript
editor.config.uploadImgAccept = ['jpg', 'jpeg', 'png', 'gif', 'bmp']
```
