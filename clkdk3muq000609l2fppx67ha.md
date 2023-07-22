---
title: "Understanding Callback Functions📞🔙"
seoTitle: ""Mastering Callback Functions in JavaScript: A Guide""
seoDescription: ""Learn how to harness the power of callback functions in JavaScript for handling asynchronous tasks. A comprehensive guide to using callbacks effectively.""
datePublished: Sat Jul 22 2023 05:15:14 GMT+0000 (Coordinated Universal Time)
cuid: clkdk3muq000609l2fppx67ha
slug: understanding-callback-functions
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689915975922/39a8ebe6-4d9c-4949-8724-61789da76c38.png
tags: web-development, backend, reactjs, frontend-development, callback-functions

---

# Welcome🤌

to this interactive blog where we will delve deeper into the world of callback functions in JavaScript! 🚀

In JS, `functions` are first-class citizens, meaning they can be passed around as arguments to other functions. A callback `function` is simply a `function` that is passed as an argument to another `function` and gets executed later, often after an asynchronous operation completes.

# **What is a callback function?💭**

There is no standard definition of what a `callback function` is, but callback functions are very common in `asynchronous programming`. The callback function is a function that is passed as an argument to another function.

The function that receives the callback is known as the `Higher-Order Function`. The callback function is then invoked inside the higher-order function to perform some specific action, routine, or event.

```javascript
// Example of a Higher-Order Function
function higherOrderFunction(callback) {
  // Perform some operations or async tasks here
  return callback();
}
```

## **Why Do We Need Callback Functions in JS? 😫**

javascript is primarily a `synchronous` scripting language, which means code runs in top-down order. However, there are situations where asynchronous behaviour is necessary and for that, we use call backs.

Callback functions are especially useful in scenarios where certain operations take time to complete, such as fetching data from a server, reading files, or responding to user interactions. By using callbacks, we can ensure that specific code executes only when the necessary data is available or a particular event occurs.

For instance, when using `setTimeout()` or `await`, the code beyond that block may start executing before the asynchronous code finishes, leading to errors or unexpected results.

Consider the following example:

```javascript
function do_sum(num1, num2) {
  var sum = 0;
  setTimeout(function() {
    sum = num1 + num2;
  }, 1000);
  return sum;
}

var sum = do_sum(10, 20);
console.log(sum); 

// Output: 0
```

In this case, the `do_sum()` function returns 0 even before the asynchronous addition is completed.

To avoid such issues, `callback functions` come to the rescue! By using a callback, we ensure that the `callback function` runs only after the containing function has completed its execution.

## **Implementing Callback Functions 💡**

Let's reimplement the above example using a `callback function`:

```javascript
function do_sum(num1, num2, callback) {
  var sum = 0;
  setTimeout(function() {
    sum = num1 + num2;
    // Call the callback function and pass the result
    callback(sum);
  }, 1000);
}

do_sum(10, 20, function(result) {
  console.log(result); // Output: 30
});
```

Here, the `do_sum()` function takes an additional parameter, which is the callback function. The callback is executed only after the asynchronous operation inside `do_sum()` is complete.

## **Types of Callback Functions 👇**

There are two types of callback functions:

## **Synchronous Callbacks 🔂**

Synchronous callbacks execute immediately during the execution of the higher-order function. They block the execution until the callback completes its task. Here's a simple example:

```javascript
// Higher-Order Function with Synchronous Callback
function synchronousHigherOrder(callback) {
  console.log("Before callback execution");
  callback(); // Execute the callback immediately
  console.log("After callback execution");
}

// Synchronous Callback Function
function synchronousCallback() {
  console.log("This is a synchronous callback function.");
}

// Calling the Higher-Order Function with Synchronous Callback
synchronousHigherOrder(synchronousCallback);
```

```javascript
// Output:
Before callback execution
This is a synchronous callback function.
After callback execution
```

In this example, the `synchronousHigherOrder` function receives the `synchronousCallback` function as a parameter. The `synchronousCallback` is executed immediately inside the `synchronousHigherOrder` function, blocking the execution until the callback is completed.

## **Asynchronous Callbacks 🥸**

`Asynchronous callbacks` are executed after the higher-order function has completed its execution. They are non-blocking, allowing the higher-order function to proceed without waiting for the callback.

Here's an example:

```javascript
// Higher-Order Function with Asynchronous Callback
function asynchronousHigherOrder(callback) {
  console.log("Before setTimeout()");
  setTimeout(function() {
    callback(); // Execute the callback after a delay
  }, 2000);
  console.log("After setTimeout()");
}

// Asynchronous Callback Function
function asynchronousCallback() {
  console.log("This is an asynchronous callback function.");
}

// Calling the Higher-Order Function with Asynchronous Callback
asynchronousHigherOrder(asynchronousCallback);
```

```javascript
//Output:
Before setTimeout()
After setTimeout()
This is an asynchronous callback function. (after 2 seconds)
```

In this example, the `asynchronousHigherOrder` function receives the `asynchronousCallback` function as a parameter. However, notice that the `asynchronousCallback` is executed after a delay of 2 seconds due to the `setTimeout` function. The `asynchronousHigherOrder` function doesn't wait for the callback to complete and continues its execution.

## **When to Use Callbacks? 🤫**

Callbacks are particularly powerful when dealing with `asynchronous functions`, such as waiting for files to load or making API requests.

Here's an example illustrating the use of callbacks for simulating a delayed function call.:

```javascript
// Simulated Asynchronous Function using setTimeout and Callback
function delayedFunction(callback) {
  setTimeout(function() {
    console.log("This function is executed after a delay.");
    callback(); // Invoke the callback function
  }, 2000); // 2 seconds delay
}

// Callback Function to Be Executed After Delay
function callbackFunction() {
  console.log("Callback function is executed.");
}

// Calling the Delayed Function with Callback
delayedFunction(callbackFunction);
```

In this example, we have a function called `delayedFunction` that simulates an asynchronous operation using `setTimeout`. Inside `delayedFunction`, we set a timeout of 2 seconds using `setTimeout`. After the delay, it logs a message and then calls the `callback` function passed as an argument.

The `callbackFunction` is the callback that will be executed after the delay. When `delayedFunction` completes its timeout, it invokes the `callbackFunction`.

When you run this code, you will see the following output:

```javascript
This function is executed after a delay.
Callback function is executed.
```

# **Key Conclusions:🔐**

* When you want one function to execute only after another function has completed its execution, we use `callback functions` in JavaScript.
    
* It needs to pass as a `parameter` to other functions to make a function callback. The function which accepts the callback as a parameter is known as the `"High order function".`
    

I hope, you now have a deep clarify the concept of `Synchronous and Asynchronous` Callbacks and demonstrate their significance in handling asynchronous tasks.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689915615948/83ef6ba5-1585-42c9-933d-1355bb98cfcf.gif align="center")

Happy coding! 🚀

Thanks for reading! 💗