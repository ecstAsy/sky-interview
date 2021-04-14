<h3 align='center'>Flex布局</h3>

### 定义
> Flex 是 Flexible Box 的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性。

### 属性
* 父组件
  - flex-direction
  - flex-wrap
  - flex-flow
  - justify-content
  - align-items
  - align-content
* 子组件
  - order
  - flex-grow
  - flex-shrink
  - flex-basis
  - flex
  - align-self
### 父组件属性分析
* __flex-direction__: 决定主轴的方向（即项目的排列方向）
  ```css
  flex-direction: row | row-reverse | column | column-reverse;
  ```
  - row(默认值) ：主轴为水平方向，起点在左端。
  - row-reverse ： 主轴为水平方向，起点在右端。
  - column：主轴为纯直方向，起点在上端。
  - column-reverse：主轴为纯直方向，起点在下端。
* __flex-wrap__: 如果一条轴线排不下，如何换行。
  ```css
  flex-wrap: nowrap | wrap | wrap-reverse;
  ```
  - nowrap(默认值)：不换行。
  - wrap：换行，第一行在上方。
  - wrap-reverse：换行，第一行在下方。
* __flex-flow__:flex-direction属性和flex-wrap属性的简写形式，默认值为row nowrap。
  ```css
  flex-flow: row<flex-direction> | nowrap。<flex-wrap>;
  ```
* __justify-content__: 项目在主轴上的对齐方式。
  ```css
  justify-content: flex-start | flex-end | center | space-between | space-around;
  ```
  - flex-start（默认值）：左对齐。
  - flex-end：右对齐。
  - center： 居中。
  - space-between：两端对齐，项目之间的间隔都相等。
  - space-around：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。
* __align-items__:项目在交叉轴上如何对齐。
  ```css
  align-items: flex-start | flex-end | center | baseline | stretch;
  ```
  - flex-start：交叉轴的起点对齐。
  - flex-end：交叉轴的终点对齐。
  - center：交叉轴的中点对齐。
  - baseline: 项目的第一行文字的基线对齐。
  - stretch（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。
* __align-content__:多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。
  ```css
  align-content: flex-start | flex-end | center | space-between | space-around | stretch;
  ```
  - flex-start：与交叉轴的起点对齐。
  - flex-end：与交叉轴的终点对齐。
  - center：与交叉轴的中点对齐。
  - space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。
  - space-around：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
  - stretch（默认值）：轴线占满整个交叉轴。
### 子组件属性分析