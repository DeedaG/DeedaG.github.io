---
layout: post
title:      "Finishing My Javascript Project "
date:       2019-05-14 18:11:32 -0400
permalink:  finishing_my_javascript_project
---



I am finally finished with my javascript project.  I will submit it for review after writing this blog post.  I am using these blog posts for encouragement for others behind me as well as for myself.  I will break down my struggles and successes while putting this project together.  Understanding certain concepts were the key to my breakthroughs.  

 When I first started this project over a week ago, I was concerned about many aspects of javascript that I didn't completely understand.  Namely, ajax, prototypes, get requests, post requests, serializers, and jquery selectors, debugging, and "this" were concepts that I really didn't fully understand.  I can safely say that I am much more aware of their powers after struggling through this project.  **Ajax** is a cool tool that allows data to be displayed without leaving the page that you are viewing.  You can either keep information that may be necessary for a user, hide information after user interactions, or display new information.   
 
 **Prototypes** are lifesavers in that you can call any and all attributes that you might need and use them to present your views quite easily.  Along with generating a serializer for your object model, the chosen attributes can simply be pulled into methods and used any way necessary in any view.  The possibilities are endless!  Run a rails **serializer** for your object, set up a class with your model, and set "this.attribute" equal to "obj.attribute" and you can customize methods of all kinds.  Then, those methods can simply be called on a new object.
 
 **Get requests and post requests** made sense while running through the labs, but I really didn't see exactly how it all fit together until the end of this project.  Get 
 requests literally pull data from a page and then ajax can display it without a page refresh.  The difficult part of getting it working is the syntax and becoming familiar with html once again at this stage in the game.  I used a post request to display my form data, but before I got it working, I didn't realize that the form must be displayed, serialized, and then after posting to the correct page, the data is in json format and requires modification to html.  It all makes so much sense once it develops right before your eyes.  Plus, making use of inspect tools, highlighting elements and copying them is wonderful stuff.  
 
 
 Sharp lookup methods are another wonderful discovery.  Just place your id after one of these like getElementById() or div after querySelector and any place on your page can be manipulated.  functions can be run and results can be displayed in these areas or information can be obtained.  **Jquery selectors** also work easily too with $() around the element.  These element and search tools can be placed in the console for information about exactly "what" data is retrieved or "where" the search lies on the page.  
 
 
 **Debugging** is much easier with chrome.  Debugging works just like pry except that simply hovering over variables and certain data creates a display of the contents above or near.  It makes decisions about how to work with data much easier.  Placing a debugger line by line often helped me to see exactly where problems were lurking.    
 
 **"This"** is also a nifty little tool that almost works like the subject of a sentence and allows all of the data from a form or div to be help in a generic word that relates only to the current scope of the function.  Wiring of functions works easily when all pertinant data can be thrown around with this word.
 
 While these are just some concepts that are necessary for putting the Javascript project together and making it work.  These were key points that clicked for me.  The point of learning javascript even made much more sense after grasping these concepts.
 
 Happy learning!
