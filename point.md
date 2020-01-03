##new IGis.Point(pointOptions)  
生成一个点对象。  
返回值：生成的point对象。
  
名称|类型|默认值|介绍  
-|-|-|-   
<a herf="#pointOptions">pointOptions</a>| object| |点的样式属性。 
  
#####<a name="pointOptions">pointOptions </a>  
  
名称|类型|默认值|介绍  
-|-|-|-   
show|boolean|false|是否显示点。  
pixelSize |number |1.0 |以像素为单位指定大小。  
color |Color |Color.YELLOW |指定点的颜色。  
outlineColor |Color |Color.RED |点外边线颜色。  
outlineWidth |number |0 |点外边线的宽度。  
disableDepthTestDistance |number |0 |指定距相机多少米禁用深度测试。      
  
    const pointOptions = {
                show: true,
                pixelSize: 2.0,
                color: IGis.Color.WHITE,
                outlineColor: IGis.Color.RED
            };
    const point = new IGis.Point(pointOptions);