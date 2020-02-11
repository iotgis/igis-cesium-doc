##new IGis.Polyline(polylineOptions)  
根据提供的点集画一条线。  
返回值：生成的point对象。
  
名称|类型|默认值|介绍  
-|-|-|-   
<a herf="#polylineOptions">polylineOptions</a>| object| |点的样式属性。 
  
#####<a name="polylineOptions">polylineOptions </a>  
  
名称|类型|默认值|介绍  
-|-|-|-   
show|boolean|true|是否显示线。  
width |number |1.0 |线的宽度。  
material |Material |Color.Green |指定线的材质。  
clampToGround |boolean |true|是否贴地形。  
positions |数组 | |用于画线的点集。  
  
            var point2 = [120.15122140, 30.23081891,0];
            var point1 = [120.15645621, 30.22905741,0];
            var positions=[];
            positions.push(point1[0],point1[1],0,point2[0],point2[1],0);
            var line=new IGis.Polyline({
                positions:positions,
                width:5,
                material:new IGis.Color.RED
            })
            var polyline = IGis.Tags.add({polyline:line});