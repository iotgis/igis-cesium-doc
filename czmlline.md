# CzmlLine

通过czml模拟行车路径，路径导航。

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| [options](czmlline.md) | object |  | 标签label的样式属性。 |

#### [labelOptions](czmlline.md)

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| multiplier | number | 1.0 | 时间流逝速度。 |
| label | object |  | label信息。 |
| billboard | object |  | billboard信息。 |
| model | object |  | 模型信息。 |
| pathMaterial | object |  | 路径材质。 |
| pathWidth | number |  | 路径宽度。 |
| timeInterval | number |  | 两点间的时间间隔。 |

```text
  let _options={
        points:[],  //[{lon,lat,alt}]
        multiplier:1,
        label:{
            "fillColor": [
                {
                    "interval": "2019-12-01T00:00:00Z/2019-12-06T00:00:00Z",
                    "rgba": [
                        255, 255, 0, 255
                    ]
                }
            ],
            "font": "bold 10pt Segoe UI Semibold",
            "horizontalOrigin": "CENTER",
            "outlineColor": {
                "rgba": [
                    0, 0, 0, 255
                ]
            },
            "pixelOffset": {
                "cartesian2": [
                    0.0,-60.0
                ]
            },
            "scale": 1.0,
            "show": [
                {
                    "interval": "2019-12-01T00:00:00Z/2019-12-06T00:00:00Z",
                    "boolean": true
                }
            ],
            "style": "FILL",
            "text": "Test Vehicle",
            "verticalOrigin": "BOTTOM"
        },
        billboard: {
            "image": vehicle_normal,
            "scale": 1,
            "eyeOffset": {
                "cartesian": [0.0, 0.0, -1]
            },
            "horizontalOrigin": "CENTER",
            "verticalOrigin": "BOTTOM"
        },
        model:{},
        point:{},
        pathMaterial: {
            "solidColor": {
                "color": {
                    "interval": "2019-12-01T00:00:00Z/2019-12-06T00:00:00Z",
                    "rgba": [
                        255, 255, 0, 255
                    ]
                }
            }
        },
        pathWidth:15,
        ClockRange:Cesium.ClockRange.CLAMPED,
        timeInterval: 1,
    }  

new IGis.CzmlLine(_options);
```

## Methods

### updatePosition\(point,type,message\)

通过传入的经纬度更新行车路径。

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| time | number |  | 两点间的时间间隔。 |
| point | 数组\[\] |  | 最新位置的经纬度。 |
| type | string |  | 行车状态（normal，warning，offline）。 |
| message | string |  | 车上方要显示的信息。 |

`_this.czml.updatePosition(time,[120.56465,34.165453,0],type:"normal",message:"正常行驶");`

### cancel\(\)

取消路径规划和导航。

### cancelTracked\(\)

取消视角跟随。

### tracked\(\)

视角跟随。

