
### 使用方法
<img   src="https://duxiangguo.github.io/dui-weex/zh-cn/image/dui-tabbar.gif" width="240"/>

```vue
<template>
    <div>
        <dui-tabbar :tabItems="tabItems" titleSize="30px" selectedColor="#83c6c2" borderBottomColor="#83c6c2"	showSelectedLine=true  v-model="currentTab"></dui-tabbar>
        <slider class="flex1" @change="onSliderChange" :index="currentTab" :infinite="false">
            <div class="width750">
                <text>{{tabItems[currentTab].title}}</text>
            </div>
            <div class="width750">
                <text>{{tabItems[currentTab].title}}</text>
            </div>
            <div class="width750">
                <text>{{tabItems[currentTab].title}}</text>
            </div>
            <div class="width750">
                <text>{{tabItems[currentTab].title}}</text>
            </div>
        </slider>
    </div>
</template>

<script>
    import {duiTabbar} from  'dui-weex'
    module.exports = {
        components: {
            duiTabbar
        },
        data() {
            return {
                tabItems:[{title: "第一页"},{title: "第二页"},{title: "第三页"},{title: "第四页"}],
                currentTab:0
            }
        },
        methods: {
            onSliderChange(e){
                this.currentTab= e.index;
            }
        }
    }
</script>
```
### 可配置参数

| Prop | Type | Required | Default | Description |
|-------------|------------|--------|-----|-----|
| tabItems| `Number` |`N`| `[]` |标签展示内容|
| value | `Number` |`N`| `0` | 当前展示第几项支持v-model|
| height | `String` |`N`| `100px` | 标签高度|
|titleSize | `String` |`N`| `22px` | 文字大小|
|background | `String` |`N`| `#ffffff` | 背景颜色|
|selectedBackground | `String` |`N`| `#ffffff` | 选中的背景颜色|
|normalColor | `String` |`N`| `#818181` | 未选中文案颜色|
|selectedColor | `String` |`N`| `#4ca4fe` |选中文案颜色|
|borderBottomColor | `String` |`N`| `#4ca4fe` | 底边颜色|
|showSelectedLine | `Boolean` |`N`| `false` | 图标的大小|

### 事件回调


```
@change="change"  
```
