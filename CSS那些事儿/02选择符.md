**通配符选择器**
通配符一般用来对页面所有元素应用样式
```css
* {
	margin:0;
	padding:0;
} /*将页面所有元素的内外补丁设为0*/
```
可以对特定元素的所有后代元素应用样式
```css
	<style type="text/css">
	* {color:#000;} /*将页面中的所有颜色设置为黑色*/
	p {color:#00F;} /*将p标签中的颜色设置为蓝色*/
	p * {color:#F00;} /*将p标签中的所有后代颜色设置为红色*/
	</style>
	<p>我还是蓝色的，<span>我是红色的</span><em>我也是红色的</em></p>
```
---
**后代选择器**
作用于某个元素中的后代元素
```css
	<style type="text/css">
	p strong {
		color:#F00; /* 定义p标签中的span标签内文字的颜色为红色 */
		font-size:18px;/* 定义文字大小为18px */
		text-decoration:underline; /* 定义文字有下划线 */
	}
	</style>
```
**子选择符**
主要作用是定义子元素对象的样式，无法定义子元素以外的任何元素
```css
	body > strong {
		color:#F00; /*定义p标签所包含的span标签元素内的文字颜色为红色*/
	}
```
---
**相邻选择符**
其主要作用是匹配同一个父级下某个元素之后的元素，例如：定义与p标签相邻的strong元素，可以这样定义：
```html
	p + strong {
		color:#F00; /*定义p标签相邻的span标签内的文字颜色为红色*/
	}
```
**属性选择符**
E代表任何一个HTML标签，attr代表E标签中的任意一个属性，value代表该属性中存在的属性值。

---
E[attr]将匹配具有 “attr” 属性的E标签元素，忽略该属性的属性值。例如，我们需要定义页面中所有带有class属性的标签。
```html
	<style type="text/css">
		*[class] {
			color:#F00; 
			font-size：18px；	
		}
	</style>
	<p class="paragraphs">带class属性的标签</p>
	<p>不带class属性的标签</p>
```
---
E[attr="value"]匹配具有“attr”属性且属性值为“value”的E标签元素。例如，定义 type 属性值为 text 的 input 标签元素的样式：
```html
	<style type="text/css">
	input[type="text"] {
		text-align:center;
		border:1px solid #F00;
		background-color:#E8;
	} /*定义type属性值为text的input标签元素的样式*/
	</style>
	<form method="post" action="">
		<input type="text" value="这是个文本框" />
		<input type="password" value="这是个密码框" />
	</form>
```
---
E[~="value"]匹配具有“attr”属性且属性值是具有空格符隔开的字段，其中一个字段等于value的E标签元素。
```html
	<style type="text/css">
	p[title~="css"] {
		font-size:20px;
		color:#F00;
		margin:0;
	}
	</style>
	<p title="css html">title 属性值为"css html"的段落标签,有空格字符隔开。</p>
	<p title="css+html">title 属性值为"css+html"的段落标签，无空格隔开。</p>
```
---
E[attr|="value"]匹配具有“attr”属性且属性值必须是以value值开始及使用连字符（-）分隔E标签元素。
```html
	<style type="text/css">
	p[title|="css"] {
		font-size:20px;
	}
	</style>
	<p title="html-css">title 属性值为html-css的段落标签，因为不是以value值开始及使用连字符分隔，并未被定义CSS样式。</p>
	<p title="css-html">title 属性值为html-css的段落标签，是以value值开始及使用连字符分隔，被定义了CSS样式。</p>
```
---
**ID选择符**
类选择符以 # 为前缀，ID选择符与类选择符用法类似，但一个页面中使用ID选择符不要出现同名ID。

---
**选择符组合**
```html
	<style type="text/css">
	.myContent {
		font-size:12px; /*将页面中所有类名为myContent的标签中文字定义为12px */
	}
	p.myContent {
		font-size:18px;
	} /*定义类名为myContent的段落标签p的样式*/
	</style>
	
```


