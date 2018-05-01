# MINI - UI
这里是一个小程序UI框架，封装了一些常用组件及样式，方便开发。

> 当前版本使用mpvue转换小程序，开放时使用vue.js，请确保对vue有一定了解。（[vue](https://cn.vuejs.org/v2)）

## 快速使用

1. 初始化一个mpvue项目（更多参考[mpvue](http://mpvue.com/mpvue/quickstart/)）

现代前端开发框架和环境都是需要 Node.js 的，如果没有的话，请先下载 nodejs 并安装。

然后打开命令行工具

```bash
# 1. 先检查下 Node.js 是否安装成功
$ node -v
v8.9.0

$ npm -v
5.5.1

# 2. clone一个初始化项目
$ git clone git@github.com:gatinul/mpvue-init.git

# 3. 进行npm包安装
$ npm install 

# 3. 或者切换到国内 taobao 源再安装
$ npm set registry https://registry.npm.taobao.org/

$ cnpm install

```

2. 搭建小程序环境

这一步请去[微信公众平台](https://developers.weixin.qq.com/miniprogram/dev/devtools/devtools.html)下载小程序的开发者工具

3. 将小程序与mpvue关联起来开发调试

打开小程序开发者工具，用自己的appid点击新建项目，选择刚才clone下载的初始化项目。进入到小程序开发页面，此时可以把开发者工具自带的编辑器关闭了，只要关心它的调试器就好了。在自己喜欢的编辑器里打开clone下的初始化项目，在当前目录下执行 `npm run dev` ，不要关闭命令行，可以边编写代码边看小程序开发者工具调试啦~

[假装有图]

## 使用组件

使用组件可以快速开发。

### 什么是组件：
1. 组件是一个个封装好的代码单元
2. 组件会一些功能和样式
3. 组件之间可以互相传递数据

### 组件的引入
在引用组件的vue文件中
```vue
<template>
 <cells
    className="after_title"
    :dataSource="cellList"
  >
</template>
<script>
 import cells from '@/components/cells'

 data () {
    return {
      cellList: [ {
        title: '我的订单',
        dot: '7'
      }, {
        title: '我的二级能人',
        dot: '3'
      }, {
        title: '我的二维码',
        dot: 'New'
      }]
    }
  },
 components: {
    cells
  },
</script>
```

这样就可以使用cells组件，cells组件封装了一些内容，具体参见[cells](./components/cell.md)





