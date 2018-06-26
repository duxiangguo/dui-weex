# dui-weex


## 安装
```shell
npm i dui-weex -S
```

## 使用
```vue
<template>
    <div>
       <dui-rate :count="count" @change="change"></dui-rate>
    </div>
</template>

<script>
    import {duiRate} from  'dui-weex'
    module.exports = {
        components: {
            duiRate
        },
        data() {
            return {
                count:5
            }
        },
        methods: {
            change(e){
                console.log(e)
            }
        }
    }
</script>
```

## 使用前
```json
// 增加一个plugins的配置到 .babelrc 中
{
  "plugins": [
    ["import",[ {
        "libraryName": "dui-weex",
        "libraryDirectory": "src/components",
        "style": false
    }]]
  ]
}
```





## 最后
- 此UI组件是我们在使用weex-eros开发的项目中抽离出的，推荐在[EROS](https://bmfe.github.io/eros-docs/#/)上使用该UI组件。
- UI组件中有参考[weex-ui](https://github.com/alibaba/weex-ui)的部分，非常感谢！
