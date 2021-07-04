# Onchange

## Set Onchange Callback

When the `onchange` function set, it will be executed automatically after the content change due to user's actions, such as mouse click, keyboard typing and so on.

In the default case , `onchange` will executed automatically when the use does not operate for 200ms. If you want change delay time of `onchange`, you can use `editor.config.onchangeTimeout` property. More info about it, you can see [set history config](../02-deal content/07-history.md)

```jsx
const E = window.wangEditor
const editor = new E("#div1")

// set onchange callback
editor.config.onchange = function (newHtml) {
    console.log('new html when change before', newHtml)
}
// set the execution frequency of onchange, it's initialized to 200 milliseconds.
editor.config.onchangeTimeout = 500 // Change to 500 ms

editor.create()
```

# onSelectionChange

## Set onSelectionChange Callback

v4.7.5+

When the `onSelectionChange` function set,the user's selection operation (mouse select text, Ctrl + a select all ...) will automatically trigger the `onSelectionChange` function 

Three callback parameters are `text`, `HTML` and `selection`, which are `currently selected text`, `currently selected HTML` and `native selection object`

```js
const E = window.wangEditor;
const editor = new E("#div1");
// set onSelectionChange callback
editor.config.onSelectionChange = function (newSelection) {
  console.log("onSelectionChange", newSelection);
  /**
    {
       text:'wangeditor', // currently selected text
       html: '<p>wangeditor</p>', // currently selected HTML
       selection: selection, // native selection object
    }
   */
};
editor.create();
```

