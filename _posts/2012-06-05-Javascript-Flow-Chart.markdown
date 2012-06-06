---
layout: post
title: Javascript Flow Chart
tags: 
 - 2012
 - Programming
 - Science Fiction Tower Power
---

These past few work days I've been going through my code with a fine-tooth comb.  Robey and I were partially looking at unneeded repetitions or code run unnecessarily.  Mostly we were putting together a flow chart construction of how the functions interacted.  This was done mainly for my benefit, so that I could more easily identify where any bugs might be located.

![Science Fiction Tower Power basic flow chart](https://dl.dropbox.com/u/21971644/Blog%20Images/Blog%20Pics%20for%20Entries/June%202012/sftpjsflowchart.png)

This process was incredibly helpful.  It helped me to identify several lengthy areas that could be simply cut down by creating another function.  There was also some code that I was able to simply strike out because it's become obsolete based on other updates.  

There were two bugs in particular that had been bothering me.  The first bug occurred when the player attempted to submit a solution after the spaceship had collided with the world.  When this happened the 'kersplat' image that normally would show up and slowly fade, now would remain until the next time a ship collided with the planet.  

The awesome part about this first bug, was that it was rather difficult realizing what exactly was causing the effect, and so determining how to solve it took a bit.  After some puzzling and a helpful Robey, we identified that is was caused by what I mentioned above.  To solve this I ran my **submitsolution()** function begin with an *if* block.  This *if* block identified whether or not the problem was visible, before it allowed a person to submit any information.  Basically, it stopped allowing accidental answer submissions when the problem wasn't visible.  

The second bug occured when the player attempted to answer a problem but was unsuccessful and the ship 'kersplatted' (and a new ship was thus generated).  The answer box would keep the old data the player had entered, therefore making it difficult for the player to answer the next problem without deleting the old numbers. 

To solve this I simply used the *.val()* jQuery function.  This function *$().val()* allows you to alter what appears in the input box in a variety of ways.  Luckily I just wanted to make the submission box blank everytime a new ship was created.  My end code was simply *$("#inputproblem" + problemnumber).val("");*  This little bit of code is able to update any input box with an empty string.  

But what was the most interesting discovery of this process?  Learning that your naming conventions are incredibly important, especially in the beginning.  You want your function to very easily tell you what it does.  If you need to change things later, and then never rename your function accordingly, it can make reading your code that much harder.  It's already hard enough sometimes...why make it worse?  
  
