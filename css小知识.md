### css知识点记录  
1. 对于`position:absolute`,元素定位将相对于最近的一个已定位的父元素，如果没有的话<font color="red">相对于浏览器</font>   
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
4. margin的零活运用（双飞翼布局）  
   1. margin百分比  
      规定基于父元素的宽度的百分比的外边距  
   2. margin负边距  
5. 设置初始化`ie`盒模型：`box-sizing:border-box`
   ```css
   html {
       box-sizing: border-box;
   }
   *,
   *:after,
   *:before {
       box-sizing: inherit;
   }
   ```
   选择请*无法覆盖到伪元素，所以要给`:after`和`:before`分别设置，  
   然后通过继承的方式应用到所有元素，方便为某个元素和其后代元素设置`box-sizing:content-box`
6. `body`有默认`8px`的`margin`
7. `transparent`：全透明黑色  
8. `:not`选择器  
   ![:not](./assets/not.png)  
9. 宽高等比例缩放：  
   ```html
   <div class="box">
        padding
   </div>
   ```
   ```css
   .box {
        width: 20%;
        background-color: pink;
    }
    .box::after {
        content: '';
        display: block;
        /* 现在伪元素的父亲是box,高度应该和box的高度相等 */
        padding-top: 100%;
    }
   ```  
10. 消失边界线：  
    效果图：  
    ![边界消失](./assets/边界消失.png)  
    ```html
    <div class="ul-container">
        <ul>
            <li>测试</li>
            <li>消失</li>
            <li>边界线</li>
            <li>右侧</li>
            <li>边界线</li>
            <li>消失</li>
            <li>测试</li>
        </ul>
    </div>
    ```
    ```css
    .ul-container {
        overflow: hidden;
    }
    .ul-container, 
    ul{
        width:300px;
        margin-left: -1px;
    }
    li{
        float:left;
        width:99px;
        border-left:1px solid #999;
    }
    ```  
    小技巧：<font color="red">父元素添加`overflow:hidden`，`li`添加反向边框，`ul`增加一个负的`margin`来实现</font>