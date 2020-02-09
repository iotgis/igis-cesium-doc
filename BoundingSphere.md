##new IGis.BoundingSphere(center,radius)  
创建一个具有中心和半徑的包圍球。    
  
名称|类型|默认值|介绍  
-|-|-|-   
center|Cartesian3||边界球的中心。  
radius|number|0.0|边界球的半径。    
  
###### 代码示例
    var center=new IGis.Cartesian3(x,y,z);
    var boundingSphere=new IGis.BoundingSphere(center,10);