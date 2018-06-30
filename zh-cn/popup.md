
### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-popup.gif" width="240"/>

```vue
<template>
    <div>
        <dui-popup v-model="show" :pos="pos" :width="width"></dui-popup>
        <dui-button @click="open('top','750')" text="弹出顶部弹层"></dui-button>
        <dui-button @click="open('bottom','750')" text="弹出底部弹层"></dui-button>
        <dui-button @click="open('left','500')" text="弹出左侧弹层" ></dui-button>
        <dui-button @click="open('right','500')" text="弹出右侧弹层" ></dui-button>

    </div>
</template>

<script>
    import {duiPopup,duiButton} from  'dui-weex'
    module.exports = {
        components: {
            duiPopup,duiButton
        },
        data() {
            return {
                show:false,
                pos:'left',
                width:750
            }
        },
        methods: {
            open(value,width){
                this.width=width;
                this.show=true;
                this.pos=value
            }
        }
    }
</script>

```
### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| value| `Boolean` |`N`| `false` |支持v-model双向数据绑定|
| showMask | `Boolean` |`N`| `true` | 是否展示蒙层|
| pos | `String` |`N`| `bottom` | 打开蒙层方向|
| duration | `Number` |`N`| `300` |打开时间|
|backgroundColor | `String` |`N`| `#FFFFFF` | 背景颜色|
|height | `Number` |`N`| `840` | 上下方向打开时候使用|
| width | `Number` |`N`| `750` | 左右方向打开时候使用|

