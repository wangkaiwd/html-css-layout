### css知识点记录  
1. 对于`position:absolute`,元素定位将相对于最近的一个以定位的父元素，如果没有的话<font color="red">相对于`body`</font>   
2. 行内块特征：  
    1. 设置高度无效，但可以通过`line-height`来设置父元素高度，使它居中
    2. <font color="red">**对`margin`仅设置左右方向有效，上下无效；`padding`设置上下左右都有效**</font>  

3. flex布局的知识导图：  
    ![flex](./assets/flex布局导图.png)  
    重点：  
        1. `flex-grow`:定义项目的放大比例，默认为0，即存在剩余空间也不放大  
        2. `flex-shrink`:定义项目的缩小比例，默认为1，即如果空间不足，该项目将缩小  
        3. `flex`: 项目在容器上如何伸缩。  
            <font color="red">1个值： 无单位：grow,有单位：basis  </font>  
            2个值:  无单位：grow & shrink,有单位：grow & basis  
            3个值：grow & shrink & basis  
        4. `flex-basis`: 在不伸缩的情况下子容器的原始尺寸。主轴为横向时代表宽度，主轴为纵向时代表高度。