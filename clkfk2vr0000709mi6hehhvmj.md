---
title: "Event Loop in JS 🥱"
seoTitle: "Understanding Event Loops in JavaScript: A Simple Explanation"
seoDescription: "Discover the concept of event loops in JavaScript and how they manage the flow of tasks. Learn how event loops ensure smooth execution of events and tasks i"
datePublished: Sun Jul 23 2023 14:50:12 GMT+0000 (Coordinated Universal Time)
cuid: clkfk2vr0000709mi6hehhvmj
slug: event-loop-in-js
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689777425161/1e4b903c-9890-424d-acba-92dc4a8356c1.webp
tags: javascript, web-development, javascript-framework, frontend-development, event-loop

---

Welcome to an interactive journey🚀 into the world of the event loop!

In this blog💀, we will explore the key components of the event loop and how they work together to enable asynchronous behaviour in JavaScript. By the end of this article, you'll have a solid understanding of the call stack, web API, event queue, event loop.

So, let's dive right in!

In simple terms🫡, an event loop in JavaScript is like a traffic controller that manages the flow of tasks in your code. Imagine a busy intersection where cars represent tasks or events. The event loop's job is to make sure that each car (task) gets a turn to move forward.

# Have a look at this 👇

![JavaScript Runtime Environment: Web API, Task Queue and Event Loop -  slawinski.dev](https://res.cloudinary.com/slawinski-dev/image/upload/v1648757381/javascript-runtime-environment.png align="left")

# Call Stack:

The call stack💫 is like a stack of plates🍽️. When you call a function, you place a plate on top of the stack. The function at the top is always the one being executed. When a function finishes, its plate is removed, and the one below it becomes the current function.

# Web API:

Web API🙇‍♀️ refers to various functionalities provided by the browser, like timers⌛, making HTTP requests, or manipulating the DOM. When you use these functionalities in your code, they are handled by the browser outside of the JavaScript engine.

# Event Queue:

The event queue🧿 is like a waiting line📈. When an asynchronous task completes or an event occurs, it gets added to the queue. Tasks/events wait in line until the call stack is empty and ready to execute them.

# Event Loop:

The event loop🦹 is the traffic cop👮‍♀️ of JavaScript. It constantly checks if the call stack is empty. If it is, the event loop takes the next task/event from the event queue and puts it on the call stack for execution. This ensures tasks/events are processed in the order they were added.

# Callback Execution:

Callbacks🤙 are functions that are executed later, usually after an asynchronous task completes. When an asynchronous task finishes, its corresponding callback is added to the event queue. The event loop picks🛻 up the callback and puts it on the call stack to be executed when it's its turn.

oHH, Sorry for the confusion! Let's dive into the code part thennnn.

```javascript
// Call Stack:
console.log("Start"); // [1]
setTimeout(() => {    // [2]
  console.log("Callback executed"); // [4]
}, 2000);
console.log("End");   // [3]

// Web API:
// The setTimeout function is a web API provided by the browser. It schedules the execution of the callback function after a delay of 2000 milliseconds.

// Event Queue:
// The event queue holds tasks/events waiting to be processed. In this case, the callback function is added to the event queue after the timer expires.

// Event Loop:
// The event loop constantly checks if the call stack is empty. If it is, it takes the next task/event from the event queue and puts it on the call stack for execution.

// Callback Execution:
// After 2000 milliseconds, the callback function is picked up by the event loop and put on the call stack for execution. It logs "Callback executed" to the console.

// Output:
// Start
// End
// Callback executed
```

# In summary👀,

the event loop continuously➿ checks the `call stack` and `event queue`. When the call stack is empty, it moves tasks from the `event queue` to the `call stack` for execution. This allows asynchronous operations like the `setTimeout` function to delay the execution of the callback until other synchronous code has finished🤌.

I hope this code example🤦 helps you understand the concepts of the event loop, call stack, web API, event queue, and callback execution practically!

Congratulations on mastering the event loop!

Apply your newfound knowledge🔪, create amazing web experiences, and keep pushing boundaries.

Thank you for joining us on this journey💖. Happy coding and farewell for now!