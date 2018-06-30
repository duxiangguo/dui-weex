
### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-button.png" width="240"/>

```vue
<template>
    <div>
        <dui-button @click="onClick" text="常规按钮" ></dui-button>
        <dui-button :disabled="true" text="禁用按钮" @click="onClick" ></dui-button>
        <dui-button textSize="30" textColor="#cccccc" text="改变字体颜色和大小" @click="onClick"></dui-button>
        <dui-button  text="改变背景颜色" btnColor="#1989FF" @click="onClick"></dui-button>
        <dui-button btnHeight="60px" text="按钮高度60px" @click="onClick"></dui-button>
        <dui-button btnWidth="500px" text="按钮宽度500px" @click="onClick"></dui-button>

    </div>
</template>
<script>
    import {duiButton} from  'dui-weex'
    module.exports = {
        components: {
            duiButton
        },
        data() {
            return {
            }
        },
        methods: {
            onClick(){
               console.log('您点击了该按钮')
            }
        }
    }
</script>

```
### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| text| `String` |`N`| `确认` |按钮文案|
| textSize | `Number` |`N`| `55` | 文案字体大小|
| textColor | `String` |`N`| `#ffffff` | 文案字体颜色|
| disabled | `Boolean` |`N`| `false` | 是否禁用按钮|
| unBtnColor | `String` |`N`| `#cccccc` | 禁用时展示的颜色|
| btnColor | `String` |`N`| `#ff2d4d` |按钮背景颜色|
| btnWidth | `String` |`N`| `700px` | 按钮宽度|
| btnHeight | `String` |`N`| `88px` | 按钮高度|

### 事件回调


```
@click="click"  按钮事件回调
```
