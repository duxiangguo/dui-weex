
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
