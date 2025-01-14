# :is

## 作用

：is的值后面可以跟组件名(字符串)，或则可以是一个组件对像，来决定当前按渲染对象

```html
<template>
  <div>
    <!-- 动态渲染当前选中的组件 -->
    <component :is="currentComponent" />
    
    <button @click="changeComponent('A')">显示组件 A</button>
    <button @click="changeComponent('B')">显示组件 B</button>
  </div>
</template>
```

## 配合keep-alive来缓存切换组件

```html
<template>
  <div>
    <!-- 动态组件并缓存 -->
    <keep-alive>
      <component :is="currentComponent" />
    </keep-alive>
    
    <button @click="changeComponent('ComponentA')">显示组件 A</button>
    <button @click="changeComponent('ComponentB')">显示组件 B</button>
  </div>
</template>
```