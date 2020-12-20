# 学习flex弹性布局总结

目标

> 掌握内容布局方式：flex 弹性布局。

认识 flex 

* 是一种布局模式（用做内容布局）：称为 弹性布局。

作用

* 控制 容器 内 子元素的 排布方式，对齐方式，排序顺序
* 调整 子元素的 宽度 ，高度 使其在不同 分辨率 下 能 更好的填充 空间。子元素能很好的 自适应 容器大小。 

使用场景

* flex布局最适合应用程序的组件和小规模布局（一维布局）

flex中的名词概念

* 最外层的是 flex容器，里面的子元素称为flex子项。

* 主轴 与 交叉轴  转换 成  水平方向，垂直方向

## 使用flex布局方式

1. 块级元素  display ： flex
2. 行内元素  display：inline-flex  

加了 display:flex 后的 容器内对 直接 子元素 的 影响

* 会将直接子元素 设置 成 display ：block,嵌套的子元素没有影响.
* 解决了 上下 margin 重叠 的问题， 父 子元素 的margin-top不会重叠
* 干掉的 float ，使用 float 不会起作用

## 作用在 flex 容器 上的 css属性

1. 主轴方向  flex-direction (row)  用来控制子项整体**排列方向**，row 是从左往右还是从右往左，column 是从往下还是从下往上
2. 是否换行  flex-wrap (nowrap) 子项整体单行显示还是换行显示，如果换行，则下面一行是否反方向显示。看到单词wrap一定是与换行显示相关的：word-wrap属性，white-space:nowrap，pre-wrap。
3. 主轴方向 是否换行  flex-flow (row nowrap) 属性是flex-direction和flex-wrap的缩写，表示flex布局的flow流动特性。
4. 水平排布内容方式  justify-content（normal） 子项的 水平方式  排布方式 ：正常文档流排布，子项居中排布，子项空格环绕排布，子项空格两边排布。
5. 单行垂直对齐子项  align-items（stretch）   子项垂直方向上的对齐方式：拉伸对齐（子项一样高），顶部对齐，底部对齐，居中对齐，基线对齐
6. 多行垂直对齐内容 align-content  则是指明 垂直方向 每一行flex元素的对齐和分布方式。如果所有flex子项只有一行，则align-content属性是没有任何效果的。



## 作用在 flex 子项 上的 css 属性

1. order 改变某一个flex子项的排序位置。
2. flex-grow  （0 不放大）  放大因子，扩展的就是flex子项所占据的宽度，扩展所侵占的空间就是除去元素外的剩余的空白间隙。值越大，元素越放大。
3. flex-shrink （1  等比缩小） 缩小因子， 值越大，缩小得越多。
4. flex-basis （auto） 指定子项的大小  当 row 是 宽， 当 column 是 height
5. flex  flex-grow  flex-shrink  flex-basis  的缩写。（0，1，auto）， 快捷值   等比放大等比缩小  auto(1,1,auto). 不放大不缩小 none（0，0，auto）
6. align-self  可覆盖 align-item ，设置特殊的 垂直对齐方式



## 总结

flex 是 display的一个属性，他约束了一套 控制 子元素 排列，对齐，排序，大小的 规则



## 学习文章

[flex 布局的基本概念](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)

[写给自己看的display: flex布局教程](https://www.zhangxinxu.com/wordpress/2018/10/display-flex-css3-css/)

[CSS3 Flexbox 布局完全指南(图解 Flexbox 布局详细教程)](https://www.html.cn/archives/8629)

[A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)