---
layout: post
title:      "Beginning Javascript"
date:       2019-05-30 00:36:32 +0000
permalink:  beginning_javascript
---



*Scope, hoisting, context, (`this`)*, and the behavior of *ES6 syntaxes* are important concepts in Javascript. Understanding how these concepts work will make Javascript much easier to learn and use.  
 
 **Scope** 
 
 Scope is a term that refers to the space where variables can be accessed.  There are three different levels of scope; global, function, and block scoping.  These levels make up the different types of boundaries where scope is determined.  
 
1. Global scope refers to window or the entire file.  Variables declared outside of functions are said to have global scope.  
  
2. Function scope refers to the environment inside a function.  Variables declared inside a function are said to have function scope.  Functions nested inside of other functions also have access to outer function variables and follow up the scope chain.  Scope chain refers to the way the javascript engine looks for variables.  Javascript begins looking for requested variables inside the current function scope and moves outward until it finds a value assigned to the called variable.  Javascript will look as far as global scoped variables if none exist in the function environment.
  
3. Block scoping refers to the variables declared in a block of code.  It is important to remember that *var* variables are not block scoped while *const* and *let *variables do have block scope.  Variables declared in blocks can only be used in the block unless they are declared with *let* or *const*.  It is helpful to have a clear understanding of var, let, and const to fully grasp the concepts of *scope* and *hoisting*. 
 
 
**Variables and Hoisting **

Variables can de declared in Javascript with var, let, and const.  Variables may also be declared without either of these, but they become global variables.  Global variables can cause unneccessary confusion because they can be overwritten without any sort of error message. 

1.*Var *declarations can also cause confusion because they get hoisted in such a way that can cause them to be accessed and read as undefined.  The Javascript engine runs in two phases, compilation and execution. Javascript assigns*var variables to an undefined value during compilation and stored in memory.  When the execution phase runs, *var** variables are read as undefined when functions are invoked if they are declared after they are used.  

2.*Let* and *const* do not work in this way and will simply return error messages if they are not assigned before they are used.   Other rules concerning declaration of variables in Javascript arise when reassigning values.  *Const* values cannot be changed or reassigned while *var* and *let* variables can be reassigned.  Lastly, it is important to remember that *var* variables are not block scoped, while const and let are block scoped. 
 
 
**Context and `This`**

*Context* is another important concept that refers to the object to which a function belongs.  It determines the value for *`this`*.  Objects include keys that can point to functions, which are then called methods in Javascript.  The *context* of these functions is the object on which the function is called and is also equal to the value for *`this`* inside these functions.  

When creating a new instance of an object, the same rule applies.  The value of `this` is equal to the new instance because it is created in the *context* of the object on which the new operator is called. 

When a function is a stand alone function and not a method on an object, the *context* determines the value for * `this`* equal to window or undefined.  

*Context* depends on where a function is declared, and so *`this`* does also.  Every time a new function is declared, a new context is created unless it is created with an *arrow function* which does not get its own context.    


**ES6 syntaxes**
 
 *ES6 syntaxes* refer to the more recent version of Javascript that makes *const* and *let* available options for declaring variables.  They are not hoisted in the same way that *var*  variables are treated, and cause less confusion if variables are not declared before functions are invoked.  *Let* variables as mentioned earlier can be block scoped as well as *const*, except that *const* cannot be reassigned like *let* statements.  Most importantly, *let* and *const* variables will throw errors if they are not defined when used, which makes them easy to correct.
 
 
 **Closure**
 
 *Closure* is one last concept that is important to grasp.  *Closure* refers to the ability to work with arguments in functions and "close off" the contents of a function's environment.  This offers a way to set counters that only count inside the scope of the function.  It is a self invoking function and can only be changed by the argument that the function takes.  An example of *closure* is shown below:
 
      var count = (function () {
         var counter = 0;
         return function (startVal) {counter += 1; return counter}
      })();

   count(3); 
	      returns  4
   count(10); 
	     returns  11
  
Count becomes a function because it is assigned to a function that returns a function.  Count(startVal) can make use of the scope of the anonymous function, without changing the anonymous function.  Arguments can be passed in, but the function is not changed.      
 
