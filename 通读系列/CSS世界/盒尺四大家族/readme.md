# 盒尺寸四大家族

##### 替换元素和非替换元素 

替换元素：修改某个属性值呈现的内容就可以被替换的元素被称为"替换元素"。

替换元素和非替换元素的区别就是src和content。



## 深入了解Content元素

##### content和替换元素关系解析

1.使用content生成的文本是无法选中，无法复制的。

2.不能左右:empty 伪类。

3.content动态生成值无法获取。



##### 了解content开启闭合符号生成

```css
<p lang="ch"><q>这本书很赞！</q></p> 
<p lang="en"><q>This book is very good!</q></p> 
<p lang="no"><q>denne bog er fantastisk!</q></p> 
/* 为不同语言指定引号的表现 */ 
:lang(ch) > q { quotes: '“' '”'; } 
:lang(en) > q { quotes: '"' '"'; } 
:lang(no) > q { quotes: '«' '»'; } 
/* 在 q 标签的前后插入引号 */ 
q:before { content: open-quote; } 
q:after { content: close-quote; }
```



![](.\01.png)



##### 深入理解content计数器

​	1.属性counter-reset:"计数器-重置""的有意思。起个名字，默认是0。

​	2.counter-increment:计数器递增。



##### 温和的padding

使用label模拟按钮

```css
label { 
 display: inline-block; 
 line-height: 20px; 
 padding: 10px; 
}
```



##### 激进的margin属性

margin负数，表示充分可利用空间

CSS 等高布局



##### 正确看待CSS世界里的margin合并

1.父级和第一个/最后一个子元素，案例:https://demo.cssworld.cn/4/3-3.php

2.相邻兄弟元素margin合并。

3.空块级元素的margin合并

###### margin合并计算规则

1.正正取最大值

2.正负值相加

3.负负值最负值



##### 深入理解CSS中的margin:auto

###### margin:auto的填充规则如下:car:  ：​

1.如果一侧定值，一侧auto,则auto为剩余空间大小。

2.如果两侧均是auto，则平分剩余空间。



使用margin:auto 垂直居中:

```css
.son { 
 position: absolute; 
 top: 0; right: 0; bottom: 0; left: 0; 
 width: 200px; height: 100px; 
 margin: auto; 
}
```

