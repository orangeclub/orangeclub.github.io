

<html>
<head>

    <meta charset="utf-8"> 
	<link href ="public/css/metro.css" media="all" rel="stylesheet">
    <meta content="authenticity_token" name="csrf-param" />
<meta content="QmE0+eGX9YG41KrjM7AjeR/in9/URUgWp5Smigkh6D0=" name="csrf-token" />
    <script src="javascripts/jquery.js"></script>
	<script href = "js/project.js"></script>
	<>

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
</html>