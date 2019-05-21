# 2.x Version Blog
from 2016，create a new version 2.x for blog，fit almost all the screens.
- React + Redux + DvaJS + UmiJS等
- Preview(2.x)： http://kquanr.com/2.x
- 3.x：http://kquanr.com
- 1.x：http://kquanr.com/1.x
- more...

## Usage
* UmiJS：https://umijs.org
* DvaJS：https://dvajs.com
* React：https://reactjs.org
* Sass：http://sass.bootcss.com/docs/sass-reference
* Redux-Devtools（本地开发利器/时间旅行器）：https://github.com/gaearon/redux-devtools
* 脚手架市场：http://scaffold.ant.design

## Features

* 📦 **开箱即用**，内置 react、react-router 等
* 🏈 **类 next.js 且[功能完备](https://umijs.org/guide/router.html)的路由约定**，同时支持配置的路由方式
* 🎉 **完善的插件体系**，覆盖从源码到构建产物的每个生命周期
* 🚀 **高性能**，通过插件支持 PWA、以路由为单元的 code splitting 等
* 💈 **支持静态页面导出**，适配各种环境，比如中台业务、无线业务、[egg](https://github.com/eggjs/egg)、支付宝钱包、云凤蝶等
* 🚄 **开发启动快**，支持一键开启 [dll](https://umijs.org/plugin/umi-plugin-react.html#dll) 和 [hard-source-webpack-plugin](https://umijs.org/plugin/umi-plugin-react.html#hardSource) 等
* 🐠 **一键兼容到 IE9**，基于 [umi-plugin-polyfills](https://umijs.org/plugin/umi-plugin-react.html#polyfills)
* 🍁 **完善的 TypeScript 支持**，包括 d.ts 定义和 umi test
* 🌴 **与 dva 数据流的深入融合**，支持 duck directory、model 的自动加载、code splitting 等等

## Comments
* 2016年接触react和redux栈时用的组合是[react-redux](https://github.com/reactjs/react-redux) + [redux-thunk](https://github.com/gaearon/redux-thunk) ，后来换到[redux-saga](https://redux-saga.js.org)，再后来看到支付宝团队的[新架构方案](https://github.com/sorrycc/blog/issues/6)，便开始着手这方面对的尝试，试着重构博客和写一些商业产品。

* 市面上的前后端轮子和框架是越来越多了，但很多领域还是万变不离其宗吧。就像编程、设计、摄影...很多东西传递的思想和基础也只是在迭代性的发生改变和升级，组件、分治布局、通信、数据交流...，共同组成一个弹性、可扩展的视觉空间。

## Guides
- [airbnb javascript standard](https://github.com/airbnb/javascript)
- [Ant Design introduce](https://ant.design/docs/spec/introduce-cn)
- [JD Front-End Coding Guidelines](https://guide.aotu.io)

## Structure
```
├── package.json       # 项目依赖包及scripts
├── config             # 全局配置入口 - UmiJS
│ ├── config           # 构建及webpack等配置
│ ├── router.config.js # 路由配置
│ ├── plugin.config.js # 插件配置（三方、封装的插件配置）
├── dist               # 打包静态目录(npm run build)
├── src                # 项目业务代码
│ ├── /assets/         # 静态文件
│ ├── /components/     # 公共组件
│ ├── /locales/        # 系统数据配置（Language Data）等配置
│ ├── /layout/         # 平台布局 => header + content + footer + sidebar(可选)
│ ├── /models/         # model数据层 => DvaJS
│ ├── /pages/          # 路由及页面层 => routes + document.ejs(首页模板)
│ ├── /services/       # 服务api
│ ├── /styles/         # 全局样式 => core + mixin + function + theme...
│ ├── /utils/          # 全局工具函数
│ │──global.js         # 全局Index
│ │──global.scss       # 全局Style

- Home(首页)
  - components => Header + content1 + content2 + ... + Footer
  - index.js
  - index.scss

- Exception
  - 403
  - 404
  - 500
  - 110

- User
  - Login
  - Register

```

## Usage

```bash
#本地开发
$ git clone git@github.com:PhotoArtLife/blog2.x-mux-club.git 请选择SSH方式
$ mkdir your-blog-name -> cd your-blog-name 
$ npm install
$ npm start # visit http://localhost:8000（或online ip支持同局域网移动端开发适配）

#线上部署
测试环境：
$ npm run build(可选)
$ ssh 

#Issue
npm install可能会出现部分依赖包安装不上的情况，可以试下国内代理的方式：npm install --registry=https://registry.npm.taobao.org