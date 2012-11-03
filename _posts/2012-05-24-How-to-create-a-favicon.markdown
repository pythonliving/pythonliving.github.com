---
layout: post
title: How to create a favicon
tags: 
 - 2012
 - Graphics
---

What's a [favicon](http://en.wikipedia.org/wiki/Favicon)?  It's an image file that contains several images.  It was originally implemented by Microsoft with IE5, but has since grown to be a part of all browsers.   It's that small icon that is located on the tab of every browser page, but is also known as the shortcut icon, Web site icon, URL icon or bookmark icon.  Not everyone creates one for their page.

Creating a favicon isn't very difficult, if you know how to use Gimp and have an image already created.  I always use this [egressive page](http://egressive.com/tutorial/creating-a-multi-resolution-favicon-including-transparency-with-the-gimp) as a reference when I need to make one.  It's fairly detailed so I've written a much more simplified version below.

Create your initial image file (I use .png because it's easy) and make sure it's square.  The image itself doesn't have to be, as long as the transparent space surrounding it creates a square canvas.  Then scale that image to be 128 by 128 pixels, save it as favicon128.png, then scale it again until you have 5 different image files with sizes of 128, 64, 48, 32, 16 saved as favicon128.png and down respectively.  

Then create a new file with a canvas size of 128 and load all the other files in as layers.  Starting with the smallest image on the top and largest on the bottom, order the images by size appropriately.  Once complete you'll see all the images on top of each other.

To finish, save this new file as 'favicon.ico' and make sure to indicate .ico as the file type.  Save the ico file in the root directory of the website you want it to appear in.  Now you're done.  

As I said above it's a simple description of how to make an ico file, so if you have any issues you might check out the egressive page I linked above.  It's much more exhaustive.  There are also some useful links on the wikipedia page.                  