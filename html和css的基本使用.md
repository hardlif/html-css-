# 	html和css的基本使用

# HTML

## 1.注释

快捷键ctrl+/

## 2.div层级标签

## 3.标题标签

![image-20220423135139726](./images\image-20220423135139726.png)

![image-20220423135220069](./images\image-20220423135220069.png)

## 4.段落标签

![image-20220423135254410](./images\image-20220423135254410.png)

****



![image-20220423135455645](./images\image-20220423135455645.png)

***



## 5.换行标签

<br>

![image-20220423135624681](./images\image-20220423135624681.png)

## 5.5.水平分割线标签

***

![image-20220423135907987](./images\image-20220423135907987.png)

<hr> 

![image-20220423140017815](./images\image-20220423140017815.png)

## 6.文本格式化标签

![image-20220423140054413](./images\image-20220423140054413.png)



![image-20220423140410169](./images\image-20220423140410169.png)

## 7.图片标签



![image-20220423140610419](./images\image-20220423140610419.png)

![image-20220423140809027](./images\image-20220423140809027.png)

./表示当前路径，不加默认当前路径

## 属性注意点

![image-20220423140906048](./images\image-20220423140906048.png)

### alt属性

![image-20220423141009868](./images\image-20220423141009868.png)

### title属性

![image-20220423141119036](./images\image-20220423141119036.png)

### width和height属性

![image-20220423141430140](./images\image-20220423141430140.png)

## 绝对路径

![image-20220423141645562](./images\image-20220423141645562.png)

## 相对路径

![image-20220423141735653](./images\image-20220423141735653.png)

![image-20220423141852036](./images\image-20220423141852036.png)

![image-20220423141905749](./images\image-20220423141905749.png)

![image-20220423142034619](./images\image-20220423142034619.png)

## 8.音频标签

![image-20220423142112718](./images\image-20220423142112718.png)

![image-20220423142300922](./images\image-20220423142300922.png)

## 9.视频标签

![image-20220423142326879](./images\image-20220423142326879.png)

直接在autoplay属性后面加 muted即可实现

![image-20220423142552535](./images\image-20220423142552535.png)

## 10.超链接标签

![image-20220423142635182](./images\image-20220423142635182.png)

![image-20220423142727032](./images\image-20220423142727032.png)

如果开发初期没决定跳转到哪个界面，链接填#

![image-20220423142957324](./images\image-20220423142957324.png)

```html

<html>
	<head>
		<meta charset="utf-8">
		<!-- 内部样式表 -->
		<!--在head中<style>语句<style/>叫内部样式表-->
		<style type="text/css">
			/* 被style标签包围的范围是CSS环境，可以写CSS代码 */

			/* 标签样式表 */
			p{
				color:red;
			}

			/* 类样式 */
			.f20{
				font-size:20px;
			}
		</style>
		<!-- 引用外部的CSS样式表文件 -->
		<link rel="stylesheet" href="css/demo01.css"><!--在引用别的文件叫做外部样式表-->
	</head>
	<body>
		<!--
		<p><font color="red">这里是段落一</font></p>
		<p><font color="red">这里是段落二</font></p>
		-->
		<p>这里是段落一</p>
		<p>这里是段落二</p>
		<p class="f20">这里是段落三</p><!--这里class设置此处为f20类-->
		<p id="p4">这里是段落四</p>	<!-- id属性在整个HTML文档中，尽量保持唯一（虽然重复也不会报错） -->

		<div>
			<p><span style="font-size:60px;font-weight:bolder;color:yellow;">HELLO</span></p><!--在标签里加style=""叫嵌入式样式表,-->
			<span class="f32">World</span>
			<p class="f32">!!!</p>
        </div>
	</body>
</html>

<!--
1. 为什么需要CSS
2. CSS的最基本的分类: 标签样式表、类样式表、ID样式表
3. CSS从位置上的分类：嵌入式样式表、内部样式表、外部样式表
-->
```



## css优先级

```html
<html>
    <head>
        <title>
            这里是标题
  
        </title>  
     <style type="text/css">

     </style>
     <link rel="stylesheet" href="css/stylecss.css">
        <meta charset="utf-8">
    </head>
    <body>
    <p>例子一</p>
    <p class="f20">例子二</p>
    <div>
        例子三
        <p>例子四</p>
<!--嵌入式样式表优先级最高-->
        <scan  style="font-size:60px;font-weight:bolder;color:yellow;" class="f20">例子五</scan>
        <p class="f20">例子六</p>

    </div>
        
    </body>
</html>
<!--优先级总的来说是按就近原则来适配的-->
```

## div内部常用属性

```java
<html>
	<head>
		<meta charset="utf-8">
		<style type="text/css">
			#div1{
				width:400px;
				height:400px;
				background-color:greenyellow;

				/* 1. border 边框样式 */
				border-width:1px;			/*边框粗细*/
				border-style:solid;		/*边框样式：solid(实线) , dotted(点状线) ... */
				border-color:blue;			/*边框颜色*/

				/* border:4px double blue;*//* 组合设置等同于上面三个的效果*/

				/* border-top : 4px dotted blue;
				等同于border-top-width: 4px;
				border-top-style:dotted;
				border-top-color:blue;
				*//*上边框*/
			}

			#div2{
				width:150px;
				height:150px;
				background-color:darkorange;
				
				margin-top:100px;
				margin-left:100px;
				
				/*margin:100px 100px 50px 150px;*/ /* 一个值，四个方向统一；两个值：上下、左右；三个值：上、左右、下；四个值：上右下左 */
			
				/* padding : 填充 */
				padding-top:50px;
				padding-left:50px;
			}

			#div3{
				width:100px;
				height:100px;
				background-color:aquamarine;
				/*
				margin-top:50px;
				margin-left:50px;
				*/
			}
			#div4{
				width:200px;
				height:200px;
				margin-left:100px;
				background-color:greenyellow;
			}
			body{
				margin:0;
				padding:0;
			}
		</style>
	</head>
	<body>
		<div id="div1">
			<div id="div2">
				<div id="div3">&nbsp;</div>
			</div>
		</div>
		<div id="div4">&nbsp;</div>

	</body>
</html>

<!-- 
  有时会出现子层的margin-top应用与父层的情况
原理：margin折叠（Collapsing Margins）

毗邻的两个或多个外边距 (margin) 在垂直方向会合并成一个外边距。

这里的毗邻指没有上下padding-top,padding-bottom,border-top,border-bottom,元素内容不为空。

最常见的margin折叠是<p>元素并列时，每个p都有上下1em的margin，但相临的p只会显示1em的间隔而不是2em。

本例中两个div是父子关系，并且没有padding-top和border-top，即父元素和子元素上边重合。也属于毗邻的范畴，所以也出现了margin折叠，本例显示了子元素的margin-top；

 详细的margin重合计算可以参考这篇：http://www.cr173.com/html/17041_1.html

避免这个问题只要使条件不符合或者隐藏margin：给父元素加padding/border,父子间添加其他元素，或者设置为浮动，定位都行。

IE中的情况还没有具体测试过，后面补全。
-->
```

## 11.列表标签![image-20220423143559603](./images\image-20220423143559603.png)

### 1.类表使用场景

![image-20220423143720725](./images\image-20220423143720725.png)

### 2.无序列表

![image-20220423143839235](./images\image-20220423143839235.png)

![image-20220423144119781](./images\image-20220423144119781.png)

![image-20220425012914330](./images\image-20220425012914330.png)

### 3.有序列表

![image-20220423144032320](./images\image-20220423144032320.png)

![image-20220423144157373](./images\image-20220423144157373.png)

### 4.自定义列表

![image-20220423144236756](./images\image-20220423144236756.png)

![image-20220423144542340](./images\image-20220423144542340.png)

## 12.表格标签

![image-20220423145217387](./images\image-20220423145217387.png)

![image-20220423145411653](./images\image-20220423145411653.png)

![image-20220423145439355](./images\image-20220423145439355.png)

![image-20220423150334229](./images\image-20220423150334229.png)

![image-20220423150603968](./images\image-20220423150603968.png)

![image-20220423150814316](./images\image-20220423150814316.png)

![image-20220423150839484](./images\image-20220423150839484.png)

![image-20220423150910829](./images\image-20220423150910829.png)

*<caption> 标签*必须直接放置到 <table> 标签之后。每个表格只能规定一个标题。通常标题会居中显示在表格上方

#### 合并单元格

![image-20220423151109657](./images\image-20220423151109657.png)

![image-20220423151540933](./images\image-20220423151540933.png)

## 13.表单标签

### firm标签内写input系列标签

### 定义和用法

<form> 标签用于为用户输入创建 HTML 表单。

表单能够包含 [input 元素](https://www.w3school.com.cn/tags/tag_input.asp)，比如文本字段、复选框、单选框、提交按钮等等。

表单还可以包含 [menus](https://www.w3school.com.cn/tags/tag_menu.asp)、[textarea](https://www.w3school.com.cn/tags/tag_textarea.asp)、[fieldset](https://www.w3school.com.cn/tags/tag_fieldset.asp)、[legend](https://www.w3school.com.cn/tags/tag_legend.asp) 和 [label 元素](https://www.w3school.com.cn/tags/tag_label.asp)。

**表单用于向服务器传输数据。**

### 提示和注释

**注释：**form 元素是块级元素，其前后会产生折行。

![image-20220423171523594](./images\image-20220423171523594.png)

### 1.input标签

![image-20220423153020189](./images\image-20220423153020189.png)

![image-20220423152948263](./images\image-20220423152948263.png)

#### 1.文本框

![image-20220423152927144](./images\image-20220423152927144.png)

![image-20220423153118489](./images\image-20220423153118489.png)

![image-20220423153142522](./images\image-20220423153142522.png)

#### 2.单选框

![image-20220423165017549](./images\image-20220423165017549.png)

#### 3.文件

```html
<input type="file">
```



![image-20220423165327419](./images\image-20220423165327419.png)

#### 4.按钮

![image-20220423165709152](./images\image-20220423165709152.png)

#### 属性value指定按钮上的文字

![image-20220423170238935](./images\image-20220423170238935.png)

```html
<input type="button">
<input type="submit">
<input type="reset">
```



#### 5.button标签![image-20220423170344728](./images\image-20220423170344728.png)

```html
    <button>按钮标签</button>
```

#### 6.select标签

![image-20220423171744414](./images\image-20220423171744414.png)

```html
 <select name="getwife">
            <option value="1">1年</option>
            <option>2年</option>
            <option>3年</option>
            <option>4年</option>
            <option>5年</option>
            <option>6年</option>
            <option>7年</option>

        </select>
```

#### 7.textarea文本域标签

![image-20220423171942793](./images\image-20220423171942793.png)

#### 8.label标签

##### 定义和用法

<label> 标签为 input 元素定义标注（标记）。

label 元素不会向用户呈现任何特殊效果。不过，它为鼠标用户改进了可用性。如果您在 label 元素内点击文本，就会触发此控件。就是说，当用户选择该标签时，浏览器就会自动将焦点转到和标签相关的表单控件上。

<label> 标签的 for 属性应当与相关元素的 id 属性相同。

![image-20220423172457474](./images\image-20220423172457474.png)

#####  应用场景

单选框可以点单选框后的文字来实现点到单选框的效果

方法一

```html
<input type="radio" value="male" name="gender" checked id="man"><label for="man">男</label>
              <input type="radio" value="male" name="gender" id="women"/><label for="women">女</label><br/>
```

注意：两个id不能相同，否则无效

方法二

```html
<label ><input type="radio" value="male" name="gender" checked id="man">男</label>
              <label><input type="radio" value="male" name="gender" id="women"/>女</label><br/>
```

## 14.字符实体

![image-20220423174137528](./images\image-20220423174137528.png)

![image-20220423174239345](./images\image-20220423174239345.png)

```html
多个空格      会合并成一个
所以空格用&nbsp;就不会出现合并成一个的情况
```

# CSS

设计理念

![image-20220425014104247](./images\image-20220425014104247.png)

## 1.语法规则

![image-20220423200149352](./images\image-20220423200149352.png)

注意height，width的百分比形式是相对于父级标签的

```html
    <head>
        <style type="text/css">
            .div1{
                background-color: yellowgreen;
                height: 20%;
            }
            .div2{
                background-color: tomato;
                width: 15%;
                height: 80%;
                float: left;
            }
            .div3{
                background-color: rgb(235, 9, 255);
                width: 85%;
                height: 65%;
                float: left;
            }
            .div4{
                background-color: rgb(8, 4, 241);
                width: 85%;
                height: 15%;
                float: left;
            }
            .div5{
                background-color: rgb(8, 4, 241);
                width: 50%;
                height: 100%;
                float: left;
                border: 4px dotted rgb(32, 193, 204) ;                 
            }
            div{
                position: relative;
                /* top:20px; */
            }
            .divmain{
                width: 80%;
                height: 100%;
                margin-left: 10%;
            }
            body{
				margin:0;
				padding:0;
                background-color: antiquewhite;
			}
        </style>
        
    </head>
```

![image-20220423200342933](./images\image-20220423200342933.png)

## 2.CSS引入方式![image-20220423200424189](./images\image-20220423200424189.png)

```html
内联式在head中
外联式<link rel="stylesheet" href="路径">stylesheet表示连接的是样式表(CSS)
内联式比如在div标签里指定<div style="color:blue;background-color: aqua;font-size:30px;"></div>

```

小结

![image-20220423201227039](./images\image-20220423201227039.png)

## 基础选择器

![image-20220423201540314](./images\image-20220423201540314.png)

### 1.标签选择器

![image-20220423201628596](./images\image-20220423201628596.png)

### 2.类选择器

![image-20220423201821491](./images\image-20220423201821491.png)

```html
4.        <div class="class1 class2"></div>
5.			.class1,.class2{
                color: aqua;
            }
```

### 3.id选择器

![image-20220423202520053](./images\image-20220423202520053.png)

### 4.通配符选择器

![image-20220423202943233](./images\image-20220423202943233.png)

```html
    *{
        margin: 0;
        padding: 0;
    } 
```

## 字体和文本样式

### 字体样式

![image-20220423203757433](./images\image-20220423203757433.png)

### 1.文字大小

![image-20220423203843981](./images\image-20220423203843981.png)

### 2.字体粗细

![image-20220423204407710](./images\image-20220423204407710.png)

###  3.字体倾斜

![image-20220423204742292](./images\image-20220423204742292.png)

### 4.字体系列font-family

![image-20220423205220909](./images\image-20220423205220909.png)

![image-20220423205320005](./images\image-20220423205320005.png)

![image-20220423205722796](./images\image-20220423205722796.png)

### 字体font相关属性连写

![image-20220423231842102](./images\image-20220423231842102.png)

```html
        font: italic 400 30px 宋体;
	    font:  400 30px 宋体;	
		font: 30px 宋体;
```

### 文本样式

### 1.文本缩进

![image-20220423232748622](./images\image-20220423232748622.png)

![image-20220423232856084](./images\image-20220423232856084.png)

```html
text-indent: 20px;缩进20像素
text-indent: 2em;缩进2个font-size的像素
```

### 2.文本水平对齐

![image-20220423233349959](./images\image-20220423233349959.png)

![image-20220423233527868](./images\image-20220423233527868.png)

```html
  body{
        text-align: center;
    }
```

### 3.文本修饰

![image-20220423233929779](./images\image-20220423233929779.png)

![image-20220423234100042](./images\image-20220423234100042.png)

text-decoration: none;一般用于超链接(超链接默认有下划线)使其没有下划线

### 4.行高

![image-20220423234454369](./images\image-20220423234454369.png)

```html
font: italic 400 16px 宋体;默认行高为1
font: italic 400 16px/2 宋体;这样设置了行高为2
```

## Crome调试工具

![image-20220424002028465](./images\image-20220424002028465.png)

在浏览器调试界面点击数字按上下键可以调整值。点击数字后按tab可以扩充css语句。

![image-20220424002156757](./images\image-20220424002156757.png)

删除线表示属性值被覆盖

在浏览器调不会影响源码

## 颜色

![image-20220424002541194](./images\image-20220424002541194.png)

## 样式折叠问题

![image-20220423205850786](./images\image-20220423205850786.png)

![image-20220423205958381](./images\image-20220423205958381.png)

## 扩展

![image-20220424122116874](./images\image-20220424122116874.png)

div的盒子模型上下没有距离

原理后面讲

## 选择器进阶

![image-20220424135207866](./images\image-20220424135207866.png)

### 1.后代选择器



![image-20220424141626511](./images\image-20220424141626511.png)

所有选择器都支持包括id和类选择器

![image-20220424141751026](./images\image-20220424141751026.png)

### 2.子代选择器

![image-20220424141816931](./images\image-20220424141816931.png)

![image-20220424141942312](./images\image-20220424141942312.png)

### 3.并集选择器

![image-20220424142018334](./images\image-20220424142018334.png)

### 4.交集选择器

![image-20220424142430211](./images\image-20220424142430211.png)

![image-20220424142506885](./images\image-20220424142506885.png)

### 5.hover伪类选择器

![image-20220424142603578](./images\image-20220424142603578.png)

![image-20220424142824439](./images\image-20220424142824439.png)

### 6.属性选择器

[value]{

}

选择所有value的值

## emmet语法

![image-20220424143004593](./images\image-20220424143004593.png)

![image-20220424143408640](./images\image-20220424143408640.png)

![image-20220424143537411](./images\image-20220424143537411.png)

![image-20220424143710757](./images\image-20220424143710757.png)

![image-20220424143942254](./images\image-20220424143942254.png)

## 背景

![image-20220424144043383](./images\image-20220424144043383.png)

### 1.背景颜色

![image-20220424144058572](./images\image-20220424144058572.png)

### 2.背景图片

![image-20220424144357282](./images\image-20220424144357282.png)

### 3.背景平铺

![image-20220424144743163](./images\image-20220424144743163.png)

![image-20220424144930185](./images\image-20220424144930185.png)

背景和背景图片是两个东西，遵循css重叠规则

### 4.背景位置

![image-20220424145318198](./images\image-20220424145318198.png)

![image-20220424145940006](./images\image-20220424145940006.png)

### 5.背景属性连写

### ![image-20220424155312093](./images\image-20220424155312093.png)

![image-20220424160053431](./images\image-20220424160053431.png)

### 6.img标签和背景图片的区别

![image-20220424160743762](./images\image-20220424160743762.png)

img一般用于重要图片，背景图一般不重要图片

### 7.背景图片大小

![image-20220428142640883](./images\image-20220428142640883.png)

只写一个属性默认为宽

![image-20220428143812396](./images\image-20220428143812396.png)

![image-20220428143656787](./images\image-20220428143656787.png)

## 元素显示模式

![image-20220424161000306](./images\image-20220424161000306.png)

可以用w+h+bgc的表现来确定标签的元素显示模式

### 1.块级元素

![image-20220424161037175](./images\image-20220424161037175.png)

![image-20220424162153817](./images\image-20220424162153817.png)

特性：

1.每个块级元素都是独自占一行。 

2.元素的高度、宽度、行高和边距都是可以设置的。   

3.元素的宽度如果不设置的话，默认为父元素的宽度（父元素宽度100%）。***块元素可以继承父元素的宽，但高不可以继承，可设置块元素的宽或者由内容撑开\***

4.块级元素可以设置margin,padding属性（注意行内块元素和行内元素在用padding的时候，其父元素最好设置padding:0px;margin:0px;不设置有可能会没有效果）



元素类型可以通过display转换

块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p

#### 额外注意：

行级元素只能嵌套行级元素、块级元素可以嵌套任何元素

**特殊的: p标签不能嵌套div、a标签不能套a标签**

### 2.行内元素

![image-20220424161824552](./images\image-20220424161824552.png)



![image-20220424163745927](./images\image-20220424163745927.png)

### 3.行内块元素

![image-20220424162348240](./images\image-20220424162348240.png)

行内块元素注意的问题：

***行内块元素默认对齐方式是基线对齐 verticle-align:base-line***

对于一个inline-block行内块元素，如果内部没有inline内联元素，或者overflow不是visible，则该元素的基线就是它margin的底边缘。

解决方法

方法1：加 verticle-align: top / middle / bottom**

给盒子加上verticle-align就好了

方法2：添加浮动：float ，只是浮动脱离标准流，不那么好控制**

方法3: 添加内容（字符串等内容）容就好

**不设置宽高的话由内容撑开，可以指设计一个宽高，另外一个属性由内容撑开**

### 4.元素显示模式转换

![image-20220424163452501](./images\image-20220424163452501.png)

#### HTML嵌套模式注意点

![image-20220424164233749](./images\image-20220424164233749.png)

![image-20220424164223822](./images\image-20220424164223822.png)

## css特性

### 1.继承

![image-20220424171026915](./images\image-20220424171026915.png)

![image-20220424171424395](./images\image-20220424171424395.png)

![image-20220424171806287](./images\image-20220424171806287.png)

默认：不继承

“display、border、margin和padding属性是不继承的。 在所编写的规则中使用inherit的特殊值的话,可以让border、margin和padding被继承,但是display除外。”

### 2.层叠性

![image-20220424171838221](./images\image-20220424171838221.png)

### 3.优先级

#### a.优先级的基本使用

![image-20220424223206082](./images\image-20220424223206082.png)

![image-20220424224030445](./images\image-20220424224030445.png)

![image-20220424224039983](./images\image-20220424224039983.png)

#### b.权重叠加运算

![image-20220424232250432](./images\image-20220424232250432.png)

![image-20220424232236420](./images\image-20220424232236420.png)

![image-20220424224325295](./images\image-20220424224325295.png)

  ![image-20220424232202467](./images\image-20220424232202467.png)

![image-20220424232141552](./images\image-20220424232141552.png)

### 浏览器排错

对于一个标签如果设置的style没生效，那么进去浏览器中找到这个标签，查看该标签有没有style设置，如果没有那么则是源码中style中有语法错误。

上一行出错下一行也会收到影响

部分效果生效说明没生效的代码出了问题  ，可能使用了中文标点

### PxCook的基本使用

psd文件用开发模式打开会生成很多信息。设计模式可以使用尺子量像素，吸管吸颜色

### 盒子模型

#### 内减模式

可以省去计算盒子所占的大小在style内设置  box-sizing: border-box;

![image-20220425001712771](./images\image-20220425001712771.png)

#### 1.盒子模型介绍

![image-20220425000500628](./images\image-20220425000500628.png)

![image-20220425001301056](./images\image-20220425001301056.png)

#### 2.内容区域的宽度和高度

![image-20220425001741324](./images\image-20220425001741324.png)

#### 3.边框(border)

![image-20220425001945362](./images\image-20220425001945362.png)

![image-20220425002425799](./images\image-20220425002425799.png)

![image-20220425002457848](./images\image-20220425002457848.png)

![image-20220425002633868](./images\image-20220425002633868.png)

![image-20220425002643631](./images\image-20220425002643631.png) 

某一个方向

![image-20220425002816642](./images\image-20220425002816642.png)

![image-20220425003107909](./images\image-20220425003107909.png)

#### 新浪微博导航案例

![image-20220425003555974](./images\image-20220425003555974.png)

![image-20220425004740079](./images\image-20220425004740079.png)

#### 4.内边距(padding)

![image-20220425005355171](./images\image-20220425005355171.png)

![image-20220425005555118](./images\image-20220425005555118.png)

4.5CCS3盒子模型

![image-20220425010133645](./images\image-20220425010133645.png)

![image-20220425010310001](./images\image-20220425010310001.png)

#### 5.外边距(margin)

和内边距设置方式一样

#### 6.清除默认内外边距

![image-20220425011125058](./images\image-20220425011125058.png)

![image-20220425011310618](./images\image-20220425011310618.png)

版芯居中

设置magin: 0 auto;auto表示左右的值相等，导致了居中

#### 7.外边距折叠现象

##### a.合并现象

![image-20220425014234008](./images\image-20220425014234008.png)

##### b.塌陷现象

![image-20220425014731922](./images\image-20220425014731922.png)

推荐使用overflow：hidden

##### c.行内元素的垂直内外边距

![image-20220425015952433](./images\image-20220425015952433.png)

可使用line_height来实现垂直内外边距的效果

### css浮动

#### 1.结构伪类基本用法

![image-20220425141142729](./images\image-20220425141142729.png)

![image-20220425144344285](./images\image-20220425144344285.png)

#### 2.结构伪类公式

![image-20220425144838407](./images\image-20220425144838407.png)

#### 3.伪元素

![image-20220425144951166](./images\image-20220425144951166.png)

![image-20220425150612538](./images\image-20220425150612538.png)

#### 3.标准流

![image-20220425150918820](./images\image-20220425150918820.png)

![image-20220425152121624](./images\image-20220425152121624.png)

浏览器解析行内块或行内标签的时候，如果标签换行书写会产生一个空格的距离

#### 4.浮动的作用和特点

![image-20220425184646339](./images\image-20220425184646339.png)

![image-20220425184522817](./images\image-20220425184522817.png)

如果不想顶对齐可以设置外边距margin——top。

![image-20220425184700051](./images\image-20220425184700051.png)

![image-20220425190931408](./images\image-20220425190931408.png)

#### ![image-20220425193928957](./images\image-20220425193928957.png)

#### 脱标

脱标具有行内块的特点可以设置宽高，并由内容撑开

#### 导航栏

主导航是li>a结构

#### 5.清除浮动

![image-20220425212757604](./images\image-20220425212757604.png)

##### a.浮动带来的影响

![image-20220425213655122](./images\image-20220425213655122.png)

父子级标签，子级浮动，父级没有高度，后面的标准流盒子会受影响

##### b.清楚浮动的方法

###### i.直接设置父元素的高度

![image-20220425214053035](./images\image-20220425214053035.png) 

###### ii.额外标签法

![image-20220425214440641](./images\image-20220425214440641.png)

###### iii.单伪元素清除法

![image-20220425224150937](./images\image-20220425224150937.png)

![image-20220425224135294](./images\image-20220425224135294.png)

###### iv.双伪元素清除法

![image-20220425224820977](./images\image-20220425224820977.png)

![image-20220425224632398](./images\image-20220425224632398.png) 

before设置元素模式为table不是块级元素所以不会发生外边距塌陷



# 项目实战

一般设计思路

![image-20220426013156359](./images\image-20220426013156359.png)

## 1.准备工作

项目根目录包含img，css文件夹和index.html

index.html是首页,名字唯一，不然服务器找不到。

整个路径必须为英文，因为服务器不支持中文

## 2.版心和清除默认样式

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/*版心*/
.wrapper {
    width: 1200px;
    margin: 0 auto;
}

a {
    text-decoration: none;
}

li {
    list-style: none;
}

.clearfix::before::after {
    display: table;
    content: '';
}

.clearfix::after {
    clear: both;
}

body {
    background-color: #f3f5f7;
}
```

## 3.head布局

```css
.header {
    background-color: red;
    height: 42px;
    /* margin-top: 30px;
    margin-bottom: 30px; */
    margin: 30px auto;
}
```

## 4.logo和nav布局

```css
.logo {
    width: 198px;
    height: 42px;
    margin-right: 79px;
    float: left;
}

.headerNavigate {
    /* width: 237px; */
    height: 18px;/*对于文字可以不设置宽，浮动后会自动延长*/
    background-color: black;
    margin: 12px 0;

    float: left;
}

.headerNavigate li {

    display: inline-block;
}
<div class="header wrapper">
        <img src="./imgs/logo.png" alt="学成在线" class="logo">
        <div class="headerNavigate">
            <li><a href="#">课程</a></li>
            <li><a href="#">首页</a></li>
            <li><a href="#">职业规划</a></li>
        </div>


    </div>
```

5.nav布局完成

```css
.nav li {
    /* width: 54px; */
    margin-right: 45px;
    padding: 0 9px;
    display: inline-block;
}
.nav li:hover{
    border-bottom: 2px solid #00a4ff;
}

.nav li:last-child{
    margin-right: 0;
}
```

![image-20220426145707335](./images\image-20220426145707335.png)

## 4.布局和文本框

![image-20220426154420038](./images\image-20220426154420038.png)

```css

.search{
    float: left;

    width: 412px;
    height: 40px;
    margin-left: 94px;
    /* border: 1px solid red; */
    
}

.searchText{
    float: left;

    width: 362px;
    height: 40px;
    border-top: 1px solid blue;
    border-left: 1px solid blue;
    border-bottom: 1px solid blue;
    border-right: none;
    padding: 12px 21px;
    padding-right: 0px;
}
/*/如果想控制placehodlder那么样式为*/
.searchText ::placeholder{
    font-size: 16px;
    color: #bfbfbf;
    font-family: MicrosoftYaHei;
    font-weight: 400;
}
.searchImg{
 float: left;
}
```

## 5.按钮

```css
//装饰性的图片用背景图
.searchImg{
 float: left;

 width: 50px;
 height: 40px;
 background-image: url(../imgs/btn.png);

 border: none;
}
```

## 6.用户

![image-20220426161805393](./images\image-20220426161805393.png)

```css
.user{
    float: right;

    margin-right: 35px;
    text-align: center;
    /* margin-top: 35px; */
    /* margin-bottom: 35px; */
    height: 42px;
}
.user img{
    /* 调节图片垂直对齐方式, middle:居中 */
    vertical-align: middle;
}
.user span{
    display: inline-block;
    line-height: 42px;
}
```

```html
    <!-- 用户 -->
        <div class="user">
            <img src="./imgs/user.png" alt="">
            <span>用户名</span>
        </div>
```

项目不做笔迹了。

# css定位

![image-20220427150010626](./images\image-20220427150010626.png)

## 1.网页的常见布局模式

![image-20220427150242025](./images\image-20220427150242025.png)

## 2.定位的常见场景

![image-20220427150310319](./images\image-20220427150310319.png)

## 3.定位的基本使用

![image-20220427150354966](./images\image-20220427150354966.png)

![image-20220427150436656](./images\image-20220427150436656.png)

## 4.相对定位

![image-20220427150744653](./images\image-20220427150744653.png)

![image-20220427151738119](./images\image-20220427151738119.png)

![image-20220427151643009](./images\image-20220427151643009.png)

![image-20220427151721217](./images\image-20220427151721217.png)

![image-20220427152135295](./images\image-20220427152135295.png)

## 5.绝对定位

![image-20220427152648815](./images\image-20220427152648815.png)

![image-20220427152638641](./images\image-20220427152638641.png)

![image-20220427153256834](./images\image-20220427153256834.png)

实现圈中窗口，可以使用绝对定位，而他的父级一般使用相对定位，因为绝对定位要有已经定位的父级，才会相对于父级的位置改变，不然是相对于浏览器的位置改变

![image-20220427154527597](./images\image-20220427154527597.png)

## 6.居中

### 方法1：

![image-20220427162149042](./images\image-20220427162149042.png)

```css
    <style>
        div{ 
            position: absolute  ;
            left: 50%;
            margin-left: -150px;
            /* margin: 0 auto; */
            top: 50%;
            margin-top: -150px;
            width: 300px;
            height: 300px;
            background-color: pink;
        }
    </style>
```

### 方法2：

```css
    <style>
        div{ 
            position: absolute  ;
            left: 50%;
            /* margin-left: -150px; */
            /* margin: 0 auto; */
            top: 50%;
            /* margin-top: -150px; */
            transform: translate(-50%,-50%);
            width: 300px;
            height: 300px;
            background-color: pink;
        }
    </style>
```

tranform:translate(x,y)移动x,y距离，以自己为参照物

## 7.固定定位

![image-20220427171737846](./images\image-20220427171737846.png)

![image-20220427172000355](./images\image-20220427172000355.png)

## 8.元素层级问题

![image-20220427173035561](./images\image-20220427173035561.png)

![image-20220427173340448](./images\image-20220427173340448.png)

z-index:相当于权重，谁大谁在上面

无论是否是不是其他元素的子级，只要有定位，按定位的标准看

# css装饰

![image-20220427173517994](./images\image-20220427173517994.png)

## 1.了解基线

![image-20220427173750666](./images\image-20220427173750666.png)

对于浏览器行内块和行内元素默认和文字一样的规则底部基线对齐

## 2.文字对齐问题

![image-20220427173916656](./images\image-20220427173916656.png)

## 3.垂直对齐模式

![image-20220427174016430](./images\image-20220427174016430.png)

![image-20220427174319588](./images\image-20220427174319588.png)

vertical-align属性介简单介绍一下：

设置垂直居中（使用场景，最少两种）

vertical-align：top     把元素的顶端与行中最高元素的顶端对齐

middle  把此元素放置在父元素的中部。

bottom  使元素及其后代元素的底部与整行的底部对齐。

%:元素的baseline移动到行盒baseline的%(以line-height做计算)

px:元素的baseline移动到行盒baseline的绝对长度，可以负数 

[CSS vertical-align 属性 (w3school.com.cn)](https://www.w3school.com.cn/cssref/pr_pos_vertical-align.asp)

## 4.光标类型

![image-20220428030021935](./images\image-20220428030021935.png)

![image-20220428030400392](./images\image-20220428030400392.png)

## 5.圆角边框（radius）

![image-20220428031000522](./images\image-20220428031000522.png)

![image-20220428030849704](./images\image-20220428030849704.png)

![image-20220428031306373](./images\image-20220428031306373.png)

![image-20220428031227125](./images\image-20220428031227125.png)

## 6.溢出显示效果(overflow)

​	![image-20220428031409887](./images\image-20220428031409887.png)

## 7.显示隐藏

![image-20220428031938527](./images\image-20220428031938527.png)

![image-20220428031858448](./images\image-20220428031858448.png)

## 8.元素整体透明度

![image-20220428032224251](./images\image-20220428032224251.png)

## 9.盒子阴影

![image-20220428143924379](./images\image-20220428143924379.png)

![image-20220428144315660](./images\image-20220428144315660.png)

## 10.过渡

![image-20220428145100992](./images\image-20220428145100992.png)

![image-20220428145032669](./images\image-20220428145032669.png)

## 11.骨架

### DOCTYPE

![image-20220428160656174](./images\image-20220428160656174.png)

![image-20220428160719751](./images\image-20220428160719751.png)

## 网页语言

![image-20220428161414916](./images\image-20220428161414916.png)

## 字符编码

![image-20220428163700511](./images\image-20220428163700511.png)

## SEO

![image-20220428200931301](./images\image-20220428200931301.png)

![image-20220428201009363](./images\image-20220428201009363.png)

## ICO图标设置

![image-20220428201206530](./images\image-20220428201206530.png)

![image-20220428201450029](./images\image-20220428201450029.png)

# 小兔鲜项目

## 1.精灵图

![image-20220428141710264](./images\image-20220428141710264.png)

精灵图使用步骤

![image-20220428141821632](./images\image-20220428141821632.png)

![image-20220428142517906](./images\image-20220428142517906.png)

## 2.项目结构搭建

![image-20220428202733784](./images\image-20220428202733784.png)

![image-20220429022858472](./images\image-20220429022858472.png)

# CSS进阶

## 1.字体图标

下载iconfont文件夹引入项目，引入iconfont文件夹中的css文件

使用时用如下格式

```html
<i class="iconfont icon-QRcode">二维码</i>
```

iconfont固定 后面的从iconfont中的demo文件找类名引入

iconfont固定原因![image-20220430183938657](./images\image-20220430183938657.png)

iconfont引入了字体之后才可引用后面他自己的字体类名

改字号和属性

```html
.iconfont{
font-size:60px;
}
```

不能使用标签因为类选择器的权重大于标签选择器

## 2.购物车

![image-20220430194958475](./images\image-20220430194958475.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./iconfont/iconfont.css">
    <style>
        .icon-cart-Empty-fill{
            color: #f40;
        
        }  
        li  {
                list-style: none;
            }
        a{
            text-decoration: none;
        }
    </style>
</head>
<body>
        <ul>
            <li><a href="">
                <span class="iconfont icon-cart-Empty-fill"></span>
                <span>购物车</span>
                <span class="iconfont icon-arrow-down"></span></a></li>
        </ul>
</body>
</html>
```

## 3.svg图标上传

![image-20220430195433650](./images\image-20220430195433650.png)

iconfont.cn网站上传

## 4.平面转换

![image-20220430200730390](./images\image-20220430200730390.png)

![image-20220430201048185](./images\image-20220430201048185.png)

### 1.位移

![image-20220430201327920](./images\image-20220430201327920.png)

![image-20220430201416605](./images\image-20220430201416605.png)

### 2.旋转

![image-20220430210802835](./images\image-20220430210802835.png)



![image-20220430210903356](./images\image-20220430210903356.png)

#### 转换原点

![image-20220430211344724](./images\image-20220430211344724.png)

![image-20220430211736725](./images\image-20220430211736725.png)

### 3.多重转换

![image-20220430212229063](./images\image-20220430212229063.png)

### 4.缩放

![image-20220430212705926](./images\image-20220430212705926.png)

缩放重中心点放大

普通的改变宽高是从坐标轴放大

![image-20220430214023911](./images\image-20220430214023911.png)

### 5.渐变

![image-20220430214607277](./images\image-20220430214607277.png)

![image-20220430215048142](./images\image-20220430215048142.png)

### 6.空间转换

![image-20220501124554584](./images\image-20220501124554584.png)

##### 空间位移

![image-20220501124755883](./images\image-20220501124755883.png)

![image-20220501125259014](./images\image-20220501125259014.png)

##### 透视

![image-20220501125603222](./images\image-20220501125603222.png)

![image-20220501125616091](./images\image-20220501125616091.png)

![image-20220501130150187](./images\image-20220501130150187.png)

##### 空间旋转

![image-20220501130937967](./images\image-20220501130937967.png)

rotateZ效果类似于平面旋转

3d效果父级都应该加透视

![image-20220501131518972](./images\image-20220501131518972.png)

![image-20220501131737259](./images\image-20220501131737259.png)

##### 立体呈现

![image-20220501132307939](./images\image-20220501132307939.png)

##### 3d导航

![image-20220501133603583](./images\image-20220501133603583.png)

##### 空间缩放

![image-20220501140926549](./images\image-20220501140926549.png)

### 7.动画

![image-20220501142848336](./images\image-20220501142848336.png)

![image-20220501143333660](./images\image-20220501143333660.png)

![image-20220501161950770](./images\image-20220501161950770.png)

#### from to

![image-20220501162636976](./images\image-20220501162636976.png)

#### 百分比

![image-20220501163059079](./images\image-20220501163059079.png)

#### 动画属性

![image-20220501163149745](./images\image-20220501163149745.png)

![image-20220501165032062](./images\image-20220501165032062.png)

![image-20220501165446193](./images\image-20220501165446193.png)

![image-20220501215614309](./images\image-20220501215614309.png)

#### 逐帧动画

![image-20220501215847998](./images\image-20220501215847998.png)

![image-20220501220203617](./images\image-20220501220203617.png)

#### 无缝走马灯

![image-20220501233149884](./images\image-20220501233149884.png)

要复制前面的图才会有无缝的效果

#### 多组动画

![image-20220501223550815](./images\image-20220501223550815.png)

![image-20220501224152315](./images\image-20220501224152315.png)

动画的开始状态和默认状态相同，可以省略from只写一个to

#### 复合属性

![image-20220501164332685](./images\image-20220501164332685.png)

![image-20220501164822722](./images\image-20220501164822722.png)

### 8.设置背景大图

```css
*{
    margin: 0;
    padding: 0;
}
html{
    height: 100%;
}
body{
    height: 100%;
    background-image: url(../imgs2/f1_1.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center 0;
}
```

html高设为100%后body才可以继承高度

### 9.电脑网页和手机网页的不同

![image-20220502123541658](./images\image-20220502123541658.png)

### 10.浏览器模拟器

### 11.分辨率

![image-20220502130433000](./images\image-20220502130433000.png)

![image-20220502130450613](./images\image-20220502130450613.png)

![image-20220502130753085](./images\image-20220502130753085.png)

![image-20220502131259244](./images\image-20220502131259244.png)

### 12.视口

视口标签

规定html的宽度

没有视口标签手机端默认宽度980px，电脑端默认和逻辑分辨率一致

```html
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### 13.百分比布局

![image-20220502135605067](./images\image-20220502135605067.png)

![image-20220502135837082](./images\image-20220502135837082.png)

### 14.flex布局

![image-20220502143642370](./images\image-20220502143642370.png)

![image-20220502143828297](./images\image-20220502143828297.png)

![image-20220502145042204](./images\image-20220502145042204.png)

![image-20220502145325043](./images\image-20220502145325043.png)

![image-20220502145532118](./images\image-20220502145532118.png)

#### 主轴对齐方式



![image-20220502145810538](./images\image-20220502145810538.png)

![image-20220502145831066](./images\image-20220502145831066.png)

##### center

![image-20220502150056924](./images\image-20220502150056924.png)

##### between

![image-20220502150121100](./images\image-20220502150121100.png)

##### evenly

![image-20220502150227380](./images\image-20220502150227380.png)

##### around

![image-20220502150315671](./images\image-20220502150315671.png)

#### 侧轴对齐模式

![image-20220502151133513](./images\image-20220502151133513.png)

![image-20220502151333336](./images\image-20220502151333336.png)

![image-20220502151939843](./images\image-20220502151939843.png)

盒子如果不拉伸具有行内块特点，宽高由内容撑开，如果拉伸了，宽由内容撑开，高拉伸至父级    

#### 伸缩比

![image-20220502153607679](./images\image-20220502153607679.png)

#### 主轴方向

![image-20220503142942100](./images\image-20220503142942100.png)

![image-20220503143320525](./images\image-20220503143320525.png)

#### 弹性盒子换行

![image-20220503143905732](./images\image-20220503143905732.png)

![image-20220503143808458](./images\image-20220503143808458.png)

## 移动适配

![image-20220504190732263](./images\image-20220504190732263.png)

### rem

![image-20220504192335169](./images\image-20220504192335169.png)

百分比布局之前一定要设置一个高，否则后面的元素都没有高度，故不能进行移动适配 	

![image-20220504193135572](./images\image-20220504193135572.png)

### 媒体查询

![image-20220504195607546](./images\image-20220504195607546.png)

![image-20220504195823763](./images\image-20220504195823763.png)![image-20220504195823626](./images\image-20220504195823626.png)

![image-20220504202616994](./images\image-20220504202616994.png)

### flexible

![image-20220504204117222](./images\image-20220504204117222.png)

### less语法

![image-20220504204322941](./images\image-20220504204322941.png)

```less
.father{
    width: (95/35.5) rem;
    background-color: red;
    .son{
        width: (40/35.5) rem;
        background-color: pink;
    }
}
```



由上面的less语法生成下面的css语法

```css
.father {
  width: 2.67605634 rem;
  background-color: red;
}
.father .son {
  width: 1.12676056 rem;
  background-color: pink;
}
s
```



![image-20220504204837496](./images\image-20220504204837496.png)

![image-20220504204921646](./images\image-20220504204921646.png)

#### 注释

![image-20220504205544705](./images\image-20220504205544705.png)

#### 加减乘除

![image-20220504210127511](./images\image-20220504210127511.png)

```less
.oo{
    width: 120+50px;
    height: 150-80px;
    background-color: red;
}
.o1{
    width: 100*5px;
    height: (100/5rem);
    background-color: pink;
}
```

#### 嵌套

![image-20220504211205558](./images\image-20220504211205558.png)

![image-20220504211254579](./images\image-20220504211254579.png)

```less
.father{
    width: (95/35.5rem);
    background-color: red;
    .son{
        width: (40/35.5rem);
        background-color: pink;
        &:hover{
            width: 40rem;
        }
    }
}
```

&表示**当前选择器**,上面less生成

```css
.father {
  width: 2.67605634rem;
  background-color: red;
}
.father .son {
  width: 1.12676056rem;
  background-color: pink;
}
.father .son:hover {
  width: 40rem;
}

```

#### 变量

![image-20220504212321679](./images\image-20220504212321679.png)

变量可以带单位，比如:37.5rem

方便批量修改

#### 导入less文件

![image-20220504214801411](./images\image-20220504214801411.png)

#### 导出

##### 方法一

![image-20220504215041683](./images\image-20220504215041683.png)

在less"less.compile": {}中加 "out":"导出路径"

```json
{
    "workbench.colorTheme": "Visual Studio Dark - C++",
    "editor.suggestSelection": "first",
    "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
    "files.exclude": {
        "**/.classpath": true,
        "**/.project": true,
        "**/.settings": true,
        "**/.factorypath": true
    },
    "security.workspace.trust.untrustedFiles": "open",
    "code-runner.runInTerminal": true,
    "files.autoSaveDelay": 500,
    "files.autoSave": "afterDelay",
    "explorer.confirmDragAndDrop": false,
    "explorer.confirmDelete": false,
    "less.compile": {
        "out": "../css/"
    }
}
```

##### 方法二

在less文件第一行加

```less
// out:导出路径
```

注意没有引号

#### 禁止导出

![image-20220504220338382](./images\image-20220504220338382.png)

### VW/VH

使用px转换时，假如是x单位的像素，那么写的时候为 （x/视口的一百分之一vh）vh要在括号内部，不然识别不了

![image-20220505124545419](./images\image-20220505124545419.png)

![image-20220505130046893](./images\image-20220505130046893.png)

![image-20220505130210077](./images\image-20220505130210077.png)

### 媒体查询min-width max-width

![image-20220506141136440](./images\image-20220506141136440.png)

![image-20220506141921081](./images\image-20220506141921081.png)

![image-20220506141152020](./images\image-20220506141152020.png)

#### 书写顺序

![image-20220506141956885](./images\image-20220506141956885.png)

![image-20220506141851325](./images\image-20220506141851325.png)

#### 完整写法

![image-20220506142112453](./images\image-20220506142112453.png)

![image-20220506142213007](./images\image-20220506142213007.png)

#### 媒体类型

![image-20220506142305914](./images\image-20220506142305914.png)

#### 媒体特征

 ![image-20220506142333303](./images\image-20220506142333303.png)

#### 外链css引入

![image-20220506142825360](./images\image-20220506142825360.png)

![image-20220506143245056](./images\image-20220506143245056.png)

#### 媒体隐藏

![image-20220506144214525](./images\image-20220506144214525.png)

### BootStrap

![image-20220506150040887](./images\image-20220506150040887.png)

#### 使用步骤

![image-20220506151838949](./images\image-20220506151838949.png)

#### 栅格系统

![image-20220506152901538](./images\image-20220506152901538.png)

![image-20220506153156499](./images\image-20220506153156499.png)

![image-20220506153737481](./images\image-20220506153737481.png)

![image-20220506162401381](./images\image-20220506162401381.png)s

![image-20220506162328821](./images\image-20220506162328821.png)

#### css全局样式

进官网里有案例

#### 组件

![image-20220506201241164](./images\image-20220506201241164.png)	

#### 字体图标

![image-20220506214631594](./images\image-20220506214631594.png)

类名在官网复制

#### 插件使用

![image-20220506220245760](./images\image-20220506220245760.png)

#### 下拉菜单

```html
    <div class="dropdown">
        <a id="dLabel" data-target="#" href="http://example.com/" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">
        Dropdown trigger
        <span class="caret"></span>
        </a>
    
        <ul class="dropdown-menu" aria-labelledby="dLabel">
            <li>选项1</li>
            <li>选项1</li>
            <li>选项1</li>
        </ul>
    </div>

    <script src="./js/jquery.js"></script>
    <script src="./lib/bootstrap-3.4.1-dist/bootstrap-3.4.1-dist/js/bootstrap.min.js"></script>
```

## gird流布局

![image-20220805104430041](D:\BaiduNetdiskDownload\学习笔记\java\java笔记\javaTyporeImgs\image-20220805104430041.png)

### 基本语法

```css
        .gird{
            display: grid;
            width: 600px;
            grid-template-columns: 1fr 1fr 1fr;/*对于列宽，父级剩余宽度按fr比例划分*/
            grid-template-columns: 100px 100px 100px;/*固定子元素宽度*/
            grid-template-rows: 100px 100px 100px;/*对于行高*/
            align-items: center;/*让子元素在grid一列的竖直方向居中*/
            justify-items: center;/*让子元素在grid一列的水平方向居中*/
            align-content: center;/*让gird的xy轴在盒子内居中对齐*/
            justify-content: center;/*让gird的xy轴在盒子内垂直对齐*/
            column-gap: 10px;/*列间距*/
            row-gap: 10px;/*行间距*/
        }
```



### 流式区域布局

![image-20220805110420593](D:\BaiduNetdiskDownload\学习笔记\java\java笔记\javaTyporeImgs\image-20220805110420593.png)

![image-20220805110524701](D:\BaiduNetdiskDownload\学习笔记\java\java笔记\javaTyporeImgs\image-20220805110524701.png)

## 自定义css属性

[使用 CSS 自定义属性（变量） - CSS（层叠样式表） | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Using_CSS_custom_properties)

## :root

[:root - CSS（层叠样式表） | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:root)

### 更改全局样式

![image-20220813090259365](D:\BaiduNetdiskDownload\学习笔记\java\java笔记\javaTyporeImgs\image-20220813090259365.png)

![image-20220813090916782](D:\BaiduNetdiskDownload\学习笔记\java\java笔记\javaTyporeImgs\image-20220813090916782.png)
