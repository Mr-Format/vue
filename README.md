# vue 练习项目
- Mr-Format
- 2019/6/16

## 开发工具：
+ vue
+ webpack
+ npm
+ vue-resource
+ vue-router
+ Mint UI
+ MUI
+ Vuex
+ JSON

## 制作首页 App 组件
1. 完成 Header 区域，使用的是 Mint-ui 中的 Header 组件
2. 制作底部的 Tabber 区域，使用的是 MUI 的 Tabbar.html
+ 制作购物车小图标：
+ 1.添加扩展图标的 css 样式
+ 2.添加字体的 ttf 文件
+ 3.修改购物车图标的类 mui-icon mui-icon-extra mui-icon-extra-cart
3. 在中间区域放置 router-view 来展示路由匹配到的组件

### 修改 tabbar 为 router-link

## 设置路由高亮

## 点击 tabbar 链接，显示对应路由组件

## 首页轮播图布局
1. 将数据保存在 data
2. 使用 v-for 循环渲染每个 item

## 首页图标
1. 布局
2. 图片
3. 字体

## 创建新闻资讯路由

## 新闻资讯页面
1. 绘制界面 使用 MUI 中的 media-list
2. 写入数据
3. 渲染

## 新闻列表详情页面
1. 设置每一项的 router-link
2. 创建详情页面组件 newsInfo.vue
3. 在路由模块中关联列表和详情页面

## 新闻详情页面的数据渲染

## 单独封装 comment 子组件
1. 创建 comment.vue 组件模版
2. 导入 comment 组件
+ `import comment from './comment.vue'`
3. 将 comment 注册为子组件
4. 在页面中引用子组件

## 获取评论数据

## 评论加载更多
1. 绑定点击事件，（请求下一页数据）
2. 点击加载更多， 让 pageIndex++ ,然后重新获取新的数据
3. 点击加载更多时使用数组拼接， 以防原有数据被覆盖

## 发表评论功能
1. 把文本框做双向数据绑定
2. 为发表按钮绑定点击事件
3. 检查评论内容
4. 通过 vue-resource 发送请求，将评论内容提交给服务器
5. 重新刷新评论列表
+ 当评论成功后，在客户端手动拼接评论内容，然后调用 unshift 将最新评论追加到 data 的 comments 中 

## 设置图片分享路由组件

## 图片列表组件页面结构及样式
1. 顶部导航条
2. 图片列表

### 顶部导航
1. 使用 MUI 中的 tab-top-webview-main.html
2. 去掉 mui-fullscreen 类
3. 初始化 JS 组件

```
mui('.mui-scroll-wrapper').scroll({
	deceleration: 0.0005 //flick 减速系数，系数越大，滚动速度越慢，滚动距离越小，默认值0.0006
});
```
* 坑： mui.js 与 webpack 存在 严格模式 的冲突
* 解决： 禁用 webpack 的严格模式
1. npm install babel-plugin-transform-remove-strict-mode
2. .babel 设置 "plugins": \["transform-remove-strict-mode"]
3. 解决 mui-bar-item 类的冲突

## 图片列表区域
1. 图片列表加载使用 mint-ui 提供的组件： lazy-load
2. 渲染列表数据

### 图片列表加载和改造

## 图片放大显示

## 图片缩略图功能
1. 使用 vue-preview 插件
2. 获取图片列表，使用 v-for 渲染

## 商品列表

## 商品详情

## 商品评论

## 添加购物车动画
1. javascript钩子
2. 设置小球动态位移

## 绑定购物车商品数字

## webpack 打包出现的问题
1. webpack 和 babel 版本不兼容
2. 本地 API 文档（JSON）没有打包进 dist 
3. 图片相对路径在打包后引用路径错误
