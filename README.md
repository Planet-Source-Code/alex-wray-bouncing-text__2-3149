<div align="center">

## Bouncing text


</div>

### Description

Bounces a picture round the screen
 
### More Info
 
Just create an image called east.bmp in the same folder as the page. It's just a nice little effect. Secret effects! Press D to slow it down, S to speed it up and R to reverse it! Have fun, and please rate my code!


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Alex Wray](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/alex-wray.md)
**Level**          |Beginner
**User Rating**    |4.6 (23 globes from 5 users)
**Compatibility**  |
**Category**       |[Controls/ Forms/ Graphics/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-graphics-menus__2-59.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/alex-wray-bouncing-text__2-3149/archive/master.zip)





### Source Code

```
<html>
<body>
<script>
  function getbrowserwidth(){
  	if (navigator.userAgent.indexOf("MSIE") > 0){return document.body.clientWidth;}
  	else{return window.outerWidth;	}}
  function getbrowserheight(){
    if (navigator.userAgent.indexOf("MSIE") > 0){return document.body.clientHeight;}
    else{return window.outerHeight;}}
var widh=getbrowserwidth()
var heigt=getbrowserheight()
var curmov = -3
var curmovl = -3
function document.onkeypress() {
if (window.event.keyCode==100) {
curmov=(curmov/2)
curmovl=(curmovl/2)
}
if (window.event.keyCode==115) {
curmov=(curmov*2)
curmovl=(curmovl*2)
}
if (window.event.keyCode==114) {
curmovl=(curmovl*-1)
curmov=(curmov*-1)
}
}
function changcm() {
if (thing.style.posTop<=0) {
curmov = curmov*-1
}
if (thing.style.posTop>=(heigt - 75)) {
curmov = curmov*-1
}
if (thing.style.posLeft<=0) {
curmovl = curmovl*-1
}
if (thing.style.posLeft>=(widh - 120)) {
curmovl = curmovl*-1
}
setTimeout("changcm()", 5)
}
function al() {
alert("you got me!")
}
function movit() {
thing.style.posTop = thing.style.posTop + (curmov)
thing.style.posLeft = thing.style.posLeft + (curmovl)
setTimeout("movit()", 2)
}
</script>
<body bgcolor="#FFFFCC">
<div id="thing"
	style="position:absolute;
		top: 50;
		left: 180;
		z-index: 0">
<img src="lane2.bmp" height="70" width="100" onClick="alert('you got me!')"/>
</div>
<body onLoad="movit();changcm()">
</body>
</html>
```

