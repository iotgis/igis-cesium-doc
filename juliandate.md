##IGis.JulianDate(julianDayNumber, secondsOfDay, timeStandard)
 代表天文朱利安日期，它是自4712年1月1日（公元前4713年）正午以來的天数。为了提高精度，此类將日期的整数部分和日期的秒数部分存储在单独的组件中。为了安全进行算数运算并表示seconds秒，日期始终存储在国际原子时间标准中 TimeStandard.TAI。  

名称|类型|默认值|介绍  
-|-|-|-  
julianDayNumber|number |0.0 |儒略日数，代表整天数，小数日也将得到正确的处理。  
secondsOfDay |number |0.0 |当前朱利安天数的秒数，小数秒，负秒和大于一天的秒数将被正确处理。  
timeStandard|TimeStandard|TimeStandard.UTC|定义前两个参数的时间标准。  

### Methods  
####IGis.JulianDate.fromDate(date, result)
根据JavaScript时间创建一个JulianDate时间。
返回值：JulianDate格式的时间。  
  
名称|类型|默认值|介绍  
-|-|-|-  
date|Date | |一个JavaScript时间。  

###### 代码示例  
    var data = IGis.JulianDate.fromDate(new Date());  

  
