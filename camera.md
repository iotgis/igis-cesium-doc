# Camera

由位置、方向和视锥体定义的相机。

## Methods

### IGis.Camera.flyTo\(options\)

飞行至指定地点。

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| [options](camera.md) | object |  | 相机飞行至指定地点的属性。 |

#### [options](camera.md)

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| position | object或者\[\] | {lon:116.391134,lat:39.901334,alt:800} | 摄像机目的地经纬高位置。{lon,lat,alt} 或者\[position\[0\],position\[1\],position\[2\]\]。 |
| orientation | object或者\[\] | {heading:0,pitch:Math.PI/4,roll:0,} | 摄像机的偏转角度。heading:弧度的航向分量，pitch:弧度的螺距分量，roll:滚动分量\(以弧度为单位\)。 |

### IGis.Camera.setView\(options\)

将相机视野放置到指定位置。

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| [options](camera.md) | object |  | 相机飞行至指定地点的属性。 |

#### [options](camera.md)

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| position | object或者\[\] | {lon:116.391134,lat:39.901334,alt:800} | 摄像机目的地经纬高位置。{lon,lat,alt} 或者\[position\[0\],position\[1\],position\[2\]\]。 |
| orientation | object或者\[\] | {heading:0,pitch:Math.PI/4,roll:0,} | 摄像机的偏转角度。heading:弧度的航向分量，pitch:弧度的螺距分量，roll:滚动分量\(以弧度为单位\)。 |

