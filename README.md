# css-review
重读《css权威指南》
## 知识点梳理
#### 第一章
1. `@import`必须放在style容器中，必须放在其他css规则之前，否则不起作用。
2. `@import`可以限制所导入的样式表应用于一种活或种媒体，如：

	> @import url(sheet2.css) all;
	> @import url(blueworld.css) screen;
	> @import url(zany.css) projection, print;
	
#### 第二章
1. 将同时有`href`和`title`属性的HTML超链接的文本设置为粗体，可以写作：

	> a[href][title] { font-weight: blod; }

2. 根据部分属性值选择：
	
	> p[class~="warning"] { font-weight: bold; }
	> img[title~="Figure"] { border: 1px solid gray; }
	
	`~`是关键，即根据属性值中出现的一个用空格分隔的词来完成选择，不需要完全匹配
	
3. 根据语言选择：
	
	> *:lang(fr) { font-style: italic; }
	
4. 结合伪类：

	> a:link:hover { color: red; }
	> a:visited:hover { color: maroon; }
	
5. 设置首字母样式：

	> p:first-letter { color: red; font-size: 200%; }
	
6. 设置第一行的样式：

	> p:first-line { color: purple; }
	
#### 第五章
1. font属性可以用很宽松的方式来指定。font-style、font-weight和font-variant这三个属性值可以按任何顺序来写。此外，如果其中某个属性的值为normal，则可以忽略。而后两个属性值font-size和font-family不仅要以此顺序（font-size在前，font-family在后）作为声明中的最后两个值，而且font声明中必须有这两个值。
2. font可以设置line-height，font-size的值必须要在line-height之前，而且这两个属性总要有`“/”`分割。

#### 第六章
1. `text-align`不会控制元素的对齐，而只影响其内部内容。`justify`两端对齐，文本行的左右两端都放在副元素的内边界上，然后，调整单词和字母间的间隔，使各行的长度恰好相等。
2. `vertical-align`不影响块级元素中内容的对齐。不过，可以用它来影响表单元格中元素的垂直对齐。

#### 第七章
1. 如果正常流中一个块元素的`margin-top`或`margin-bottom`设置为au会自动计算为0。遗憾的是，如果值为0，就不能很容易地将正常流元素在其包含块中垂直居中。
2. 如果块级正常流元素的高度设置为auto，而且只有块级子元素，其默认高度将是从最高块级子元素的外边框边界到最低块级子元素外边框之间的距离。因此，子元素的外边距会超出包含这些子元素的元素。不过，如果块级元素有上内边距或下内边距，或者有上边框或下边框，其高度则是从其最高子元素的上外边距边界到其最低子元素的下外边距边界之间的距离。
3. `display: run-in`使某些块级元素成为下一个元素的行内部分。如果一个元素生成`run-in`框，而且该框后面是一个块级框，那么该run-in元素将成为块级框开始处的一个行内框。只有当`run-in`框后面是一个块级框时`run-in`才起作用。如果不是这样，`run-in`框本身将成为块级框。

#### 第八章
1. 元素内边距的百分值是相对于其父元素的width计算，上下内边距与左右内边距一致，也是相对于宽度计算而不是相对于高度。

#### 第十章
1. rect(...)只接受长度单位和auto，不接受百分数单位。
2. visibility属性可以继承，要想将一个hidden元素的后代元素可见，必须显式地声明后代元素为visible。
3. 


