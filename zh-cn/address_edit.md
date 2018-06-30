### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/di-address-edit.gif" width="240"/>

```vue
<template>
    <div>
        <dui-address-edit :province="province" :city="city" :area="area"></dui-address-edit>
    </div>
</template>

<script>
    import {duiAddressEdit} from  'dui-weex'
    module.exports = {
        components: {
            duiAddressEdit
        },
        data() {
            return {
                province:[{title:'黑龙江'}],
                city:[{title:'哈尔滨'}],
                area:[{title:'南岗区'}]
            }
        },
        methods: {
        }
    }
</script>
```


### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| addButtonInfo| `Object` |`N`| `{btnColor:'#ff4e24',disabled:false,text:'保存',textColor:'#fff'}` |添加按钮详情 |
| delButtonInfo | `Object` |`N`| `{btnColor:'#fafafa',disabled:false,text:'删除',textColor:''}` |删除按钮详情|
| showDelButton | `Boolean` |`N`| `false` | 是否展示删除按钮|
| province | `Object` |`Y`| `[]` |省份数据源|
| city | `Object` |`N`| `[]` |市数据源|
| area | `Object` |`N`| `[]` |区数据源|
| tabItems | `Object` |`N`| `[{title: "请选择",value:''},{title: "",value:''},{title: "",value:''}]` |默认展示省市区|
| data | `Object` |`N`| `{address:'请选择收件地区',addressId:'',consignee:'',telphone:'',dictAddress:'',Postcodes:'',isDefault:true}` |编辑时候展示的数据|
### 事件回调


```
@getAddress="getAddress"  监听选择省份信息的时候返回选择的value
```

```
@addAddress="addAddress"  监听添加按钮返回输入的数据数据类型参看data
```

