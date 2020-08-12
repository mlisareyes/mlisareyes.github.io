---
layout: post
title:      "JavaScript Project"
date:       2020-07-28 19:35:34 -0400
permalink:  javascript_project
---

**Asynchronous vs. Synchronous Programming**

Asynchronous programming is a challenging topic, especially for new web developers first learning it. What always helps me to understand a topic is to make sure that I am able to explain it simply. In order to explain what asynchronous programming is, first let me explain to you what it is not, which is synchronous programming.

Synchronous programming will run your code in the order that it was invoked, in sequential order. It will have to wait for one task to complete in order to move onto the next one. 

Take a look at the code below:

```
function endFunc() {
  console.log('End')
};

function startFunc() {
  console.log('Start')
};

function otherFunc() {
  console.log('this statement is in between the start and end')
};

startFunc();
otherFunc();
endFunc();
```

I first declared three sets of functions, and then invoked each function in a specific order. Take a look at the result:
```
Start
this statement is in between the start and end
End
```

The functions called above printed to the console in the order in which it was invoked.


On the other hand, in asynchronous programming, JavaScript will allow you to execute other tasks while awaiting completion of another task. Simply put, you don’t have to wait for one request to complete before moving onto the next request.

Take a look at the code below:
```
console.log('Start');

setTimeout(() => {
  console.log('We are in the timeout');
}, 5000);

console.log('End')
```

The above code shows a console.log that will print out ‘start’

Then a setTimeout function which takes in callback function that will run after at least 5 seconds.

Then, another console.log is invoked to print out ‘end’

The result below shows that it didn’t print out in sequential order. What happened is that the console.log didn’t wait for the setTimeout function to finish running. It printed ‘End’ while the setTimeout function was running and waiting 5 seconds to print the statement. 

```
Start
End
We are in the timeout
```
