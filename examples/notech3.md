# ch3 Vue基础

## 生命周期钩子

8+3个

计算属性有缓存机制，能减少重复计算次数，效率更高。

## 条件渲染 v-if v-show

控制DOM节点是否被渲染。
v-if    会从DOM中删除和添加
v-else-if
v-else
v-show  仍然存在于DOM中，但display:none。 性能更高

## 列表渲染 v-for

* 改变数组的方式：
1. 直接改变对象的引用
2. 调用变异方法
3. 调用 `Vue.set / vm.$set` 方法

注：通过 下标or点属性 赋值不会刷新View。

`<template>` 占位，类似React中的 `<DocumentFragment>`
