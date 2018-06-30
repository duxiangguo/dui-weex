### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-payinput.gif" width="240"/>
```vue
<template>
    <div>
        <dui-button text="打开" @click="openPayInput"></dui-button>
        <dui-paynumber-keyboard :show="show" @close="close" @input="input"> </dui-paynumber-keyboard>
    </div>
</template>

<script>
    import {duiPaynumberKeyboard,duiButton} from  'dui-weex'
    module.exports = {
        components: {
            duiPaynumberKeyboard,duiButton
        },
        data() {
            return {
                show:false
            }
        },
        methods: {
            openPayInput(){
                this.show=true
            },
            close(){
                this.show=false
            },
            input(value){
              console.log(value)
            }
        }
    }
</script>

```
### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| show| `Boolean` |`Y`| `false` |是否显示键盘|
| title | `String` |`N`| `''` | 标题默认为空不展示|
| length | `Number` |`N`| `6` |密码长度|
| rightButton | `String` |`N`| `&#xe90C` | 右侧删除按钮文案，可以设置icon|


### 事件回调

```
@input="input" 点击按键时触发
```

```
@close="close" 点击关闭按钮时触发,有一个关闭相关的回调逻辑,需要设置`show=false`
```

```
@delete="delete" 点击删除键时触发
```
