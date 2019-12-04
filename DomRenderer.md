##new IGis.DomRenderer();  
为dom绑定三维坐标，并随着渲染实时的转屏幕坐标，实现dom随三维坐标点移动。  
 
  
###Methods  
####openDomRender(dictionary,elementId)  
打开浮框渲染。
    
  
名称|类型|默认值|介绍
-|-|-|-    
dictionary|Array||domId和position的集合，{domId:position}。
elementId|string||想要显示的特定dom的Id，如果不填，则显示dictionary中的所有dom。 

####closeDomRender()   
关闭浮框渲染。