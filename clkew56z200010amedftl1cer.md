---
title: ""this" Keyword in JS🤌"
seoTitle: "Demystifying the "this" Keyword in JavaScript"
seoDescription: "Unravel the secrets of JavaScript's "this" keyword. Learn how it works, its behavior in different contexts, and master its powerful applications. Explore pr"
datePublished: Sun Jul 23 2023 03:40:09 GMT+0000 (Coordinated Universal Time)
cuid: clkew56z200010amedftl1cer
slug: this-keyword-in-js
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689814662229/b843cd0f-177d-4244-be48-707dd56be0af.jpeg
tags: web-development, backend, reactjs, frontend-development, this-keyword

---

👋🏻 Hey there, JavaScript enthusiasts!

Today, we're going to dive into the mysterious world of JavaScript's `"this"` keyword. It's a powerful and widely used feature, but it can be a bit tricky to grasp at first.

Don't worry🥳; we'll make it crystal clear with some examples.

# **What is "this" in JavaScript?💭**

In JavaScript, the `"this"` keyword refers to the object from which it's called. Its value depends on how the function containing `"this"` is invoked.

# 🌐 **"this" Inside Global Context**

When you reference `"this"` in the global context (not inside any function), it points to the "window" object.

```javascript
console.log(this); // Output: [Window] (referring to the window object)
```

# **"this" Inside Function Context ⚡**

If a function containing `"this"` is called from the global scope, `"this"` will point to the "window" object.

```javascript
var myNum = 100;

function WhatIsThis() {
    var myNum = 200;

    console.log("myNum = " + myNum); // Output: myNum = 200
    console.log("this.myNum = " + this.myNum); // Output: this.myNum = 100
}

WhatIsThis(); // inferred as window.WhatIsThis()
```

In this example, the function `"WhatIsThis()"` is called from the global scope (window object), so `"this"` inside the function refers to the window object. Accessing `"myNum"` without `"this"` refers to the local variable inside the function.

# 💡 **"this" Inside Object Method**

When `"this"` is used inside an object's method, it refers to the object itself.

```javascript
const student = {
    name: 'Manvith',
    age: 21,

    greet() {
        console.log(this); // Output: { name: 'Manvith', age: 21, greet: [Function: greet] }
        console.log(this.name); // Output: Manvith
    }
}

student.greet();
```

Here, `"this"` refers to the "student" object.

# 🧿**"this" Inside Inner Function**

When you access `"this"` inside an inner function (inside a method), `"this"` refers to the global object.

```javascript
javascriptCopy codeconst student = {
    name: 'manvith',
    age: 21,

    greet() {
        console.log(this); // Output: { name: 'manvith', age: 21, greet: [Function: greet] }
        console.log(this.age); // Output: 21

        function innerFunc() {
            console.log(this); // Output: [Window] (referring to the global object)
            console.log(this.age); // Output: undefined
        }

        innerFunc();
    }
}

student.greet();
```

In this example, `"this"` inside the `"innerFunc()"` refers to the global object, while `"this.age"` outside `"innerFunc()"` refers to the "student" object.

# "**this" Inside Function with Strict Mode🔪**

When `"this"` is used in a function with strict mode, it becomes `"undefined."`

```javascript
javascriptCopy code'use strict';
this.name = 'Chhakuli';

function greet() {
    console.log(this); // Output: undefined
}

greet();
```

But don't worry, you can still make it work with the `"call()"` function:

```javascript
javascriptCopy code'use strict';
this.name = 'Chhakuli';

function greet() {
    console.log(this.name); // Output: Chhakuli
}

greet.call(this); // Treats greet() as a method of the global object
```

# 🙇‍♂️ **Conclusion**

Using `"this"` can be a powerful shortcut, but be mindful of how the context can change its value and behaviour, especially in strict mode. We've only scratched the surface of this topic, so feel free to explore more in-depth discussions about the `"this"` keyword.

Happy coding💗,

keep exploring the amazing world of JavaScript! Bye for now! 👋🏻😄