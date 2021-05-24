# 内联元素与流



## x-height

​	middle指的是基线往上1/2 x-height 高度。



## 内联元素的基石line-height

​	对于非替换元素的纯内联元素，其可视高度完全由line-height决定.

行距=line-height - font-size



## 为什么line-height 可以让内联元素"垂直居中"

​	1.要让单行文字垂直居中，只需要line-height这个一个属性就可以了。

​	2.多行文本或者替换元素的垂直居中实现原理需要vertical-align属性才可以。

 

## vertical-align

​	作用的前提：只能应用于内联元素以及display值为table-cell的元素。

