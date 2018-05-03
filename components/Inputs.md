# Inputs 文本输入框

用于接受单行文本。因Input与小程序自带组件冲突，所以命名为Input。

## 如何使用

```html
<Inputs
  label="用户"
  placeholder="请输入用户名"
  disabled="true"
  password="true"
  type="number"
  max="8"
>
</Inputs>
```

## API

|属性|说明|类型|默认值|
|--|--|--|--|
|label|输入框前的文字提示|String||
|placeholder|输入框为空时的填写提示语|String||
|disabled|是否禁用输入框（只读）|Boolean|false|
|password|是否密文显示输入内容|Boolean|false|
|type|输入框的类型|String|text|
|max|最大输入长度，为-1时不限制长度|Number|140|




