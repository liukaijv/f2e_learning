# Flexbox指南 

## 基本要素

+ **主轴（main axis）：**伸缩容器的主轴，伸缩项目主要沿着这条轴进行排列布局。小心，它不一定是水平的；这主要取决于“justify-content”属性
+ **主轴起点（main-start）和主轴终点（main-end）：**伸缩项目放置在伸缩容器内从主轴起点（main-start）向主轴终点（main-start）方向。
+ **主轴尺寸（main size）：**伸缩项目在主轴方向的宽度或高度就是主轴的尺寸。伸缩项目主要的大小属性要么是宽度，要么是高度属性，由哪一个对着主轴方向决定。
+ **侧轴（cross axis）：**垂直于主轴称为侧轴。它的方向主要取决于主轴方向。
+ **侧轴起点（cross-start）和侧轴终点（cross-end）：**伸缩行的配置从容器的侧轴起点边开始，往侧轴终点边结束。
+ **侧轴尺寸（cross size）：**伸缩项目的在侧轴方向的宽度或高度就是项目的侧轴长度，伸缩项目的侧轴长度属性是「width」或「height」属性，由哪一个对着侧轴方向决定。

## 属性

### display:flex | inline-flex;(适用于伸缩容器，也就是伸缩项目的父元素)

这个是用来定义伸缩容器，是内联还是块取决于设置的值。这个时候，他的所有子元素将变成flex文档流，称为伸缩项目。

    display: other values | flex | inline-flex;

请注意：

+ CSS的columns在伸缩容器上没有效果。
+ float、clear和vertical-align在伸缩项目上没有效果。

### flex-direction（适用于伸缩容器，也就是伸缩项目的父元素）

这个主要用来创建主轴，从而定义了伸缩项目放置在伸缩容器的方向。

    flex-direction: row | row-reverse | column | column-reverse

+ **row(默认值)：**在“ltr”排版方式下从左向右排列；在“rtl”排版方式下从右向左排列。
+ **row-reverse：**与row排列方向相反，在“ltr”排版方式下从右向左排列；在“rtl”排版方式下从左向右排列。
+ **column：**类似 于row，不过是从上到下排列
+ **column-reverse：**类似于row-reverse，不过是从下到上排列。

### flex-wrap(适用于伸缩容器，也就是伸缩项目的父元素)

这个主要用来定义伸缩容器里是单行还是多行显示，侧轴的方向决定了新行堆放的方向。

    flex-wrap: nowrap | wrap | wrap-reverse 

+ **nowrap(默认值)：**伸缩容器单行显示，“ltr”排版下，伸缩项目从左到右排列；“rtl”排版上伸缩项目从右向左排列。
+ **wrap：**伸缩容器多行显示，“ltr”排版下，伸缩项目从左到右排列；“rtl”排版上伸缩项目从右向左排列。
+ **wrap-reverse：**伸缩容器多行显示，“ltr”排版下，伸缩项目从右向左排列；“rtl”排版下，伸缩项目从左到右排列。（和wrap相反）

### flex-flow（适用于伸缩容器，也就是伸缩项目的父元素）

“flex-direction”和“flex-wrap”属性的缩写版本。同时定义了伸缩容器的主轴和侧轴。其默认值为“row nowrap”。

    flex-flow: <‘flex-direction’> || <‘flex-wrap’>  

### justify-content（适用于伸缩容器，也就是伸缩项目的父元素）

用来定义伸缩项目沿着主轴线的对齐方式。当一行上的所有伸缩项目都不能伸缩或可伸缩但是已经达到其最大长度时，这一属性才会对多余的空间进行分配。当项目溢出某一行时，这一属性也会在项目的对齐上施加一些控制。

    justify-content: flex-start | flex-end | center | space-between | space-around

+ **flex-start(默认值)：**伸缩项目向一行的起始位置靠齐。
+ **flex-end：**伸缩项目向一行的结束位置靠齐。
+ **center：**伸缩项目向一行的中间位置靠齐。
+ **space-between：**伸缩项目会平均地分布在行里。第一个伸缩项目一行中的最开始位置，最后一个伸缩项目在一行中最终点位置。
+ **space-around：**伸缩项目会平均地分布在行里，两端保留一半的空间。
