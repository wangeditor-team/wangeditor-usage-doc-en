# Event hooks in the editing area

## What it is

If you want to monitor various event callbacks in the editing area, such as mouse click, keyup, paste, click image, click link, scroll, etc., you don’t need to write it yourself. The editor is all defined and open to use.

```
// eventHooks 
{
    dropEvents: Function[]
    clickEvents: Function[]
    keyupEvents: Function[]
    tabUpEvents: Function[] // tab （keyCode === ）Up 
    tabDownEvents: Function[] // tab （keyCode === 9）Down 
    enterUpEvents: Function[] // enter （keyCode === 13）up 
    deleteUpEvents: Function[] // del（keyCode === 8）up 
    deleteDownEvents: Function[] // del（keyCode === 8）down 
    pasteEvents: Function[] // paste
    linkClickEvents: Function[] // click
    textScrollEvents: Function[] // scroll
    toolbarClickEvents: Function[] // click toolbarl
    imgClickEvents: Function[] //click image
    // etc
}
```

For all eventHooks and the internal implementations, please refer to [code](https://github.com/wangeditor-team/wangEditor/blob/master/src/text/index.ts#L13)

## How to use 

Using eventHooks is very simple, for example, it is used in the [linked tooltip source code](https://github.com/wangeditor-team/wangEditor/blob/master/src/menus/link/bind-event/tooltip-event.ts). Define a function and push to the corresponding eventHooks.

```
// function showLinkTooltip() { /* show tooltip */ }
// function hideLinkTooltip() { /* hide tooltip */ }

//  click link to show tooltip
editor.txt.eventHooks.linkClickEvents.push(showLinkTooltip)

// click other place ，like keyupEvents，or scroll，to hide tooltip
editor.txt.eventHooks.clickEvents.push(hideLinkTooltip)
editor.txt.eventHooks.keyupEvents.push(hideLinkTooltip)
editor.txt.eventHooks.toolbarClickEvents.push(hideLinkTooltip)
editor.txt.eventHooks.textScrollEvents.push(hideLinkTooltip)
```