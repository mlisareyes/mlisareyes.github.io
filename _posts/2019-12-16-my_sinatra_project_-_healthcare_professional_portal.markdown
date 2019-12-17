---
layout: post
title:      "My Sinatra Project - Healthcare Professional Portal"
date:       2019-12-16 00:02:23 -0500
permalink:  my_sinatra_project_-_healthcare_professional_portal
---


If you're anything like me, then to learn and understand a topic or idea, you must be able to explain things in the most simplest of ways. 

Einstein said,


> If you can't explain it simply, you don't understand it well enough.
> 

Before starting this Sinatra project, I was only able to somewhat grasp the details of CRUD actions (Create, Read, Update, Delete), RESTful Routes and its HTTP verbs (get, post, patch, delete), and MVC (Model-View-Controller), but if someone were to ask me to explain these and how they all interact, I'd be at a loss for words.  After creating a Sinatra app from scratch, however, I was not only able to dive into the process of what is needed to fully execute my idea, but I was also able to finally articulate CRUD/MVC/HTTP verbs and how they all interact. Here's my process...

**My Idea:**

I wanted to create a portal where a healthcare professional (i.e. a doctor, nurse, med. tech) could sign up for the portal by creating a unique username and password, which would then allow the user to create patients in the system and to add information such as the patient's name, birthdate, gender, and any notes pertaining to the patient and their visit with the healthcare professional. Each user could then only view and edit the patient(s) she/he created. 
 
 **Things I've Learned From Past Mistakes:**
After I had finished my initial CLI project from a couple months ago, I was able to go over my code with a couple different instructors, and the feedback that I've gotten was crucial to begining to understand how to build the bare bones of my Sinatra project. ***Separation of concerns*** was a software developing principle that I didn't know would be valuable until now. Of course, it is important to have working code, but if it's not specfically organized in the way that separates each different element of the code for a singular purpose, then later on, it makes it difficult for you, and anyone else that touches that code, to then maintain it and extend the code with additional features. 

So here's where the **MVC** file structure comes into play. MVC, which means Models, Views, and Controllers, are used to separate each different functionality of the code. 

* **Models** represent the object/data that is being created. In my case, my model objects were *Users* and *Patients*. 
* **Views** contains code that will be displayed in the browser. In my case, it was being able to see the home page, sign up page, user home page, an index of all the patients created by the user, and the patients' detailed information.
* **Controllers** contains the HTTP verbs used for the models and views files to interact with each other.

**Below shows a table of the CRUD actions and HTTP verbs being put to use:**

|   NAME   |     PATH       |   HTTP VERB     |            PURPOSE                   |
|----------|----------------|-----------------|--------------------------------------| 
| Index    | /patients        |      GET        | Displays all patients              |
| New      | /patients/new      |      GET        | Shows new form for new blog entry    |
| Create   | /patients         |      POST       | Creates a new blog post              |
| Show     | /patients/:id      |      GET        | Shows one specified blog post        |
| Edit     | /patients/:id/edit |      GET        | Shows edit form for one blog post    |
| Update   | /patients/:id      |      PATCH        | Updates a particular blog post       |
| Delete  | /patients/:id      |      DELETE     | Deletes a particular blog post       |

 
 





