##new IGis.DrawGraphicalHelper()   
  
绘制图形。  
  
###Methods  
  
####drawGraphical(_drawingMode)  
绘制图形。    
  
 名称|类型|默认值|介绍  
-|-|-|-    
_drawingMode|string|"line"|要绘制图形类型"line","circle","rectangle","polygon","line"。  

  
#######示例代码  
    var drawGraphical=new IGis.DrawGraphical();
    drawGraphical.drawGraphical("circle");


####savePolygon()  
保存当前绘制的图形。    


####drawPolygon(shapeJson)  
根据json，绘制出里面的图形。     
  
  名称|类型|默认值|介绍  
-|-|-|-    
shapeJson|json||要绘制图形的特定格式json。  
#######代码示例  
   
               var shape = {
                "Polygon": [
                    {
                        "name": "武汉凯瑞酒店",
                        "material":{
                            "stripe":{
                                "evenColor":IGis.Color.RED.withAlpha(0.5),
                                "oddColor":IGis.Color.WHITE.withAlpha(0.5)
                            }
                        },
                        "points": [
                            {
                                "longitude": 114.4105341000,
                                "latitude": 30.4279953800
                            },
                            {
                                "longitude": 114.4127764200,
                                "latitude": 30.4256455700
                            },
                            {
                                "longitude":114.4164116100,
                                "latitude": 30.4246513800
                            },
                            {
                                "longitude":114.4168816500,
                                "latitude":30.4280620100
                            },
                            {
                                "longitude":114.4140209700,
                                "latitude":30.4298640900
                            }
                        ]
                    }
              
                ]
            }
            var drawGraphical=new IGis.DrawGraphical();
            drawGraphical.drawPolygon(shape);

####deletePolygon(classify, value)  
   根据json，绘制出里面的图形。   

  
名称|类型|默认值|介绍  
-|-|-|-    
classify|string||要以什么类型为标准删除图形，支持"id","name","type"。如果不填，则默认删除当前加载的所有图形。    
value|string||对应删除类型的值。   
  
#######代码示例   
 
            var drawGraphical=new IGis.DrawGraphical();  
            drawGraphical..deletePolygon("id","265135");    
 
            drawGraphical..deletePolygon("name","武汉凯瑞酒店"); 

            drawGraphical..deletePolygon("type","polygon");       


####editPolygon()  
 编辑图形，双击选中模型，拖动编辑位置以及顶点位置。   

########代码示例
            var drawGraphical=new IGis.DrawGraphical();
            drawGraphical..editPolygon(); 
