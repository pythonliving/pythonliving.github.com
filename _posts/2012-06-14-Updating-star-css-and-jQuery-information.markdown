---
layout: post
title: Updating the star css and jQuery data
tags: 
 - 2012
 - Programming
 - Science Fiction Tower Power
---

The function from yesterday created an object that housed the information necessary to create the stars.  Today's function puts the star on the screen.

    function updatestar(star, id){
      id = id + 1;
      $("#" + 'star' + id).css({
         'display':'block',
         'position': 'absolute',
         'right': star['right'] + '%',
         'top': star['top'] + '%',
         'height': star['height'],
         'width': star['height'],
         'background-color': star['background-color'],
         '-webkit-transform': 'rotate(' + star['rotation'] + 'deg)',
         '-moz-transform': 'rotate(' + star['rotation'] + 'deg)',
         '-o-transform': 'rotate(' + star['rotation'] + 'deg)',
         '-ms-transform': 'rotate(' + star['rotation'] + 'deg)',
         'transform': 'rotate(' + star['rotation'] + 'deg)',
         'opacity': star['opacity']
        });
    }

My function **updatestar(star, id)** will take the star object created by the **makestar()** function (inputted here as the variable *star*) and an id.  The id identifies which html div the star css info will go into.  

Going from top to bottom, you can note how many of the css attributes have a corresponding key from the star object.  There are only two that don't, and they are the attributes that make the star actually display and determine it's position.  If you have any questions about how these aspects of css work, you can look it up on the [Mozilla Developer Network](https://developer.mozilla.org/en-US/) website.  [W3schools](http://w3schools.com/) is also helpful, but not nearly as comprehensive.  
