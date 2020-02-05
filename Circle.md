##new IGis.Circle(circleOptions)  
生成一个圆形。  
返回值：生成的圆形。
  
名称|类型|默认值|介绍  
-|-|-|-   
<a herf="#circleOptions">circleOptions</a>| object| |圆的样式属性。 
  
#####<a name="circleOptions">circleOptions </a>  
  
名称|类型|默认值|介绍  
-|-|-|-   
show|boolean|false|是否显示点。  
radius |number |10.0 |圆的半径大小。  
color |Color |Color.WHITE |指定圆的颜色。  
zIndex |number |0 |指定圆的遮挡顺序。  

  
    const circleOptions = {
                show: true,
                radius: 20,
                color: IGis.Color.RED.withAlpha(0.3)
            };
    const circle = new IGis.Circle(circleOptions);