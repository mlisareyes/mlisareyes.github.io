---
layout: post
title:      "React: Props vs State"
date:       2020-10-27 19:22:04 -0400
permalink:  react_props_vs_state
---

Today, React is one of the most used JavaScript libraries for front-end development, and if you want to have a deeper understanding of React, you must understand the importance and the differences between state and props. Both state and props give React the ability to make it dynamic, but in different ways. However, in order to differentiate the two, we must first explain what a React Component is.

**What is a React Component?**
The [official React documentation](https://reactjs.org/docs/components-and-props.html) explains that 
> “Components let you split the UI [or User Interface] into independent, reusable pieces, and think about each piece in isolation.” 

In other words, components contain pieces of code that can be used again that directly apply to a web application’s interface (I.e. an app’s appearance, behavior, and state). 

*So what does props have to do with components?*

**Props**
There is a way to pass information to other components, and that’s through the use of props. Props are uni-directional, which means you pass the data from parent to child only. You can pass the props value into your components, which can otherwise be described as attributes or properties of data. 

**State**
In contrast, state isn’t passed down from parent to child component. Instead, state is data that is directly initialized and managed by a class component. The way state is updated is through the use of the function `.setState`, which basically initializes (or sets up) and updates state within the component. 


**The key differences:**
1. Props are used to pass down data from a parent to child component, whereas state is used for managing data within a component (cannot be accessed outside its component)
2. Props are immutable and should never be changed in a child component & state is mutable, with the ability to be mutated inside the component using the `.setState()` method. 
