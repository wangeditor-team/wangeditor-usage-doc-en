# Maxlength
**WangEdit cannot implement `max-length` currently.**

There is no standard implementation of `max-length`.

`max-length` is commonly used to limit pure text like `<input>` and `<textarea>`. But rich text editor contains image, code, table etc. It is more complicated than pure text. Those non text will take a plenty of place in `editor.txt.html()` result.

If you really need to `max-length` the rich text edit, you can get the text by `editor.txt.text()`, then check the length of text in `onchange` event handler, and do what you want. But it may have some unexpected problems, you should play to the score.

If you have a better idea, welcome [issues](https://github.com/wangeditor-team/wangEditor/issues).

