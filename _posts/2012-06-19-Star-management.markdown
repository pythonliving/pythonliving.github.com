---
layout: post
title: Star management...much easier when coding 
tags: 
 - 2012
 - Programming
 - Science Fiction Tower Power
---

This last function runs the functions **makestar()** and **updatestar()** and manages all the stars created therefrom.  

    function updatestars(currenttime){
      var newstars = [];
      while (stars.length < 20) {
        var star = makestar(currenttime);
        stars.push(star); 
      }
      for (var i = 0; i < stars.length; i+=1){
        var star = stars[i];
        updatestar(star, i);
        if (star['duration'] > currenttime - star['creationtime']){
          newstars.push(star);
         }     
      }
      stars = newstars;
    }

The only variable this function needs to run appropriately is a designation for the current time.  Then the fun begins.

To start the function creates an empty object (in python this is known as a dictionary).  Then a while loop runs, which adds a newly created star object (via the **makestar()** function) to the global object **stars** as long as the length of the global object is less than 20.

Then a **for** loop runs, which takes one of the values in the **stars** object and runs **updatestar()** on it.  Then a check is run, to determine whether or not the star should still be visible based on the duration and and creationtime values stored in the object.  If the duration of star visibility is greater than the currenttime listed in the game and the initial creationtime of the star, the **star** will be added to the **newstars** object and thus displayed on the screen.  Basically that's the age of the star.  

Technically the stars are never specifically removed from the object, because javascript has what is known as 'garbage collection'.  The programming language was built in such a way that allows you to simply stop holding onto information.  When you stop holding on to it, or collecting it, it's handled by something written in the language itself.  Anything more specific than that I can't tell you...it's something I'll be learning more about another day I understand.  Basically, once the duration is no longer greater than the currenttime minus the creationtime, (in other words the duration of the star is spent), the star will simply cease to exist within the code.  

So far so good.  Here is an image or what my current stars look like.

![Spaceships with stars in the background](https://dl.dropbox.com/u/21971644/Blog%20Images/Blog%20Pics%20for%20Entries/June%202012/basicstars.PNG)

          
