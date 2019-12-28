##new IGis.WMTSImageProvider(options)  
    
提供由Web地图服务（WMS）服务器托管的平铺图像。    
  
  
名称|类型|默认值|介绍  
-|-|-|-   
<a herf="#options">options</a>| object ||具有以下属性的对象。 
  
#####<a name="options">options</a>  
 名称|类型|默认值|介绍  
-|-|-|-    
url|String||WMTS服務的URL或tile-URL模板。tile-URL模板应包含以下变量：{style},{TileMatrixSet},{TileMatrix},{TileRow},{TileCol}。如果实际值是硬编码的，或者服务器不需要，则前两个是可选的。{s}关键字可用于指定子域。   
layers |string ||WMTS请求的图层名称。
format|string|'image/jpeg'|MIME类型，用于从服务器检索图像。    
style|object||WMTS请求的样式名称。  
tileWidth|number|256|每个图块的宽度（以像素为单位）。
tileHeight|number|256|每个图块的高度（以像素为单位）。
minimumLevel|number|0|图像提供者支持的最低详细程度。
maximumLevel|number||图像提供者支持的最高详细程度。  
  
#######代码示例  
      var layerProvider = new IGis.WMTSImageProvider({
            url: "http://t0.tianditu.gov.cn/cia_w/wmts?service=wmts&request=GetTile&version=1.0.0&LAYER=cia&tileMatrixSet=w&TileMatrix={TileMatrix}&TileRow={TileRow}&TileCol={TileCol}&style=default&format=tiles&tk=8b207a527da69c7a32f636801fa194d4",
            layer: "tiandituImgMarker",
            style: "default",
            format: "image/jpeg",
            tileMatrixSetID: "tiandituImgMarker",
            show: true,
            maximumLevel: 16
            });
      viewer.imageryLayers.addImageryProvider(layerProvider);