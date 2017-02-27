# html+css 基础教程

## html和css的关系
- html 是网页内容的载体
- css 样式是表现
- javascript 是控制网页上行为交互

## 标签的语法
- 便签一般是闭合的，<></>
- 一般是成对出现
- 便签之间可以嵌套
- HTML便签不区分大小写

##　html文件的文本结构
```
<html>
    <head>...</head>
    <body>...</body>
</html>
```

## head标签
```
<head>
    <title>...</title>
    <meta>
    <link>
    <style>...</style>
    <script>...</script>
</head>
```
## html语义化
- 理解标签的用途
- 优点
1. 更容易被搜索引擎搜索
2. 更容易让屏幕阅读器读出网页内容

### body标签 文档的主要内容
### p标签文章的段落
###　h1~h6标题标签
### em,strong ,
- em 没有strong 更加强调
- 国内流行strong
- em 为斜体，strong为加粗
### span标签，没有语义，作用是为了设置单独的样式

### q标签，短文本引用,默认样式是双引号
### blockquote便签，长文本引用，默认样式为缩进样式
### br便签，换行显示文本
1. 一般使用4.0的写法 <br/>
2. 空标签一般有<br/><hr/><img/>
3. html 中忽略空格和回车
### 空格&nbsp;
### hr标签 添加水平线
### address标签 为网页加入地址信息 
### code 标签 加入代码 小段代码
### pre 标签 加入打断代码
### ul,li无序列表，展示新闻信息列表
### div 容器，布局大块
- div要合理命名，
- id唯一 ，class多种
### table>thead>tr>th>tbody>tr>td>tfoot>tr>td
- table表格在每添加css之前，浏览器中没有显示表格线的
- 表头，th中的文本默认是粗体居中显示;
- caption标签添加标题
- summary属性添加摘要，网页中不可见
### a便签，锚点链接
- href 链接的地址
-  title 鼠标划过显示的文本
- target 页面打开的位置
- download 下载
- mailto在网页中链接Email地址
![](http://img.mukewang.com/52da4f2a000150b714280550.jpg)

### <img>标签，为网页插入图片
- src 图像的位置
- alt 图像不见时，提示文本
- title 提供在图像可见时对图像的描述（鼠标划过）
- 图片格式 gif png jpeg
### 表单标签，用户交互
- method :get post
- action: 服务器提交的地址
1.所有表单控件（文本框、文本域、按钮、单选框、复选框等）都必须放在 <form></form> 标签之间（否则用户输入的信息可提交不到服务器上哦！）
2.method : post/get 的区别

### input标签
- type 类型 text，submit,password,radio,button,checkbox,reset;
- name 文本框命名，以备后台程序ASP 、PHP使用。
- 为文本输入框设置默认值

### 文本域 textarea标签
- 支持多行文本输入
- <textarea>标签是成对出现的，以<textarea>开始，以</textarea>结束。
- cols ：多行输入域的列数
- rows ：多行输入域的行数
- 在<textarea></textarea>标签之间可以输入默认值
- 注意这两个属性可用css样式的width和height来代替：col用width、row用height来代替。

### 单选框和复选框，让用户选择
- radio 单选框
- checkbox 复选框
- value 提交数据到服务器的值（后台程序PHP使用）
- name：为控件命名，以备后台程序 ASP、PHP 使用
- checked：当设置 checked="checked" 时，该选项被默认选中
- 同一组的单选按钮，name 取值一定要一致，比如上面例子为同一个名称“radioLove”，这样同一组的单选按钮才可以起到单选的作用。

### 下拉列表  select>option
- value 向服务器的提交值  
- 标签内的文字为显示的值
- selected="selected"：设置selected="selected"属性，则该选项就被默认选中
- multiple 多选

### 提交按钮，提交数据 input 
- type：只有当type值设置为submit时，按钮才有提交作用
- value：按钮上显示的文字

### 重置按钮 重置表单信息 reset
- type：只有当type值设置为reset时，按钮才有重置作用
- value：按钮上显示的文字

### label标签
- label标签不会向用户呈现任何特殊效果，它的作用是为鼠标用户改进了可用性。如果你在 label 标签内点击文本，就会触发此控件。就是说，当用户单击选中该label标签时，浏览器就会自动将焦点转到和标签相关的表单控件上
- <label for="控件id名称">
- 标签的 for 属性中的值应当与相关控件的 id 属性值一定要相同。

——————————————————————————————————————————————————————————————————

## css样式

### css语法
- css 样式由选择符和声明组成，而声明又由属性和值组成，如下图所示：
![](http://img.mukewang.com/52fde5c30001b0fe03030117.jpg)
- 选择符:又称选择器，指明网页中要应用样式规则的元素，如本例中是网页中所有的段（p）的文字将变成蓝色，而其他的元素（如ol）不会受到影响。
- 声明：在英文大括号“｛｝”中的的就是声明，属性和值之间用英文冒号“：”分隔。当有多条声明时，中间可以英文分号“;”分隔，如下所示：
- 最后一条声明可以没有分号，但是为了以后修改方便，一般也加上分号。
- 就像在Html的注释一样，在CSS中也有注释语句：用/*注释语句*/来标明（Html中使用<!--注释语句-->)。就像下面代码：  

### css样式的写法
- !important>内联>嵌入>外部样式表
但是嵌入式>外部式有一个前提：嵌入式css样式的位置一定在外部式的后面
其实总结来说，就是--就近原则（离被设置元素越近优先级别越高）。

### css选择器
1. 标签选择器
2. 类选择器. 不能写中文
3. id选择器#
4. 子选择器，>
5. 空格 后代选择器
6. 通用选择器 *
7. 伪类选择器 :hover
8. 分组选择符 ，

### css继承
CSS的某些样式是具有继承性

### 特殊性
靠权重决定选择哪种选择符
还有一个权值比较特殊--继承也有权值但很低，有的文献提出它只有0.1，所以可以理解为继承的权值最低

### 层叠
权重相同，后者覆盖前者

### 重要性
最高权值 !important

### 字体排版
- font-family
- font-size
- font-weight
- font-style
- text-decoration
- text-indent
- line-height
- letter-spacing
- word-spacing
- text-align 块状元素中的文本、图片设置居中样式

### 元素分类
1.常用的块状元素有：
<div>、<p>、<h1>...<h6>、<ol>、<ul>、<dl>、<table>、<address>、<blockquote> 、<form>
2. 常用的内联元素
<a>、<span>、<br>、<i>、<em>、<strong>、<label>、<q>、<var>、<cite>、<code>
3. 内联块元素
<img>、<input>

### 块级元素
- 设置display:block就是将元素显示为块级元素。如下代码就是将内联元素a转换为块状元素，从而使a元素具有块状元素特点。
- 每个块级元素都从新的一行开始，并且其后的元素也另起一行。（真霸道，一个块级元素独占一行）
- 元素的高度、宽度、行高以及顶和底边距都可设置。
- 元素宽度在不设置的情况下，是它本身父容器的100%（和父元素的宽度一致），除非设定一个宽度。

### 内联元素
- 当然块状元素也可以通过代码display:inline将元素设置为内联元素。
1. 和其他元素都在一行上；
2. 元素的高度、宽度及顶部和底部边距不可设置
3. 元素的宽度就是它包含的文字或图片的宽度，不可改变

### 内联块元素
- 内联块状元素（inline-block）就是同时具备内联元素、块状元素的特点，代码display:inline-block就是将元素设置为内联块状元素。(css2.1新增)，<img>、<input>标签就是这种内联块状标签
1. 和其他元素都在一行上
2. 元素的高度、宽度、行高以及顶和底边距都可设置。

### 盒子模型
- content+padding+border+margin
- border:1px solid red;
1.border-style（边框样式）常见样式有：
dashed（虚线）| dotted（点线）| solid（实线）
2.border-color（边框颜色）中的颜色可设置为十六进制颜色
border-color:#888
3. border-width（边框宽度）中的宽度
thin | medium | thick

### 布局模型
- CSS包含3种基本的布局模型，用英文概括为：Flow、Layer 和 Float。
1、流动模型（Flow）
2、浮动模型 (Float)
3、层模型（Layer）

- 流动模型，流动（Flow）是默认的网页布局模式。也就是说网页在默认状态下的 HTML 网页元素都是根据流动模型来分布网页内容的。
1. 第一点，块状元素都会在所处的包含元素内自上而下按顺序垂直延伸分布，因为在默认状态下，块状元素的宽度都为100%。实际上，块状元素都会以行的形式占据位置。如右侧代码编辑器中三个块状元素标签(div，h1，p)宽度显示为100%。
2. 第二点，在流动模型下，内联元素都会在所处的包含元素内从左到右水平分布显示。（内联元素可不像块状元素这么霸道独占一行）

- 浮动模型
1.任何元素在默认情况下是不能浮动的，但可以用 CSS 定义为浮动，如 div、p、table、img 等元素都可以被定义为浮动

- 层模型
层布局模型就像是图像软件PhotoShop中非常流行的图层编辑功能一样，每个图层能够精确定位操作，但在网页设计领域，由于网页大小的活动性，层布局没能受到热捧
- 三种形式
1.绝对定位(position: absolute)
2.相对定位(position: relative)
3.固定定位(position: fixed)

### 颜色值缩写
### 长度值 
1. px
2. em
3. rem
4. %

### css样式技巧
- 水平居中设置-行内元素
如果被设置元素为文本、图片等行内元素时，水平居中是通过给父元素设置 text-align:center 来实现的
- 水平居中设置-定宽块状元素
满足定宽和块状两个条件的元素是可以通过设置“左右margin”值为“auto”来实现居中的。我们来看个例子就是设置 div 这个块状元素水平居中：
- 水平居中总结-不定宽块状元素方法
1.加入 table 标签
2.改变块级元素的 display 为 inline 类型（设置为 行内元素 显示），然后使用 text-align:center 来实现居中效果。如下例子：
3.设置 position:relative 和 left:50%：利用 相对定位 的方式，将元素向左偏移 50% ，即达到居中的目的

- 垂直居中-父元素高度确定的单行文本
1.父元素高度确定的单行文本的竖直居中的方法是通过设置父元素的 height 和 line-height 高度一致来实现的

- 垂直居中-父元素高度确定的多行文本
1.方法一：使用插入 table  (包括tbody、tr、td)标签，同时设置 vertical-align：middle。
css 中有一个用于竖直居中的属性 vertical-align，在父元素设置此样式时，会对inline-block类型的子元素都有用。下面看一下例子：
2.在 chrome、firefox 及 IE8 以上的浏览器下可以设置块级元素的 display 为 table-cell（设置为表格单元显示），激活 vertical-align 属性，但注意 IE6、7 并不支持这个样式, 兼容性比较差。

### 隐性改变display类型
1. 有一个有趣的现象就是当为元素（不论之前是什么类型元素，display:none 除外）设置以下 2 个句之一
2. position : absolute
3. float : left 或 float:right 
4 内联元素会被转化行内块元素，可设置宽高