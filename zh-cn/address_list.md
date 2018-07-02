### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-address-list.gif" width="240"/>

```vue
<template>
    <div>
        <dui-address-list @addAddress="addAddress" @checkAddress="checkAddress" @editAddress="editAddress"></dui-address-list>
    </div>
</template>

<script>
    import {duiAddressList} from  'dui-weex'
    module.exports = {
        components: {
            duiAddressList
        },
        data() {
            return {

            }
        },
        methods: {
            addAddress(){
				console.log('您点击了添加地址')
            },
            checkAddress(){
				console.log('您选择了该地址')
            },
            editAddress(){
				console.log('您编辑了改地址')
            }
        }
    }
</script>
```

### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| color | `String` |`N`| `#5da3f6` | 选中颜色|
| voidColor | `String` |`N`| `#7c7c7c` | 未选中颜色|
| showIndex | `Number` |`N`| `0` | 默认选中|
| list | `Object` |`N`| `[{consignee:'',telphone:'',province:'',city:'',area:'',addressInfo:''}]` | 数据源|
### 事件回调


```
@addAddress="addAddress"  点击添加事件
```

```
@checkAddress="checkAddress"   选择地址事件 
```

```
@editAddress="editAddress"  编辑地址事件 
```

```
注一：返回数据类型参考list参数
```
