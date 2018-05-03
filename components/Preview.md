# Preview 信息概览卡片
用以展示概览信息，底部可包含1-2个操作按钮

## 如何使用

```html
<Preview
  :title = "title"
  :content = "content"
  cannelText = "驳回"
  sureText = "通过"
  @cannel="reject"
  @sure="resolve"
>
</Preview>
```
> `:title 和 title的区别` 
:title 的值会被javascript表达式计算，而title的值则被作为原始值传递

也可以与v-for一起使用

```html
<Preview
  v-for="(item, index) in reviewList"
  :key = "index"
  :title = "item.title"
  :content = "item.content"
  cannelText = "驳回"
  sureText = "通过"
  @cannel="reject"
  @sure="resolve"
>
</Preview>
```

## API

|属性|说明|类型|默认值|
|--|--|--|--|
|title|概览卡片的标题,label为左侧文字，text为右侧文字|Object||
|content|概览卡片的中间内容，为数组，包含了多个object，其中每个object中同样有label和text|Array||
|cannelText|取消按钮的文字，当有取消按钮时必填|String||
|sureText|确认按钮的文字，当有确认按钮时必填|String||

## 事件

### cannel
取消按钮，使用`@cannel`注册

携带content：content为此卡片中间内容的所有内容
携带title：title为此卡片标题的所有内容

示例代码

```js
// 在使用组件时，注册reject和resolve事件
<Preview
  v-for="(item, index) in reviewList"
  :key = "index"
  :title = "item.title"
  :content = "item.content"
  cannelText = "驳回"
  sureText = "通过"
  @cannel="reject"
  @sure="resolve"
>
</Preview>

// methos中写点击函数
reject (content, title) {
  console.log(content)
  console.log(title)
},
resolve (content, title) {
  console.log(content)
}
```

### sure
确认按钮，使用`@sure`注册，使用方法同cannel