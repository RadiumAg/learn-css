# CSS 选择器

### 1.   选择器

**定义**

平常使用的CSS声明前面的标签、类名等。例如:

**标签选择器**

```
body { font: menu }
```

**类选择器**

```
.container { background-color:blue }
```



### 2. 选择符

**后代关系(空格)**
```
   .container img { object-fit:cover; }
```


**父子关系(>)**
```
   ol > li 
```

**兄弟关系(~)**

```
button ~ button {margin-left: 10px;}
```

**列(||)**

```
.col || .td {background-color:black}
```



### 3.伪类(:)

```
a:hover {color:black}
```



### 4.伪元素

如::beofre,::after,::first-letter等

# CSS优先级规则概览

#### 0级别

通配选择器，选择符和逻辑组合伪类，其中，通配选择器写做星号(*)：

```
* { color: #000 }
```

逻辑组合伪类

​	:not,:is()和:where等，这些伪类本身不影响CSS优先级。影响优先级的是括号里面的选择器。

**1级别**

标签选择器

```
<div></div>
```

**2级别**

类选择器，属性选择器和伪类

**3级别**

ID选择器

**4级别**

style属性内联

**5级别**

!important

注意:

1. CSS选择器的优先级与DOM元素的层级没有任何关系

2. 增加CSS选择器优先级的小技巧:

   ```
   重复标签本身
   .foo.foo
   
   借助属性标签
   .foo[class] {}
   #foo[id] {}
   ```

   



