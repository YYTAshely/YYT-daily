# CSS伪类

## :not

- 用于选择不满足条件的元素
- 常用于设置兄弟元素的间距，如第一个不设置margin-left，其他的设置
- element:not(selector)
- 可以结合其他选择器一起使用


```CSS
div:not(:first-child){
    margin-left:5px;
}
```

## :has

- 选择含有特定子元素的选择器的伪类

## :is

- 选择多个类名，而不需要建立多个选择器

```css
ul li:is(.two, .four, .six) {
      background-color: red;
    }
/*将ul中类名为two、four和six的li设置为红色*/
```

## :where

- 与is相同，选择多个类名，而不需要建立多个选择器

### is和where的区别

- is在选择器的权重计算中起作用，优先级由选择器列表中，优先级最高的决定】
- where不创建新的层级，也就是说优先级为0，只是起到语法上的辅助

## nth-child

- 选取父元素的第n个子元素
- selector:nth-child(n)
- n可以为odd、even或则3n
- -n+3为前三个
- 按照父元素内所有子元素的顺序，不关心类型
