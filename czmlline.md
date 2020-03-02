##new IGis.CzmlLine(options,scanOptions)  
通过czml模拟行车路径，路径导航。  
  
名称|类型|默认值|介绍  
-|-|-|-   
<a herf="#options">options</a>| object ||标签label的样式属性。
<a herf="#scanOptions">scanOptions</a>| object ||扫描面样式属性，当enableScan为true时才有用。
  
#####<a name="options">labelOptions</a>    
  
名称|类型|默认值|介绍  
-|-|-|-   
multiplier|number|1.0| 时间流逝速度。    
label|object||label信息。   
billboard|object||billboard信息。   
model|object||模型信息。   
pathMaterial|object||路径材质。   
pathWidth|number||路径宽度。  
timeInterval|number||两点间的时间间隔。  
enableScan|boolean|false|是否为路径添加跟随的扫描面。  

#####<a name="scanOptions">scanOptions</a>    
  
  
名称|类型|默认值|介绍  
-|-|-|-    
radius|number|100|扫描面半径。    
scanColor|Color||扫描面颜色。
duration |number |30 |扫描一圈所用的时间（秒）。   
  
  
      let _options={
            points:[],  //[{lon,lat,alt}]
            multiplier:1,
            label:{
                "fillColor": [                                                     //文字填充色
                    {
                        "interval": "2019-12-01T00:00:00Z/2019-12-06T00:00:00Z",
                        "rgba": [
                            0, 0, 0, 255
                        ]
                    }
                ],
                "font": "10pt Segoe UI Semibold",         //字体字号
                "horizontalOrigin": "CENTER",             //横向位置
                "outlineColor": {
                    "rgba": [
                        0, 0, 0, 255
                    ]
                },
                "pixelOffset": {                         //视觉偏移
                    "cartesian2": [
                        0.0, -60.0
                    ]
                },
                "scale": 1.0,                           //放大级别
                "show": [
                    {
                        "interval": "2019-12-01T00:00:00Z/2019-12-06T00:00:00Z",  //显示时间
                        "boolean": true           //是否显示
                    }
                ], 
                "style": "FILL",                  //填充方式
                "text": "测试测试56224865244",     //文本内容
                "verticalOrigin": "BOTTOM",        //纵向位置
                "backgroundColor":{               //背景颜色
                    "rgba": [
                        255, 255, 255, 255
                    ]
                },
                "showBackground":"true"       //是否显示背景
            },
            billboard: {
                "image": vehicle_normal,
                "scale": 1,
                "eyeOffset": {
                    "cartesian": [0.0, 0.0, -1]
                },
                "horizontalOrigin": "CENTER",
                "verticalOrigin": "BOTTOM"
            },
            model:{},
            point:{},
            pathMaterial: {
                "solidColor": {
                    "color": {
                        "interval": "2019-12-01T00:00:00Z/2019-12-06T00:00:00Z",
                        "rgba": [
                            255, 255, 0, 255
                        ]
                    }
                }
            },
            pathWidth:15,
            ClockRange:Cesium.ClockRange.CLAMPED,
            timeInterval: 1,
        }  
  
    new IGis.CzmlLine(_options);
  
###Methods   
####updatePosition(currentTime,time,point,type,message)   

通过传入的经纬度更新行车路径。

名称|类型|默认值|介绍  
-|-|-|-    
currentTime|||当前位置对应的时间戳。 
time|number||两点间的时间间隔。 
point|数组[]||最新位置的经纬度。  
type |string||行车状态（normal，warning，offline）。   
message|string||车上方要显示的信息。   
   
` _this.czml.updatePosition(20200227,5,[120.56465,34.165453,0],type:"normal",message:"正常行驶"); `   
  
####cancel()  
取消路径规划和导航。  
  
####cancelTracked()  
取消视角跟随。  
  

####tracked()  
视角跟随。   

####on(fn)  
返回czml中图片的实时位置。

名称|类型|默认值|介绍  
-|-|-|-    
fn|function||回调函数。 
#######代码示例  
     var czml = new IGis.CzmlLine(options);
     czml.on(function (position) {
              console.log(position);
     })
####changeType(options)  
更改行车过程中的一些属性值。  

名称|类型|默认值|介绍  
-|-|-|-    
<a herf="#options">options</a>|object||需要修改的属性对象，包含以下属性。 
#####<a name="options">options</a>  
 名称|类型|默认值|介绍  
-|-|-|-    
type |string |"normal" |车辆运行状态，包含"normal","warning","offline"三种。  
message |string ||车上方要显示的信息。  

########代码示例
    czml.changeType({
         type:"warning",
         message:"警报，车辆非正常行驶"
     });

  

####positionCorrect(timePoList)  
修正已经行驶过的路线。  

 
 名称|类型|默认值|介绍  
-|-|-|-    
timePoList |数组 ||含有时间戳的位置数组(按时间值排好序，索引为0的为时间最小值)。  
message |string ||车上方要显示的信息。  

########代码示例
      var point2 = [120.1532214, 30.24081891];
      var point1 = [120.15945621, 30.21905741];
      var array = new Array();
      var a1 = {
        currentTime: 3,
        position: IGis.Cartesian3.fromDegrees(120.1532214, 30.24081891, 0)
      };
      var a2 = {
        currentTime: 6,
        position: IGis.Cartesian3.fromDegrees(120.15945621, 30.21905741, 0)
      };
      array.push(a1);
      array.push(a2)
      czml.positionCorrect(array);

