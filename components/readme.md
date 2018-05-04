# Components 组件
这里包含了一些会经常用到的组件，合理使用组件可大大提升开发速度

## 使用组件

使用组件可以快速开发。

### 什么是组件：
1. 组件是一个个封装好的代码单元
2. 组件会一些功能和样式
3. 组件之间可以互相传递数据

### 组件的引入
在引用组件的vue文件中
```js
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