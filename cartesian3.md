##new IGis.Cartesian3(longitude,latitude,height)  
通过x,y,z来定义的笛卡尔坐标信息。  
  
名称|类型|默认值|介绍  
-|-|-|-   
x|number|0.0|X组件。  
y|number|0.0|Y组件。  
z|number|0.0|Z组件。    
###### 代码示例
    var cartesian3=new IGis.Cartesian3(x,y,z);
  
###Methods  
  
####IGis.Cartesian3.fromDegrees(longitude, latitude, height, ellipsoid)    
通过给定的经纬度值返回一个笛卡尔坐标值
  
  
名称|类型|默认值|介绍  
-|-|-|-   
longitude| number|0.0 |经度，弧度值。  
latitude| number |0.0 |纬度，弧度值。  
height |number |0.0 |高度，米。     
ellipsoid|Ellipsoid |Ellipsoid.WGS84 |位置所在的椭圆体。   
  
###### 代码示例  
    var cartesian3 = IGis.Cartesian3.fromDegrees(116.45624,40.53441,0);