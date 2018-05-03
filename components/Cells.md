# Cells 单行列表
简短的单行列表，如果列表中显示内容多的话，请使用[Lists](./Lists.md)

## 如何使用

```html
<Cells
  title="待审核能人"
  @cellClick="review"
  dot="point"
>
</Cells>
```
也可以与v-for一起使用，循环插入cells组件

```html
<Cells
  v-for="(item, index) in cellList"
  :key="index"
  :title="item.title"
  :dot="item.dot"
  link=true
  @cellClick="cellClick"
>
</Cells>
```

## API

|属性|说明|类型|默认值|
|--|--|--|--|
|title|单行列表左侧的名称|String||
|dot|是否有角标，空则没有，point渲染为一个右侧的小红点|String||
|link|是否在最右侧有箭头，代表可跳转|Boolean|false|

## 事件

### cellClick

单行列表点击事件，在组件标签中使用 `@cellClick` 插入

携带title: 可获取到当前点击的cell的title值

示例代码
```js
// 插入cells组件
<Cells
  title="待审核能人"
  @cellClick="review"
  dot="point"
>
</Cells>
// 在methods中写点击函数
methods: {
  review (title) {
    console.log(title) // 待审核能人
  }
}
```