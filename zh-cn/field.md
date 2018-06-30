### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-filed.gif" width="240"/>
```vue
<template>
    <div>
        <div class="width750 height100 center background-color-gay">
            <text>不可编辑</text>
        </div>
        <dui-field formType="text" label="姓名" content="张三" @change="touchClick"></dui-field>
        <div class="width750 height100 center background-color-gay">
            <text>带验证类型输入框</text>
        </div>
        <dui-field formType="input" :required="true"  requiredType="telphone"></dui-field>
        <dui-field formType="input" label="身份证" placeholder="请输入省份证" :required="true"  requiredType="idCard"></dui-field>
        <div class="width750 height100 center background-color-gay">
            <text>验证码输入框</text>
        </div>
        <dui-field formType="sms" label="验证码" placeholder="请输入验证码" @getCode="getCode"></dui-field>
        <div class="width750 height100 center background-color-gay">
            <text>开关</text>
        </div>
        <dui-field formType="switch"  label="设为默认" @change="switchClick"></dui-field>
    </div>
</template>

<script>
    import {duiField} from  'dui-weex'
    module.exports = {
        components: {
            duiField
        },
        methods: {
            touchClick(){
				console.log('您点击了不可编辑输入框')
            },
            getCode(){
				console.log('您点击了获取验证码')
            },
            switchClick(value){
				console.log(value)
            }
        }
    }
</script>
```

### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| formType| `String` |`N`| `input` |表单类型支持input、text、switch、sms|
| disabled | `Boolean` |`N`| `false` | 是否禁用表单组件|
| required | `Boolean` |`N`| `false` | 当表单是input的时候是否开启验证|
| requiredType | `String` |`N`| `` | 验证类型telphone、cardNumber、idCard|
| requiredColor | `String` |`N`| `#DC143C` |左侧需要验证时展示的颜色|
|rightIcon | `String` |`N`| `` | 右侧图标|
|inputType | `String` |`N`| `text` | 输入框类型|
|inputValue | `String` |`N`| `` | 输入框默认值|
|inputColor | `String` |`N`| `#000000` | 输入框文字颜色|
|inputMaxlength | `Number` |`N`| `30` | 输入框最大长度|
|placeholder | `String` |`N`| `请输入手机号` | 输入框提示用户文字|
|label | `String` |`N`| `手机号` | 标题文字|
|content | `String` |`N`| `17603666581` | 表单类型为text时展示的内容|
|showTopBorder | `Boolean` |`N`| `true` | 是否展示上边框|
|showBottomBorder | `Boolean` |`N`| `false` | 是否展示下边框|
|codeColor | `String` |`N`| `#00cc66` | 发送验证码背景颜色|
### 事件回调


```
@change="change"  当表单类型是text、switch的时候监听这个事件并会返回switch选择的结果
```
```
@checkResult="checkResult" 当表单类型是input的时候监听这个事件返回表单验证结果
```
```
@rightClick="rightClick"  监听右侧图标点击事件
```
```
@getCode="getCode"  监听发送验证码事件
```
*