##new IGis.ScreenSpaceEventHandler()  
  
鼠标点击事件。  
  
###Methods  
  
####mouseevent(eventType,fn)  
  
名称|类型|默认值|介绍  
-|-|-|-      
eventType|ScreenSpaceEventType||鼠标点击类型。  
fn|||回调函数，返回点击的实体和点击的坐标位置。{pickedPosition,pickedEntity,pickedPoint}  
  
     const handler = new IGis.ScreenSpaceEventHandler();
     handler.mouseevent(IGis.ScreenSpaceEventType.LEFT_CLICK, function (obj) {
                console.log(obj)
     })   
  

######说明  
     返回值中的 obj.pickedPosition 为所点击的地球表面的点坐标，一般来说高度为0；
               obj.pickedEntity 为所点击的实体（模型、图形等），没有点击到则为undefined；
               obj.pickedPoint 为点击到实体时，实体表面被点击的点坐标。