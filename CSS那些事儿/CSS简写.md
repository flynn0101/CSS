**内外补丁**根据上右下左的顺时针方向可以罗列以下四种简写方式：

```
property：value1； 表示所有边都是一个值 value 。
property：value1  value2； 表示 top 和 bottom 的值是 value1，right 和 left 的值是 value2 。
property：value1  value2  value3；表示 top 的值是 value1，right 和 left 的值是 value2，
                                  bottom 的值是 value3 .
property：value1  value2  value3  value4； 表示 top 的值是 value1，right 的值是 value2，
                                           bottom 的值是 value3，left的值是 value4 。
```

**边框属性**

```
div {
border-width:1px; /*定义边框大小为1px*/
border-style:solid; /*定义边框样式为实线*/
border-color:#FF0000; /*定义边框颜色为红色*/
}
/*简写为*/
div {border:1px solid #FF0000;}
```

 **背景简写**

```
body {
background-color:#FF0000; /*背景定义为红色*/
background-image:url(background.gif); /*定义背景图片*/
background-repeat:no-repeat; /*背景图片无平铺*/
background-attachment:fixed; /*将背景图片固定，不随页面滚动而滚动*/
background-position:0 0; /*定义背景图片的位置，必须先定义背景图片才有效*/
}
/*以上代码可简写为*/
body {
background:#FF0000 url(background.gif) no-repeat fixed 0 0;
}
```

定义背景不需要将所有属性都用上，背景中相关属性的默认值如下：

```
background-color:transparent
background-image:none
background-repeat
background-attachment:scroll
background-position:0% 0%
```

**字体简写**

```
body {
	font-style: italic; /*定义字体为斜体*/
	font-variant: small-caps; /*定义字体为小型的大写字母，针对英文*/
	font-weight: bold; /*将文字加粗*/
	font-size:12px; /*定义字体大小为12px*/
	line-height:140%; /*定义字体行高为140%*/ 
	font-family: "Lucida Grande",sans-serif; /*定义字体名称*/
}
/*以上代码可简写为*/
body {font:italic small-caps bold 12px/140% "Lucida Grande",sans-serif;}
```

简写时，文字大小及行高之间是以 “/” 隔开，字体属性并不是所有属性都一定需要，但 font-size 及 font-family 是必不可少的。
我们能从 font 属性的默认值中得到答案：

```
body {
	font-style: normal;
	font-variant: normal;
	font-weight: normal;
	font-size: medium;  /*默认为medium*/
	line-height: normal;
	font-family: "Time New Roman"； /*默认*/
}
```

**表的简写**

```
li {
	list-style-type: suare; /*将列表的预设标记定义为实心方块*/
	list-style-position: inside; /*列表项目标记放置在文本且环绕文本根据标记对齐*/
	list-style-image: url(image.gif); /*覆盖预设标记用image.gif图片代替*/		
}
/*根据 list-style 的语法，可将列表属性简写为：*/
li {list-style: url(image.gif) inside square;}
list-style 属性值可省略，省略的部分会以相应的默认值代替：
list-style-type:disc;
list-style-position:outside;
list-style-image:none;
/*对于list-style的预设列表项在实际中经常以图片代替，
图片不是用list-style-image属性实线的，
而是用background背景属性实线的。
前提是需要设置列表的list-style:none属性*/
```






















