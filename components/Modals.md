# Modals 弹出框
弹出框，用来在页面弹出一层显示，如果只有少数文字（不涉及图片等），直接使用wx.showModal即可

## 如何使用

```html

<Modals
  :showModal="showModal"
  title="我的二维码"
  okText="保存"
  cannelText="关闭"
  @modalOk="save"
  @modalCannel="cannel"
>
<img style="height:130px;width:150px;margin:5px auto" src="http://218.25.255.9/pcenterew/upload/qrc/20180411151756120754.png" />
</Modals>
```
在Modals标签中，可插入其它标签或组件展示在modal框中间内容中

与其它组件一起使用

```html
<Modals
  :showModal="showModal"
  title="我的二维码"
  okText="保存"
  cannelText="关闭"
  @modalOk="save"
  @modalCannel="cannel"
>
  <Qrcodes
    content="http://broad.10010lt.com/chbb/e10010/online/index.do?ID=20180309130005082820"
    width="150"
    height="130"
    >
  </Qrcodes>
</Modals>
```


## API

|属性|说明|类型|默认值|
|--|--|--|--|
|showModal|控制modal框显隐|Boolean||
|title|modal框的标题|String||
|okText|确认按钮的文字|String||
|cannelText|取消按钮的文字|String|||

## 事件

### modalOk

确认按钮，在组件中使用`@modalOk`使用

### modalCannel

取消按钮，在组件中使用`@modalCannel`使用

