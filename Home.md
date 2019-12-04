##new IGis.Home(viewer)  
  
一个简单的按钮能让摄像机从当前位置飞行到默认位置。
  
名称|类型|默认值|介绍  
-|-|-|-  
viewer|Viewer||The viewer  
<a herf="#options">options</a>|object||摄像机飞行至默认位置属性。   

###Methods   
  
####homeButton(options,classOptions)  
创建一个按钮能让摄像机从当前位置飞行到默认位置。  
    
名称|类型|默认值|介绍  
-|-|-|-  
viewer|Viewer||The viewer  
<a herf="#classOptions">classOptions</a>|object||home按钮的样式对象。

  
#####<a name="classOptions">classOptions</a>
  
  
名称|类型|默认值|介绍
-|-|-|-  
id|string||所创建dom的Id。  
domType|string|"div"|所创建dom的类型。  
fatherDom|{HTMLElement}|document.body|所创建dom的父级dom。  
class|string||创建dom的样式类名。
  
####home(options)  
摄像机飞行至默认位置。
  
名称|类型|默认值|介绍  
-|-|-|-  
viewer|Viewer||The viewer  
<a herf="#options">options</a>|object||摄像机飞行至默认位置属性。  
  
 
  
#####<a name="options">options</a>  
  
名称|类型|默认值|介绍  
-|-|-|-  
position|object或者[]|{lon:116.391134,lat:39.901334,alt:800}|摄像机目的地经纬高位置。{lon,lat,alt} 或者[position[0],position[1],position[2]]。  
orientation|object或者[]|{heading:0,pitch:Math.PI/4,roll:0,}|摄像机的偏转角度。heading:弧度的航向分量，pitch:弧度的螺距分量，roll:滚动分量(以弧度为单位)。
