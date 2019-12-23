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
layurl|string|'http://www.google.cn/maps/vt?lyrs=s@800&x={x}&y={y}&z={z}'|底图地址,默认为谷歌地图。
layerurl|string||地形数据地址。
enableSkyBox|boolean|true|是否创建天空盒。
skyBoxSources|object|{positiveX,negativeX,positiveY,negativeY,positiveZ,negativeZ}|天空盒资源。


               

