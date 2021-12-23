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
