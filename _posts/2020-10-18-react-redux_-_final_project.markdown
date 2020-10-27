---
layout: post
title:      "React-Redux - Final Project"
date:       2020-10-18 22:41:21 -0400
permalink:  react-redux_-_final_project
---


I have finally made it to my last project of my Flatiron School journey where I was met with the task of creating a project that implemented React and Redux. This project has been the most difficult project during my journey at Flatiron, because this is the first project where I had to navigate the waters on my own, and didn’t really know where to go or even where to start. Although I’d like to talk about the various topics within React and Redux, for simplicity’s sake, I will explain [redux-thunk](https://github.com/reduxjs/redux-thunk).

**What is Redux Thunk?**
Redux Thunk is a popular [middleware](https://redux.js.org/advanced/middleware) used in Redux to make asynchronous requests in Redux. The use of Redux Thunk allows for delayed actions. To better understand this, the word “thunk” by itself is a programming technique used to delay a calculation or computation until its result is needed. 

**Why Is Redux Thunk Useful?**
Without the use of the Redux Thunk middleware, Redux will only be able to support synchronous data flow, where you would have to be mindful of when the action creators you are calling, where you would have to specify which ones run first. With Redux Thunk, action creators can dispatch the result of other action creators without needing to know whether they are synchronous or asynchronous. 

**What Does Redux Thunk Do?**
1. It allows you to return a function inside of the action creator, whereas normally, it would return a plain JavaScript object. 
2. This function then receives the store’s dispatch function as its argument, and then this allows you to dispatch multiple actions from that returned function. 

Strangely, “actions” in Redux don’t actually do anything because they’re just plain JavaScript objects. Without the function within the action that you are able to use because of Redux Thunk, that action won’t actually do something. 

Even after finishing the project, I still struggle with grasping various concepts with React and Redux, but the beauty of coding is that there’s always more to learn, and thus, master. In truth, I, like many other coders new to both React and Redux, still struggle with grasping Redux Thunk, so I open the floor to any critiques of this blog. If there’s anything I learned from Flatiron School, it’s that coding wasn’t meant to be learned alone, and that the only way I’ll learn to grasp this material more is to just keep coding! 
