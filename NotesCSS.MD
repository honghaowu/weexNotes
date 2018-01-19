
## [1.通用样式](#1)
## [2.文本样式](#2)
## <h2 id="1">1.通用样式</h2>
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
  > Flexbox 包含 flex 容器和 flex 成员项，
#### flex容器    
  1. 在Weex 中，Flexbox 是默认且唯一的布局模型，所以你不需要手动为元素添加 display: flex; 属性。   
  2. flex-direction主轴的排列方向，默认column,row/column;注意,在一般的前端flex布局中，默认是row.  
  3. justify-content，flex成员项在主轴上的排列，flex-start:左对齐，flex-end:右对齐，enter:居中对齐，space-between：两端对齐，space-around:两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。
  4. align-items属性定义项目在交叉轴上如何对齐：  
     > stretch：默认值，拉伸高度100%，与flex容器一样高  
     > flex-start:上对齐；  
     > flex-end: 下对齐，  
     > center：中间对齐。
#### flex成员项  
  > flex:1;平分空间
### 定位position：
  - relative 是默认值，指的是相对定位；
  - absolute 是绝对定位，以元素的容器作为参考系；
  - fixed 保证元素在页面窗口中的对应位置显示；
  - sticky 指的是仅当元素滚动到页面之外时，元素会固定在页面窗口的顶部。
### transform支持如下：
  > translate( [, ]?)/translateX( )/translateY( )/scale( )/scaleX( )/scaleY( )/rotate( )/rotateX( ) v0.14+/rotateY( ) v0.14+/perspective( ) Android 4.1及以上版本支持 v0.16+/transform-origin: number/percentage/keyword(top/left/right/bottom)
### transition 
  > transition-property：过渡的属性  
  > transition-duration:指定transition过渡的持续时间 
  > transition-delay： 延迟时间  
  > transition-timing-function： 过渡的曲线：
### 伪类   
  > Weex 支持四种伪类：active, focus, disabled, enabled    
  > 所有组件都支持 active, 但只有 input 组件和 textarea 组件支持 focus, enabled, disabled。
### 线性渐变：  
  > background-image: linear-gradient(to top,#a80077,#66ff00)   
  > 不支持 background 简写.
## <h2 id="2">2.文本样式</h2>
   > 适用于text和input组件中的文本    
   > *color<br>font-size<br>font-weight<br>font-style<br>text-align<br>text-decoration<br>text-overflow* > 
   > **lines:number;仅在<text> 组件中支持。默认值是 0 代表不限制行数。,例如设为3.则表示显示3行，超出部分，显示省略号**
