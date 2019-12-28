##new IGis.WMSImageProvider(options)  
    
提供由Web地图服务（WMS）服务器托管的平铺图像。    
  
  
名称|类型|默认值|介绍  
-|-|-|-   
<a herf="#options">options</a>| object ||具有以下属性的对象。 
  
#####<a name="options">options</a>  
 名称|类型|默认值|介绍  
-|-|-|-    
url|String||WMS服務的URL。該網址支持與相同的關鍵字。  
layers |string ||服务包含的图像，以逗号（,）分割。
parameters|object|| 附加参数，用于通过GetMap URL传输到WMS服务器。  
tileWidth|number|256|每个图块的宽度（以像素为单位）。
tileHeight|number|256|每个图块的高度（以像素为单位）。
minimumLevel|number|0|图像提供者支持的最低详细程度。
maximumLevel|number||图像提供者支持的最高详细程度。  
  
#######代码示例  
    var wms = new IGis.WMSImageProvider({
                url: "http://124.239.10.7:8088/geoserver/ows?service=WMS",
                layers: "igis:hd5",
                parameters: {
                    transparent: true,
                    format: "image/png",
                    srs: "EPSG:4326",
                    styles: ""
                }
            });
      viewer.imageryLayers.addImageryProvider(wms);