# The callback

You can use the callback function to handle the different stages of uploading pictures. The code example is as follows.

```javascript
editor.config.uploadImgHooks = {
    // before upload
    before: function(xhr) {
        console.log(xhr)

        // You can prevent users from uploading.
        return {
            prevent: true,
            msg: '需要提示给用户的错误信息'
        }
    },
    // The picture is uploaded and the result is returned, the picture is inserted successfully.
    success: function(xhr) {
        console.log('success', xhr)
    },
    // The picture has been uploaded and server has returned the result, but an error occurred when inserting the picture.
    fail: function(xhr, editor, resData) {
        console.log('fail', resData)
    },
    // Error uploading pictures, it is usually http request error
    error: function(xhr, editor, resData) {
        console.log('error', xhr, resData)
    },
    // Timeout while uploading pictures
    timeout: function(xhr) {
        console.log('timeout')
    },
    // The picture is uploaded and the result is returned, and I want to insert the picture into the editor by yourself.
    // For example, the format returned by the server is not `{errno: 0, data: [...] }` this style, you can use `customInsert`.
    customInsert: function(insertImgFn, result) {
        // `result` is the interface returned by th server.
        console.log('customInsert', result)

        // `insertImgFn` can insert pictures into the editor, pass in the picture's src and execute the function.
        insertImgFn(result.data[0])
    }
}
```