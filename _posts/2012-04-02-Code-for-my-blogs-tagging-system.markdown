---
layout: post
title: Code for my blog's tagging system
tags: 
 - 2012
 - Programming
---

I created a tagging system for my blog, so that I or others could easily peruse the entries I've written.  I figured if I ever end up writing a book about learning to program, then it would be great to have my resource already cataloged.  

In order to create my tagging system, I had to sort through all the tons of documentation on how others out there did it.  This is probably the most difficult part of programming; understanding what others have out there and how to use it.  In the end  I set mine up simply, thankfully.  If not, I might not have been able to rexplain it to you here.  

Using the blog setup [jekyll](https://github.com/mojombo/jekyll), I inserted the following code in the right side bar under **blog content**.  The code inserted is shown below in liquid/html:
		
    {{ "{% for tag in site.tags " }} %}
    <p>
    	<a href="/tags.html#{{"{{tag[0]"}}}}>{{"{{tag[0]""}}}}</a>
    </p>
    {{"{% endfor"}} %}
		
As seen on my right under **blog content**, this code provides a large list of all tags included in my blog posts.  If you click on the title **blog content**, it will take you to the tags.html page of my website.  

To create the tags page, I created a new html file.  The top section of this file is separated by the three dashes, and indicates the layout file name and the title of the page.  This section is in yaml.  The bottom section is in html/liquid.  

    ---
    layout: main
    title: betterlivingthroughpython
    ---
    {{ "{% for tag in site.tags"}} %}
    <h2><a name="{{"{{tag[0]"}} }}">{{"{{tag[0]"}}}}</a></h2>
    <ul>
    	{{ "{% for post in tag[1]"}} %}
    		<li><a href="{{"{{ post.url "}}}}">{{ "{{post.title"}}}} -- {{"{{ post.date | date: \"%B %d, %Y\" "}}}}</a></li>
    	{{ "{% endfor "}} %}
    </ul>
    {{ "{% endfor "}} %}

I use the **main** layout, so that my tags page will have the same layout imagery as the rest of the site.  The liquid section indicates that for each tag in the site's collection of tags, there should be a list of the entries with that tag(along with their titles and date posted) shown below the tag header.  Due to this structure, the same post may show up multiple times on my tags page, under multiple headers.  For each tag a post has, the post will show up in the list for those subsequent tags.

Considering the amount of documentation out there on how to organize, collect, and group your tags I'm glad I stuck with this more simplistic approach.  It may not be as dynamic, but for a beginning programmer I understand how it works and I can more easily find blog entries.       