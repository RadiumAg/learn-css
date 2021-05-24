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

![](C:\Users\Iloveprpr\Desktop\lean-css\通读系列\盒尺四大家族\01.png)

