# H5和CSS3基础

主要学习PC端的**网站布局**；

**目的**：精通网页的布局！

# H5基础

没有兼容性问题的HTML标签

## 简介

### 网页

网页是组成网站中的一个页面，网页通过浏览器来阅读；

网页由图片、文字、音频、视频、链接等元素组成，通常是HTML文件；

HTML:(Hyper Text Markup language)超文本标记语言；

THML文件中由一些html标签组成；

超文本：超越文本限制，超级链接文本；

### 常用的浏览器

**常用的浏览器**：

	IE、Firefox、Chrome、Safari、Opera(五大浏览器)
	Edge和IE都是微软的浏览器

**内核（渲染引擎）**：

	IE：Trident（猎豹、360、百度）
	Firefox:Gecko
	Safari:Webkit（苹果）
	Chrome/Opera:Blink(Blink是WebKit的一个分支)
	国产浏览器：Webkit、Blink

### Web标准

**W3C组织**制定了web标准；

**作用**：浏览器不同，显示的页面有些许差异

**Web标准构成**：

	结构：对网页元素进行整理分类，主要是HTML；
	表现：设置网页元素的版式、颜色、大小等外观样式，主要是CSS；
	行为：网页模型的定义及交互编写，主要是JavaScript；

**结构最重要**

### HTML标签

#### HTML语法规范

1.成对出现;

2.所有的元素都包含在```<html></html>```;

3.也有单标签```<br />```;

**标签关系**:

1.包含关系

	<head>
		<title></title>
	</head>

2.并列关系

	<head></head>
	<body></body>

#### HTML基本结构标签

基本结构标签也成为骨架标签:

	<html>:根标签；
	<head>:文档头部，head标签中必须设置title标签；
	<title>:文档标题，让网页拥有自己的标题；
	<body>:文档主体，页面的内容基本都是放在这个里面；

#### 开发工具

1.HBuilder（我现在使用）；

2.记事本（传统），缺点是不方便；

3.Dreamweaver、Sublime、VSCode；

#### HTML常用的标签(一)

```<!DOCTYPE html>```文档类型声明标签，这个标签表示是H5标签；

```<html lang='en'>```中```lang='en'```定义了文档的语言，比如中文```lang='zh-CN'```;

	作用：提示浏览器;
	
```<meta charset='utf-8'```定义字符集，其他：GB2312、BIG、GBK,如果没有定义字符集会出现乱码；

**常用标签**

记住每个标签的语义；

根据语义，在合适的位置放置合适的标签，让页面结构更清晰；

**标题标签h1~h6**

	h：head的缩写；
	
**段落和换行标签**

	<p></p>:paragragh 段落
	<br />:break 打断，换行
	
**文本格式化**

粗体、斜体、下划线：突出重要性；

	<strong></strong>/<b></b>:加粗；
	<em></em>/<i></i>:倾斜;
	<del></del>/<s></s>:删除线；
	<ins></ins>/<u></u>:下划线；

建议：优先使用前面一个标签，语义更强烈；

**<div>和<span>标签**

无语义，当作盒子使用；

div:分割，分区；

	特点：独占一行；

span:跨度；

	特点：行内元素；
	
**图像标签和路径**

	<img src='图像url' />
	
src:是<img>的属性；（必要属性）

属性：属于谁的特性；

其他属性：

	alt:图片无法显示时的替换文本；
	title:提示文本，鼠标放在图片上提示的文字；
	width:图像的宽度；
	height:高度；（在改变图像大小的时候，只需要修改一个，然后等比例缩放）
	border:边框；border="15px"//一般有CSS来实现；

路径：

	相对路径：图片相对于文件的位置；同一级路径，直接写图片的名字；下一级路径使用'/';上一级路径使用'../';
	绝对路径：图片的绝对位置，通常是从盘符开始的；
	
**超链接标签**

	<a href='跳转目标' target='目标窗口弹出的方式'></a>

href:链接，外部链接（http）,内部链接（**.html）,空连接（'#'）,下载链接（文件/压缩包路径）;

target:_self(默认，当前窗口)、_blank(打开新的窗口);

锚点链接：点击链接，可以快速定位到页面的某个位置；

	<a href="#a">:锚点链接；
	<h3 id="a">:锚点；

#### HTML中的注释和特殊字符

**注释**

	<!-- -->
	ctrl+/

注释帮助我们理解代码；

让我们能想到之前写的代码；

**特殊字符**

	&nbsp; //空格
	&lt; //<小于
	&gt; //>大于
	&amp; //&

注意：不要忘记';'

[特殊符号查询](http://m.htmlchar.115cha.com/)

#### HTML常用标签(二)

**表格标签**

表格作用：展示、显示数据，让数据显示非常规整；老前端会用来布局；

	<table>表格
		<tr>行
			<td>单元格</td>列
			<td></td>列
			<td></td>列
				……
		</tr>
	</table>

<td>:单元格 table data；

<th>:表头 table head，特点：文字加粗居中显示；

表格属性：一般有css设置；

	align:center left right;//表格的对其方式；
	border:1或'';//表格边框；
	cellpadding:像素;//表格内边框；
	cellspacing:像素;//单元格之间的距离；
	width:像素;//表格的宽度；
	height:像素;//表格的高度；

结构标签：

	<thead>:头部
	<tbody>:表格主体

合并单元格：

	跨行合并：rowspan='单元格个数';
	跨列合并：colspan='单元格个数';

**列表标签**

用于布局：整齐、整洁、有序；

无序列表：

	<ul>
		<li></li>
		<li></li>
		<li></li>
			…
	</ul>

有序列表：

	<ol>
		<li></li>
		<li></li>
		<li></li>
			…
	</ol>

他们有自己的样式，可以用css去掉；

ul、ol中只能放li标签！

li中可以放任意元素；

自定义列表：

	<dl>
		<dt></dt>
		<dd></dd>
		<dd></dd>
		<dd></dd>
			…
	</dl>

dl:定义列表；

dt:定义项目/名字；

dd:定义项目进行解释；

**表单标签**

表单用于收集用户信息；

组成：表单域、表单控件、提示信息

表单域：（将表单中的数据送到后台中）

	<form action='url地址' method='提交的方式' name='表单域名称'>
	各种表单控件
	</form>

表单控件：(表单元素)

	<input type='属性值' />：输入，

type属性决定元素的形式：

	text 文本
	password 密码
	radio (单选按钮)
	checkbox (多选按钮)
	submit 提交按钮
	reset 重置按钮
	button 按钮(不会提交数据)
	file 文件域，上传图像的时候使用，浏览文件
	hidden
	image
	email
	number
	date

name:给radio相同的名字才能实现单选按钮，checkbox也要设置一样的name；

value:当前控件的值，用于传回后台

checkde:默认选则

maxlength:输入的最大长度

**label标签**

结合表单一起使用；

<label>可以绑定一个表单元素；

	<label for='name'>male</label>
	<input type='text' id='name' />

**select下拉表单元素**

	<select>
		<option></option>
		<option></option>
		<option></option>
				…
	</select>

注意select也属于表单，所以要包含在form中；

selected属性：选中；

**textarea表单文本域元素**

用于定义多行输入：

	<textarea></textarea>
	
clos:列（每行字数）

rows:行数

一般用js来实现这两个属性，实际开发中不会使用；

每一个表单元素都有一个name元素；

表单域、文本域、文件域；

**查阅文档**

[W3C:中文网站w3cschool](https://www.w3school.com.cn/)

也可以下载w3cschool的离线文档；

[MDN](https://developer.mozilla.org/zh-CN/)

******
******

#CSS3基础

(css参考手册)[http://css.doyoe.com/]

没有兼容性问题的CSS样式；

美化网页，布局页面；

HTML具有局限性：只关注内容的语义，显示元素内容；HTML做样式非常臃肿、繁琐；

CSS(cascading style sheets)层叠样式表、级联样式表；

CSS也是一种标记语言，可以美化HTML，让HTML布局更加简单；

CSS让HTML专注做结构，样式交给CSS；将结构和样式分离；

## 语法规范

选择器+声明的样式

	选择器{
		属性：值；
		属性：值；
		……
	}

**style标签**

将样式表写在```<style></style>```中;

**代码风格**

1.格式

	紧凑型：h3{color: red;font-size: 15px;}
	展开型：p{
			color: red;
			font-size: 15px;
	}//可以后期使用压缩工具对代码进行压缩

2.空格规范

	在冒号后面保留空格；
	在选择器后选择空格；

## 基础选择器

两大类：基础选择器、复合选择器；

选择器的作用：根据不同的需求将不同的标签选择出来；

CSS做了两件事：1.找出标签；2.设置样式；

### 标签选择器

	标签名 {
	
	}

优点：可以将页面中同类的标签全部选择出来；

缺点：不能进行差异化设置；

### 类选择器

可以单独选择某一个或者某几个元素；

	.类名 {
		
	}
	在元素中设置一个class

命名规则：

	头部：head
	内容：content/container
	尾：footer
	导航栏：nav
	侧栏：sidebar
	栏目：column
	页面外围控制整体布局宽度：wrapper
	左右中：left right center
	登录条：loginbar
	标志：logo
	广告：banner
	页面主题：main
	热点：hot
	新闻：news
	下载：download
	子导航：subnav
	菜单：menu
	子菜单：submenu
	搜索：search
	友情链接：friendlink
	页脚：footer
	版权：copyright
	滚动：scroll
	内容：contain
	标签：tags
	文章列表：list
	提示信息：msg
	小技巧：tips
	栏目标题：title
	加入：joinus
	指南：guide
	服务：service
	注册:register
	状态：status
	投票：vote
	合作伙伴：partner	

**多类名**

	class="name1 name2"

使用场景：提取公共样式，减少代码；标签可以调用公共的类也可以调用自己独有的类；统一修改也比较方便。

### id选择器

	#id名{
		属性：值；
		属性：值；
		属性：值；
		……
	}
	在元素中设置一个id;

每个id在每个HTML文档中只能出现一次！

class可以被多个元素使用，id只能被一个元素使用；

通常id与js搭配使用，class通常与css结合使用；

### 通配符选择器

*：匹配所有的元素

	* {
	
	}

## 字体属性

### 字体系列

	font-family:"微软雅黑";

字体：宋体,微软雅黑,Microsoft yahei,Arial,Helvetice;

提倡使用系统默认字体；

### 字体大小

	font-size: 30px;
	
px:像素；

chrome默认字体为：16px;

不同的浏览器文字的大小可能不同，可以手动给body指定一个大小；

### 字体的加粗

	font-weight: 700;//不要单位，等价于bold;

normal：默认，正常字体；=400

bold:加粗；=700

像素

### 字体样式

	font-style:normal;

normal:默认值，正常；

italic：斜体；

oblique：将倾斜的字体变成字体；

### 字体的符合属性

	font: [style] [weight] [size]/[line-heigh]t [family];

要求：严格按照这个顺序，每个属性值以空格隔开；size和family必须设置，其他可以省略。

## 文本属性

文本外观样式：颜色、对齐、装饰、缩进、行间距；

### 颜色

预定义颜色：red、blue、black……

十六进制：#000000（使用较多）

RGB:rgb(200,0,0)//red,green,blue

注意：颜色值可以用吸管工具吸取过来；

### 对齐文本

	text-align:center

左中右：left center right

### 装饰文本

	text-decoration: underline;
	
none:默认值，没有装饰；

underline:下划线；

line-through:删除线，贯穿线；

overline:上划线；

### 文本缩进

	text-indent:10px;

**em相对单位**

	1em=当前字体的一倍大小；
	2em=当前字体的两倍大小；

### 行间距

	line-height: 20px;

行间距=上间距+文字高度+下间距；

改变行间距相当于改变上下间距；

**工具**：FSCapture

## 引入方式

css三种样式表：

	1.行内式，行内样式表；适合修改简单样式；在标签的内部协商style属性；只控制当前标签；并没有实现结构和样式分离。
	2.嵌入式，内部样式表；理论上可以放在HTML中的任何地方，一般放在<head>中；这种方式可以控制真个页面的样式；实现了结构和样式的部分分离。
	3.链接式，外部样式表（常用）；在外面创建一个css文件，在css文件中写样式，然后将css文件引入进来；引入<link rel="stylesheet" href="css文件路径" />。

## Chrome调试方式

打开调试工具：ctrl+F12

## Emmet语法

前身是ZenCoding，使用缩写，提高HTML/CSS的编写速度；

### 快速生成HTML机构语法

	标签名+tab：快速生成标签
	标签名*n：生成多个标签
	父标签>子标签：生成父子级标签
	兄弟标签+兄弟标签：兄弟关系标签
	标签.classname/#idname:生成一个有类名/id的标签
	.classname$*n:生成一个类名为classname1-classnamen的标签
	标签{msg}:生成带有文字的标签

注意以上结构都配合tab键使用。

### 快速生成CSS样式语法

	首字母+tab;
	首字母+值+tab;

### 快速格式化代码

	ctrl+shift+F

## 复合选择器

建立在基础选择器之上，对基本选择器进行组合；

常用的符合选择器有：后代选择器、子选择器、并集选择器、伪类选择器……

### 后代选择器

用于选择父元素中的子元素；

	父元素 子元素{
		……
	}//以空格隔开

### 子代选择器

选择最近一级的子类；

	父元素>子元素{
		……
	}//以>隔开

### 并集选择器

可以选择多组标签，同时定义相同的样式；

	元素1,元素2,…{
		……
	}//以,分割，相当于和

规范：并集选择器喜欢竖着写；最后一个选择器不需要加逗号；

### 伪类选择器

向某些选择器添加特殊的效果：链接；或者选择某个元素；

以(:)表示，比如：:hover;:first-child;

**链接伪类**

	a:link：选择所有未被访问过的链接；
	a:visited：选择访问过的链接；
	a:hover：选择鼠标悬停的链接；
	a:active：选择鼠标点下还未弹起的链接。

建议:按照LVHA的顺序；

**结构伪类**

[结构伪类](https://github.com/chengpingping/H5andCSS3#%E4%BC%AA%E7%B1%BB%E9%80%89%E6%8B%A9%E5%99%A8)

**:focus伪类选择器**

获得焦点/光标的元素；

	input:focus{
		……
	}

## 元素显示模式

元素以什么方式进行显示；元素可以分为不同的种类，一般分为块元素和行元素；

### 分类

**块元素**

常见：h,p,div,ul,ol,li

特点：

	1.独占一行；
	2.宽度，高度，内外边距都可以改变；
	3.宽度默认为父级元素宽度一样；
	4.一个容器/盒子里可以放行内或则块级元素；

注意：

	文字（p,h）元素不能放块级元素；

**行元素**

常见：a,strong,b,em,i,del,s,ins,u,span;也叫内联元素。

特点：

	1.一行可以放多个元素；
	2.宽，高设置无效；
	3.默认的宽度是本身的宽度；
	4.行内元素只能放文字和其他行类元素；

注意：

	a中不能放a；
	a中可以放块级元素；

**行内块元素**：

特殊标签：img,input,td。

特点：

	1.同时具有块级元素和行内元素的特点；
	2.相邻行内块元素一行可以放置多个，但是他们之间有空白缝隙，默认的宽度为内容的宽度；
	3.可以设置宽度、高以及内外边距；

### 转换

将一个模式的元素转换为另外一个元素；

	display:block;//转换为块级元素
	display:inline;//转换为行内元素
	display:inline-block;//转换为行内块元素

**snipaste截图工具**

	F1截图
	F3将截图固定到桌面
	Alt+点击取色（shift切换取色模式）
	ESC/双击取消图片在桌面上的固定

## 背景

背景属性可以设置：背景颜色、背景图片、背景平铺、背景图片的位置，背景图像的固定；

### 背景颜色

	background-color:transparent;

transparent:默认值，透明；

color：颜色（参考前面）；

### 背景图片

	background-image:none|url(图片路径);

优点：容易控制图片的位置；

### 背景平铺

	background-repeat:repeat|no-repeat|repeat-x|repeat-y;

repeat:默认值，平铺；

### 背景图片位置

	background-position: x y;

x,y指坐标；可以使用方位名词，也可以用精确的单位；

**方位名词**：left,right,top,bottom,center;

使用方位名词时，如果时两个值他们的顺序没有任何影响；只有一个值时，第二个值自动补充为center；

**精确的移动像素**：使用精确的像素时，有严格的顺序，第一个值一定是x，第二个值一定是y；

**混合单位**：第一个为x，第二个为y;

### 背景附着

	background-attachment:scroll|fixed;

scroll:默认是，滚动；

fixed:背景固定；

### 背景复合性写法

	background:color image repeat attachment position;

### 背景色半透明

	background:rgba(red,green,blue,alpha);
	
alpha:0-1，从透明到不透明；（IE9+才兼容）

tips:可以将小数的0省掉；

## 三大特性

层叠性、继承性、优先级

### 层叠性

样式冲突时，前面的样式会被覆盖；

### 继承性

子标签会继承父标签中的一些样式；

inherit：继承；

可以继承的样式：文字相关的样式，以及color；

**行高的继承**

	font:size/line-height family;

行高:可以时像素值；也可以是倍数，倍数是字体大小的倍数；

## 注释
