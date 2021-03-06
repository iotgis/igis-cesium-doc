##new IGis.Loader()  
加载器。  
  
###Methods  


####gltfLoader(url,positon,options)  
gltf加载器。  
返回值:加载的entity    
  
名称　| 类型 |默认值|介绍  
-------  |------|-   |------- 
url |string ||模型的地址。  
position |IGis.Cartographic ||模型位置，经纬度。  
<a herf="#gltfoptions">options</a> |object  ||设置模型的属性。详细见下表。    
  
#####<a name="gltfoptions">options</a>
  
名称　| 类型 |默认值|介绍  
-------  |------|-   |-------
heading |number |0.0 |航向分量，模型的朝向角度,弧度值。  
pitch  |number |0.0 |螺距分量，模型的俯仰角度，弧度值。  
roll |number |0.0 |滚动分量，模型的旋转角度，弧度值。  
color |IGis.Color |Color.White |模型的颜色。  
scale |number |1.0 |模型放大倍数。  
show |boolean |true |是否显示模型。  
enableZoomto |boolean |false |是否将模型在视野中放大居中。  
id|string||模型Id。
######代码示例

    var loader = new IGis.Loader();
    var position=new IGis.Cartographic(116.25642,40.26245,0);
    var options={
         heading:0,
         pitch:0,
         roll:0,
         scale:1,
         id:"123"
    }
    loader.gltfLoader("./model/a.gltf",position,)
 
   
###tilesLoader3D(url,enableZoomto)   
3Dtiles模型加载。  
返回值：加载的3Dtiles模型。  
  
名称　| 类型 |默认值|介绍  
-------  |------|-   |------- 
url |string ||模型的地址。
enableZoomto|boolean|false|是否将模型在视野中放大居中。  
######代码示例   
      
    var loader = new IGis.Loader();
    var url = "http://192.168.10.121:8010/hangzhoushifan/tileset.json";
    loader.tilesLoader3D(url);
###geojsonLoader(url,options,fn)  

geojson加载器。  
返回值：回调函数，转换为EntityCollection的通用数据dataSource。   
  
名称　| 类型 |默认值|介绍  
-------  |------|-   |-------   
url|string  ||geojson的地址。  
<a herf="#geojsonoptions">options</a>|object||geojson的属性值。    
  

  
#####<a name="geojsonoptions">options</a>
名称　| 类型 |默认值|介绍  
-------  |------|-   |-------  
height |number |0 |生成区块的高度。  
fill |boolean |true |是否用颜色将区块填充。    
color |数组[{name,color}]| |对应每个区块的名称和颜色。  
outline |boolean |true |是否绘制轮廓线。  
outlineColor |IGis.Color|Color.WHITE |轮廓线的颜色。  
outlineWidth |number |1.0 |轮廓线宽度。   
  
  
######代码样例：    
    var url = "./Geojson/110100.json";
    var loader = new IGis.Loader();
    var options = {
          height: 0,
          fill: false
     }
    loader.geojsonLoader(url, options, function (dataSource) {
        loader.geoJsonLabels(dataSource);    //添加四色图对应label
    })
###geoJsonLabels(dataSource,options)  
给geojson绘制label标签。  
  
名称　| 类型 |默认值|介绍  
-------  |------|-   |-------   
dataSource|object  ||数据源，转换为EntityCollection的通用数据（geojsonLoader的返回值可使用）。    
<a herf="#labeloptions">options</a>|object||label的属性值。  
  
#####<a name="labeloptions">options</a>
名称　| 类型 |默认值|介绍  
-------  |------|-   |-------  
font |string |"24px sans-serif" |字体大小样式。  
name |string |"GEOLABLE" |label的名称。  
scale |number |1.0 |label的放大倍数。  
showBackground |boolean |false |是否显示背景。  
backgroundColor |Color||label背景色。  
fillColor |Color |Color.WHITE |label填充色。  
outlineWidth |number |1.0 |边框宽度。  
outlineColor |Color |Color.BLACK |边框颜色。  
disableDepthTestDistance |number |Number.POSITIVE_INFINITY |在什么高度关闭深度测试 设置为Number.POSITIVE_INFINITY 则关闭深度测试,设置为0则开启深度测试。    
######代码示例
    var url = "./Geojson/110100.json";
    var loader = new IGis.Loader();
    var options = {
          height: 0,
          fill: false
     }
    loader.geojsonLoader(url, options, function (dataSource) {
        loader.geoJsonLabels(dataSource);    //添加四色图对应label
    })
  
###removeGltf(entity)  
移除通过Loader加载的gltf模型。  
  
名称　| 类型 |默认值|介绍  
-------  |------|-   |-------    
entity|object||要移除的gltf模型，如果不填，则移除场景中所有的gltf模型。    
  
#######代码示例
    loader.removeGltf();

###remove3dtiles(tileset)  
移除通过Loader加载3dtiles模型。  

名称　| 类型 |默认值|介绍  
-------  |------|-   |-------  
tileset |object ||要移除的3dtiles模型，如果不填，则移除所有的3dtiles模型。
  #######代码示例  

    loader.remove3dtiles();

###removeGeojson(dataSource)  
移除通过Loader加载的geojson。  

名称　| 类型 |默认值|介绍  
-------  |------|-   |-------  
 dataSource |object||dataSource 数据源，转换为EntityCollection的通用数据（geojsonLoader的返回值），如果不填，则移除所有的geojson。  
  
#######代码示例  
    loader.removeGeojson();

###removeGeoJsonLabels(label)  
移除通过geoJsonLabels加载的label。  

名称　| 类型 |默认值|介绍  
-------  |------|-   |-------  
 label |object||移除label，如果不填，则移除所有的label。 
  
#######代码示例
    loader.removeGeoJsonLabels();