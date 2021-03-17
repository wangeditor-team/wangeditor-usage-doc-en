# Set Menu Tooltip

## editor.config.showMenuTooltips

The editor's menu tooltip can be configured via `editor.config.showMenuTooltips`.

```js
const E = window.wangEditor
const editor = new E('#div1')

// Hide menu tooltip
editor.config.showMenuTooltips = false

editor.create()
```

## editor.config.menuTooltipPosition

The upper or lower position can be displayed through the `editor.config.menuTooltipPosition` configuration.

```js
const E = window.wangEditor
const editor = new E('#div1')

// if you want the tooltip appear on top of the menu，you can set: 
editor.config.menuTooltipPosition = 'up' // default configuration

// if you want the tooltip appear on bottom of the menu，you can set:
// editor.config.menuTooltipPosition = 'down'

// Choose one of the above configurations

editor.create()
```