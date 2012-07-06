---
layout: post
title: Adjusting some css color intensity using trigonometry
tags: 
 - 2012
 - Programming
 - Science Fiction Tower Power
---

The next part of this javascript code, is the function **intensity()**.  It calls four variables and is, in some ways, the more complicated of the functions (mathematically at least).  The function itself is called within the **twinkle()** function, and sets the varying duration, age, delay and cycle of the color intensity of each star.  Here is the function itself:

    function intensity(duration, age, delay, cycle){
      if (age < delay){
        return 0;
      }else if (age < duration - delay){
        return (-1*Math.cos((age-delay)*2*cycle*Math.PI/(duration-delay*2)) + 1)/2;   
      }else{
        return 0;
      }
    }

Although this function takes several values it only returns one; the new color intensity.  Using two **if** blocks it first determines if the age of the star is less than the delay.  The age of the star is the length of time the star has existed on the screen.  The delay is the amount of time before this color shows up.  Therefore as long as the delay is greater than the age of the star, the new color intensity will not appear as the functions returns zero.  

Then comes the **else if** block.  This block determines, that if the age of the star is greater than the duration (total life span of the star) minus the delay, then a new color intensity value will be returned.  This color intensity is created based on the trig function listed here.  

If neither of those two situations apply, then the function once again returns zero.       