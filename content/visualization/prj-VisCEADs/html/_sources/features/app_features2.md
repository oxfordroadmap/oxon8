---
jupytext:
  formats: ipynb,md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.16.2
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

```{raw-cell}
---
editable: true
raw_mimetype: ''
slideshow:
  slide_type: skip
tags: [remove-cell]
---
!pip install ipypublish
```

```{raw-cell}
---
editable: true
raw_mimetype: ''
slideshow:
  slide_type: skip
tags: [remove-cell]
---
!pip install jupyterlab_myst
```

```{code-cell} ipython3
---
editable: true
raw_mimetype: ''
slideshow:
  slide_type: skip
tags: [remove-cell]
---
## import local modules from sibling folders
import sys
# append the path of the parent directory
sys.path.append("..")

from pyVisCEADs import pyVisCEADs as VC
import panel as pn
pn.extension(design='fast')     
pn.extension('tabulator')
pn.extension('echarts')  # ECharts

locale = VC.locale
UI_label = VC.UI_label

from myst_nb import glue
```

```{code-cell} ipython3
VC.myExplorer.get_df ( r='江苏', y='2017', NorE = "E")
```

```{code-cell} ipython3
VC.myExplorer.get_df ( r='江苏', y='2017')
```

```{code-cell} ipython3
pn.Row(VC.gen_Sankey_TopN_Nodes ('江苏', '2017', TopN=15))
```

+++ {"editable": true, "slideshow": {"slide_type": ""}}

# CEADs 可视化基本信息：visCEADs 说明

**[VisCEADs 中国各省各行业脱碳路线：投入产出网络仪表盘](https://oxon8.netlify.app/visualization/prj-visCEADs/index.zh)**，基于 [中国碳核算数据库](https://www.ceads.net.cn/)(Carbon Emission Accounts & Datasets，CEADs)  数据，提供可视化仪表盘。

## VisCEADs 技术特性
VisCEADs 有以下技术特性：

* VisCEADs 只需使用现代浏览器即可使用，无需下载任何软件。
* VisCEADs 第一次启用需读入所需代码及数据，通常需30-50秒，读完后即可使用不延时。
* VisCEADs 交互功能说明在右侧有提示相关用法，用户亦可自行调整全屏或布局。
* VisCEADs 基于开源代码套件再开发，具高度客制化特性。


此文件依序介绍仪表盘各组件。

## VisCEADs 信息特性
``投入产出网络``指由``投入产出表``构成的网络图，表达一经济体的各部门之间的**经济联系和影响**，此经济数据分析方法可用于产业政策与治理、环境政策与治理等。

### 參考
* 中国统计局，2023/01/01，[投入产出表的分析要点有哪些，《领导干部统计知识问答》](https://www.stats.gov.cn/zs/tjws/tjfx/202301/t20230101_1903477.html)
* [中国统计局 投入产出表](https://data.stats.gov.cn/ifnormal.htm?u=/files/html/quickSearch/trcc/trcc01.html&h=740)


### 投入产出网络特性

```{note}
投入产出网络特性（若没額外说明）在此文件指：
* 网络 ``节点``：指特定 ``行业`` ，该节点 `大小` 及/或 `颜色` 可以用来可视化 **指标** 或 **分类**。
* 网络间的 ``边缘`` ：指特定两节点 ``行业`` 间的投入-产出关系，具有 **方向性**，该边缘 `宽度` 可以用来可视化**投入产出值**。
```

+++

## VisCEADs 仪表盘布局

仪表盘布局如下：

* 主图：提供交互网络及信息
* 侧边栏：提供交互控件
* 副图表（分页）：提供更多图表信息

![figures/VisCEADs_layout.png](../figures/VisCEADs_layout.png)

+++

# 主图：投入产出网络仪表盘

位于首页正上方位置，主图展示投入产出网络，列出该 ``省`` 及该 ``年`` 的投入产出网络关系。可点选 `拖拽` 图元素排版。可 `鼠标悬浮(hover)` 网络 ``节点`` 及 ``边缘`` ，见实际数据信息。

```{code-cell} ipython3
:tags: [remove-input]

VC.pn_Echart_Graph
```

+++ {"editable": true, "slideshow": {"slide_type": ""}}

## 主图鼠标悬浮(hover)效果

实际数据信息，目前版本包括行业部门的 ``CO2排放`` 、 ``碳排强度`` 、 ``总产出`` 、 ``增加值`` 、 ``进口`` 、 ``出口`` 、 ``最终使用`` 、 ``产出合`` 、及 ``投入合`` 。若有额外客制化需求，请洽[澳恪森](mailto:h.liao@ieee.org?subject=客制化VisCEADs)。

![figures/VisCEADs_layout.png](../figures/VisCEADs_layout_hover_info.png)

+++ {"editable": true, "slideshow": {"slide_type": ""}}

## 主图搭配侧边栏交互效果

于首页，主图左侧有以下控制套件，选取后，投入产出网络主图会**随选响应变化**。

（主图全屏时相关控件位于右侧。）

### 控制套件：选择年份、地区

* ``年份`` 可选 ``2012`` 、 ``2015`` 、 ``2017`` 、及 ``2017新`` 。其中 ``2017新`` 开始采用较为不同的行业分类。
* ``地区`` 可选CEADs数据集中有提供之各省市。

```{code-cell} ipython3
:tags: [remove-input]

pn.Column(  UI_label[locale]["### Explore a year and place"],
            VC.widget_year_slider, VC.widget_reg_select, #widget_reg_autocomplete, 
            pn.layout.Divider())
```

+++ {"editable": true, "slideshow": {"slide_type": ""}}

### 控制套件：主要指标

主要指标可选：
* ``CO2排放``
* ``总产出``
* ``碳排强度``

主要指标选取基于[《2024—2025年节能降碳行动方案》国家政策](https://www.gov.cn/zhengce/202405/content_6954583.htm)中的具体单位 ``国内生产总值能源消耗`` 和 ``二氧化碳排放`` 指标，以提供坚实的科学基础。

```{note}
选取主要指标后，投入产出网络的**节点大小会随选响应变化**。适合用来比较各 ``节点（行业）`` 的排放和产出如何**发展与污染**有效脱钩（包括关键指标 ``碳排强度`` ），打断经济发展与环境污染水平之间的关系。
```

```{code-cell} ipython3
:tags: [remove-input]

pn.Column(  UI_label[locale]["### Focus a main indicator"],
            VC.widget_indicator_main_sel,
            pn.layout.Divider())
```

### 控制套件：调整网络参数

调整可视化参数，此可视化使用百度-Apache Echarts的可视化套件，可以调整下列两者参数：
1. ``引力``：网路各节点往中心吸
2. ``斥力``：网路各节点弱或无关系的互斥
引力-斥力 模型为重力模型，假定两节点间的关系愈强，则吸引力愈强，若弱关系甚至无关系，或有互相排斥力。

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
tags: [remove-input]
---
pn.Column(  UI_label[locale]["### Adjust the network"],
            pn.pane.Str(UI_label[locale]["Visualization parameters"]),
            VC.wg_slider_gravity, VC.wg_slider_repulsion)
```

## 副表及副图：投入产出行业数据及可视化

位于首页正下方位置，副表及副图整合于各 ``分页表 (tabs) `` 中，列出相关图表如下述。

```{note}
所有表格均有排序功能，可以按 ``排名`` 或 ``数值`` 进行排序比较。
```

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
tags: [remove-input]
---
VC.pn_tabs_primary 
```

### 分页1 → 行业（表格）：节点

#### 指标 ``主要``、 ``次要``、``任选`` 共三项选择器及分页，含基本统计

此处分别有：``主要``、 ``次要``、``任选`` 共三项选择器及分页可供用户对产业的 ``产值`` 及 ``环境影响`` 进行探究比较。

```{note}
此处含进口出口等计有 ``16 (原数据共 30) 指标``，并列出投入 `百分位排名`、`百分比`、`排名`、`值` 等基本统计及信息。
```

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
tags: [remove-input]
---
VC.pn_Node
```

#### 过滤器：节点

此处选择器（可多选）方便用户过滤相关产业（节点）。
#### 过滤器：最小值

此处可设置小值进行过滤。

-----

+++

### 分页2 → 行业间投入产出（表格）：边缘

#### ``投入``- ``产出`` 值比较，含基本统计

此处按原始数据特性，列出投入产出值的 ``百分位排名``、``百分比``、``排名`` 等基本统计。

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
tags: [remove-input]
---
VC.pn_Edge
```

#### 过滤器：**投入**-**产出** 节点

此处有分 **投入**-**产出** 的对映选择器（可多选）方便用户过滤相关产业（节点）。
#### 过滤器：最小值

此处可设置小值进行过滤。

---

+++ {"editable": true, "slideshow": {"slide_type": ""}}

### 分页3 → 指标走势（图）：核心行业指标历史走势

此处列出 指标 ``任选`` 选择器，并允许用户选择 ``地区``，比较前7名的相关行业指标历史走势。

```{note}
可点选图说文字， ``设置/取消`` 走势高亮。
```

```{code-cell} ipython3
glue("pn_TopN_Trendlines", VC.pn_TopN_Trendlines)
```

+++ {"editable": true, "slideshow": {"slide_type": ""}}

```{glue:} pn_TopN_Trendlines
```

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
---
VC.pn_TopN_Trendlines
```

### 分页4 → 核心桑基（图）：核心投入产出行业关系

此处允许用户选择 ``地区`` 及 ``年份``，比较前7名的核心投入产出行业关系桑基（图）。

```{note}
可点选 ``拖拽`` 图元素排版。
```

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
tags: [remove-input]
---
VC.pn_TopN_Sankey
```

#### 核心桑基（图）：客制化

比较前15名的 ``北京`` , ``2017新`` 核心投入产出行业关系桑基（图）。

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
tags: [remove-input]
---
VC.pn.pane.ECharts( VC.gen_Sankey_TopN_Nodes ('北京', '2017新', TopN=15) )
```

#### 核心桑基（图）：客制化

比较前15名的 ``江苏`` , ``2017`` 核心投入产出行业关系桑基（图）。

```{note}
可点选 ``拖拽`` 图元素排版。
```

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
tags: [remove-input]
---
VC.pn.pane.ECharts( VC.gen_Sankey_TopN_Nodes ('江苏', '2017', TopN=15) )
```

# 小结

``CEADs 投入产出网络仪表盘`` 展示了 数据可视化 作为 数据驱动决策 的可能性。基于科学实证的相关产出及环境影响的信息及情报，将能有效提供 [``精准脱碳`` 决策参考](https://oxon8.netlify.app/project/prj-visCEADs/)。

```{code-cell} ipython3

```
