
## 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-rate.gif" width="240"/>

```vue
<template>
    <div>
       <dui-rate :count="count" @change="change"></dui-rate>
    </div>
</template>

<script>
    import {duiRate} from  'dui-weex'
    module.exports = {
        components: {
            duiRate
        },
        data() {
            return {
                count:5
            }
        },
        methods: {
            change(e){
                console.log(e)
            }
        }
    }
</script>

```
### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| value| `Number` |`N`| `0` |已评分数，支持v-model双向数据绑定
| count | `Number` |`N`| `5` | 评分的总分数|
| color | `String` |`N`| `#ff2d4d` | 选中时的颜色|
| size | `Number` |`N`| `55` | 图标的大小|
| voidColor | `String` |`N`| `#ff2d4d` |未选中颜色|
|disabledColor | `String` |`N`| `0` | 禁用选择的颜色|
|disabled | `Boolean` |`N`| `false` | 是否禁用选择|

### 事件回调


```
@change="change"  返回选中的分数
```
