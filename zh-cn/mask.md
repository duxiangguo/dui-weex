
### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-mask.gif" width="240"/>

```vue
<template>
        <div >
            <dui-mask v-if="show" @click="close"></dui-mask>
            <dui-button text="打开蒙层" @click="open" ></dui-button>
        </div>
</template>

<script>
    import {duiMask,duiButton} from  'dui-weex'
    module.exports = {
        components: {
            duiMask,duiButton
        },
        data() {
            return {
                show:false
            }
        },
        methods: {
            open(){
                this.show=true
            },
            close(){
                this.show=false
            }
        }
    }
</script>
```

### 说明
```
使用v-if来控制蒙层的展示和隐藏  
```



### 事件回调


```
@click="click"  
```
