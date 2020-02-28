# js 开发规范

> 以最小commit为原则，防止同事提交代码风格不一致，导致冲突，以下规则为必须，后续可以根据大家开发习惯进行修改

# 开发前

1. 前端开发规范严格按照 [eslint-config-alloy](./eslint-config-alloy.md) 配置编辑器
2. 项目中已经引入eslint配置，需要及时处理 eslint 的错误或者警告提示


## 命名

- 组件名应该以高级别的 (通常是一般化描述的，功能的) 单词开头，以描述性的修饰词结尾。如 `SearchButtonClear.vue`
- 完整单词的组件名 不要简写

## 组件大小写 PascalCase

```vue
<MyComponent/>
```

## Prop 名大小写

```js
props: {
  greetingText: String
}
```

## 多个 attribute 的元素,一行一个

```html
<img
  src="https://vuejs.org/images/logo.png"
  alt="Vue Logo"
>
```

## 模板中简单的表达式

> 组件模板应该只包含简单的表达式，复杂的表达式则应该重构为计算属性或方法。

```html
<!-- 在模板中 -->
{{ normalizedFullName }}
```

```js
// 复杂表达式已经移入一个计算属性
computed: {
  normalizedFullName: function () {
    return this.fullName.split(' ').map(function (word) {
      return word[0].toUpperCase() + word.slice(1)
    }).join(' ')
  }
}
```

## 简单的计算属性

> 应该把复杂计算属性分割为尽可能多的更简单的属性。

```js
computed: {
  basePrice: function () {
    return this.manufactureCost / (1 - this.profitMargin)
  },
  discount: function () {
    return this.basePrice * (this.discountPercent || 0)
  },
  finalPrice: function () {
    return this.basePrice - this.discount
  }
}
```

## 指令缩写

统一使用指令缩写如 @event :value 不使用 v-on v-bind


## 自闭和

```vue
<MyComponent/>
```

## vue中实例选项的顺序书写

> 每个属性之间添加空行，方便阅读

- el
- name
- components
- directives
- filters
- extends
- mixins
- props
- watch
- beforeCreate
- created
- beforeMount
- mounted
- beforeUpdate
- updated
- activated
- deactivated
- beforeDestroy
- destroyd
- methods

## 单文件组件的顶级元素的顺序

```html
<!-- ComponentB.vue -->
<template>...</template>
<script>/* ... */</script>
<style>/* ... */</style>
```

## 必须在 v-if/v-else-if/v-else 中使用 key

```html
<div
  v-if="error"
  key="search-status"
>
  错误：{{ error }}
</div>
<div
  v-else
  key="search-results"
>
  {{ results }}
</div>
```

## 元素选择器应该避免在 scoped 中出现。

## 函数命名规范

**浏览器事件**

- onClickBtn
- onMouseMoveBtn
- onMouseUpBtn
- onMouseenterBtn

**业务事件**

- handleLoginParams
- handleRegisterBody

**请求函数**

- fetchSomething

