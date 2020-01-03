##new IGis.Compass(viewer,options)  
创建罗盘。
  
名称|类型|默认值|介绍  
-|-|-|-
viewer|Viewer||The viewer  
<a herf="#options">options|object||罗盘属性  
  
###Members  
  
####<a name="options">options</a>  
  
名称|类型|默认值|描述  
-|-|-|-
defaultResetView|数组[]或者object||用于在使用重置导航重置地图视图时设置默认视图控制。接受的值是经纬度{lon,lat,alt}或者矩形范围{west,south,east,north}。
enableCompass|boolean|true|用于启用或禁用罗盘。true是启用罗盘，false是禁用罗盘。默认值为true。如果将选项设置为false，则罗盘将不会添加到地图中。
enableZoomControls|boolean|true|用于启用或禁用缩放控件。true是启用，false是禁用。默认值为true。如果将选项设置为false，则缩放控件将不会添加到地图中。
enableDistanceLegend|boolean|true|用于启用或禁用距离图例。true是启用，false是禁用。默认值为true。如果将选项设置为false，距离图例将不会添加到地图中。
enableCompassOuterRing|boolean|true|用于启用或禁用指南针外环。true是启用，false是禁用。默认值为true。如果将选项设置为false，则该环将可见但无效。
class|string||罗盘样式。