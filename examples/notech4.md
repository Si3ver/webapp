# ch4

## 1. 3个bug

1. 使用is解决h5标签上的一些小bug。
2. 子组件的data必须是函数。
3. ref获取Vue组件引用。

## 2. 父子组件间数据传递 （单向数据流！）

父-子 ：通过props属性.

子组件不能修改父组件，若需要改变，先复制一份到成为自己的数据属性。

子-父 ：通过出发事件传值。

## 3. 组件参数校验

props属性参数检查

```vue
// 类型约束
prps: {
    content: [Number, String]
}
// 更多约束
props:{
    content: {
        type: String,
        required: false,
        default: 'default value',
        validator: function(value){     // 检查器
            return (value.length > 5)
        }
    }
}
```

## 4. 绑定原生事件

`@click.native`

## 5. 非父子组件间传值

* 两种方式
1. vuex
2. 发布订阅模式/观察者模式/Bus总线机制

## 6. 子Vue中使用插槽slot

从父组件->子组件优雅地传递DOM内容
具名插槽

## 7. 作用域插槽

用于父组件给子组件传一些格式等信息。

## 8. 动态组件与v-once指令

根据`:is=xxx`的值，动态创建和销毁组件。
`v-once`可以提高性能，创建一次后放在内存里。
