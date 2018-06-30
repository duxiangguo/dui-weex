
### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-icon.png" width="240"/>

```vue
<template>
        <div>
              <dui-icon name="&#xe6d9;" ></dui-icon>
        </div>
</template>

<script>
    import {duiIcon} from  'dui-weex'
    module.exports = {
        components: {
            duiIcon
        }
    }
</script>
```
### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| name| `String` |`N`| `&#xe64C;` |字体编码|
| size | `String` |`N`| `50px` | 图标大小|
| iconStyle | `Object` |`N`| `#ff2d4d` | 图标样式|
| isDefault | `Boolean` |`N`| `true` |是否使用默认字体文件|
 |url | `String` |`N`| `bmlocal://iconfont/iconfont.ttf` | 字体文件url|

### 事件回调


```
@iconClick="iconClick"  返回选中的字体name
```
