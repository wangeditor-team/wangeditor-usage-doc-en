# The Callback

You can use the callback function to handle the different stages of uploading images. The code example is as follows.

```javascript
editor.config.uploadImgHooks = {
    // before upload
    before: function(xhr) {
        console.log(xhr)

        // You can prevent users from uploading.
        return {
            prevent: true,
            msg: 'the msg for user'
        }
    },
    // The image is uploaded and the result is returned, the image is inserted successfully.
    success: function(xhr) {
        console.log('success', xhr)
    },
    // The image has been uploaded and server has returned the result, but an error occurred when inserting the image.
    fail: function(xhr, editor, resData) {
        console.log('fail', resData)
    },
    // Error uploading images, it is usually http request error
    error: function(xhr, editor, resData) {
        console.log('error', xhr, resData)
    },
    // Timeout while uploading images
    timeout: function(xhr) {
        console.log('timeout')
    },
    // The image is uploaded and the result is returned, and I want to insert the image into the editor by myself.
    // For example, the format returned by the server is not `{errno: 0, data: [...] }` this style, you can use `customInsert`.
    customInsert: function(insertImgFn, result) {
        // `result` is the interface returned by th server.
        console.log('customInsert', result)

        // `insertImgFn` can insert images into the editor, pass in the image's src and execute the function.
        insertImgFn(result.data[0])
    }
}
```