##new IGis.Clock(options) 
用于跟踪和模拟时间的简单时钟。 
   
名称|类型|默认值|介绍  
-|-|-|-  
<a herf="#options">options</a>|object||时钟的属性。

###Members  
  
<a name="options>options</a>

名称|类型|默认值|介绍  
-|-|-|-  
startTime|JulianDate||时钟的开始时间。  
endTime|JulianDate||时钟的停止时间。 
currentTime|JulianData||当前时间。  
multiplier|number|1.0|确定调用Clock时要提前多少时间，负值允许向后前进。  
clockRange|ClockRange|ClockRange.UNBOUNDED|确定在开始时间或结束时间到达时时钟应如何表现。  
canAnimate|boolean|true|指示是否可以提前时间。例如，如果正在缓冲数据，则可能为false。当canAnimate和shouldAnimate都为true时，时钟才会走。  
shouldAnimate|boolean|true|指示是否可以提前时间。当canAnimate和shouldAnimate都为true时，时钟才会走。  
  
###### 代码示例
    var options={
            startTime:IGis.JulianDate.fromDate(new Date()),
            stopTime:Cesium.JulianDate.fromDate(new Date(Date.parse(new Date()) + 86400000)),
            currentTime:Cesium.JulianDate.fromDate(new Date()),
            multiplier:1,
            clockRange:Cesium.ClockRange.LOOP_STOP,
            canAnimate:true,
            shouldAnimate:true
    }
    var clock=new IGis.Clock(options);