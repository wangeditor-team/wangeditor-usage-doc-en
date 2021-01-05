# Destroy Editor
You can destory editor instanc by using `editor.destroy()`. The following example of Vue2.0:

```js
import E from 'wangeditor'

export default {
  data() {
    return {
      editor: null
    }
  },
  mounted() {
    // create editor
    this.editor = new E(`#demo`)
    this.editor.create()
  },
  beforeDestroy() {
    // destroy editor
    this.editor.destroy()
    this.editor = null
  }
}
```