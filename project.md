---
layout: page
title: Project
---

<head>

    <meta charset="utf-8"> 
	<link href ="public/css/metro.css" media="all" rel="stylesheet">
    <meta content="authenticity_token" name="csrf-param" />
<meta content="QmE0+eGX9YG41KrjM7AjeR/in9/URUgWp5Smigkh6D0=" name="csrf-token" />
    <script src="js/jquery.js"></script>
	<script src = "js/project.js"></script>
	

    <script>

        var _gaq = _gaq || [];
        _gaq.push(['_setAccount', 'UA-34648935-2']);
        _gaq.push(['_trackPageview']);

        (function() {
         var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
         ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
         var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
         })();
     </script>
     <script>


    $(document).ready(function() {
        $('#navlinks ul li').hover(
        function() {
            $(this).css('border-right-color', 'white');
        },
        function() {
            $(this).css('border-right-color', '#BEBEBE');
        });
        $('#external-links li').hover(
        function() {
            $(this).css('background', '#333');
        },
        function() {
            $(this).css('background', '#222');
        });
    });
    </script>
    <script>
    $(function() {
        $('.element').each(function (idx, raw_elem){
            var elem = $(raw_elem);
            var desc = $('.desc', elem),
                cover = $('.cover', elem),
                block = $('.block', elem);
            var details_showing = false,
                video_inside = $('iframe', block).length != 0;

            block.css({top:elem.height()});
            cover.css({top:0});

            elem.click(function() {
                if (!details_showing) {
                    block.stop().show().animate({top:0}, 100);
                    cover.stop().animate({ top: -elem.height() }, 200);
                    desc.stop().animate({ bottom : -desc.height() }, 200);

                    details_showing = true;
                } else {
                    block.stop().animate({ top: elem.height()}, 100);
                    cover.stop().animate({ top: 0 }, 200);
                    desc.stop().show().animate({ bottom : 0 }, 200);

                    details_showing = false;
                }
            });

            var timeout_id;

            elem.hover(function() {
                elem.css({"border-color": "#78a", "box-shadow": "#567 0px 0px 16px", "-webkit-animation" : "handon 1s"});
                if (!details_showing) desc.stop().show().animate({ bottom : 0 }, 200);
                else { clearTimeout(timeout_id); }
            }, function() {
                elem.css({"border-color": "#111", "box-shadow": "black 0px 0px 16px", "-webkit-animation" : "handoff 1s"});
                desc.stop().animate({ bottom : -desc.height() }, 200);
                if (!video_inside && details_showing) {
                    timeout_id = setTimeout(function() {
                        block.stop().animate({ top: elem.height()}, 100);
                        cover.stop().animate({ top: 0 }, 200);

                        details_showing = false;
                    }, 500);
                }
            })

        })
        $('#rpanel').height($(document).height() + 50);

    });
    </script>
    <script>
    $(function() {
        $('.element').each(function (idx, raw_elem){
            var elem = $(raw_elem);
            var desc = $('.desc', elem),
                cover = $('.cover', elem),
                block = $('.block', elem);
            var details_showing = false,
                video_inside = $('iframe', block).length != 0;

            block.css({top:elem.height()});
            cover.css({top:0});

            elem.click(function() {
                if (!details_showing) {
                    block.stop().show().animate({top:0}, 100);
                    cover.stop().animate({ top: -elem.height() }, 200);
                    desc.stop().animate({ bottom : -desc.height() }, 200);

                    details_showing = true;
                } else {
                    block.stop().animate({ top: elem.height()}, 100);
                    cover.stop().animate({ top: 0 }, 200);
                    desc.stop().show().animate({ bottom : 0 }, 200);

                    details_showing = false;
                }
            });

            var timeout_id;

            elem.hover(function() {
                elem.css({"border-color": "#78a", "box-shadow": "#567 0px 0px 16px", "-webkit-animation" : "handon 1s"});
                if (!details_showing) desc.stop().show().animate({ bottom : 0 }, 200);
                else { clearTimeout(timeout_id); }
            }, function() {
                elem.css({"border-color": "#111", "box-shadow": "black 0px 0px 16px", "-webkit-animation" : "handoff 1s"});
                desc.stop().animate({ bottom : -desc.height() }, 200);
                if (!video_inside && details_showing) {
                    timeout_id = setTimeout(function() {
                        block.stop().animate({ top: elem.height()}, 100);
                        cover.stop().animate({ top: 0 }, 200);

                        details_showing = false;
                    }, 500);
                }
            })

        })
        $('#rpanel').height($(document).height() + 50);

    });
    </script>
	<style>
	@font-face {
    font-family: 'DINEngschriftRegular';
    src: url('/fonts/dinengsc-webfont.eot');
    src: url('/fonts/dinengsc-webfont.eot?#iefix') format('embedded-opentype'),
         url('/fonts/dinengsc-webfont.woff') format('woff'),
         url('/fonts/dinengsc-webfont.ttf') format('truetype'),
         url('/fonts/dinengsc-webfont.svg#DINEngschriftRegular') format('svg');
    font-weight: normal;
    font-style: normal;
}

@font-face {
    font-family: 'EurostileRegular';
    src: url('/fonts/eurostile-regular.eot');
    src: url('/fonts/eurostile-regular.eot?#iefix') format('embedded-opentype'),
         url('/fonts/eurostile-regular.woff') format('woff'),
         url('/fonts/eurostile-regular.ttf') format('truetype'),
         url('/fonts/eurostile-regular.svg#EurostileRegular') format('svg');
    font-weight: normal;
    font-style: normal;
}

/*
@font-face {
    font-family: 'EurostileBold';
    src: url('type/EurostileBold.eot');
    src: url('type/EurostileBold.eot?#iefix') format('embedded-opentype'),
         url('type/EurostileBold.woff') format('woff'),
         url('type/EurostileBold.ttf') format('truetype'),
         url('type/EurostileBold.svg#EurostileBold') format('svg');
    font-weight: bold;
    font-style: normal;
}*/

body {
	color: #888;
	font-family: EurostileRegular, Helvetica, Arial, sans-serif;
	margin:0;
	font-size: 14px;
	overflow-y: scroll;
    background:#333 url("/images/noise.png");
}

hr {
	color: #fff;
	background-color: #222;
	border: 0;
	height: 1px;
}

footer a:hover {
	color: #fff;
	text-decoration: none;
}

.medium-font {
	font-size: 18px;
}
.big-font {
	font-size: 24px;
}

.center {
	text-align: center;
}

#rpanel {
    padding-top: 241px;
    margin-left: 500px;
    box-sizing: border-box;
}

#rpanel a:link, #rpanel a:visited {
    color: white;
    text-decoration: none;
}

#rpanel a:hover {
    color: rgb(122, 213, 221);
}


header {
    min-width: 800px;
    margin-top: 30px;
    margin-bottom: 30px;

    position: absolute;
}

nav {
    width: 80px;
    margin-right: 0;
    margin-left: auto;
    margin-top: 50px;

    position: relative;
    z-index: 1;
}

nav ul {
    padding: 0;
}

nav li {
    list-style: none;
    font-weight: bold;
    text-align: right;
    padding: 5px 11px 5px 0;
    color: black;
    margin-top:10px;

    font: normal 20px DINEngschriftRegular;
}

nav li.activated a {
    color: #ccc;
}

nav a {
    color: #777;
	text-decoration: none;

    margin: 0px;
    display: block;
    width: 100%;
    height: 100%;
}

nav a:hover {
    color: #999999;
}

header {
    margin: 0;
}
header .title {
    float: left;

    width:390px;
    padding-right: 4px;

    margin-left: 500px;
	font: bold 100px DINEngschriftRegular;

}

header .title a {
    color: #555;
}

header .title a:hover {
    color: #666;

    -webkit-animation: title-on 0.5s;
}

header .title small {
    font-size: 50px;
}

header a {
    text-decoration: none;
}

header .owner {
	font: bold 30px DINEngschriftRegular;
	color: rgb(58, 65, 71);
    margin-left: 415px;
    display: none;
}

header .words {
	margin-top: 5px;
	padding-left: 120px;
}

#lpanel {
    text-align: right;
    width: 350px;
    float: left;
    background: black;
    border-right: 1px solid rgb(39, 39, 39);
    /*box-shadow: #181818 0px 0px 30px;*/
}

#about {
    margin-top: 56px;
	padding-bottom: 15px;
    padding-right: 10px;
	color: #444;
    font-family: DINEngschriftRegular;
    border-bottom: 1px dotted #333;
}

#label {
    text-align: right;
    font-size: 25px;
    font-weight: bold;
    color: black;
}

#content {
    padding-left: 5px;
    margin-left: 10px;
}
#content .element {
	padding: 5px;
}
#content .element .title {
	margin: 20px 0px;
    margin-top: 5px;
	color: #ccc;
	font-weight: bold;
	font-size: 16px;
}

#content .element .content {
    margin-top: 40px;
}

#external-links {
    padding-right: 100px;
    padding-left: 0px;
}

#external-links li {
    list-style: none;
    display: inline-block;
    margin-top: 50px;
    margin-left: 20px;
    background: #222;

    color: white;
    font-weight: bold;
    text-decoration: none;

    vertical-align: top;
}

#external-links li a
{
    color: white;
    font-weight: bold;
    text-decoration: none;

    display: block;

    padding: 10px;

    border:2px solid #303030;
    box-shadow: inset 0px 0px 8px #070707;
}

#external-links li .whole
{
    height: 80px;
    width: 80px;
    position: relative;
}

#external-links li .desc
{
    font-size: 12px;
    font-weight: normal;

    color: gray;
    margin-top: 24px;

    position: absolute;
    bottom: 0px;
    right: 0px;
}

footer {
	padding-top: 50px;
	padding-bottom: 20px;
    padding-right: 11px;
	font-size: 12px;
    line-height: 18px;
    color: #555;
}

footer a:link, footer a:visited, footer a:active{
	color: #555;
	text-decoration: none;
}
footer a:hover{
	color: #777;
	text-decoration: none;
}

#bg {
    left: 400px;
}


#category {
    background: rgb(66, 84, 121);/*rgb(43, 43, 63)*/
    padding-left: 150px;
    margin-left: -150px;
    font: normal 30px DINEngschriftRegular;

    margin-top: -41px;

    color: silver;

    display: block;/* hidden first*/
}

#exhibition {
    margin-left: -40px;
    margin-top: -14px;
    width: 600px;
    position: relative;
}

#exhibition .element {
    width: 200px;
    height: 150px;
    background: #222;
    box-shadow: black 0px 0px 16px;
    border: solid 1px #111;
    position: absolute;
    overflow: hidden;

    margin: 40px;

    color: #aaa;
    font-size: 14px;

    cursor: pointer;
}

#exhibition .element .container {
    padding: 2px 10px;
}

#exhibition .featured {
    width: 440px;
    height: 340px;

    font-size: 16px;
}

#exhibition .element .name {
    color: #aaa;
    margin-left: -2px;
    text-shadow: 2px 3px 2px #331;
    font: normal 30px DINEngschriftRegular;
}

#exhibition .element .desc {
    background: rgba(0, 0, 0, 0.5);
    width: 100%;
    position: absolute;
    bottom: 0px;

    display: none;
}

#exhibition .featured .name {
    font-size: 50px;
}

#exhibition .element .block {
    background: rgba(0, 0, 0, 0.8);

    height: 100%;
    width: 100%;
    position: absolute;

    display: none;
}

#exhibition .element .wrapper {
    position: relative;
}

#exhibition .element .links {
    margin: 0px;
    padding: 0px;

    list-style: none;
    text-align: right;

    font: normal 20px DINEngschriftRegular;

    position: absolute;
    right: 10px;
    bottom: -2px;
}

#exhibition .element .links li {
    display: inline-block;
    margin: 2px 8px;
    margin-right: 0px;

    padding: 2px 6px;
    
}

#exhibition .featured .links li {
    font-size: 30px;
    padding: 4px 8px;
    margin: 4px 8px;
    margin-right: 0px;
}

#exhibition .links a:link, #exhibition .links a:visited, #exhibition .links a:active{
	color: #9999ff;
	text-decoration: none;
}

#exhibition .links a:hover {
    color: white;
}


#rpanel .button {
    background: #191919;
    border: solid 1px white;
    padding: 4px 12px;
    border-radius: 5px;

    cursor: pointer;

    margin-right: 10px;
}

#rpanel .button-wrapper a:link, #rpanel .button-wrapper a:visited {
    color: #666;
}

#rpanel .button-wrapper a:hover {
    color: rgb(122, 213, 221);
}

@-webkit-keyframes title-on{
    from {
        color: #555;
    }
    to {
        color: #666;
    }
}
@-webkit-keyframes title-off{
    from {
        color: #666;
    }
    to {
        color: #555;
    }
}

@keyframes title-on{
    from {
        color: #555;
    }
    to {
        color: #666;
    }
}
@keyframes title-off{
    from {
        color: #666;
    }
    to {
        color: #555;
    }
}
 @-webkit-keyframes handon {
            from {
                box-shadow:black 0px 0px 16px;
                border-color: #111;
            }
        }
        @-webkit-keyframes handoff {
            from {
                box-shadow: #567 0px 0px 16px;
                border-color: #78a;
            }
            to {
                box-shadow:black 0px 0px 16px;
                border-color: #111;
            }
        }

        @keyframes handon {
            from {
                box-shadow:black 0px 0px 16px;
                border-color: #111;
            }
        }
        @keyframes handoff {
            from {
                box-shadow: #567 0px 0px 16px;
                border-color: #78a;
            }
            to {
                box-shadow:black 0px 0px 16px;
                border-color: #111;
            }
        }
	</style>
</head>
<body>
	<div id="exhibition">
        <div class="featured element" style="top: 0px; left: 0px;
            background-image: url('images/portfolio/Saviors.png')">
            <div class="container cover" style="position:absolute;"><div class="name"> SAVIORS </div></div>
            <div class="desc"><div class="container"> Four-player cooperative tactical shooter. Save the world! </div></div>
            <div class="block">
                <ul class="links">
                    <li><a target="_blank" href="http://saviors-dev.tumblr.com"  >DevBlog</a></li>
                </ul>
                <div class="container">
                    <div class="name">SAVIORS</div> 
                    <div class="details">Thesis. A local multiplayer game about risk, trust and sacrifice.<br/><br/>In a fictional dystopian background, you are called upon to save the world. The game is designed to encourage players communication and collaboration. Players make strategic decisions to occupy cities and upgrade the tech tree, and also use a lot of tactics to fight with enemies. Think about XCOM meets Monaco meets Pandemic.<br/><br/>Will be featured with procedural generation, distinct weapons and abilities.<br/><br/></div>
                </div>
            </div>
        </div>
     
	
</body>
