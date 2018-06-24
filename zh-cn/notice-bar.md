
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
