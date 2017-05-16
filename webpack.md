
### webpack初步认知

---

> [Gulp和webpack的区别（理解+面试）](http://blog.csdn.net/xllily_11/article/details/51782005)

---

### webpack1入门

---

> [Webpack1.x开发模式使用指南（早期细理解，不错）](http://blog.csdn.net/q1056843325/article/details/54600090)

> [webpack入门（早期粗理解）](http://www.w2bc.com/Article/50764?f=cnblog)

> [用Webpack构建React基础工程（较早版本，还行）](http://www.jianshu.com/p/4df92c335617)

> [Webpack傻瓜指南（一）基础知识](https://zhuanlan.zhihu.com/p/20367175?columnSlug=FrontendMagazine)

> [Webpack傻瓜指南（二）开发和部署技巧](https://zhuanlan.zhihu.com/p/20397902?columnSlug=FrontendMagazine)

> [Webpack傻瓜指南（三）和React配合开发](https://zhuanlan.zhihu.com/p/20522487?columnSlug=FrontendMagazine)

> [Webpack 系列（一般）](http://www.cnblogs.com/sloong/p/5826818.html)

> [Webpack多入口文件、热更新等体验（通用内容，2的语法，不错）](http://www.cnblogs.com/cqhaibin/p/6581308.html)

> [webpack1踩过的坑](http://blog.csdn.net/weizengxun/article/details/53448885)

---

### webpack1进阶

---

> [webpack1的loader扩展和plugin扩展（不错）](http://www.tuicool.com/articles/mEBNJfA)

> [扩展 HtmlwebpackPlugin 插入自定义的脚本（不错）](http://www.cnblogs.com/haogj/p/5649670.html)

---

### webpack常用包

- [webpack 预编译、模块化方案、打包工具](https://doc.webpack-china.org/configuration/)

    - webpack：基础包
    - [webpack-dev-server](https://segmentfault.com/a/1190000006670084?hmsr=toutiao.io)：构建 NodeJs 服务器

- [babel 转码器](https://excaliburhan.com/post/babel-preset-and-plugins.html) 

-     $ npm install babel-core babel-loader babel-preset-es2015 babel-preset-react --save-dev

    - babel-core：核心功能
    - babel-loader：允许 webpack 使用 babel，依赖 bable-core
    - babel-preset-es2015：解析ES6
    - [babel-preset-stage-0/1/2/3](http://www.cnblogs.com/chris-oil/p/5717544.html)：增补解析 ES6
    - babel-preset-React：解析 JSX
    - [babel-plugin-import](http://blog.csdn.net/github_36085116/article/details/61201627)：实现 antd 按需加载
    - [babel-polyfill](https://segmentfault.com/a/1190000008706628)：垫片，新 API 的 polyfill

- [loader 加载器](https://doc.webpack-china.org/loaders/)

    - babel-loader：详见上面 babel
    
    
-     $ npm install css-loader style-loader --save-dev

    - css-loader：能使用 @import 和 url(…) 替代 require()
    - style-loader：将计算后的样式加入页面中（通过 js 直接以 style 标签形式加载 css ，不推荐）
    
    
-     $ npm install less-loader less --save-dev

    - less-loader：加载 less 文件并编译成 css 文件，强依赖于 less 包
    
    
-     $ npm install sass-loader node-sass webpack --save-dev

    - sass-loader：加载 sass 文件并变异成 css 文件，强依赖于 node-sass 包（node-sass 强依赖于 python2.7 环境和部分 vs2013 包）和 webpack
    
    
-     $ npm install postcss-loader autoprefixer --save-dev

    - postcss-loader：[帮助理解: 关于PostCSS](http://www.tuicool.com/articles/fmUjUvZ)
    - autoprefixer：postcss的插件，用于 css3 的兼容前端处理
    
    
-     $ npm install url-loader file-loader --save-dev

    - url-loader：将图片转换为 base64 
    - file-loader：图片或 web 字体文件打包
    
- [plugin 插件](https://doc.webpack-china.org/plugins/)

-     $ npm install extract-text-webpack-plugin@1.0.1 --save-dev   # for webpack1

    - html-webpack-plugin：自动生成 html5 文件
    - extract-text-webpack-plugin：独立分离 css 文件
    - clean-webpack-plugin：在 building 前删除上次 build 生成的文件
    - copy-webpack-plugin：在 building 时直接复制文件

- react、redux

    - react：0.14.3 支持 IE8, 15.3.1 不支持；用于创建组件 component
    - react-dom：版本同上，用于渲染组件 render
    - [react-router](http://www.tuicool.com/articles/iAvmyuj)：路由，[版本1（评论有官方中文文档）](https://zhuanlan.zhihu.com/p/20381597)、[版本2](http://www.ruanyifeng.com/blog/2016/05/react_router.html?utm_source=tool.lu)[ --（按需加载）](https://segmentfault.com/a/1190000007141049)、[版本3](http://blog.csdn.net/mjzhang1993/article/details/53706775)、[版本4（大改）](https://zhuanlan.zhihu.com/p/25696969)[--v4文档说明](https://www.oschina.net/news/83093/react-router-v4)
    - react-cookie：操作 cookie 
    - [redux](http://www.cnblogs.com/xianyulaodi/p/5399264.html)：基础库
    - [react-redux](https://zhuanlan.zhihu.com/p/25800767)：react 官方绑定 redux 实现，2个 API ：Provider 和 connect
    - [redux-thunk](http://www.ruanyifeng.com/blog/2016/09/redux_tutorial_part_two_async_operations.html)：改造 store.dispatch ，使其可以接受函数作为参数，异步请求后 dipatch 的都需要 
    - redux-promise：：改造 store.dispatch ，使其可以接受 pormise 对象作为参数
    - redux-logger：生成日志
    
- [兼容ie8](http://note.youdao.com/noteshare?id=73e6e3d8c262427ed224c43e92a0801c&sub=AB30FE58DEEF4AD6BFD532D748C42DA4)

    - es3ify-loader：解决 es3 环境下基本兼容，如 default 关键字、数组尾逗号去除
    - babel-polyfill：解决 es3 环境下 es6 API 缺失，如 Object.assign，祥见上面babel。（该垫片包含定制过的 core-js）
    - core-js（可选）：解决 es3 环境下 API 缺失，可自由引入所需垫片（减小引入体积）
    - console-polyfill：ie8控制台不输出
    - [es5-shim/es5-sham](https://www.v2ex.com/t/250434)：解决 es3 环境下 es5 API 缺失，如 Object.defineProperty
    - html5shiv：h5标签问题
    - es6-promise：全环境的 polyfill 通过 require('es6-promise').polyfill(); 实现
    - fetch-ie8：[fetch 的 IE8 兼容，参考这里](https://segmentfault.com/a/1190000003810652)
    
- 其他工具

    - classnames：各种姿势组合类名
    - history：用于管理 session history，管理堆栈、导航、会话持久状态，可以创建 router 需要的 history（如，[添加根路径](https://zhuanlan.zhihu.com/p/20381597)）
    - store：用于兼容实现跨浏览器的本地存储
    - [axios](http://www.tuicool.com/articles/amQBruF):JS HTTP库/Ajax库，基于 promise
    - moment：日期操作库
    - WebUploader:flash+h5文件上传
    - jiathis:分享按钮
    - clipboard:剪贴板
    - jweixin-1.0.0:微信JS功能接口

### webpack2的一些东西

---
> [官方文档: webpack2（中文）](https://doc.webpack-china.org/configuration) 

> [简单demo: v1和v2对比](http://lucyhao.com/2017/04/19/webpack2%20vs%20webpack1/)

> [阿里巴巴: v2的详细说明（重要）](http://www.tuicool.com/articles/BVzMNb)

> [官方文档: 从v1迁移到v2](https://doc.webpack-china.org/guides/migrating/)

---