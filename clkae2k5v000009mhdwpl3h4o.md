---
title: "Hoisting in JavaScript"
seoTitle: "HOISTING, hoisting in javascript, function declarations"
seoDescription: "Hoisting in JavaScript is a mechanism where variable and function declarations are moved to the top of their respective scopes during compiliation"
datePublished: Thu Jul 20 2023 00:03:08 GMT+0000 (Coordinated Universal Time)
cuid: clkae2k5v000009mhdwpl3h4o
slug: hoisting-in-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689745790904/80cc5765-77c0-4279-ab77-4065461a8de1.png
tags: hosting, javascript, web-development, javascript-framework

---

# What is Hoisting in JavaScript?

Hoisting in JavaScript is a mechanism😮‍💨 where variable and function declarations are moved to the top of their respective scopes during the compilation phase, before the code is executed.

# Variable Hoisting:

Here's an example to illustrate hoisting🚀:

```javascript
console.log(x); 
var x = 10;
// Output: undefined
```

You might wonder, why the output is `Undefined` ??

In the above code, even though `x` is accessed before it is declared, it doesn't result in an error. This is because🫡, during hoisting, the variable declaration `var x` is moved to the top of its scope. However, the initialization `x = 10` is not hoisted, so `x` has an initial value of `undefined` when it is logged.

# Hoisting of `let` and `const` Variables:

The big difference😭 between var and const/let hoisting. Behind the scenes, variables that are declared with `let and const` are also hoisted, but unlike var, they do not receive the default value of `undefined`.

So what happens if we call let/const variables before they are initialized?🤔

This means that hoisted `let` and `const` variables are in the "temporal dead zone" (TDZ) until they are actually declared in the code.

Accessing `let` and `const` variables before their declaration in the code will result in a `ReferenceError`.

<mark>Example 1:</mark>

```javascript
javascriptCopy codeconsole.log(x); // Output: ReferenceError: x is not defined
let x = 10;
```

<mark>Example 2:</mark>

```javascript
javascriptCopy codeconsole.log(y); // Output: ReferenceError: y is not defined
const y = 20;
```

# Function Hoisting🥰

Hoisting of Function Declarations:

* Function declarations are fully hoisted, meaning they are moved to the top of their scope during the hoisting phase.
    
* This allows functions to be called before they are actually declared in the code.
    

<mark>Example 3:</mark>

```javascript
javascriptCopy codefoo(); // Output: "Hello"

function foo() {
  console.log("Hello");
}
```

<mark>Example 4:</mark>

```javascript
javascriptCopy codebar(); // Output: "Hi"

function bar() {
  console.log("Hi");
}
```

#   
Simplified Illustrations: Revisiting the Four Examples💀

* <mark>Example 1 and Example 2</mark> demonstrate the TDZ concept for `let` and `const` variables, where accessing them before declaration results in a `ReferenceError`.
    
* <mark>Example 3 and Example 4</mark> showcase the hoisting of function declarations, allowing them to be called before their actual declaration in the code.
    

# Arrow Function Hoisting👇

The hosting behaviour of `arrow functions` and regular functions are not the same. Let’s take a look at the example below:

```javascript
greet(); // Uncaught TypeError: printGreeting is not a function

var greet = () => {
  console.log("Hello World");
};
```

OH, WHY DOES IT HAPPEN😂??

In this code, when we try to call `greet()` before it is assigned, a `TypeError` is thrown. This occurs due to the following steps:

1. The variable `greet` is declared using `var`, so it is hoisted to the top of the current scope.
    
2. During the hoisting phase, `greet` is initialized with the value `undefined`.
    
3. Since `greet` is an arrow function assigned to a variable, the assignment itself is not hoisted.
    
4. When attempting to call `greet` before the assignment, it still holds the value of `undefined`, which is not a callable function.
    
5. As a result, a `TypeError` is thrown, indicating that `greet` is not a function.
    

To resolve the issue, we need to ensure that the assignment of the arrow function to the `greet` variable occurs before the function call:

```javascript
javascriptCopy codevar greet = () => {
  console.log("Hello World");
};

greet(); // Output: Hello World
```

In this corrected code, the assignment of the arrow function to the `greet` variable is done before the function invocation, allowing it to execute successfully🥰.

# Conclusion🫡:

**Now we know that**

* Hoisting doesn't physically move the code; it's a JavaScript mechanism.
    
* Understanding hoisting helps prevent bugs and confusion in your code.
    
* To avoid issues like `undefined variables` or `reference errors` due to hoisting:
    
    * Declare variables at the top of their respective scopes.
        
    * Initialize variables when declaring them.
        
* Understanding hoisting is essential for predictable JavaScript code.
    
* Structure your code based on how variables and function declarations are hoisted to prevent errors and improve readability.
    

Thanks for reading to the end!

**Happy Coding :)❤️**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689745855340/6f5399fa-6032-403c-a62f-757b7b8ffcdd.gif align="center")