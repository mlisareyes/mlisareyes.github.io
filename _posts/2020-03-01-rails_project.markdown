---
layout: post
title:      "Rails Project "
date:       2020-03-01 18:49:12 -0500
permalink:  rails_project
---


This is a test. There is no content yet. Content will be added later on. 

Under Construction.

Object associations are one of those topics that I felt seemed simple enough to understand, but hard when putting it into code. It took me some time before I started my Rails project because I was trying to wrap my head around what exactly associations are. This led me to overthink how I need to implement it into my app for it to function well. 

Here’s how I made sense of the chaos in my brain:

**1. What do I want my app to do?**
•	A doctor, or in this case a user, could keep track of their patients and appointments
•	Doctor can enter a new patient in the system with their information
•	Doctor can schedule an appointment with a patient already in the system
•	Doctor can write notes on the patient, which includes notes during a patient’s visit with the doctor
•	Patient is only a specific doctor’s patient if an appointment is scheduled

**2. How will a User be connected to the Patient?**
•	Create a many-to-many relationship; a doctor can have many patients, and patients can have many doctors through appointments.  

**3. Could another object model be used to connect a patient and a user? **
•	I found out that this was not necessary. I had another object model, Notes, but after debate, it made sense that a user should only make a note on a patient if there’s an appointment with them.

**4. How do you delete an object when there’s a foreign key?** 
`*	Dependent: :Destroy`

I ran into an error when a user could not delete their own patient because the user was not directly assoctiated with the patients, it was through appointments. Adding that one line solved the problem. 












