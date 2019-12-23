##Tags  
增加删除标签。  
  
###Methods  
  
####add（options）     
将标记（点，广告牌，标签）添加到场景。    
  
返回值：添加的tag对象。
  
名称|类型|默认值|介绍  
-|-|-|-   
<a herf="#options">options</a>| object| |要添加的tag的属性。     
  
#####<a name="options">options</a>  
  
名称|类型|默认值|介绍  
-|-|-|-   
position|数组[]||要添加标记的经纬高。  
label |object | |要添加的标签标记。  
point |object ||要添加的点标记。  
billboard |object | |要添加的广告牌标记。  
polyline |object ||要添加的线标记。  
id |string ||指定所添加标记的ID。    
  
     const lon = 120.15221524;
     const lat = 30.23124660;
     const po = new IGis.Point();
     const bill = new IGis.Billboard({image: ""});
     IGis.Tags.add({position: [lon, lat,0], point: po,billboard:bill,id:"555"});

####addList(optionList)      
  
将要添加的标记集合添加到场景中。  
  
将标记（点，广告牌，标签）添加到场景。  
  
名称|类型|默认值|介绍  
-|-|-|-   
<a herf="#optionList">optionList</a>| 数组[object]| |要添加的tag的集合。   
  
#####<a name="optionList">optionList</a>    
  
      const po = new IGis.Point();
      const bill = new IGis.Billboard({image: ""});
      const taglist=[{position:[120.15221524,30.23124660,0],point:po,billboard:bill},{position:[121.15221524,42.23124660,0],point:po,billboard:bill}]
      IGis.Tags.addList(taglist);

  
####remove（tag）   
  
移除标签。  
    
 
名称|类型|默认值|介绍  
-|-|-|-   
tag|object||要移除的标签，如果不传值，则移除通过IGis.Tags.add()添加的所有标签。   


    IGis.Tags.remove();
  
