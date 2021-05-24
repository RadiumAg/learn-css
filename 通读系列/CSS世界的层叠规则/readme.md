# CSS世界的层叠规则

## 层叠上下文规则

1.谁大谁上

2.后来居上



## 层叠上下文的创建

1.根层叠上下文

2.z-index值为数值的定位元素的传统"层叠上下文"，对于position值为relative/absolute以及Firefox/IE浏览器(不包括Chrome浏览器)下含有position:fixed 生命的定位元素，当其z-index值不是auto的时候，会创建层叠上下文。

3.其他CSS3属性

​	1.元素为flex布局元素，同时z-index值不是auto。

​	2.元素的opacity值不是1.

​    3.元素的transform值不是none.

​    4.元素mix-blend-mode值不是normal。

​    5.元素的filter值不是none。

​    6.元素的isolation值是isolate.

​    7.will-change属性值为上满2-6的任意一个

​    8.元素的-webkit-overflow-scrolling设为touch。