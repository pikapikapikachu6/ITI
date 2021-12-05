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

- 指定宽度: "grid-template-columns"  
  固定宽度：  
  .grid {  
    &emsp; display: grid;  
    &emsp; grid-template-columns: 100px 100px 100px; // 三列   
  }  
  浮动宽度：  
  .grid {  
    &emsp; display: grid;  
    &emsp; grid-template-columns: 1fr 1fr 1fr; // fr表示剩余空间  
  }

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

  


