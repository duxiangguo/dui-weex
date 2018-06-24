

## 地址编辑 dui-address-edit
### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| btnColor| `String` |`N`| `#ff4e24` |按钮颜色
| textColor | `String` |`N`| `#fff` | 按钮文案颜色|
| text | `String` |`N`| `确认` | 按钮文案|
| disabled | `Boolean` |`N`| `false` | 是否禁用按钮|
| province | `Object` |`Y`| `[]` |省份数据源|
| city | `Object` |`N`| `[]` |市数据源|
| area | `Object` |`N`| `[]` |区数据源|
| tabItems | `Object` |`N`| `[]` |默认展示省市区|
| currentTab | `Number` |`N`| `0` |选择省的时候默认展示省还是市或者是区|

### 事件回调


```
@getAddress="getAddress"  监听选择省份信息的时候返回选择的value
```

```
@addAddress="addAddress"  监听添加按钮返回输入的数据
```
### 记一个bug选择联系人现在不好使没有完成
