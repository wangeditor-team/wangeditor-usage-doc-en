# Custom Alert

When you want customize alert that use `editor.config.customAlert` . By default, wangEditor will be invoking `window.alert`.

You can easy to customize alert style:

```jsx
import { message } from 'antd';

const editor = new E('#div1')
// take Ant Design as an example
editor.config.customAlert = function (s, t) {
  switch (t) {
    case 'success':
      message.success(s)
      break
    case 'info':
      message.info(s)
      break
    case 'warning':
      message.warning(s)
      break
    case 'error':
      message.error(s)cus
      break
    default:
      message.info(s)
      break
  }
}

editor.create()
```