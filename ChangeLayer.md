##new IGis.ChangeLayer(viewer)  
  
切换图层。
  
名称|类型|默认值|介绍  
-|-|-|-  
viewer|Viewer||The viewer  

###Methods   
  
####layerButton(url,classOptions)  
创建一个按钮可以切换图层。  
    
名称|类型|默认值|介绍  
-|-|-|-  
url|string|'http://www.google.cn/maps/vt?lyrs=s@800&x={x}&y={y}&z={z}'|要切换的图层地址，默认为谷歌地图。  
<a herf="#classOptions">classOptions</a>|object||图层切换按钮的样式对象。

  
#####<a name="classOptions">classOptions</a>
  
  
名称|类型|默认值|介绍
-|-|-|-  
id|string||所创建dom的Id。  
domType|string|"div"|所创建dom的类型。  
fatherDom|{HTMLElement}|document.body|所创建dom的父级dom。  
class|string||创建dom的样式类名。
  
####changelayer(url)  
切换图层。
  
名称|类型|默认值|介绍  
-|-|-|-  
viewer|Viewer||The viewer  
url|string|'http://www.google.cn/maps/vt?lyrs=s@800&x={x}&y={y}&z={z}'|要切换的图层地址，默认为谷歌地图。  
 
  
