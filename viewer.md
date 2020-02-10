#new IGis.Viewer(IGisConcainer,options) 
初始化地球并配置组件。  

名称　| 类型 |默认值|介绍  
-------  |------|-   |-------  
IGisConcationer|string||地球容器。  
<a href="#options">options</a>|object||组件属性。

###<a name="options">options</a> 

名称|类型|默认值|介绍
-|-|-|-
compass|boolean|true|是否开启罗盘,默认为ture。  
home|boolean|true|是否创建home按钮,默认为true。
morphviewer|boolean|true|是否创建2D/3D转换按钮,默认为true。
changelayer|boolean|true|是否创建切换图层按钮,默认为true。
copyright|boolean|true|是否显示版权信息,默认为true。
fps|boolean|true|是否显示每秒传输帧数,默认为true。
sceneMode|string|3D|场景模式，如果填"2D",则默认加载2D场景模式，如果填"3D",则默认加载3D场景模式。  
fullscreenButton|boolean|false|是否显示全屏按钮，如果设为true，这有默认的全屏按钮。  
enableSkyBox|boolean|true|是否创建天空盒。   
skyBoxSources|object|{positiveX,negativeX,positiveY,negativeY,positiveZ,negativeZ}|天空盒资源。  
wmtsImageryProvider|||由WMTS服务器托管的平铺图像。   
wmtsImageryProvider|||由WMTS服务器托管的平铺图像,当同时有wmtsImageryProvider和wmsImageryProvider时，优先使用wmtsImageryProvider。  
layerurl|string|'http://www.google.cn/maps/vt?lyrs=s@800&x={x}&y={y}&z={z}'|底图地址,默认为谷歌地图，当同时有wmtsImageryProvider和wmsImageryProvider时，优先使用其他两个。
terrainUrl|string||地形数据地址。
######代码示例  
     this.viewer = new IGis.Viewer("demo", {
                compass: false,
                home: true,
                morphview: true,
                changelayer: true,
                positionMessage: true,
                copyright: false，
                sceneMode:"2D",
                layerurl: "http://webrd02.is.autonavi.com/appmaptile?lang=zh_cn&size=1&scale=1&style=8&x={x}&y={y}&z={z}"
          });   
   
  
######示例2

          var wmts = new IGis.WMTSImageProvider({
                url:'http://124.16.10.7:8088/geoserver/gwc/service/wmts/rest/igis:tdtm3/{style}/{TileMatrixSet}/{TileMatrixSet}:{TileMatrix}/{TileRow}/{TileCol}?format=image/png',
                layer: "igis:tdtm3",
                style: "",
                format: "image/png",
                tileMatrixSetID: "EPSG:900913"
            });
          
            this.viewer = new IGis.Viewer("demo", {
                compass: false,
                home: true,
                morphview: true,
                changelayer: true,
                positionMessage: true,
                copyright: false,
                wmtsImageryProvider:wmts
            });
               

