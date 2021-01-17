# Limit Images' Size and Type

# Limit Images' Size
The default image size is 5M, you can modify it yourself.
```javascript
editor.config.uploadImgMaxSize = 2 * 1024 * 1024 // 2M
```

# Limit Images' type
You can push the accepted types in `uploadImgAccept` array.
```javascript
editor.config.uploadImgAccept = ['jpg', 'jpeg', 'png', 'gif', 'bmp']
```
