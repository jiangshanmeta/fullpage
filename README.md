fullpage
=================================================================
this is my fullpage plugin based on jQuery for desktop and mobile
you can use it for creating your personal pages and webApp
Here is a  [Demo](http://jiangshanmeta.github.io/myWork/org/myFullpage/myFullpage.html) on PC
Here is another [Demo](http://jiangshanmeta.github.io/myWork/org/myFullpage/mobile.html) on mobile

##Usage
Fullpage needs to follow a simple.Here is the structure of HTML
```html
	<div id="myFullpage">
		<div class="section">
			<!-- your own code here-->
		</div>
		<div class="section">
			<!-- your own code here-->
		</div>		
	</div>
```
Here you do not need to set the HTML of navbar,it will be create by js

```js
	$("#myFullpage").fullpage({
			speed:800,   //speed of scrolling
			navigation:true,	  //create the navbar
			navpos:"right",	//the position of navbar
		//	navigationTooltips:["section1"],//tooltips of navbar
			continuous:false,		//continuous at the first or last section
			keyboard : true,				//support keyboard
			mobile : true,					//support touch event in mobile
			method : "swing",				//the method of animate in jQuery
			horizontal : false,				// horizontal or vertical
			onLeave : function(index){		//what todo before leaving the section
											//index means the number of current section
			},
			afterLoad : function(index){	//what todo after coming to the new section 
											//index means the number of current section
			}
	})

```

##setting

- **speed**  *(default:800)* - the speed of scrolling 切换页面所需时间

- **navigation** *(default:true)*  -whether or not you will have a navbar 是否有navbar的设定

- **navpos** *(default:right)* - the position of navbar ,which can be 'right' 'left' or 'bottom' 导航条的位置

- **navigationTooltips** - tooltips of navbar 

- **continuous**   -continuous at the first or last section 在第一页和最后一页是否可以继续切换

- **keyboard** -support keyboard 是否支持键盘事件，仅支持方向键切换

- **mobile** -support touch event in mobile 是否支持移动端的touch事件

- **horizontal** *(default:false)*- horizontal or vertical 是否是水平的 默认为垂直的

- **onLeave** -what todo before leaving the section 离开页面时的回调函数，此时的index是要离开页面的index

- **onLeave** -what todo after coming to the new section  进入新页面的回调函数，此时的index是新页面的index


you can also use data-speed data-method data-navpos to set 