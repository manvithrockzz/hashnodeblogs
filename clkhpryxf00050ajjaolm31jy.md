---
title: "Arrow Function in JS🥵"
seoTitle: ""Arrow Functions in JavaScript: Empower Your Code""
seoDescription: ""Discover the power of arrow functions in JavaScript. Learn their concise syntax, lexical scoping, and how they revolutionize coding. Embrace cleaner code n"
datePublished: Tue Jul 25 2023 03:05:13 GMT+0000 (Coordinated Universal Time)
cuid: clkhpryxf00050ajjaolm31jy
slug: arrow-function-in-js
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1690116768025/02620b5d-7e1a-4c01-aa90-049414125144.jpeg
tags: javascript, web-development, nodejs, reactjs, arrowfunction

---

Hey there, fellow developers!

Today👀, we're going to dive deep into the wonderful world of arrow functions in JavaScript. Arrow functions were introduced in ECMAScript 6 (ES6) and have since become a popular and powerful feature.

# Fundamentals,

Let’s revise😚 some basics before getting into the concept of the `arrow function`. There are `two` well-defined ways of defining the function in JS and you must surely have an idea about this before getting into the concept of the `arrow function`

```javascript
// Example 1 : 
function add(num1, num2) {
  return num1 + num2;
}

// Example 2 : 
var sum = function (num1, num2) {
  return num1 + num2;
};
```

The above examples are simple and it’s okay for most of you, but some of you might not know😂 about the `second way`. Both functions have some different behaviours and for those who don’t know let me tell you that.

`Function 1` is hoisted and `Function 2`isn’t. Hosting means you can call the function before defining and it will work.

If you wanna know more about, Hoisting, feel free to explore❤️‍🔥 more about it.

# **Introduction🤌**

> ***One of the most popular features introduced in ES6 is the arrow function (also known as the fat arrow function). It’s a concise way of defining function.***

![The Difference Between Regular Functions and Arrow Functions | by Ashutosh  Verma | Better Programming](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS0hjIkaTM6YKmad_mQKwvHLIzMfklQS48gaWxPwEj9uelxQrXboEWbD9J8YR2LYRgV4ZQ&usqp=CAU align="left")

`Arrow functions` are a compact and concise way to write functions in JavaScript. They provide an alternative syntax to traditional function expressions

ok,ok,ok, I got youuuu. Will get your all doubts, I promise.

## **What are Arrow Functions?**

An **arrow function expression** is a compact alternative to a traditional [function expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function), with some semantic differences and deliberate limitations in usage:

* Arrow functions don't have their own [bindings](https://developer.mozilla.org/en-US/docs/Glossary/Binding) to [`this`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this), [`arguments`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments), or [`super`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super), and should not be used as [methods](https://developer.mozilla.org/en-US/docs/Glossary/Method).
    
* Arrow functions cannot be used as [constructors](https://developer.mozilla.org/en-US/docs/Glossary/Constructor). Calling them with [`new`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new) throws a [`TypeError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError). They also don't have access to the [`new.target`](http://new.target) keyword.
    

# **Writing your first arrow function🧨**

write your `first arrow function` and run it. There is **two way of writing the arrow function** and both have a different use case.

```javascript
// Example 3 : Arrow Function are mostly written as below
var yourname = () => {
  console.log("My name is manvith");
};

// Example 4 : Arrow function can also be written as below
var yournameprint = () => console.log("My name is printing");
```

> ***The arrow function can’t be hoisted, which means you need to define it before using it.***

# Difference between Arrow Fn and Regular Fn? 🫠

`Arrow functions` and `regular functions` (also known as traditional functions) share a lot of similarities, but there are some crucial differences💭 between the two.

Let's Explore those!

1. **Syntax:**
    
    * Arrow Functions: Concise syntax using `=>`.
        
    * Regular Functions: Defined with `function` keyword, function name, and curly braces.
        
2. `this` **Keyword:**
    
    * Arrow Functions: Lexically inherit `this` from surrounding code.
        
    * Regular Functions: Have their own `this` context, which can change based on how they're called.
        

**Example: Using** `setTimeout`

```javascript
const car = {
  brand: "Tesla",
  model: "Model S",
  honkArrow: () => {
    console.log(`Arrow: ${this.brand} ${this.model} honks!`);
  },
  honkRegular: function () {
    console.log(`Regular: ${this.brand} ${this.model} honks!`);
  },
};

setTimeout(car.honkArrow, 1000);
setTimeout(car.honkRegular, 2000);
```

In the above example, We can see the `honkArrow`(Arrow Functions) doesn’t have its own `this`, But the `honkRegular`(Regular Function) has it’s own `this` binding.

Also,

* Arrow functions don't have their own `this` context; they inherit it from the surrounding code.
    
* Regular functions have their own `this` context, which is determined by how the function is called.
    

As a result, `arrow functions` may lead to unexpected behaviour 😇 when accessing `this`, especially in object methods or asynchronous code. Regular functions are generally safer in such cases.

# **Implicit return🫡**

Regular functions usually require a `return` statement to provide a result. If the `return` statement is missing, the function will implicitly return `undefined`.

In contrast, arrow functions have a special behaviour:

if they contain a single expression, they will automatically return the result of that expression without needing an explicit `return` statement. This makes arrow functions more concise in such cases.

**See the example below:**

```javascript
// With Regular functions
function add(a, b) {
  return a+b;
}
sum(10,20); // Output: 30


// With Arrow functions
const add = (a, b) =>a+b;
sum(10,20); //Output: 30
```

# **Conclusion💁‍♀️**

`Arrow functions` have revolutionized JavaScript by offering concise syntax, lexical scoping, and avoiding `this`\-related issues. Use them judiciously and consider the context of use for cleaner, more readable code.

Hopefully, this article helped you learn about JavaScript `arrow functions`, how they work and how to use them.

Now Go, Master arrow functions,

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690116229897/41f2dd6b-2305-4c5e-bf56-ce73a0252cc2.gif align="center")

code elegantly. Happy coding!

Feel Free to hit the red-hearts!💗