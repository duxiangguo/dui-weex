# 地址编辑

## 可配置参数

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

## 事件回调


```
@getAddress="getAddress"  监听选择省份信息的时候返回选择的value
```

```
@addAddress="addAddress"  监听添加按钮返回输入的数据
```

# 地区选择

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

# 输入框

### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| formType| `String` |`N`| `input` |表单类型支持input、text、switch、sms|
| disabled | `Boolean` |`N`| `false` | 是否禁用表单组件|
| required | `Boolean` |`N`| `false` | 当表单是input的时候是否开启验证|
| requiredType | `String` |`N`| `` | 验证类型telphone、cardNumber、idCard|
| requiredColor | `String` |`N`| `#DC143C` |左侧需要验证时展示的颜色|
|rightIcon | `String` |`N`| `` | 右侧图标|
|inputType | `String` |`N`| `text` | 输入框类型|
|inputValue | `String` |`N`| `` | 输入框默认值|
|inputColor | `String` |`N`| `#000000` | 输入框文字颜色|
|inputMaxlength | `Number` |`N`| `30` | 输入框最大长度|
|placeholder | `String` |`N`| `请输入手机号` | 输入框提示用户文字|
|label | `String` |`N`| `手机号` | 标题文字|
|content | `String` |`N`| `17603666581` | 表单类型为text时展示的内容|
|showTopBorder | `Boolean` |`N`| `true` | 是否展示上边框|
|showBottomBorder | `Boolean` |`N`| `false` | 是否展示下边框|
|codeColor | `String` |`N`| `#00cc66` | 发送验证码背景颜色|
### 事件回调


```
@change="change"  当表单类型是text、switch的时候监听这个事件并会返回switch选择的结果
```
```
@checkResult="checkResult" 当表单类型是input的时候监听这个事件返回表单验证结果
```
```
@rightClick="rightClick"  监听右侧图标点击事件
```
```
@getCode="getCode"  监听发送验证码事件
```

# 商品页行动点


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

# 通告栏


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
|rollingLength | `Number` |`N`| `800` |滚动长度
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

# 数字键盘


### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| show| `Boolean` |`Y`| `false` |是否显示键盘|
| theme | `String` |`N`| `default` | 样式风格，可选值为 default custom|
| showMask | `Boolean` |`N`| `false` |是否展示蒙层|
| closeButtonText | `String` |`N`| `确定` | 关闭按钮展示的文字 |
| closeButtonBackgroundColor | `String` |`N`| `#83c6c2` |关闭按钮的背景颜色|
|closeButtonTextStyle | `Object` |`N`| `{fontSize: '35px'}` | 关闭按钮展示文字的style|


### 事件回调

```
@input="input" 点击按键时触发
```

```
@close="close" 点击关闭按钮时触发,有一个关闭相关的回调逻辑,需要设置`show=false`
```

```
@delete="delete" 点击删除键时触发
```

# 支付输入框


### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| show| `Boolean` |`Y`| `false` |是否显示键盘|
| title | `String` |`N`| `''` | 标题默认为空不展示|
| length | `Number` |`N`| `6` |密码长度|
| rightButton | `String` |`N`| `&#xe90C` | 右侧删除按钮文案，可以设置icon|


### 事件回调

```
@input="input" 点击按键时触发
```

```
@close="close" 点击关闭按钮时触发,有一个关闭相关的回调逻辑,需要设置`show=false`
```

```
@delete="delete" 点击删除键时触发
```

# 评分


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

# 横向步骤条

### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| show| `Boolean` |`N`| `true` |是否展示描述栏
| describeBar | `Object` |`N`| `icon:'&#xe671',iconSize:100,iconColor:'#ff6600',title:'标题',description:'描述栏文字',descriptionColor:'#7c7c7c'` | 描述栏展配置信息|
| value | `Number` |`Y`| `0` | 当前处在位置|
| list | `Object` |`Y`| `[{title:'买家下单'},{title:'商家接单'},{title:'买家提货'},{title:'交易完成'}]` | 展示文案内容|
| themeColor | `Object` |`N`| `lineColor:'#727272',pointInnerColor:'#727272',highlightTitleColor:'#ff6600',pointSize:30,highlightTitleSize:40` |主题样式配置|

