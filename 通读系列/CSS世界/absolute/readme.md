#### 无依赖Position

定义

不设置left/top/bottom/right



绝对定位元素铺满相对定位元素使用: 

```html
  <div style="width: 100px; height: 100px; background-color: blue; position: relative;">
        <div style="position: absolute; background-color: aliceblue; left: 0; top:0;bottom: 0; right: 0;"></div>
    </div>
```

