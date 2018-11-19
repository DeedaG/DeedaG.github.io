---
layout: post
title:      "Sinatra Project"
date:       2018-11-19 20:49:16 +0000
permalink:  sinatra_project
---



I believe I am finished with my sinatra project.  I am waiting to check in with my project lead.  I am a bit unclear about one piece of it, but it works well as is.  My post today will walk through my efforts to put the application together.


My project is built for a dental database.  It provides storage for a dental practice for patient and assistant information and records.  I began by opening a new repository in github, and followed Avi's video review on authentication.  I didn't have much trouble following the video to set up config.ru, gems, session secret, controllers, login, logout and helper methods.  I ran into an issue in my config.ru file with Activerecord migration error message.  I had to add 'context' into the needsmigration? phrase.  Otherwise, I got an error message and found that perhaps this is a newer version.  I used password digest to authenticate the password and 'validates presence of' to validate new objects.

After working out a few kinks with mispellings, I began to run migrations for a dentist table and a patient table.  A Dentist has many Patients and a Patient belongs to a Dentist.  I added model files for each of these classes and included the appropriate relationships.  Then, I ran 'shotgun,' to make sure the wiring was correct enough to produce output and feedback for the user.  Luckily, it worked smoothly.  

I set up a login form and signup form from avi's video on authentication and was able to signup and then login through signup routes in a dentist_controller.  I made a route for '/patients' to display a list of all patients.  Since there were none, yet, I added patients through ''shotgun' to make sure they would save.  I was able to see what worked and what didn't work from that interaction.  I then added create, read, update, and delete routes in the patients_controller.  There were some kinks in all of these, but I worked them out by reviewing the restful routes lab, the authentication video, and shotgun interactions. 

Once the patients_controller was working, I created a migration to create an assistants table and then added an assistants model.  After running rake db:migrate, I copied the routes from the patients_controller to a newly created assistants_controller.  I merely changed the names from patient to assistant.  This worked fairly quickly.   I tested the adding, editing, and deleting actions in shotgun and added some tweeks to the wording of the index, new, edit, and show pages.  

First of all, the signup page needed a login option for a dentist who was already signed up.  Next the index page needed buttons to view each patient in the directory and the same for the assistant directory.  Then, the show page needed options to return to the patient or assistant directories and also to edit and delete.

Finally, I added readme and spec.md files.  I explained my code that met requirements and put together a readme narrative.  Throughout the coding work, I committed my changes to github with short explanations.  Sometimes, I needed to just save my work while I was figuring things out, but it helps to know where I stopped tinkering each time.

Next, I will put together a video of the working code and create a video of myself thinking through the creating process of this application.  

Happy coding,




I

belongs_to: dentist

has_many :patients

Rake db:migrate provides a schema that I can refer to 
