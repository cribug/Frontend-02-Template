#css

##at-rules

- @charset
- @import
- <font color='red'>@media</font>
- @page
- @counter-style
- <font color='red'>@keyframes</font>
- <font color='red'>@fontface</font>
- @support
- @namespace



## rule

- Selector

  - selector_group
  - slector
    - \>
    - \<sp\>
    - +
    - ~
  - simple_slector
    - type
    - *
    - .
    - #
    - :
    - ::
    - :not()

- Declaration

  - Key

    - variables
    - properties

  - Value

    - calc
    - number
    - length

    

## 选择器语法

###简单选择器

- *
- div svg|a
- .cls
- \#id
- [attr=value]
- :hover
- ::before

### 复合选择器

- \<简单选择器>\<简单选择器>\<简单选择器>

- *或者div必须写在最前面
- 伪类伪元素写在最后面

###复杂选择器

- \<复杂选择器>\<sp>\<复杂选择器>
- \<复杂选择器>">"<复杂选择器>
- \<复杂选择器>"~"\<复杂选择器>
- \<复杂选择器>"+"\<复杂选择器>
- \<复杂选择器>"||"\<复杂选择器>



## 选择器优先级

[a, b, c, d]

- `a` 行内样式
- `b` ID选择器
- `c` 类选择器、属性选择器、伪类选择器
- `d` 标签选择器、伪元素

$ S = aN^3+bN^2+cN^1+d $

IE 老版本N取255，后来大部分浏览器选择 65536，现在浏览器选的值更大。



## 伪类

### 链接/行为

- :any-link
- :link
- :visited
- :hover
- :active
- :focus
- :target

### 树结构

- :empty
- :nth-child()
- :nth-last-child()
- :first-child
- :last-child
- :only-child

### 逻辑型

- :not 伪类
- :where
- :has



## 伪元素

- ::before
- ::after
- ::first-line
- ::first-letter

