# 1 盒（Box）

##盒模型四部分

content

padding

border

margin

##box-sizing

content-box：width = content宽度

border-box：width = content宽度 + border宽度\*2 + padding宽度\*2

# 2 正常流

排版：文字、盒

我们如何写字？

- 从左到右书写
- 同一行写的文字都是对齐的
- 一行写满了，就换到下一行

正常流排行

- 收集盒进行
- 计算盒在行中的排布
- 计算行的排布



先不考虑writing-mode

行内级格式上下文：IFC（inline-level-formatting-content）文字 + inline-box = line-box

块级格式上下文：BFC（block-level-formatting-content）line-box + block-level-box

# 3 正常流的行级排布

基线对齐（baseline）

c++底层库 freeType，处理各种字体文件库，大部分软件使用的字体库

css行模型：

- baseline（基线）
- text-top（上缘）
- text-bottom（下缘）
- line-top
- line-bottom



不建议行内盒使用基线对齐

vertical-align： top（相对于行顶缘对齐）

vertical-align： bottom（相对于行底缘对齐）

# 4 正常流的块级排布

第一代排版：float+clear

第二代排版：flexbox

第三代排版：grid



float堆叠现象

不建议使用float排版



Margin Collapse（留白的折叠，边距折叠现象），只会存在BFC里

# 5 BFC合并

- Block Container：里面有BFC的
  - block
  - inline-block
  - table-cell
  - flex item
  - grid cell
  - table-caption
- Block-level Box：外面有BFC的(display)
  - block
  - flex
  - table
  - grid
- Block Box：（Block Container + Block-level Box）里外都有BFC

# 6 Flex 排版

收集盒进行

计算盒在主轴方向的排布

计算盒在交叉轴方向的排布



分行：

​	根据主轴尺寸，把元素分行进行

​	如果设置了no-wrap，则强行分配进第一行



计算主轴方向：

​	找出所有flex元素

​	把主轴方向的剩余尺寸按比例分配给这些元素

​	若剩余空间为负数，所有flex元素为0，等比压缩剩余元素

计算交叉轴方向：

​	根据每一行中最大元素尺寸计算行高

​	根据行高flex-align和item-align，确定元素具体位置

# 7 CSS动画与绘制

## Animation

- @keyframes 定义
- animation：使用



animation

animation-name 时间曲线

animation-duration 动画的时长

animation-timing-function 动画的时间曲线

animation-delay 动画开始前的延迟

animation-iteration-count 动画的播放次数

animation-direction 动画的方向



Transition

transition-property 要变换的属性

transition-duration 变换的时长

transition-timing-function 时间曲线（cubic-bezier.com）

transition-delay 延迟



<font color='red'>贝塞尔曲线需要研究研究</font>

模拟抛物线



##8 颜色

品红，黄，青（CMY）->CMYK

红绿蓝（RGB）

<font color='red'>HSL</font>和HSV

色相H，纯度S，亮度L，明度V

# 9绘制

## 几何图形

border

box-shadow

border-redius

##文字

font

text-decoration

##位图

background-image

