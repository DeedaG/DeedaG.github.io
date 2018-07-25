---
layout: post
title:      "I Finished My CLI Project"
date:       2018-07-25 02:46:07 +0000
permalink:  i_finished_my_cli_project
---



I just finished my cli project.  I named it Daily Recipe and I scraped two websites that include vegan recipes.  My gem is set up to help someone try "going vegan" for 30 days.  

When the user first types daily recipe, they are asked, "how many days have you gone vegan?"  They are then prompted to choose 1 to 30 days and enter the number.  Once the number of days is captured, the value is changed to an integer and stored in an instance variable to be used as an index to collect vegan recipes from two arrays.  The arrays are set up by scraping the two websites and instantiating two new arrays of recipes and shoveling them into another array in a class method that can be used in my CLI class.  

Next, the user is shown the 2 recipes for the number of days they've been "eating vegan" and they are asked to choose which recipe they want to try by typing 1 or 2.  The recipes are displayed by iterating through the arrays and putsing out the two results for the particular "day."  Once the user chooses the recipe name, they are returned a link that includes more information about the recipe.  When they have used the program for more than 30 "days", the program tells the user that they are now a vegan and ends the program. 

I used bundle gem daily-recipe to set up a framework to start.  I added ```DailyRecipe::CLI.new.call```  to encapsulate my cli data and required bundler/setup and daily-recipe in a bin file called daily-recipe.  I put a shebang line at the top of the daily-recipe bin file to notify the system that i am working in ruby.  I then included my name and email along with a spec.name and summary about my daily-recipe gem in daily_recipe.gemspec.  Then, I made cli and recipe .rb files as well as a daily-recipe.rb file to hold dependencies.  The recipe.rb file holds scraped information and methods.  The daily-recipe.rb file holds "open-uri", "nokogiri", and "pry".  I also used require-relative for version, cli, and recipe .rb files.

The CLI and recipe classes include the DailyRecipe namespace so I can personalize my code.




