##new IGis.Billboard(billboardOptions)  
  
生成一个广告牌对象。  
返回值：生成的广告牌对象。  
  
  
名称|类型|默认值|介绍  
-|-|-|-   
<a herf="#billboardOptions">billboardOptions</a>| object ||图片的样式属性。 
  
#####<a name="billboardOptions">billboardOptions</a>  
 名称|类型|默认值|介绍  
-|-|-|-    
show|boolean|true|是否显示广告牌。  
image |string ||指定要用于广告牌的Image,URL或Canvas。
scale |number |2.0 |指定要用于图像大小的比例。
color |Color  |Color.WHITE |指定图像的色调。
width |number ||指定广告牌的宽度（以像素为大小），并覆盖原始大小。
height|number ||指定广告牌的高度（以像素为大小），并覆盖原始大小。
disableDepthTestDistance |number |0 |指定距相机多少米禁用深度测试。    
    
      const billboardOptions={
                show:true,
                image:"./images/bill.png",
                scale: 1.0
            }
      const billboard=new IGis.Billboard();

  