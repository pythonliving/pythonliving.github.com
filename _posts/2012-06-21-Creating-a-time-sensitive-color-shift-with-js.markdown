---
layout: post
title: Creating a time sensitive color shift with javascript
tags: 
 - 2012
 - Programming
 - Science Fiction Tower Power
---

This was a rather difficult piece of code for me.  I haven't had a lot of practice using trigonometry within code before, so Robey had to help a fair deal with this.

I'll start today by giving a brief description of what I wanted to have happen, the basics on how it was set up, and one of the simpler functions I created for this exercise.  

At this point in my code, my stars will fade in and out while only remaining one color value.  My hope was to have a kind of twinkle effect for my stars and to simulate that I was going to use a gradual color shift to emphasize it.  To do this I had to create three new functions: **twinkle(star, currenttime), intensity(duration, age, delay, cycle), and hextorgb(hex)**.

**twinkle()** is the most complex of the different functions, and will be discussed last.  The main purpose of it is to take in all the values and information provided by the subsequent functions, and make them useful when the function itself is called in **updatestar()** (previously discussed, this function simply turns the js object into rendered css).  

**intensity()** involves the trig and will be discussed later, but **hextorgb()** is the most basic one and what you'll hear about today.

**hextorgb()** does basically what it's name means, it converts hex color values into RGB color values.  

    function hextorgb(hex){
      var newhex = hex.slice(1);
      var red = newhex.slice(0,2);
      var green = newhex.slice(2,4);
      var blue = newhex.slice(4,6);
      var newred = parseInt(red, 16);  
      var newgreen = parseInt(green, 16);  
      var newblue = parseInt(blue, 16);  
      var rgb = [newred, newgreen, newblue];
      return rgb;
    }
    
Most of this function is simply creating variables out of other variables.  Using javascript's version of *slice*, I cut up the hex value (example: #dded00) into the 3 different RGB values.  For those who don't know, RGB stands for Red, Green and Blue.  The first two values in the hex color value represent Red (ex. dd), the next two green(ex. ed) and the last blue(ex. 00).  

First I create a newhex value from the inputted hex value, because my original hex values were stored as strings starting with the hash sign.  Therefore I start out by slicing that value from '#dded00' to 'dded00'.  

Then I create new values from the first two, second two and last two digits in the hex, and thus identify a variable with it's corresponding hex code.  Then I use a js built in function called **parseInt()**, which takes a variable and converts it into a number using a set base during conversion.  Here it takes our hex string values of, for example, red 'dd' and converts it into a number.  It does this by using the base set provided, 16.  Basically this says, instead of a base set of numbers that go from 1 to 10 (base 10), the base set goes from 1 to f (1,2,3,4,5,6,7,8,9,10,a,b,c,d,e,f).  Taking the base set it converts it to base 10 integer.  

The final step in this function is simply taking all the new RGB values, and putting them into an object which is returned from the function.  Alright, it's too hot in here and I want to go hiking.  I'll chat more next week.     











 
