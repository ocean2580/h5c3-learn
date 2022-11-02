## 浮动属性
float: none/left/right;
显示但不占原空间，依然在父级元素里,外边距不会合并
dispaly失效，可以设置宽高，不独行,(浮动元素之间)不会重叠

clear: both/left/right;
清除浮动,取消其他浮动元素对该元素的影响



## 定位属性
position: static/relative//absolute/fixed
  top/bottom/left/right: xx px;

static 默认值无定位
relative 相对于其正常位置
absolute 相对static以外第一个父元素（否则body）,不占空间
fixed 相对于浏览器窗口定位

z-index (定位重叠元素间)用户看到z轴顶端
  z-index: -1/1/...;



## display属性
display: none/inline/block/inline-block/table-cell/flex;
确定元素类型

none 隐藏元素的显示和位置 
block(div) 块状元素，具宽高属性，独占一行
inline(span) 行内元素，无宽高属性，不占行
inline-block 内联块元素，有宽高属性，但不独占一行
table-cell 表格单元格
flex 弹性盒

visibility: hidden; 或者 opacity: 0;  都只会隐藏显示 



## 盒子模型
content, padding, border, margin
![盒子模型](https://img.php.cn//upload/image/571/587/908/1535965813125465.png)

对象实际长度 = margin-left + border-left + padding-left + width + padding-right + border-right + margin-right

- margin 外边距
  margin-left/right/top/bottom: value;
  value 可 px, %, auto, 负值(反向移动)
  四值 设置顺时针（上右下左）
  两值 上下、左右
  margin: 10px auto;  // 上下各10px,水平居中

- 外间距合并(垂直方向)
  交集空间只显示最大的
  直接调子元素会导致父元素一起改变，要给父元素加边框（border: 1px solid red;）

- border 边框
  border-left/right/top/bottom: width style color;
    style: dotted, solid, double, dashed, none... 必须设置

- padding 内间距
   margin-left/right/top/bottom: value; 
   value 可 px, %, auto, 不能负数

水平居中 left: calc(50% - width / 2);