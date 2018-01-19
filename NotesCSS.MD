## 通用样式
### 盒模型
  1. padding margin要分写,如：padding-left/margin-left   
  2. boder写法：border-left-style,border-left-width,border-left-color  
  3. border-radius:  
      border-bottom-left-radius {length}：，非负值, 默认值 0  
      border-bottom-right-radius {length}：，非负值, 默认值 0   
      border-top-left-radius {length}：，非负值, 默认值 0   
      border-top-right-radius {length}：，非负值, 默认值 0   
  **注意： Weex 对于长度值目前只支持像素值，不支持相对单位（em、rem）。    
        Weex 盒模型的 box-sizing 默认为 border-box，即盒子的宽高包含内容、内边距和边框的宽度，不包含外边距的宽度。**
### Flex布局
  1. Flexbox 包含 flex 容器和 flex 成员项，在Weex 中，Flexbox 是默认且唯一的布局模型，所以你不需要手动为元素添加 display: flex; 属性。   
  2. flex-direction主轴的排列方向，默认column,row/column;注意,在一般的前端flex布局中，默认是row.
