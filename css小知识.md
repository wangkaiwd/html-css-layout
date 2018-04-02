### css知识点记录  
1. 对于`position:absolute`,元素定位将相对于最近的一个以定位的父元素，如果没有的话<font color="red">相对于`body`</font>   
2. flex布局的知识导图：  
    ![flex](./assets/flex布局导图.png)  
    重点：  
        1. `flex-grow`:定义项目的放大比例，默认为0，即存在剩余空间也不放大  
        2. `flex-shrink`:定义项目的缩小比例，默认为1，即如果空间不足，该项目将缩小  
        3. `flex`: 项目在容器上如何伸缩。  
            <font color="red">1个值： 无单位：grow,有单位：basis  </font>  
            2个值:  无单位：grow & shrink,有单位：grow & basis  
            3个值：grow & shrink & basis  
        4. `flex-basis`: 在不伸缩的情况下子容器的原始尺寸。主轴为横向时代表宽度，主轴为纵向时代表高度。
3. 等分布局的实现思想  
   ![等分布局](./assets/等分布局.png)  
   ![等分布局公式转换](./assets/等分布局转换.png)  
4. margin的零活运用  
   1. margin百分比  
      规定基于父元素的宽度的百分比的外边距  
   2. margin负边距
   