# WangEditor

<!-- Badge -->
![Forks badge](https://img.shields.io/badge/Forks-2.4k-green)
![Stars badge](https://img.shields.io/badge/stars-10.8K-brightgreen)
![cypress badge](https://img.shields.io/badge/E2E-Cypress-brightgreen)
![jest badge](https://img.shields.io/badge/unit%20test-jest-yellowgreen)
![build badge](https://github.com/wangeditor-team/wangEditor/workflows/build/badge.svg)
![ICS License](https://img.shields.io/badge/License-ISC-blue)

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="http://www.wangeditor.com/">
    <img src="http://www.wangeditor.com/imgs/logo.jpeg" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">wangEditor</h3>

  <p align="center">
    A lightweight rich text editor, friendly API and use extremely conventient.
    <br />
    <a href="http://www.wangeditor.com"><strong>Offical website</strong></a>
    ·
    <a href="https://doc.wangeditor.com/"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://doc.wangeditor.com/">Chinese Docs</a>
    ·
    <a href="https://codepen.io/collection/DNmPQV">View Demo</a>
    ·
    <a href="https://github.com/wangeditor-team/wangEditor/issues/new?template=bug.md">Report Bug</a>
    ·
    <a href="https://github.com/wangeditor-team/wangEditor/issues/new?template=feature.md">Request Feature</a>
  </p>
</p>

<!-- ABOUT THE PROJECT -->
## About The Project

wangEditor is a web rich text editor that use typescript develop. It's lightweight, simple, use convience and open source.

It support most of modern browsers: Chrome, Firefox, Safar, Edge, QQ, IE11 and so on.

It doesn't support mobile browers.

![Product Name Screen Shot](./images/demo.jpg)

## Usage

### Use NPM Package
```sh
npm install wangeditor --save
``` 
A few lines code for creating editor instance：

```js
import E from "wangeditor";
const editor = new E("#div1");
editor.create();
```

### Use CDN
```html
<script type="text/javascript" src="https://unpkg.com/wangeditor/dist/wangEditor.min.js"></script>
<script type="text/javascript">
  const E = window.wangEditor
  const editor = new E('#div1')
  // or const editor = new E(document.getElementById('div1'))
  editor.create()
</script>
```

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**. Before contributing wangEditor, You must read [contribution](./docs/contribution.md) docs.

<!-- LICENSE -->
## License

Distributed under the MIT License. See [MIT License](https://en.wikipedia.org/wiki/MIT_license) for more information.

<!-- CONTACT -->
## Contact

Wangfupeng - wangfupeng1988@163.com

Project Link: [https://github.com/wangeditor-team/wangEditor](https://github.com/wangeditor-team/wangEditor)

## Developer Team
We have a professional developer team, if you want to join us, you can send email to `wangfupeng1988@163.com`.

If you are a chinese developer, you can join our QQ group or read [chinese](./README-zh-cn.md) docs for more information.

## Support Us

Your support will encourage us to output more quality content.

![](https://raw.githubusercontent.com/wangeditor-team/wangEditor/docs-en-lang/docs/imgs/ali-pay.jpeg)
![](https://raw.githubusercontent.com/wangeditor-team/wangEditor/docs-en-lang/docs/imgs/wechat-pay.jpeg)
