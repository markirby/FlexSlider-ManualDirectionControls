FlexSlider-ManualDirectionControls
==================================

An extension to FlexSlider2 that allows you to use your own left/right navigation instead of the default.

## Introduction

[FlexSlider2](http://flexslider.woothemes.com/) is a reusable carousel that is highly flexible. 

The only thing it doesn't do at the moment is allow  you to specify custom HTML for left/right navigation. 

Being able to specify custom navigation is very useful when you want permanent navigation instead of the default which appears as you mouse-over, or you have custom HTML/CSS that you don't want to change.

This plugin allows you to easily replace the existing navigation with a single line of code.

## Quick start

* Take your usual flexslider setup code
* Set the option 'directionNav' to false to disable the default navigation
* Append the flexsliderManualDirectionControls() command

Example:

    $('.flexslider').flexslider({
        directionNav: false
    }).flexsliderManualDirectionControls();

Inside your code, you will need to add your navigation, and this must be within the .flexslider child elements, e.g.:

	<section class="flexslider">
		<a class="previous disabled" href="#"><img src="images/back-arrow-white.png" alt="previous" width="11" height="18" /></a>
		<a class="next" href="#"><img src="images/forward-arrow-white.png" alt="next" width="11" height="18" /></a>
		<ul class="slides">
			<li>
				<img src="images/placeholder-module.jpg" alt="placeholder-module" />
				<h2>One</h2>
			</li>
			<li>
				<img src="images/placeholder-module.jpg" alt="placeholder-module" />
				<h2>Two</h2>
			</li>
			<li>
				<img src="images/placeholder-module.jpg" alt="placeholder-module" />
				<h2>Three</h2>
			</li>
		</ul>
	</section>

## Navigation disable feature

If flexslider has animationLoop set to false, a class of disable will be applied to the elements if they cannot be used to go any further

    $('.flexslider').flexslider({
        directionNav: false,
        animationLoop: false
    }).flexsliderManualDirectionControls();
    
    
## Defaults

By default our plugin expects the following:

* An HTML element with the class 'next' to represent the next navigation
* An HTML element with the class 'previous' to represent the next navigation

By default the plugin sets the following:

* A class of 'disable' applied to the 'next' or 'previous' element if the slider can go no further

## Changing the defaults

To change any of the defaults use the following (replacing .alternativePreviousClass, .alternativeNextClass or alternativeDisabledClass with your choice):

    $('.flexslider').flexslider({
      directionNav: false
    }).flexsliderManualDirectionControls({
        previousElementSelector: ".alternativePreviousClass",
        nextElementSelector: ".alternativeNextClass",
        disabledStateClassName: "alternativeDisabledClass"
    });



