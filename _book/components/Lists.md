# Lists 列表
包含详细内容的列表，若内容较少，请使用[Cells](./Cells.md)

## 如何使用

```html
<Lists
  imgPath="https://gw.alipayobjects.com/zos/rmsportal/pdFARIqkrKEGVVEwotFe.svg"
  :content="orderList"
>
```

## API

|属性|说明|类型|默认值|
|--|--|--|--|
|imgPath|左侧图片的路径，不填则为无图片列表|String||
|content|右侧的内容，为数组格式，按数组个数自动分行|Array||

## 事件

### itemClick

列表点击事件，在组件标签中使用 `@itemClick` 插入

携带content: 可获取到当前点击的list的右侧内容

示例代码
```js
// 插入cells组件
<Lists
  v-for= "(item, index) in orderList"
  :key= "index"
  :content= "item"
  itemClick="orderQry"
>
</Lists>
// 在methods中写点击函数
methods: {
  orderQry (content) {
    console.log(content)
  }
}
```