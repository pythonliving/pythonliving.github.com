---
layout: post
title: A twinkle function, making stars better since 1929
tags: 
 - 2012
 - Programming
 - Science Fiction Tower Power
---

No this post has nothing to do with the stock market crash.  I'm just here to finish up my fancy starness.  This function processes all the other functions I've since been explaining, and uses them to create my twinkle effect.  

    function twinkle(star, currenttime){
      var intensityred = intensity(star['duration'], 
      currenttime - star['creationtime'], star['delayred'], star['cycles'][0]); 
      var intensitygreen = intensity(star['duration'], 
      currenttime - star['creationtime'], star['delaygreen'], star['cycles'][1]); 
      var intensityblue = intensity(star['duration'], 
      currenttime - star['creationtime'], star['delayblue'], star['cycles'][2]);
      var rgb = hextorgb(star['background-color']); 
      var red = Math.floor(rgb[0] * intensityred);
      var green = Math.floor(rgb[1] * intensitygreen);
      var blue = Math.floor(((rgb[2] - 64) * intensityblue) + 64);
      return "rgb(" + red + "," + green + "," + blue + ")";     
    }

To begin with **twinkle()** pulls in two variables, star and the currenttime.  The currenttime is self explanatory, and the star we've discussed before (all the css values that correspond to be the star on the screen).  Then the majority of this function simply creates variables.

The first three set the intensities of the different RGB values.  The variable **rgb** converts the background color the star is originally set to from a hex value to rgb (as discussed in [this entry](http://pythonliving.flaminglunchbox.net/2012/06/21/Creating-a-time-sensitive-color-shift-with-js.html)).  After this the actual rgb variable values (red, green, blue) are set and subsequently rounded down so that the browser can easily handle them.  

The final value returned from this function is the rgb value, which is used in **updatestar()**.  If you remember, **updatestar()** renders the various css values of the star.  Basically now, instead of a basic hex color value designated as the background-color I use **twinkle()**.  The colors update and we get the twinkle (pulsing) effect because **updatestars()** (which runs *updatestar()*) runs within the **tick()** function (which for the purposes of explanation runs 60 times a second).  If you didn't realize how much processing power your browser had yet, think about that for a while.  

   
