##Dom
  
所有创建dom相关方法的基类。   
     
###Methods   
  
####IGis.Dom.create(options)  
  
根据参数创建规定样式的dom。
返回值：{HTMLElement}，返回所创建的dom。  
  
名称|类型|默认值|介绍
-|-|-|-  
<a herf="#options">options</a>|object||创建dom所需要的属性。  
    
  
#####<a name="options">options</a>
  
  
名称|类型|默认值|介绍
-|-|-|-  
id|string||所创建dom的Id。  
domType|string|"div"|所创建dom的类型。  
fatherDom|{HTMLElement}|document.body|所创建dom的父级dom。  
class|string||创建dom的样式类名。  



  
#### IGis.Dom.createChartBox (dataOption,options)  
创建echarts图表。
返回值：{HTMLElement} 创建的图表。  
  
名称|类型|默认值|介绍
-|-|-|-  
dataOption |object ||指定图表的配置项和数据。  
<a herf="#chartOptions">options</a>|string||图表的样式类名。   
  
#####<a name="chartOptions">options</a>
名称|类型|默认值|介绍
-|-|-|-  
id |string ||配置图表的Id。  
class |string ||配置图表的样式类名。  
fatherDom |{HTMLElement} |document.body |图表的父级dom。  
    
####IGis.Dom.createMapPopup(options)  
创建弹窗。  
返回值：{HTMLElement} 创建的弹窗dom。   
  
名称|类型|默认值|介绍
-|-|-|-  
<a herf="#popupOptions">options</a>|object||创建弹窗所需要的属性。 
  
#####<a name="popupOptions">options</a>
名称|类型|默认值|介绍
-|-|-|-  
fatherDom |{HTMLElement} |document.body |弹窗的父级元素，如果不填，则默认为document.body。  
title |string ||弹窗的标题元素。  
content |string|| 弹窗的内容元素。  
actions |数组[<a herf="#action">action</a>] ||弹窗底部的按钮元素。  
  
######<a name="action">action</a>  
名称|类型|默认值|介绍
-|-|-|-  
title |string ||底部按钮显示的文字。  
id |string ||底部按钮的ID。   
imageUrl |string ||底部按钮使用的图片。    
  
####IGis.Dom.on(actiontype,fn)  
监听函数，监听鼠标操作。
返回值：dom元素的Id。  

名称|类型|默认值|介绍
-|-|-|-    
actiontype|string||鼠标操作类型，有"click"，"mouseover"。  
fn|||回调函数，返回值是所选择dom元素的Id。
   

