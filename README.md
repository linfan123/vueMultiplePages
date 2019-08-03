# Vue Multiple Pages
基于vue-cli3.0 + webpack@4.28.4的多页脚手架
> 编译速度与热跟新速度要优于webpack2.0、3.0，但相应的消耗内存变大，在node中出现内存溢出现象，如页面过多，使用
```
npm run fix-memory-limit
```
再进行
```
npm run dev
```
## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run dev
```

### Compiles and minifies for production
```
npm run build:dev  //打包开发环境
npm run build:devtest //打包开发测试环境
npm run build:test //打包测试环境
npm run build // 打包正式环境
```
在config里配置不同的打包环境使用不同的api地址等。

> 一个基于vue-cli3脚手架的多页面vue移动端模板

*添加了移动端相关工具如 mint-ui、300s点击延迟、rem、公共头部和底部、less、store、pages/public_app.js，以及微信签名和请求的封装等*


## 目录结构介绍 ##

	|-- dist                             // 打包目录
	|-- src                              // 源码目录
	|   |-- api                          // Api接口目录
	|       |-- user.js           	     //用户登录、头像上传、密码修改等用户相关api
	|   |-- assets                       // 静态资源，你的css、图片、字体等。
	|   |-- components                   //全局组件
	|   |-- config                       // 应用的配置文件
	|       |-- app.js                   // 应用的配置，名字，api请求的url，
	|       |-- page.js           	     // 每一个页面的配置,标题之类的
	|   |-- utils                        // 工具函数。和config,api一个道理，建议分类清楚。
    |       |-- app.js                   // 常用函数
    |       |-- request.js               // 请求封装
	|       |-- weixin.js                // 微信jssdk的封装，使用请先安装weixin-js-sdk
	|       |-- setHtmlFontSize.js       // 设置根元素字体大小，配合rem做屏幕适配
	|   |-- pages                        // 页面视图
	|       |-- index                    // 首页
	|       |-- common.js                // 公共的js，可以引公共的css,vue ui库等
	|-- .gitignore                       // 忽略的文件
	|-- page.config.js                   // 使用node读取pages文件夹下的文件夹配置到vue cli3
	|-- vue.config.js                    // vue cli 配置
	|-- README.md                        // 说明



## 说明
* 在css/common.less里重置样式。
* 添加了axios请求库，并做了简单的拦截。
* 添加了fastclick解决移动端300ms点击延迟。
* 已添加mint-ui库，想要添加自己 UI库,在pages/public_app.js引用即可。
* 添加rem适配移动端，设置的设计稿宽度为750，1rem=30px，可在statics/js/public.js自行修改。
* 添加了vue-lazyload图片懒加载，在pages/public_app.js中查看
* 添加页面请在pages文件夹下新建目录，在里面放置js和.vue（建议复制已有的文件夹修改名字进行开发）。
