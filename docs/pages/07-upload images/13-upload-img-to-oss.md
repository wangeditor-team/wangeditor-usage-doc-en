# Upload Img to OSS
You can reference [upload image by yourself](./10-upload%20images%20by%20yourself.md) to achieve the feature of uploading img to OSS service.

First, you should install [OSS tool](https://help.aliyun.com/document_detail/64041.html?spm=a2c4g.11186623.6.1463.7729677aEdDm5v) then coding as follows:

```js
// Every value should be got from Alibaba Cloud's control panel
let client = new OSS({
  // region: '<Your region>',
  // accessKeyId: '<Your AccessKeyId>',
  // accessKeySecret: '<Your AccessKeySecret>',
  // bucket: 'Your bucket name',
});

editor.config.customUploadImg = function (resultFiles, insertImgFn) {
    // resultFiles is files that input select.
    // insertImgFn is a function that get img url to insert editor.
    client.put('myImg', resultFiles[0])
      .then(function (res) {
        // Uploading img and return result, then insert img to editor.
        insertImgFn(res.url)
      }).catch(function (err) {
        console.log(err)
      })
}
```

In China, most of developers use Alibaba Cloud service, but you can choose cloud service which you like.