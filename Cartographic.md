##new IGis.Cartographic(longitude,latitude,height)  
通过经度、纬度、高度来定义的位置信息。  
  
名称|类型|默认值|介绍  
-|-|-|-   
longitude| number|0.0 |经度，弧度值。  
latitude| number |0.0 |纬度，弧度值。  
height |number |0.0 |高度，米。   
  
###Methods  
  
####IGis.Cartographic.fromCartesian(cartesian,ellipsoid)  
  
笛卡尔坐标转经纬度；  
返回值：Cartographic 经纬度。  
  
名称|类型|默认值|介绍  
-|-|-|-   
cartesian| Cartesian3| |要转换为经纬度的笛卡尔三维坐标。  
ellipsoid| Ellipsoid |Ellipsoid.WGS84 |位置所在的椭圆体。