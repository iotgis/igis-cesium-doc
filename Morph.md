##new IGis.Morph(viewer,classOptions2D,classOptions3D)   
二三维转换基类。 
  

  
名称|类型|默认值|介绍  
-|-|-|-
viewer|Viewer||The viewer  
<a herf="#classOptions2D">classOptions2D</a>|object||创建2D按钮属性。  
<a herf="#classOptions3D">classOptions3D</a>|object||创建3D按钮属性。    
  
 
###Methods   
  
####morphButton(classOptions2D,classOptions3D)  
创建一个2D按钮实现转二维视图；创建一个3D按钮实现转三维。  
  
名称|类型|默认值|介绍  
-|-|-|-  
<a herf="#classOptions2D">classOptions2D</a>|object||创建2D按钮属性。  
<a herf="#classOptions3D">classOptions3D</a>|object||创建3D按钮属性。      

#####<a name="classOptions2D">classOptions2D</a>  
名称|类型|默认值|介绍
-|-|-|-  
id|string||所创建dom的Id  
domType|string|"div"|所创建dom的类型。  
fatherDom|{HTMLElement}|document.body|所创建dom的父级dom。  
class|string||创建dom的样式类名。  
#####<a name="classOptions3D">classOptions3D</a>  
名称|类型|默认值|介绍
-|-|-|-  
id|string||所创建dom的Id。  
domType|string|"div"|所创建dom的类型。  
fatherDom|{HTMLElement}|document.body|所创建dom的父级dom。  
class|string||创建dom的样式类名。   
    
 
####morphTo2D()
转换为2D视图。  
####morphTo3D()
转换为3D视图。