#PIXI.js

##### Basic
	$(function () {
    	"use strict";
    	var renderer, stage, group, circle, circleTexture;

    	function init() {
       		stage = new PIXI.Stage(0x000000);
       		renderer = new PIXI.autoDetectRenderer(800, 600, null, false, true);
       		$("#animation").append(renderer.view);
			$(window).resize(onResize);
       		$(window).scroll(onScroll);
       		onResize();
        	requestAnimationFrame(animate);
		}

		function animate() {
        	renderer.render(stage);
        	requestAnimationFrame(animate);
   		}		

		function onResize() {
       		renderer.resize(window.innerWidth, window.innerHeight);
    	}

		function onScroll() {
        	//updateViewportRect();
    	}


	}	
##### Create form external asset
	var circleTexture = PIXI.Texture.fromImage("circle.png");
        var circle = new PIXI.Sprite(circleTexture);
        circle.anchor.set(0.5, 0.5);
        circle.interactive = true;
        circle.buttonMode = true;

        circle.click = function (ev) {
            //
        };

        circle.mouseover = function(mouseData){
            TweenMax.to(this, .5, {
                alpha: 0.5,
                ease: Quart.easeOut
            });
        }
        circle.mouseout = function(mouseData){
            TweenMax.to(this, .5, {
                alpha: 1,
                ease: Quart.easeOut
            });
        }
        
        circle.position.x = 400;
        circle.position.y = 300;

        circle.scale.x = .2;
        circle.scale.y = .2;

        stage.addChild(circle);
#