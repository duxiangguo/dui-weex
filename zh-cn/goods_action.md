### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-goods-action.gif" width="240"/>
```vue
<template>
    <div>
        <dui-goods-action  @collection="collection" :leftItems="leftItems"></dui-goods-action>
    </div>
</template>

<script>
    import {duiGoodsAction} from  'dui-weex'
    module.exports = {
        components: {
            duiGoodsAction
        },
        data() {
            return {
                leftItems:[{leftIcon:'&#xe6df;',leftTitle:'店铺',leftPointNumber:0,leftClick:'store'}
                    ,{leftIcon:'&#xe68a;',leftTitle:'收藏',leftPointNumber:0,leftClick:'collection'},
                    {leftIcon:'&#xe64b;',leftTitle:'购物车',leftPointNumber:5,leftClick:'shopCart'}]
            }
        },
        methods: {
            collection(){
              console.log('您点击了收藏')
            }    
        }
    }
</script>
```

### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| leftItems| `Object` |`N`| `[]` |左侧按钮配置信息|
| leftIcon | `String` |`N`| `&#xe676;` | 左侧按钮展示的图标|
| leftIconColor | `String` |`N`| | 左侧按钮图标颜色|
| leftTitle | `String` |`Y`| `店铺` |左侧按钮文案|
| leftTitleColor | `String` |`N`|  |左侧按钮文案颜色|
| leftPointNumber | `Number` |`N`| `0` |左侧按钮的提示信息为0时不展示|
| leftClick | `String` |`N`| `store` |左侧按钮监听事件名字|
| rightItems | `Object` |`N`| `[]` | 右侧按钮配置信息|
| btnTitle | `String` |`N`| `加入购物车` | 右侧按钮文案|
| btnTitleColor | `String` |`N`|  `#ffffff`|右侧按钮文案颜色|
| btnColor | `String` |`Y`| `#ffa500` |右侧按钮颜色|
| rightClick | `String` |`N`|`addShopCart`  |右侧按钮监听事件名字|

### 事件回调
```
注一：事件回调监听事件名字自己定义
```