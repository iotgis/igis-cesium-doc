##new IGis.VideoPlane(videoId,positions,options)  
创建一个用于平面，用于展示dom元素。（展示视频）  
  
  
  
名称|类型|默认值|介绍  
-|-|-|-   
videoId |string |0.0 |要展示的dom的ID。  
positions |[] |0.0 |经纬高。  
options | ||平面属性。    
  
 
#####options  
名称|类型|默认值|介绍  
-|-|-|-   
width |number |40 |plane的宽度。  
height |number |30 |plane的高度。  
normal |Cartesian3|Cartesian3.UNIT_X|平面的单位法向量（必须是单位法向量）。    
    
  
###### 代码示例   
    var videoId="videoContainer";
    var positions=[116.253,40.23554,0];
    var options={
       width:500,
       height:500,
       normal:IGis.Cartesian3.UNIT_Y
    }
    var videoPlane=new IGis.VideoPlane(videoId,positions,options);
