### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-number-keyboard.gif" width="240"/>
```vue
<template>
    <div>
        <dui-button text="打开default键盘" @click="openKeyboard('default')"></dui-button>
        <dui-button text="打开custom键盘" @click="openKeyboard('custom')"></dui-button>
        <dui-number-keyboard  :show="show" @delete="back" @close="close" @input="input" :theme="keyboardTheme" ></dui-number-keyboard>
    </div>
</template>

<script>
    import {duiNumberKeyboard,duiButton} from  'dui-weex'
    module.exports = {
        components: {
            duiNumberKeyboard,duiButton
        },
        data() {
            return {
                show:false,
                keyboardTheme:''
            }
        },
        methods: {
            openKeyboard(value){
                this.show=true;
                this.keyboardTheme=value
            },
            close(){
                this.show=false
				console.log('关闭键盘')
            },
            input(value){
				console.log(value)
            },
            back(){
				console.log('您点击了回退按钮')
            }
        }
    }
</script>

```
### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| show| `Boolean` |`Y`| `false` |是否显示键盘|
| theme | `String` |`N`| `default` | 样式风格，可选值为 default custom|
| showMask | `Boolean` |`N`| `false` |是否展示蒙层|
| closeButtonText | `String` |`N`| `确定` | 关闭按钮展示的文字 |
| closeButtonBackgroundColor | `String` |`N`| `#83c6c2` |关闭按钮的背景颜色|
|closeButtonTextStyle | `Object` |`N`| `{fontSize: '35px'}` | 关闭按钮展示文字的style|


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
