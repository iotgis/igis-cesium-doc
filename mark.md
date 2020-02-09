##Mark  
以点或图片的形式添加标记。  
  
###Methods  
  

####IGis.Mark.add(pointOptions,billboardOptions) 
鼠标左键点击添加标记。  
  
名称|类型|默认值|介绍  
-|-|-|-   
<a herf="#pointOptions">pointOptions</a>| object| |点的样式属性。 
<a herf="#billboardOptions">billboardOptions</a>| object ||图片的样式属性。
<a herf="#markOptions">markOptions</a>| object ||标记的属性。
  
#####<a name="pointOptions">pointOptions </a>  
  
名称|类型|默认值|介绍  
-|-|-|-   
show|boolean|false|是否显示点。  
pixelSize |number |1.0 |以像素为单位指定大小。  
color |Color |Color.YELLOW |指定点的颜色。  
outlineColor |Color |Color.RED |点外边线颜色。  
outlineWidth |number |0 |点外边线的宽度。  
disableDepthTestDistance |number |0 |指定距相机多少米禁用深度测试。    
  
#####<a name="billboardOptions">billboardOptions</a>  
 名称|类型|默认值|介绍  
-|-|-|-    
show|boolean|true|是否显示广告牌。  
image |string ||指定要用于广告牌的Image,URL或Canvas。
scale |number |2.0 |指定要用于图像大小的比例。
color |Color  |Color.WHITE |指定图像的色调。
width |number ||指定广告牌的宽度（以像素为大小），并覆盖原始大小。
height|number ||指定广告牌的高度（以像素为大小），并覆盖原始大小。
disableDepthTestDistance |number |0 |指定距相机多少米禁用深度测试。  
  
#####<a name="markOptions">markOptions</a>  
 名称|类型|默认值|介绍  
-|-|-|-    
id |string ||标记的Id
name |string ||标记的名称。   

####IGis.Mark.cancel()  
取消鼠标左键添加标记。  
   
###### 代码示例  
`IGis.Mark.cancel();`    
####IGis.Mark.delete()  
  
删除选中的标记。  

###### 代码示例  
`IGis.Mark.delete();`    
####IGis.Mark.deleteAll()  
  
删除所有的标记。
###### 代码示例  
`IGis.Mark.deleteAll();`    