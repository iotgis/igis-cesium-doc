##new IGis.Rectangle(west,south,east,north)  
指定为经度和纬度坐标的二维区域。  
  
  
名称|类型|默认值|介绍  
-|-|-|-   
west |number |0.0 |以弧度为单位的最西经度，范围为[-Pi,Pi]。  
south |number |0.0 |以弧度为单位的最南端的纬度，范围为[-Pi/2,Pi/2]。  
east |number |0.0 |以弧度为单位的最东经度，范围为[-Pi,Pi]。  
north |number |0.0 |以弧度为单位的最北端经度，范围为[-Pi/2,Pi/2]。  

###### 代码示例
  
    var rectangle = new IGis.Rectangle(-2,0.35,-1.4,0.532);