# Morph

创建二维和三维的转换。

## Methods

### IGis.Morph.createButton\(classOptions2D,classOptions3D\)

创建一个2D按钮实现转二维视图；创建一个3D按钮实现转三维。

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| [classOptions2D](morph.md) | object |  | 创建2D按钮属性。 |
| [classOptions3D](morph.md) | object |  | 创建3D按钮属性。 |

#### [classOptions2D](morph.md)

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| id | string |  | 所创建dom的Id |
| domType | string | "div" | 所创建dom的类型。 |
| fatherDom | {HTMLElement} | document.body | 所创建dom的父级dom。 |
| class | string |  | 创建dom的样式类名。 |

#### [classOptions3D](morph.md)

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| id | string |  | 所创建dom的Id。 |
| domType | string | "div" | 所创建dom的类型。 |
| fatherDom | {HTMLElement} | document.body | 所创建dom的父级dom。 |
| class | string |  | 创建dom的样式类名。 |

### IGis.Morph.to2D\(\)

转换为2D视图。

### IGis.Morph.to3D\(\)

转换为3D视图。

