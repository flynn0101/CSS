**伪类**
伪类可用来指定相关的选择符的状态，下面是锚点标签a的几种默认状态：
```css
	a:link {color:red;} /*默认状态*/
	a:visited {color:blue;} /*访问过后的状态*/
	a:hover {color:green;} /*经过时的状态*/
	a:active {color:black;} /*点击时的状态*/
```
伪类可以让用户在使用页面的过程中增加更多交互效果而无需大量的JavaScript来辅助完成。
```html
	<style type="text/css">
	input:hover {
		background-color:#F00;
	}
	</style>
	<form method="pos" action="">
		<input type="text/css" value="" />
	</from> /*鼠标经过文本框的时候，背景色变成红色*/
```
---
**伪对象**
伪对象是指在HTML的文档指定的信息之外，创建了文档的额外信息。
```html
	<style type="text/css">
	p:before {content:"I ";}
	p:after {content:" You";}
	</style>
	<p> Love </p>
```
