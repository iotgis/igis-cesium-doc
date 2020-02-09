##PositionMessage
在指定位置显示经纬度信息的基类。   
  
  
###Methods  
####IGis.PositionMessage.show(options)  
  
名称|类型|默认值|介绍  
-|-|-|-  
<a herf="#options">options</a>|object||容器属性。  
  
#####<a name="options">options</a>  
名称|类型|默认值|介绍  
-|-|-|-    
lon_showId|string||经度的容器ID。
lat_showId|string|| 纬度的容器ID。
alt_showId|string|| 海拔的容器ID。
elevation_showId|string|| 摄像机视角的高度。     
###### 代码示例
  
           var viewer=new IGis.viewer('Container')            
           var divoptions={
                class:"ig-latlon",
                id:"latlon_show",
                fatherDom:viewerContainer
            }
            var fatherDiv = Dom.create(divoptions);
            var lonOptions={
                // class:"ig-bottom-center",
                id:"lon_show",
                domType:"span",
                text:"经度:",
                class:"ig-lon",
                fatherDom:fatherDiv
            }
            var latOptions={
                // class:"ig-bottom-center",
                id:"lat_show",
                domType:"span",
                text:"纬度:",
                class:"ig-lat",
                fatherDom:fatherDiv
            }
            var altOptions={
                // class:"ig-bottom-center",
                id:"alt_show",
                domType:"span",
                text:"摄像机高度:",
                class:"ig-alt",
                fatherDom:fatherDiv
            }
            var elevationOptions={
                // class:"ig-bottom-center",
                id:"elevation_show",
                domType:"span",
                text:"海拔:",
                class:"ig-elevation",
                fatherDom:fatherDiv
            }


            var lon_show=Dom.create(lonOptions)

            var lat_show=Dom.create(latOptions);
            var alt_show=Dom.create(altOptions);
            var elevation_show=Dom.create(elevationOptions);
            var positionOptions={
                lon_showId:lon_show.id,
                lat_showId:lat_show.id,
                alt_showId:alt_show.id,
                elevation_showId:elevation_show.id
            }
           
            PositionMessage.viewer=viewer;
            PositionMessage.show(positionOptions);