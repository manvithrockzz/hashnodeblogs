---
title: "Understanding the Call Stack in JS🧿🔥"
seoTitle: "CALLSTACKS is all about in WEBDEVELOPMENT"
seoDescription: "The call stack: JavaScript's function tracker. It maintains execution order. Functions added on top, removed when done. Code's faithful guide."
datePublished: Fri Jul 21 2023 08:32:09 GMT+0000 (Coordinated Universal Time)
cuid: clkcbp0kv00000al5aitr58mv
slug: understanding-the-call-stack-in-js
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689754691358/7b7c459f-265b-490d-88a3-cb2baafa6250.jpeg
tags: javascript, web-development, javascript-framework, mern, callstack

---

This article aims🚀 to provide a clear explanation of what the call stack is and why? it is important in JavaScript. Understanding the call stack will help you grasp how to `function hierarchy and execution order function` in the JavaScript engine.

Before we delve👀 into the details, let's begin💪 by answering the below questions:

# What is LIFO?

LIFO stands for "Last In, First Out," and it is a principle commonly used in data structures, including the call stack. In LIFO, the last item added to the structure is the first one to be removed.

```javascript
void Bar()
{
    Console.WriteLine("Bar");
}

void Foo()
{
    Bar();
}

void Main()
{
    Foo();
}
```

1. When the `Main()` function is called, it is added to the call stack.
    
2. Inside `Main()`, the `Foo()` function is called, so `Foo()` is added to the stack above `Main()`.
    
3. Inside `Foo()`, the `Bar()` function is called, so `Bar()` is added to the stack above `Foo()`.
    
4. When `Bar()` finishes executing, it is removed from the stack.
    
5. Control returns to `Foo()`, which then completes its execution and is removed from the stack.
    
6. Finally, control returns to `Main()`, which completes its execution and is removed from the stack.
    

**output:**

```javascript
Bar
```

When you run the code, it will start by calling the `Main()` function. Inside `Main()`, it calls the `Foo()` function. Inside `Foo()`, it calls the `Bar()` function.

The execution follows these steps:

1. `Bar()` function prints "Bar" to the console.
    
2. Control returns to `Foo()` function, which then completes its execution.
    
3. Finally, control returns to `Main()` function, which also completes its execution.
    

Therefore, the **output** in the console will be "Bar"

# What is a call stack?

> ***In simpler terms, the*** `call stack` ***is a mechanism that JavaScript uses to keep track of function calls. It plays a crucial role in maintaining the order in which functions are executed.***

# How the Call Stack Works👇:

Imagine a **stack of plates**🍽️, where you always place a new plate on top and remove the topmost plate when needed. Similarly, the call stack operates based on the "last in, first out" principle (LIFO). When a function is called, it is added to the top of the stack. If that function calls another function, the new function is placed on top, forming a stack of function calls. The last function added to the stack is the first one to be executed, and when a function completes its execution, it is removed from the stack.

To better understand this concept, let's consider a simple example:

```javascript
function greet() {
  console.log("Hello!");
}

function welcome() {
  greet();
  console.log("Welcome!");
}

function main() {
  welcome();
  console.log("Main function executed.");
}

main();
```

Internally,

1. When `main()` is called, and it is added to the call stack.
    
2. Inside `main()`, `welcome()` is called, so `welcome()` is added to the stack above `main()`.
    
3. Inside `welcome()`, `greet()` is called, so `greet()` is added to the stack above `welcome()`.
    
4. When `greet()` finishes executing, it is removed from the stack.
    
5. Control returns to `welcome()`, which then completes its execution and is removed from the stack.
    
6. Finally, control returns to `main()`, which completes its execution and is removed from the stack.
    

**output💀:**

```javascript
Hello!
Welcome!
Main function executed.
```

By observing the call stack in this example, we can see how functions are added and removed from the stack, maintaining the correct execution order.

# Conclusion😭:

**The key takeaways from the call stack are:**

1. It is `single-threaded`. Meaning it can only do one thing at a time.
    
2. Code execution is `synchronous`.
    
3. It works as a`LIFO — Last In, First Out data structure`.
    

Understanding🧩 the call stack and how it handles function calls is fundamental to comprehending the flow and behaviour of your JavaScript code. It helps you ensure the correct execution🔍 order and avoid potential errors or unexpected outcomes.

Thank you for reading this article!

I hope it provided you with valuable insights on "Understanding all about call-stacks". Farewell💖, and best of luck in your endeavours!