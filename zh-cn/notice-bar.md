### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-notice-bar.gif" width="240"/>
```vue
<template>
    <div>
        <dui-notice-bar :scrollable="scrollable"></dui-notice-bar>
        <dui-button :text="text" @click="startRolling"></dui-button>
    </div>
</template>

<script>
    import {duiNoticeBar,duiButton} from  'dui-weex'
    module.exports = {
        components: {
            duiNoticeBar,duiButton
        },
        data() {
            return {
                scrollable:false,
                text:'切换为滚动模式'
            }
        },
        methods: {
            startRolling(){
				console.log('切换滚动模式成功')
                this.scrollable=true
                this.text='当前为滚动模式'
            }
        }
    }
</script>

```
### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| show| `Boolean` |`Y`| `true` |是否展示通知栏
| background | `String` |`N`| `#fff7cc` | 通知栏背景颜色|
| height | `String` |`N`| `100px` | 通知栏高度|
| title | `String` |`Y`|| 通知栏标题|
| titleStyle | `Object` |`N`| `{color:'#ff6600',fontSize:25}` |标题样式|
|leftIcon | `String` |`N`| `&#xe66B;` | 左侧文案|
|leftItem | `Object` |`N`| `{color:'#ff6600',fontSize:35}` |左侧文案样式|
|rightIcon | `String` |`N`| `&#xe646;` | 右侧文案|
|rightItem | `Object` |`N`| `{color:'#ff6600',fontSize:45}` |右侧文案样式|
|scrollable | `Boolean` |`N`| `false` | 是否滚动|
|rollingLength | `Number` |`N`| `800` |滚动长度|
### 事件回调


```
@centerClick="centerClick"  点击标题会触发该事件
```

```
@rightClick="rightClick"  点击右侧文案会触发该事件
```

```
@leftClick="leftClick"  点击左侧文案会触发该事件
```
