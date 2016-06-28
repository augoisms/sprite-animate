#spriteAnimate
- jQuery plugin for animating a sprite sheet using canvas. 
- Sprite sheet can be linear or a grid of frames.
- The class `loaded` gets added to the canvas element after the sprite has loaded. This is useful if you have a large sprite and you want to set a background image on the canvas using the first frame.

##Public Methods 
###Play
`$canvas.spriteAnimate('play');`
###Pause
`$canvas.spriteAnimate('pause');`
###Go to specified index (zero-based)
`$canvas.spriteAnimate('goTo', index);`
###Get current index (zero-based)
`$canvas.spriteAnimate('getIndex');`
###Restart sprite (useful when loop is set to false)
`$canvas.spriteAnimate('restart');`

##HTML
```
<div class="animation-ctn">
  <canvas style="width: 460; height: 368;"></canvas>
</div>
```

##JS
```
$(function(){
  var $canvas = $('canvas');
  // init sprite animation
	$canvas.spriteAnimate({
		frameWidth: 460,
		frameHeight: 368,
		numberOfFrames: 369,
		imgSrc: "/path/to/sprite.png",
		fps: 15,
		loop: true,
		debug: false,
		onFinish: function(){}
  });
});
```