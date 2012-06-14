---
layout: post
title: Creating twinkling stars with css and javascript
tags: 
 - 2012
 - Programming
 - Science Fiction Tower Power
---

Once again, my other job has interfered with my ability to program.  Great sadness I know.  This is why I never posted yesterday, but I'm back again.  Now on to more fun programming topics!

After assessing the flow of Science Fiction Tower Power, I was able to make background stars for my game.  To make these stars I had to code some, what programmers call, 'sprites'.  

To begin I had to determine how I wanted my stars to act.  This brainstorming session helped to me to pin down a fair amount of my parameters.  I wanted them to show up randomly on the screen and fade in and out or *twinkle*.  One of the more difficult things in programming is realizing that an idea of how you want things to act or look on the screen encompasses many more parameters than go into your imagination.  By that I mean, you can imagine it, but programming it requires about 3 to 4 times more information to make it a reality.

To better explain this, I'll show what information I had to create in order to make my sprites, or 'stars'.  First I created a **function** that would generate a randomized star.  

    function makestar(currenttime){
      var star = {
         'right': getRandomInt(0, 100), 
         'top': getRandomInt(0, 100),
         'height': getRandomInt(4, 8),
         'background-color': starcolors[getRandomInt(0, starcolors.length)],
         'rotation': 45,
         'opacity': 1.0,
         'duration': getRandomInt(7,15) * 1000,
         'creationtime': currenttime
      };
      return star;  
    }
  
  To randomize most of my variables I created **getRandomInt(x,y)**.  This is a basic function that takes in two variables and returns a random number in that designated the range of possible numbers.  If I inputted 1 and 20 as my variables into getRandomInt(1,20), it would mean that this function could return any number from 1 through 20 when it runs.  
  
  This function creates a javascript **object** that I can access in my next function.  As you read from top to bottom, you'll see the css position descripters *right* and *top* to specify a random star location.  The height of the star is created randomly (the width is the same size as the height, so I just take that result instead of repeating code).  
  
  To determine the background color I use the same **getRandomInt()** function, however I use it to grab a random entry in a list of various color hex values.  I use a specific pallette of colors for the game so it provides consistency, but this way I can still allow for some variation in the small stars.  

  Lastly I identify the rotation of the star (actually a square turned 45 degrees, thus making it diamond in shape, a simple way to create a star image).  Opacity is turned on full at 1.0.  The duration sets how long the star is to remain visible on the screen, and the creationtime is when the star should first appear.  
  
  The next function updates the star's css and jQuery information, and the third manages star creation and removal.  I'll chat about those next time.  Also, we're in the new office!!  Photos to come here in the near future :)
