---
layout: post
title:      "Finished Music Library CLI"
date:       2018-06-22 17:24:28 +0000
permalink:  finished_music_library_cli
---



Music Library CLI is a tough lab.  The most important parts are knowing who a method is being called on and knowing scope, and keeping files separate but understanding how they work together.  First, I read through the lab instructions twice, or maybe three times and watched the videos a few times at the bottom of the lab.  Then, I jumped into the error list, and read through the spec tests for each error.  I used learn --fail-fast as long as I could, but sometimes I could break down the errors a bit easier when I could look ahead to the next set of error messages.  Once I had the main model errors passing, I was able to tackle one relationship method at a time.  I had to refer back to the "has many/belong to through" labs several times to get the tests right.  The previous lessons helped a lot.   

I am getting a little better working with pry, and I used this many times to see what would happen with different ideas that I wanted to try.  There were times when I would get on a roll and methods were working and then times when i just had to walk away because I couldn't debug for the life of me.  I often think through the tough parts when i'm not looking at the screen.  When I come back, I could see the problem more clearly and it surprises me how easy some of the fixes are.  I am still very slow at this whole process.

I only set up one module, and I believe I was supposed to set up three.  By the time I got all of the tests passing, I didn't want to go back and change anything, so I just went with it.  There is no greater joy than getting a test to pass after struggling with it for a long long time!  I got stuck on #play_song forever.  I set up my #list_songs method fairly easily to puts out the correct response, but I struggled with the test for "playing songs."  I finally figured that I would just copy paste my #list_songs method into #play_songs and work backwards.  I figured out that I could convert my input to integer at the gets.strip point and that way, I could use an index of the songs array, that was already in order from #list_songs, to puts out the correct song and artist that is chosen by the user.  This sounds so easy, but it had me very confused.  These types of problems are how I often get stuck.  I understand how to make something work in theory, but syntax trips my plans.  

Until next time,

-Pluggin along...at a snail's pace


