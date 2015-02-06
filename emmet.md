#Emmet list

##HTML
- `! or html:5` = 
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>

</body>
</html>

script:src
	<script src=""></script>

meta:vp
	<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">

link:favicon
	<link rel="shortcut icon" type="image/x-icon" href="favicon.ico">

form:get
	<form action="" method="get"></form>

input
	<input type="text">

btn:s
	<button type="submit"></button>

Link:css 
	<link rel="stylesheet" href="style.css">

header#site-header>h1.logo>a{site name}
	<header id="site-header">
	<h1 class="logo"><a href="">site name</a></h1>
	</header>

div>div
    	<div>
        	<div></div>
    	</div>

div^div
    	<div></div>
    	<div></div>

ul>li{site name $}*4
	<ul>
		<li>site name 1</li>
		<li>site name 2</li>
		<li>site name 3</li>
		<li>site name 4</li>
    	</ul>

div#page>div.logo+ul#navigation>li*5>a
	<div id="page">
        	<div class="logo"></div>
		<ul id="navigation">
		    <li><a href=""></a></li>
		    <li><a href=""></a></li>
		    <li><a href=""></a></li>
		    <li><a href=""></a></li>
		    <li><a href=""></a></li>
		</ul>
    	</div>

header+.main+footer
	<header></header>
	<div class="main"></div>
	<footer></footer>


td[title="Hello world!" colspan=3]
	<td title="Hello world!" colspan="3"></td>

p*2>lorem
	<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quaerat, eaque, molestiae saepe aut autem in earum magnam harum enim obcaecati eum pariatur sit suscipit nisi repellat quia a ipsum reiciendis!</p
			>
	<p>Ipsum, laudantium, quia suscipit qui officia autem dicta alias explicabo illo quis voluptas corporis eveniet laborum ducimus possimus quas debitis sunt quibusdam libero deserunt. Odit nemo beatae officiis perspiciatis delectus.</p>

p>lorem3
	<p>Lorem ipsum dolor.</p>

##CSS
- `pos:s` = position:static;
- `pos:a` = position:absolute;
- `pos:r` = position:relative;
- `pos:f` = position:fixed;
- `t` = top:|;
- `t:a` = top:auto;
- `r` = right:|;
- `r:a` = right:auto;
- `b` = bottom:|;
- `b:a` = bottom:auto;
- `l` = left:|;
- `l:a` = left:auto;
- `fl:l` = float:left;
- `fl:r` = float:right;
- `fl:n` = float:none;
- `z` = z-index:|;
- `cl:b` = clear:both;
- `d` = display:|;
- `d:n` = display:none;
- `d:b` = display:block;
- `d:i` = display:inline;
- `d:ib` = display:inline-block;
- `ov:v` = overflow:visible;
- `ov:h` = overflow:hidden;
- `ov:s` = overflow:scroll;
- `ov:a` = overflow:auto;
- `m` = margin:|;
- `m:a` = margin:auto;
- `mt` = margin-top:|;
- `mt:a` = margin-top:auto;
- `mr` = margin-right:|;
- `mr:a` = margin-right:auto;
- `mb` = margin-bottom:|;
- `mb:a` = margin-bottom:auto;
- `ml` = margin-left:|;
- `ml:a` = margin-left:auto;
- `p` = padding:|;
- `pt` = padding-top:|;
- `pr` = padding-right:|;
- `pb` = padding-bottom:|;
- `pl` = padding-left:|;
- `w` = width:|;
- `w:a` = widht:auto;
- `h` = height;
- `h:a` = height:auto;
- `maw` = max-widht:|;
- `maw:n` = max-width:none;
- `mah` = max-height:|;
- `mah:n` = max-height:none;
- `miw` = min-width:|;
- `mih` = min-height:|;
- `bb` = border-bottom:|;
- `fz` = font-size:|;

