---
layout: post
title: Creating a tagging system
tags: 
 - 2012
 - Programming
---

Figuring out how to create a tagging system for my blog was not very clear at first.  It took a fair amount of searching the documentation to find a clear way of setting it up.  Much of it took testing until we were able to see information start to show up in the correct fields. 

The first problem was in realizing that I had set up the tags in my individual entries incorrectly.  So I had to go back through all the entries and change them from a simply comma separated format, to what is show at [http://www.yaml.org/](http://www.yaml.org/spec/1.2/spec.html#id2761292).  Once the tags were set up correctly, the rest of the code was rather simple.

Simple, but still something that Robey had to help me with largely.  I understand it now, however it was in a language I was not familiar with.  The tagging system was in liquid, another language that is related to Ruby.  Ruby is the language that Jekyll was written in, and Jekyll is the software that sets up my blogging system (created by [mojombo](https://github.com/mojombo)).  

Despite it being in several different languages, I've gotten the hang of 'programming languages' enough that I can start to grasp the basic syntax differences more easily than before.  The language or symbol shock isn't nearly as bad either.  The code was written rather simply in two parts.  The organization is presented on the main blog page, under the *blog content* section on the right side.  The second is a separate page created for viewing the organized blog content, the page where you can peruse all the tags.  
