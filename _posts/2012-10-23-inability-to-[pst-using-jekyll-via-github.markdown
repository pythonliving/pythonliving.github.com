---

layout: post
title: Inability to post using jekyll via github, due to lack of pagination
tags: 
 - 2012
 - Programming

---

About two weeks ago I attempted to post an entry on my blog.  It would show up in my log history on Github, would show up in dropbox where I store my posts, but wouldn't be visible on the site.  I wasn't receiving any error messages from Github; I also wasn't receiving any messages regarding a successful page build.

Robey thought it might be that the site was unable to post it, due to the fact that it was rendering every single one of my 200+ blog entries on the main page.  That was a problem I'd been meaning to fix for a while, but hadn't gotten around to it because I knew it meant diving into aspects of jekyll I still was unfamiliar with.  Looks like it caught up with me.

Last night Robey and I went through the [jekyll](https://github.com/mojombo/jekyll/wiki) documentation and inserted in the necessary code to make pagination.  For those who don't know, **pagination** *is the process of dividing (content) into discrete pages, either electronic pages or printed pages*(see [wikipedia](http://en.wikipedia.org/wiki/Pagination) for more info).  

Now my main page only renders 10 blog posts per page, and at the bottom of the page there are **Previous** and **Next** buttons.  This is super awesome, it's really hard to explain how happy it made me to finally get this added to my blog.  Not to mention I was feeling wretched at not being able to post, considering I had already written several entries.  

And without meaning to I found the limit of posts per page for jekyll via github, being at around 280 posts for my site.  I don't know where the limit came from exactly, but it feels like research somehow.  Always feels good to see progress on your blog.   


