# 增强配置


### 支持命名

| 参数        | 说明   |  类型  |
| --------   | -----:  | :----:  |
| name    | 为canvas命名 |   String     |

``` bash
var styles = {
    name: '云选',
    style: {
        normal: {
            size: 20.6,
            padding: 1,
        },
        colors: [
            "rgba(45,226,142,0.50)"
        ],
        mouseOver: {
            backgroundColor: 'rgba(56,72,195,0.60)'
        },
        selected: {
            backgroundColor: 'rgba(56,72,195,0.60)'
        }
    },
    tooltip: {
        show: true,
        formatter: (params) => {
            let r = params.data.r,
                index = params.data.index,
                str = '',
                bar = 'width:' + Math.floor(r * 100) + '%';

            if (r <= 1.0 && r >= 0.91) {
                str = '非常好'
            }
            if (r <= 0.9 && r >= 0.81) {
                str = '较好';
            }
            if (r <= 0.8 && r >= 0.71) {
                str = '一般';
            }
            if (r <= 0.7 && r >= 0.6) {
                str = '较差';
            }
            return `
            <div class="ml_tooltip">
                <div class="top">
                    <div class="level">
                        <div class="">${str}</div>
                        <div>推荐级别</div>
                    </div>
                    <div class="rank">
                        <div>No.${index}</div>
                        <div>推荐排行</div>
                    </div>
                </div>
                <div class="bar-wrap">
                    <div class="bar" style="${bar}">
                </div>
            </div>
            `;
        },
    },
    legend: {
        show: false
    },
    event: {
        onMouseOver(item, e) {},
        onState(state) {}
    }
}

```

### Tooltip对象

1.增加Tooltip弹出框边缘智能控制，通过class名称控制箭头arrow-left、arrow-right
2.增加Tooltip元素绑定事件


[实践案例](https://smartdata.b0.upaiyun.com/inmap/examples/PointOverlay01.html ':include :type=iframe width=100% height=600px')