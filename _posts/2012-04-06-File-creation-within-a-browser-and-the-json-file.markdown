---
layout: post
title: File creation within a browser and the .json file
tags: 
 - 2012
 - Programming
 - CSP Schedule Converter
---

The last function of the CSP Schedule Converter code written is a function that puts the data produced in the previous functions into their subsequent files.  Here is the code, shown below:

   var downloadDataURI = function(options) {
      options.url || (options.url = "http://download-data-uri.appspot.com/");
      $j('<form method="post" action="'+options.url+'" style="display:none"><input type="hidden" name="filename" value="'+options.filename+'"/><input type="hidden" name="data" value="'+options.data+'"/></form>').submit().remove();}

The first line first asks whether there is an options.url location already in existence.  If there isn't one, then it uses the one shown in the second section of this line.  This is necessary, however why will not make sense until I explain the next function shown.  

This next function is a jQuery function that creates a form, inputs all the information created by the previous functions discussed, and then submits it and then hides the form.  In order to create a file, like I wanted to here, you must submit the information into a form.  

The important part of the options.url is that the form cannot be submitted unless the options.url has a location specified.  The last aspect of creating this **page action** for the Chrome web store, was the creation of a manifest.json file.  

This file specifies all the necessary information for the **page action**.  You start by creating a file called 'manifest.json'.  Inside of this file the following information is contained:

    {
      "name": "CSP Game Schedule Converter",
      "version": "1.1",
      "icons": {"128": "icon.png"},
      "description": "Creates downloadable ics and csv files that you can import into Microsoft Outlook, iCalendar, and Gmail Calendar.",
  
      "content_scripts": [
        {
          "matches": ["https://secure.sports-it.com/mysam/*"],
          "js": ["jquery-1.5.1.min.js","cspcalendar.js"],
          "run_at": "document_end"  
        }  
      ]
    }    

In the first section shown the name (CSP Game Schedule Converter), version (1.1), icons (128, icon.png) and description are specified.  This information is contained in an array, that Chrome interprets.  The second section is the information needed to process all of the code.  The first list, **matches** is the webpage when the script should run.  The **js** is the name or names of the files to be run once the appropriate pages have been opened.  The last part **run_at** indicates when the javascript files should be run (which in this case is once the page is done loading).

The last part needed was to put all of these files into one file folder and zip the folder.  These files are the cspcalendar.js, jquery-1.5.1.min, manifest.json, final32.png and icon.png.  Then the zipped folder is loaded into the Chrome web store.  Once those aspects are completed, simply install the **page action** into your Chrome browser via the web store and you're good to go.