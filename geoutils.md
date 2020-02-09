##GeoUtils  
三维常用计算方法。  
  
###Methods  
  
####IGis.GeoUtils.pointInsideCircle (point, circleCenter, radius)  
判断点是否在圆内。
返回值：boolean      
  
名称|类型|默认值|介绍  
-|-|-|-   
point|对象或数组| |要判断的点的坐标。  
circleCenter| 对象或数组 ||圆心坐标。  
radius|number||圆的半径。  
######代码示例
     var point = [116.3824,39.8715];
     var inside = IGis.GeoUtils.pointInsideCircle([116.3866,39.56255,0],10);

####IGis.GeoUtils.pointInsidePolygon (point,polygonPoints)  
判断点是否在多边形内。
返回值：boolean     
  
名称|类型|默认值|介绍  
-|-|-|-   
point|对象或数组| |要判断的点的坐标。  
polygonPoints| 数组 | |多边形顶点点集。  
######代码示例  
            var lon0 = 116.38242456;
            var lat0 = 39.8715015;
            var lon1 = 116.42509602;
            var lat1 = 39.87237685;
            var lon2 = 116.38661129;
            var lat2 = 39.87709964;
            var lon3 = 116.39538159;
            var lat3 = 39.87000669;
            var lon4 = 116.37669079;
            var lat4 = 39.88379004;
            var points = [[lon1, lat1, 0], [lon0, lat0, 0], [lon3, lat3, 0], [lon2, lat2, 0]];
            var inside = IGis.GeoUtils.pointInsidePolygon([lon4,lat4,0],points);

  
####IGis.GeoUtils.pointToLine (point1, point2, count)      
 通过两点，得到直线上的若干个点(三维点)。   
 返回值：获取到的点的数组。   
  
名称|类型|默认值|介绍  
-|-|-|-   
point1|对象或数组||第一个点的坐标。  
point2| 对象或数组 | |第二个点的坐标。  
count|number||要分成的点的个数。
#######代码示例
     var positionlist = IGis.GeoUtils.pointToLine(point1, point2, 10);
  
####IGis.GeoUtils.pointToAcr (options,resultOut)    
  
通过两点，得到抛物线上的若干个点(三维点)。   
返回值：获取到的点的数组。  
  
名称|类型|默认值|介绍  
-|-|-|-  
<a herf="#options">options</a>|object||抛物线的属性。    
    
  
  
#####<a name="options">options</a>  
名称|类型|默认值|介绍  
-|-|-|-  
pt1|object或者[]||第一个点的经纬度。  
pt2|object或者[]||第二个点的经纬度。  
height|number||顶点高度。  
num|number||要分成的点的个数。

#######代码示例
     var pt1=[116.2564,40.56215,0];
     var pt2=[112.25451,39.45321,0];
     var height=500;
     var num=100;
     var options={
            pt1:pt1,
            pt2:pt2,
            height:height,
            num:num
         }
     var positionlist = IGis.GeoUtils.pointToAcr(options);
  
  
####IGis.GeoUtils.distanceP2P(point1,point2)  
计算两点的距离。   
返回值：距离（米）。
  
名称|类型|默认值|介绍  
-|-|-|-   
point1|Cartesian3||第一个点的笛卡尔坐标。  
point2| Cartesian3 ||第二个点的笛卡尔坐标。    
  
    var car0=new IGis.Cartesian3(x1,y1,z1);
    var car1=new IGis.Cartesian3(x2,y2,z2);
    var distance=IGis.GeoUtils.distanceP2P(car0,car1);
  
