##new IGis.Ellipsoid(x,y,z)  
   由方程在笛卡爾坐標系中定義的二次曲面 (x / a)^2 + (y / b)^2 + (z / c)^2 = 1。銫主要用於表示行星體的形狀。通常使用提供的常量之一來代替直接構造此對象。  
  
名称|类型|默认值|介绍  
-|-|-|-   
x|number|0.0|X方向上的半径。  
y|number|0.0|Y方向上的半径。  
z|number|0.0|Z方向上的半径。  
  
###### 代码示例  
    var ellipsoid=new IGis.Ellipsoid(x,y,z);
    