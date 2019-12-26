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



  
#### IGis.Dom.createChartBox (dataOption,options,position)  
创建echarts图表。
返回值：{HTMLElement} 创建的图表。  
  
名称|类型|默认值|介绍
-|-|-|-  
dataOption |object ||指定图表的配置项和数据。  
<a herf="#chartOptions">options</a>|string||图表的样式类名。   
position|数组||图表关联的三维位置坐标，经纬度。
  
#####<a name="chartOptions">options</a>
名称|类型|默认值|介绍
-|-|-|-  
id |string ||配置图表的Id。  
class |string ||配置图表的样式类名。  
show |boolean |true|是否显示图标。  
fatherDom |{HTMLElement} |document.body |图表的父级dom。  
    
####IGis.Dom.createMapPopup(options)  
创建弹窗。  
返回值：{HTMLElement} 创建的弹窗dom。   
  
名称|类型|默认值|介绍
-|-|-|-  
<a herf="#popupOptions">options</a>|object||创建弹窗所需要的属性。   
position|数组[]||弹窗所关联的三维经纬度。 
  
#####<a name="popupOptions">options</a>
名称|类型|默认值|介绍
-|-|-|-    
show|boolean|true|弹窗是否显示。     
id |string或number ||弹窗ID，用于与三维坐标关联。
title |string ||弹窗的标题元素。 
fatherDom |{HTMLElement} |document.body |弹窗的父级元素，如果不填，则默认为三维球容器。  
title |string ||弹窗的标题元素。  
content |string|| 弹窗的内容元素。  
actions |数组[<a herf="#action">action</a>] ||弹窗底部的按钮元素。  
  
######<a name="action">action</a>  
名称|类型|默认值|介绍
-|-|-|-  
title |string ||底部按钮显示的文字。  
id |string ||底部按钮的ID。   
imageUrl |string ||底部按钮使用的图片。     
  
######代码示例  
          IGis.DomRenderer.open();
           const options = {
              id: "popup",
              title: "这是一个弹窗",
              content: "这是弹窗的主要内容",
              show:true,
              actions: [
                  {
                      title: "方法",
                      imageUrl: "",
                      type: "555"
                  },
                  {
                      title: "方法2",
                      imageUrl: "",
                      type: "666"
                  }
                ]
            }

            const lon = 120.15221524;
            const lat = 30.23124660;
            const popup = IGis.Dom.createMapPopup(options, [lon, lat, 0]);
            IGis.DomRenderer.update(popup.id,false); //更新状态为不显示   
  
#######说明  
    弹窗类名："ig-popup"
    弹窗尾部小箭头类名："ig-popup-inner"
    弹窗头部类名："ig-popup-header"
    弹窗头部标题类名："ig-popup-header-title"
    弹窗头部关闭按钮类名："ig-popup-header-close"
    弹窗中间内容部分类名："ig-popup-body"
    弹窗尾部类名："ig-popup-footer"
    弹窗尾部方法类名："ig-popup-footer-div"
  
####IGis.Dom.on(actiontype,fn)  
监听函数，监听鼠标操作。
返回值：dom元素的Id。  

名称|类型|默认值|介绍
-|-|-|-    
actiontype|string||鼠标操作类型，有"click"，"mouseover"。  
fn|||回调函数，返回值是所选择dom元素的Id。    
  
        IGis.Dom.on("click",function (event) {
                console.log(event);
        })
     
  
####IGis.Dom.removeDom(domID)  
 
移除创建的dom元素。

名称|类型|默认值|介绍
-|-|-|-  
domID |string或者number ||要删除dom的ID。 