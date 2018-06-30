### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-area-selector.gif" width="240"/>
```vue
<template>
    <div>
        <dui-button :text="text" @click="openAreaSelector"></dui-button>
        <dui-address-selector @checkedArea="checkedArea" :show="show" @close="close"></dui-address-selector>
    </div>
</template>

<script>
    import {duiAddressSelector,duiButton} from  'dui-weex'
    module.exports = {
        components: {
            duiAddressSelector,duiButton
        },
        data() {
            return {
                show:false,
                text:'打开省市区选择'
            }
        },
        methods: {
            openAreaSelector(){
                this.text='打开省市区选择';
                this.show=true
            },
            checkedArea(value){
                this.text=value[0].title+'-'+value[1].title+'-'+value[2].title;
            },
            close(){
             this.show=false
            }
        }
    }
</script>
```

### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| show| `Boolean` |`Y`| `false` |是否显示地区选择器|
| province | `Object` |`Y`| `[]` | 省数据源， 数据格式参考tabItems|
| city | `Object` |`Y`| `[]` | 市数据源， 数据格式参考tabItems|
| area | `Object` |`Y`| `[]` | 区数据源， 数据格式参考tabItems|
| tabItems | `Object` |`N`| `[{title: "请选择",value:''},{title: "",value:''},{title: "",value:''}]` |默认选择的省市区|
|currentTab | `Number` |`N`| `0` | 默认打开省|


### 事件回调

```
@selectArea="selectArea" 没选择一项都会返回当前选择项的value
```

```
@close="close" 点击关闭按钮时触发,有一个关闭相关的回调逻辑,需要设置`show=false`
```

```
@checkedArea="checkedArea" 当省、市、区全都选择完成之后触发回调，回调数据格式参考tabItems
```
