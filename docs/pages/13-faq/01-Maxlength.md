# Maxlength
#### wangEdit cannot implement `max-length` currently.
There is no standard implementation of `max-length`.

`max-length` is commonly used to limit pure text like `<input>` and `<textarea>`. But rich text editor contains image, code, table etc.

If you really need to `max-length` the rich text edit, you can get the text by `editor.txt.text()`, and check the length of text in `onchange` event handler.

If you have a better idea, welcome [issues](https://github.com/wangeditor-team/wangEditor/issues).

