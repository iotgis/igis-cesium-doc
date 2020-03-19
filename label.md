##new IGis.Label(labelOptions)  
  
生成一个标签对象。  
返回值：生成的label对象。 
  
  
名称|类型|默认值|介绍  
-|-|-|-   
pointList|数组[{name,position}]||扫描后展示的标签。
<a herf="#labelOptions">labelOptions</a>| object ||标签label的样式属性。
  
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
distanceDisplayCondition|object|{near:0,far:Number.MAX_VALUE}|指定能看到标签的最近和最远距离。 
  
  
     const labelOptions = {
                show: true,     
                text: "这是一个label标签",
                showBackground: true,
                backgroundColor: new IGis.Color(1, 1, 1, 0.5),
                font: "30px sans-serif",
                fillColor: IGis.Color.BLACK,
                disableDepthTestDistance: Number.POSITIVE_INFINITY,
                distanceDisplayCondition:{
                      near:0,
                      far:5000
                 }

            }
      const label = new IGis.Label(labelOptions);
  