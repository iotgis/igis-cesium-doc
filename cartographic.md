##new IGis.Cartographic(longitude,latitude,height)  
通过经度、纬度、高度来定义的位置信息。  
  
名称|类型|默认值|介绍  
-|-|-|-   
longitude| number|0.0 |经度，弧度值。  
latitude| number |0.0 |纬度，弧度值。  
height |number |0.0 |高度，米。    
  
######代码示例
`var cartographic=new IGis.Cartographic(116.4545,40.15654,0);` 
  
###Methods  
  
####IGis.Cartographic.fromCartesian3(cartesian)  
  
笛卡尔坐标转经纬度；  
返回值：Cartographic 经纬度。  
  
名称|类型|默认值|介绍  
-|-|-|-   
cartesian| Cartesian3| |要转换为经纬度的笛卡尔三维坐标。  
  
    var cartesian=new IGis.Cartesian3(x,y,z);   
    var cartographic=IGis.Gratographic.fromCartesian3(cartesian);
      
