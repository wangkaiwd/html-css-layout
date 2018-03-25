### BFC (Block Formatting Context):块级格式化上下文
块级格式化上下文：用于决定块盒子的布局及浮动相互影响的范围的一个区域  

#### BFC的创建方法  
* 根元素或其它包含它的元素  
* 浮动（元素的`float`不为`none`）  
* 绝对定位元素（元素的`position`为`absolute`或`fixed`）  
* 行内块`inline-block`元素  
* 表格单元格（元素的`display:table-cell`,`html`表格单元格默认属性）  
* `overflow`的值不为`visible`的元素
* 弹性盒`flex boxes`(元素的`display:flex`)  

其中最常见的是：`overflow:hidden`,`float:left/right`,`position:absolute`。每次看到这些属性的时候，就代表了该元素创建了一个BFC了。  
一个元素不能同时存在俩个BFC中

