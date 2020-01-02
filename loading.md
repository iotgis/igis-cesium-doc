# Loading

## Loading

设置IGis遮罩层和loading图标。

## Methods

### IGis.Loading.create\(layerClass,loadingClass\)

创建遮罩层和loading图标。

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| [layerOptions](loading.md) | object |  | 遮罩层属性。 |
| [loadingOptions](loading.md) | object |  | loading属性。 |

#### [layerOptions](loading.md)

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| class | string |  | 遮罩层的样式类名 |

#### [loadingOptions](loading.md)

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| class | string |  | loading图标样式类名。 |
| IconUrl | string |  | loading图标的地址。 |
| text | string |  | loading图标下显示的文字。 |
| textclass | string |  | 文字样式类名。 |

### IGis.Loading.dispose\(\)

销毁遮罩层和loading图标。

