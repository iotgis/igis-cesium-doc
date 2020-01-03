##Scan
创建扫描面效果。    
  
###Methods  
  
####add(center,options)  
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



####delete(pointList,pointOptions,labelOptions,scan)  
清除扫描面 并以标签的形式展示扫描结果。  
  
名称|类型|默认值|介绍  
-|-|-|-   
pointList|数组[{name,position}]||扫描后展示的标签。
<a herf="#pointOptions">pointOptions</a>| object| |标签点的样式属性。 
<a herf="#labelOptions">labelOptions</a>| object ||标签label的样式属性。
scan| object ||要移除的特定的扫描面，如果不填，则移除所有的扫描面。  
  
  
#####<a name="pointOptions">pointOptions </a>  
  
名称|类型|默认值|介绍  
-|-|-|-   
show|boolean|false|是否显示点。  
pixelSize |number |1.0 |以像素为单位指定大小。  
color |Color |Color.YELLOW |指定点的颜色。  
outlineColor |Color |Color.RED |点外边线颜色。  
outlineWidth |number |0 |点外边线的宽度。  
disableDepthTestDistance |number |0 |指定距相机多少米禁用深度测试。    
  
#####<a name="labelOptions">labelOptions</a>  
 名称|类型|默认值|介绍  
-|-|-|-    
show |boolean |true |是否显示label。  
text |string |"label"|label要显示的文字。  
font |string ||字体及大小。  
scale |number |1.0 |label放大倍数。  
showBackground |boolean |true |是否显示背景颜色。  
backgroundColor |Color|Clor.AQUA |背景颜色。  
horizontalOrigin |||垂直位置。  
verticalOrigin |||水平位置。  
fillColor |Color |Color.WHITE |填充颜色。  
outlineColor |Color |Color.BLACK |外框颜色。  
outlineWidth |number |2 |边框宽度。  
disableDepthTestDistance |number |0 |指定距相机多少米禁用深度测试。   
  
  
  
####clearScanTags(tag)    
清楚扫描面标签。 

名称|类型|默认值|介绍  
-|-|-|-   
tag|object||要清除的扫描面标签，如果不填，则默认清除全部扫描面。   
  
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
duration |number |30 |扫描一圈所用的时间（秒）。  