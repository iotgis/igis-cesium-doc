##CoordTransform  
  
###Methods  
  
####IGis.CoordTransform.bd09togcj02(bd_lon, bd_lat)  
百度坐标系 (BD-09) 与 火星坐标系 (GCJ-02)的转换
即百度转谷歌、高德
  
名称|类型|默认值|介绍  
-|-|-|-   
bd_lon| number|0.0 |经度，弧度值。  
bd_lat| number |0.0 |纬度，弧度值。    

###### 代码示例  
    var position = IGis.CoordTransform.bd09togcj02;
    var longitude=position[0];
    var latitude=position[1];
  
####IGis.CoordTransform.gcj02tobd09(lng, lat)    
  
火星坐标系 (GCJ-02) 与百度坐标系 (BD-09) 的转换。    
即谷歌、高德转百度。  
  
名称|类型|默认值|介绍  
-|-|-|-   
lon| number|0.0 |经度，弧度值。  
lat| number |0.0 |纬度，弧度值。     
  
###### 代码示例  
 
    var position = IGis.CoordTransform.gcj02tobd09(116.325,40.3652);
    var longitude=position[0];
    var latitude=position[1];
####IGis.CoordTransform.wgs84togcj02(lon, lat)   
  
WGS84转GCj02。  
  
名称|类型|默认值|介绍  
-|-|-|-   
lon| number|0.0 |经度，弧度值。  
lat| number |0.0 |纬度，弧度值。    
  
###### 代码示例  
 
    var position = IGis.CoordTransform.wgs84togcj02(116.325,40.3652);
    var longitude=position[0];
    var latitude=position[1];
####IGis.CoordTransform.gcj02towgs84(lon, lat)  
GCJ02 转换为 WGS84。  
    
名称|类型|默认值|介绍  
-|-|-|-   
lon| number|0.0 |经度，弧度值。  
lat| number |0.0 |纬度，弧度值。    
###### 代码示例  

   
    var position = IGis.CoordTransform.gcj02towgs84(116.325,40.3652);
    var longitude=position[0];
    var latitude=position[1];