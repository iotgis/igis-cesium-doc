##new IGis.CzmlLine(points,options)  
通过czml模拟行车路径，路径导航。  
  
名称|类型|默认值|介绍  
-|-|-|-  
points|数组[[lon,lat]]||规划路径的点集经纬度。     
  
###Methods   
####updatePosition(point,type,message)   

通过传入的经纬度更新行车路径。

名称|类型|默认值|介绍  
-|-|-|-  
point|数组[]||最新位置的经纬度。  
type |string||行车状态（normal，warning，offline）。   
message|string||车上方要显示的信息。   
      
  
####cancel()  
取消路径规划和导航。  
  
