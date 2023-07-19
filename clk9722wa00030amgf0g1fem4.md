---
title: "All you Know about JS Closures 💀"
seoTitle: "Closures in JavaScript"
seoDescription: "Web Development- A closure is the combination of a function bundled together (enclosed) with references to its surrounding state."
datePublished: Wed Jul 19 2023 03:59:02 GMT+0000 (Coordinated Universal Time)
cuid: clk9722wa00030amgf0g1fem4
slug: all-you-know-about-js-closures
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689738854070/f72a17a0-0d5a-4755-9bdb-a2991ee86d85.png
tags: javascript, web-development, webdev, mern, closures-in-javascript

---

A detailed guide!

> A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function's scope from an inner function.

To fully understand the concept of closures, you need to understand variable accessibility, blocks, and lexical environments in JavaScript.

# Code Blocks :

In JavaScript, code blocks are used to group statements together💪 and define a new scope. They are denoted by curly braces {}. Here's a simple example to illustrate code blocks:

```javascript
// Variables declared within a block are only accessible within that block
{
  let x = 10;
  console.log(x); // Output: 10
}
// Accessing the variable outside the block will result in an error
console.log(x); // ReferenceError: x is not defined
```

This applies to any blocks of code, such as if statements, for and while loops, functions, object Literal Declarations, and so on😭.

## **Nested Functions in JavaScript**

A nested function means a function inside a function🔎.

**For example:**

```javascript
function outerFunction() {
  const outerVariable = 'I am from the outer function';
  function innerFunction() {
    console.log(outerVariable);
    console.log('I am from the inner function');
  }
  innerFunction();
}
outerFunction();
```

If we talk about code blocks, a nested function is a block of code inside a block of code.

Next, we see a little interesting!

## **Lexical Environment**

A lexical environment in JavaScript is an internal data structure that holds variable and function declarations within a specific scope. It determines the accessibility and visibility of variables, functions, and other identifiers during runtime🚀

When JavaScript code is executed💀, lexical environments are created and associated with different scopes, such as global scope, function scope, or block scope. Each lexical environment consists of two main components:

* **Environment record:** is the actual place where the variable and function declarations are stored.
    

* **Reference to the outer environment:** means it has access to its outer (parent) lexical environment.
    

**Example:**

```javascript
function outerFunction() {
  const outerVariable = 'Hello';

  function innerFunction() {
    console.log(outerVariable);
  }

  innerFunction();
}

outerFunction();
// Output: Hello
```

In this example, the output is `Hello`. When `outerFunction` is called, it executes the `innerFunction`, which logs the value of `outerVariable` to the console. Since `innerFunction` has access to the lexical environment of its containing scope (`outerFunction`), it can successfully access and print the value of `outerVariable`.

# Closures:

A closure is a behaviour that occurs when a nested function "remembers" and retains access to variables from its outer scope, even after the outer function has finished executing.

```javascript
function outerFunction() {
  const outerVariable = 'Hello';

  function closureFunction() {
    console.log(outerVariable);
  }

  return closureFunction;
}

const closure = outerFunction();
closure();
//Output: Hello
```

In this example, the output is also `Hello`. The `outerFunction` returns the `closureFunction`. When `outerFunction` is called and assigned to the variable `closure`, it creates a closure. The closure retains access to the `outerVariable` defined in its outer scope. Calling `closure()` invokes the `closureFunction`, which logs the value of `outerVariable`. The closure successfully "remembers" the value of `outerVariable` even though `outerFunction` has finished executing, resulting in the output of `Hello`.

### Ohh,,, Sorry for the confusion😮‍💨!

# Let's see how Closure and Lexical environment is related.

* Lexical environments are like containers that hold variables and functions within a scope.
    
* Closures are a behaviour that occurs when a nested function retains access to variables from its outer scope, even after the outer function has finished executing.
    
* Lexical environments enable closures by providing a way to capture and preserve variables for later use.
    

# **Conclusion**

Today you learned😍 how closures work in JavaScript.

To put it short, when you have a function inside another function, a closure is automatically created.

A closure means a function has access to the scope of the outer function. This applies even when the outer scope is destroyed.

![Describe closure concept in JavaScript - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/20210806202827/CLOSUREcopy-660x289.jpg align="left")

* A closure function can access variables from the surrounding function even after it has finished executing.
    
* This behaviour is possible because of lexical environments.
    
* Every block of JavaScript code has its own lexical environment.
    
* Lexical environments store variables and properties specific to that block of code.
    
* When you create a nested function, it keeps a reference to the lexical environment of the outer function.
    
* This reference allows the inner function to continue accessing the variables from the outer function even after the outer function has completed execution.
    

Thanks for reading.

Happy coding!

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689738958204/e62a3933-ebc2-47c0-8bd3-e3df1d9acc80.gif align="center")