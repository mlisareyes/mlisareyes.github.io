---
layout: post
title:      "JavaScript Project"
date:       2020-07-28 19:35:34 -0400
permalink:  javascript_project
---


TOPIC: AJAX

It's hard to explain something that you don't quite understand, even if you read 20 different definitions of it. That's the issue I came across when trying to understand AJAX, or Asynchronous Javascript and XML. In theory, it made sense, but implementing it was a whole different thing. I didn't quite understand it until I ran into an issue with my code where I had to implement it.

The simplest way I can explain AJAX is that it's a set of development techniques that can be used in JavaScript to update a web application without reloading or refreshing a the web page bring you to a different URL. In other words, data is being loaded asynchronously, which means that not only can you update a web page without reloading it, you are also requesting and receiving data from a server after the page initially loaded. A user will be able to continue using the web page while information is being requested from the server in the background. However, instead of using XML, I used JSON to pass the AJAX updates between the client and server. 

**My goal:**
I wanted to be able to click on an employee name within the recognition feed section of my web app, which would load information onto the web page without loading a new page to show all of the recognitions given to that employee. Basically, I wanted to fetch all the employee data from the server so that it would show up on the page. 

**Issues I ran into:**
Being unable to grab the <h3> element from the HTML document for each employee.

Being able to fetch the employee data after the click event is implemented, so that all the associated recognitions are rendered onto the page

**Solutions:**
I suddenly realized that I had to loop through the array of employee ids/names to grab each h3 element, not just one.

I needed to make sure that the app would first make a request to the server to grab all the recognitions, then it would render onto the web page. After that information is rendered, then a click event could occur, which would then initiate a request to the server for the employee data which contains all of its associated recognitions.
