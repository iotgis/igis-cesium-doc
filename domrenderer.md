##DomRenderer;  
为dom绑定三维坐标，并随着渲染实时的转屏幕坐标，实现dom随三维坐标点移动。  
 
###Members  
####dictionary  
需要渲染位置的dom字典表。
###### 代码示例  
    var options={
       id:"domId",
       position:new IGis.Cartesian3(x,y,z),
       offset:[126,239]
    }
    IGis.DomRenderer.dictionary=options;
  
###Methods  
####IGis.DomRender.open()  
打开浮框渲染。
 
###### 代码示例  
    IGis.DomRenderer.open();
####IGis.DomRender.close()   
关闭浮框渲染。   
   
###### 代码示例  
    IGis.DomRenderer.close();
####IGis.DomRender.update(domID,show)  
更新dom是否显示。    
  
名称|类型|默认值|介绍
-|-|-|-  
domID |string ||要更新状态的dom元素ID。  
show |boolean ||是否显示。      
  
###### 代码示例  
    IGis.DomRenderer.update("domId",false);
  
####IGis.DomRender.remove(popupId)   
从渲染的dom中删除指定ID的元素。    
    
  
###### 代码示例  
    IGis.DomRenderer.remove("domId");