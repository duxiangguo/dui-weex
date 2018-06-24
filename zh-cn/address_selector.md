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
@selectArea="selectArea" 返回选择项的值
```

```
@close="close" 点击关闭按钮时触发,有一个关闭相关的回调逻辑,需要设置`show=false`
```

```
@checkedArea="checkedArea" 当省、市、区全都选择完成之后触发回调，回调数据格式参考tabItems
```
