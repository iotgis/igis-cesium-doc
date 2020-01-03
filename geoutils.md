##GeoUtils  
三维常用计算方法。  
  
###Methods  
  
####IGis.GeoUtils.pointInsideCircle (point, circleCenter, r)  
判断点是否在圆内。
返回值：boolean    

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
  
####IGis.GeoUtils.pointToAcr (options,resultOut)    
  
通过两点，得到抛物线上的若干个点(三维点)。
  
####IGis.GeoUtils.distanceP2P(point1,point2)  
计算两点的距离。