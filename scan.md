##Scan()
创建扫描面效果。    
  
###Methods  
  
####IGis.Scan.add(center,options)  
添加扫描面。  
返回值：生成的扫描面scan。  
  
名称|类型|默认值|介绍  
-|-|-|-   
center|数组或object{lon,lat}| |扫描面中心点经纬度。 
<a herf="#options">options</a>| object ||扫描面样式。
  


  
#####<a name="options">options</a>  
  
名称|类型|默认值|介绍  
-|-|-|-    
radius|number|100|扫描面半径。    
scanColor|Color||扫描面颜色。
duration |number |30 |扫描一圈所用的时间（秒）。  


######代码示例  
    var scan=IGis.Scan.add([116.1564,40.6454,0],{
           radius：40，
          scanColor:IGis.Color.RED,
          duration:30
    })

####IGis.Scan.delete(scan)  
清除扫描面。
  
名称|类型|默认值|介绍  
-|-|-|-   
scan| object ||要移除的特定的扫描面，如果不填，则移除所有的扫描面。  

#######代码示例
    IGis.Scan.delete();


  
####addCircleScan(center,options)  
添加扫描面。  
返回值：生成的扫描面scan。  
  
名称|类型|默认值|介绍  
-|-|-|-   
center|数组或object{lon,lat}| |扫描面中心点经纬度。 
<a herf="#circleOptions">options</a>| object ||扫描面样式。
  
  
#####<a name="circleOptions">options</a>  
  
名称|类型|默认值|介绍  
-|-|-|-    
maxRadius|number|100|扫描面半径。    
scanColor|Color||扫描面颜色。
duration |number |30 |扫描一圈所用的时（秒）。   
######代码示例

     var scan=IGis.Scan.addCircleScan([116.1564,40.6454,0],{
           radius：40，
          scanColor:IGis.Color.RED,
          duration:30
    })