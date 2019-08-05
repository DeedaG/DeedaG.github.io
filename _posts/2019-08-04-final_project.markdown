---
layout: post
title:      "Final Project"
date:       2019-08-05 00:59:57 +0000
permalink:  final_project
---

My final project allows a user to create a pool of mortgage loans with a name, amount, and investor.  Loans and users are already seeded in and I plan to add additional functionality later.  I currently have login functioning, full crud capability, including api requests fetched from the rails backend, and several routes.  I put this app together by trial and error.  It was definitely a learning process.  Thank goodness for error messages!!!   

I realized that I have enough components working that meet the requirements for the project.  I followed the model set up in the Globetrotter videos because i did not understand redux well and I figured that would be a great way to grasp a better level of understanding.  I used create react app and created 4 models with the scaffold generator.  Next, I worked out the relationships and attributes.  I ended up with way too many migrations, but it took a while to sort out the details of the attributes and relationships.  I seeded some of the database, and then added a few more pieces here and there in rails console.  

Next, I started working out the login process.  I built a functional component for login that includes a form with a handle change method to listen for login and and handleSubmit function for updating and reseting the login form.  Next I created action creators for updating and reseting resulting in action objects that need matching reducers.  I imported the action creators into the Login component, and built matching updating and reseting reducers with an initial state being set to blank.  Next I added the loginForm reducer to the redux store which I set up though create react app.  The store then gives back a prop through the connect function and mapDispatchToProps which boosts the capability of the action creator which then returns a change in state that reflects a logged in user.  Further, I started to work on the routes in App.js which took some batck and forth.  Including withRouter function taking in connect function as an argument is a must.

I ended up with these routes:  login, pools, pools/:id, pools/:id/edit, loans, and loans/:id/edit(which i am not using).  I am struggling to figure out how to change the pool id of loans so that a user can pick and choose which loans to add or remove from a pool.  This has turned out to be a challenge as far as research and I will work on this later because I enjoy seeing it work!  I like to use these challenges as a way to understand the wiring of these projects.  I tried 4 different approaches and even though none of them worked, I learned a lot about redux in the process.  So, it was worth all of the effort and tinkering.  Anyway, App.js is doing the job so far.  

NewPoolForm.js is another part of the process that took a lot of work.  I built a simple form for creating a new pool and have option to update and delete.  The form has event listeners to handle the user's input and submission of the form and reducers handle the adding, resetting, updating, and deleting, all of which are mostly placed in a newPoolForm reducer file that is added to the redux store.  I am making this sound quick and easy but it took a very long time to get all of that set up.  I then use the connect function to use mapStateToProps and mapDispatchToProps to make these props available in the form.  I created action creaters to match all of these reducers and import the action creators into the form.  Anything, that I forgot was fixed because I relied on errors from redux state and inspecting the console and network messages.  I used the working pieces of the app to create other code which is why I say this was trial and error learning.  

After a user can login, a navbar appears.  Before login, a user sees a home/welcome page, which includes the login route and link to get the user to it.  Always import Links frome react-router- dom, which required an extra install, btw.  The navBar component is a stateless component that includes two routes from App.js that toggle between all pools or new pool.  I used a little css two change the colors after the buttons in the navBar are clicked.  The navBar includes a logout option and connects tothe redux store and takes in the state of the current user and whether or not they are logged in.  Here, the need to set cors credentials to true in the fetch request is evident because action creators are set up for asynchronous requests for login, current user and logout. 

The credentials from cors allows sessions and cookies to be turned on to get the cookies from sessions needed for login.  The sessions controller has to include methods for current_user and logout.  Actions to get pools, loans, and reset Login form are dispatched during login and getting current user.  Actions to clear the new pool form and login form are dispatched during logout.  My Logout component includes an event listener and  the logout action creator.  App.js calls getcurrentuser function during componentDidMount after mapDispatchToProps makes it available to call.  The timing of this is important because the it needs to be fired before all of the routes are available, thus being logged in.

Next, I created reducers for setting a pool object and adding a pool with an asynchronous fetch request in a post request to the backend.  I included the reducers in the redux store and then imported the action creators into the myPools component.  Here, I display all of the pools and use routes from App.js to display information about a single pool and eventually a list of all of the loans.  It is at this point, that I realize I have enough to submit this thing for review.  








