# CSS display grid
1. 二维布局方式： 行 ｜ 列  
   可以同时控制行和列的排布和对齐方式  
  
2. 由水平线和垂直线构成   
  - 两条水平线之间的区域叫做行轨道  
  - 两条垂直线之间的区域叫做列轨道  

3. 使用方式：  
-  .grid {  
    &emsp; display: grid;  
  }

4. 指定宽度: "grid-template-columns"    
-  固定宽度：    
  .grid {  
    &emsp; display: grid;  
    &emsp; grid-template-columns: 100px 100px 100px; // 三列   
  }  
- 浮动宽度：    
  .grid {  
    &emsp; display: grid;  
    &emsp; grid-template-columns: 1fr 1fr 1fr; // fr表示剩余空间  
  }

5. 设置间距： 
- 列间距：column-gap  
  .grid {  
    &emsp; display: grid;  
    &emsp; grid-template-columns: 1fr 1fr 1fr;  
    &emsp; column-gap: 24px;  
  }


- 行间距：row-gap  
  .grid {  
    &emsp; display: grid;  
    &emsp; grid-template-columns: 1fr 1fr 1fr;  
    &emsp; row-gap: 24px;  
  }

- 行和列间距统一设置：gap    
  .grid {  
    &emsp; display: grid;  
    &emsp; grid-template-columns: 1fr 1fr 1fr;  
    &emsp; gap: 24px;  
  }

6. 对齐方式：  
- 有水平方向的行轴和竖直方向的块轴
- 垂直方向上对其元素： align-items  
  a. 居中对齐： center  
  b. 靠下对齐： end
- 垂直方向上对其元素： justify-items  
  a. 居中对齐： center  
  b. 靠右对齐： end
  c. 两端对其： space-between

7. 行轨道和列轨道的尺寸小于容器，可以对轨道进行对齐：
- 行轨道：align-content  
  a. 居中对齐： center  
  b. 靠下对齐： end
- 列轨道：justify-content  
  a. 居中对齐： center  
  b. 靠右对齐： end
  c. 两端对其： space-between



  


