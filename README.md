# 2.x Version Blog
from 2016，create a new version 2.x for blog，fit almost all the screens.
- React + Redux + DvaJS + UmiJS等
- Preview(2.x)： http://kquanr.com/2.x
- 3.x：http://kquanr.com
- 1.x：http://kquanr.com/1.x
- more...
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
$ npm start # visit http://localhost:8000

#线上部署
测试环境：
$ npm run build(可选)
$ ssh 

#Issue
npm install可能会出现部分依赖包安装不上的情况，可以试下国内代理的方式：npm install --registry=https://registry.npm.taobao.org