---
layout: post
title: Working on my first file Input/Output in python
tags:
 - Programming
 - Recovery
 - python
 - 2012
---

Over the past two weeks I've been attempting to work on a small bit of python code for my day job.  My hope was to find a way to use programming to do something productive for work, thus combining my work aspirations (FlamingLunchbox) with my 9 to 5 (if at least temporarily).

I was hoping to write an itemized list of things we needed for 2013 from a specific vendor, based on the total usage from last year's purchases.  So I requested a list from the vendor and exported it to a csv file.  

From my understanding, it's easiest to manipulate a previously excel spreadsheet via *python* once it's in csv format.  This formatting simplifies the information into lines of data, separated by commas.  Since you now don't have formatting code to deal with, you can get ready to manipulate your data more quickly.

When opening a file in python, you normally place the open file in a variable.  In my code I do this with the following code: **myFile** = open("myFile.csv", "r").  When you're opening a file you must make sure to close it, or else you'll have open files mucking up your computer.  You do this by ending your code with the line **myFile.close()**.

I'm still working on how to organize the data once I've opened the file.  I know you can use **print myFile.readline()** to print out each line in your csv file.  However as I'm still stuck on how I want to organize my data, I don't have anything else concrete to post today.

If you didn't notice, I've been rather busy of late, thus the lack of posts.  My day job is rather busy at the moment, plus I've been on the last downhill streak in finishing my first afghan.  Being about 2 years in the making I'm desperately ready to be done with this project.  I'll post a picture of my monstrosity once complete. 

In case you'd like a more in depth explanation of how to open/close, read and write files in python, check out this module on **Codecademy**, [Python Track Course, File Input/Output](http://www.codecademy.com/courses/python-intermediate-en-OGNHh).  


    
