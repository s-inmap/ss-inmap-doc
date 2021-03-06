# PolygenOverlay图层

### 概述

多边形的图层。

[实践案例](https://competent-morse-8518a5.netlify.com/examples/PolygonOverlay2.html ':include :type=iframe width=100% height=600px')


### 构造函数

| 类名        | 描述   |
| --------   | -----:  |
| SSPolygenOverlay(opts: PolygenOverlay)     | 创建一个多边形图层对象。注意：图层对象实例被remove后，不可重复使用，需要重新new创建方可使用。 |



### styleOption

| 状态        | 类型   |  说明  |
| --------   | -----:  | :----:  |
| normal    | Object |   默认状态的样式配置    |
| mouseOver    | Object |   鼠标悬浮状态的样式配置    |
| selected    | Object |   鼠标选中状态的样式配置    |

### 样式描述

| 状态        | 类型   |  说明  |
| --------   | -----:  | :----:  |
| borderStyle  | String,Array |   支持字符串类型'dotted'，'dashed',支持数组类型比如：[1,4],第一个参数用于规定第一个虚线的长度。第二个参数用于规定第一个虚线与第二个虚线之间的间隔。    |


### eventOption

| 参数        | 说明   |  类型  |  默认值  |
| --------   | -----:  | :----:  | :----:  |
| onMouseOver(item, event,this)    | 多边形鼠标悬浮事件。<br> item:当前悬浮的数据对象。<br>event: 事件对象 |    Function   |     -     |
| onMouseEnter(item, event,this)   | 鼠标进入被选元素时。 <br> item:当前鼠标数据对象。 <br>event: 事件对象<br> this: 当前对象 |   Function    |     -     |
| onMouseLeave(item, event,this)    | 鼠标离开被选元素时。 <br> item:当前鼠标数据对象。 <br>event: 事件对象<br> this: 当前对象 |   Function    |     -     |