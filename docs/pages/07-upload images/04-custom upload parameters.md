# Custom Upload Parameters

Some parameters can be customized when uploading images, such as `token` which used to pass verification. These parameters will be added to `formData`, then the whole will be uploaded to the server.

```javascript
editor.config.uploadImgParams = {
    token: 'xxxxx',
    x: 100
}
```

If you need to splice parameters into url, you can add the following configuration.

```javascript
editor.config.uploadImgParamsWithUrl = true
```