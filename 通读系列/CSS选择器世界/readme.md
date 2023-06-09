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

   

# 元素选择器的级联语法

(1)元素选择器是唯一不能重复自身的选择器

(2)级联使用的时候元素选择器必须写在最前面





# 属性选择器

**1.[attr|='val']**

**定义**

属性值起始片段完全匹配选择器，表示具有attr的元素，其值要么正好是val,要么以val外加短横线- (U+002D) 开头，**|=** 用于连接需要匹配的属性和属性内容。





# 用户行为伪类

## active

**定义**

:active 伪类可以用于设置元素激活状态的样式，可以通过点击鼠标主键，也可以通过手指或者触控笔点击触摸屏触发激活状态。



**:active伪类与CSS数据**

想知道两个按钮的点击率

```css
.button-l:active::after {
   content:url(./pixel.gif?action=click&id=button1);
   display:none;
}

.button-2:active::after {
    content:url(./pixel.gifaction=click&id=button2);
    display:none;
}
```

**注意**

1.IE浏览器下`:active` 样式的应用是无法冒泡的

2.在IE浏览器下，<html>,<body>元素应用`:active`伪类设置背景色之后，背景色是无法还原的。

3.移动端`Safari` 浏览器下，`:active` 伪类默认是无效的。

## :focus伪类匹配机制

**匹配机制**

与:active不同，`:focus`伪类默认只能匹配特定的元素，包括:

1. 非disabled状态的表单元素，如`<input>` ，`<select>` ,`button`
2. 包含`href` 属性的`<a>` 元素
3. `<area>` 元素
4. HTML5的 `<summary>` 元素。

如何让普通元素响应 

1.`:focus`, 设置了`HTML` `contenteditable`属性的普通元素可以应用`:focus` 伪类。例如:

```html
<div contenteditable="true"></div>
<div contenteditable="plaintext-only"></div>
```

2.设置`tabindex`

```html
<div tabindex="-1"></div>
```



## 整体焦点伪类:focus-within

**定义**

在当前元素或是当前元素的任意子元素处于聚焦状态时去匹配。



## 键盘焦点伪类:focus-visible

**定义**

只聚焦，键盘焦点



## 超链接伪类:any-link

**定义**

1. 匹配所有设置了href属性的链接元素，包括`<a>` , `<link>` 和 `<area>` 这3种元素。
2. 匹配所有匹配 `:link` 伪类或者 `:visited` 伪类的元素











