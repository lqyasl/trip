# trip

> A Vue.js project-去哪儿旅行，vue学习练手小项目。

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

## 项目开发笔记

### 修改 标签 <meta name="viewport" content="width=device-width,initial-scale=1.0,minimum-scale=1.0,maximum-scale=1.0,user-scalable=no">
### 路劲优化，简化 ,在webpack 中配置 
+ build/webpack.base.conf.js   的alias 下面是vue-cli 配置好的

```
alias: {
  'vue$': 'vue/dist/vue.esm.js',
  '@': resolve('src'),
}
```

+ import HelloWorld from '@/components/HelloWorld' 其中的 @ 表示src目录
+ 在css 样式中 import '~@/assets/styles/varibles.styl' 其中的 ~@ 表示src目录

### 移动端快速点击 
+ npm i fastclick --save  解决300毫秒延迟
+ 在main.js 中 
+ import fastClick from 'fastclick'
+ fastClick.attach(document.body)

### css代码编辑工具 stylus
+ npm i stylus --save
+ npm i stylus-loader --save

### 阿里图标 进入网站后 /图标管理/我的项目/新建项目
### 1px 使用的是硅谷外卖 stylus/mixins.styl
+ 使用 @import '~@/assets/styles/border.styl'
+ 某一个样式下 bottom-border-1px(#ccc) 自己传一个色值

### github 创建新分支index-swiper
### 本地 git pull 将分支拉到本地  
### 切换到这个分支 git checkout index-swiper
### 轮播图 npm i vue-awesome-swiper@2.6.7 --save
+ [官网具体配置](https://github.com/surmon-china/vue-awesome-swiper)

### 轮播图 index-swiper 开发完成后 
+ git add .
+ git commit -m 'swiper finished'
+ git push
+ git checkout master
+ git merge origin/index-swiper  将远程index-swiper 分支的文件 合并到本地的master主分支
+ git push 

### 在浏览器中自动打开
+ config/index.js 
+ 修改里面的配置，把autoOpenBrowser:false改为autoOpenBrowser:true即可

### 布局 高度
+  height 0
   padding-bottom 33.9% 
+ 用padding-bottom 的值撑开高度 即高宽比







For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
