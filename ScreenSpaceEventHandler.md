##new IGis.ScreenSpaceEventHandler()  
  
鼠标点击事件。  
  
###Methods  
  
####moustevent(eventType,entity,fn)  
  
名称|类型|默认值|介绍  
-|-|-|-      
eventType|ScreenSpaceEventType||鼠标点击类型。  
fn|||回调函数，返回点击的实体。  
  
     const handler = new IGis.ScreenSpaceEventHandler();
     handler.moustevent(IGis.ScreenSpaceEventType.LEFT_CLICK, function (entity) {
                console.log(entity)
     })