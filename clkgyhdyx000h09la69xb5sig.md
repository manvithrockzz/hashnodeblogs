---
title: "Understanding Spread and Rest Operators 💗🔪"
seoTitle: "Unraveling the Power of the Three Dots in JavaScript: Spread and Rest"
seoDescription: "Master the magic of the three dots in JavaScript with informative examples. Learn how Spread and Rest operators enhance code efficiency in ES6."
datePublished: Mon Jul 24 2023 14:21:09 GMT+0000 (Coordinated Universal Time)
cuid: clkgyhdyx000h09la69xb5sig
slug: understanding-spread-and-rest-operators
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689861887784/be4570ca-363e-42b5-ae99-9f13d226a611.png
tags: software-development, web-development, frontend-development, rest-operator, spread-operator

---

In the enchanting world of ES6, we encounter a mysterious trio of three dots (...) that hold immense power. These three dots are known as the `Spread Operator` 🧈 and the `Rest Operator` 💆‍♂️.

While their syntax is the same, their purposes differ significantly, making them both magical and sometimes confusing. In this interactive blog, we will unravel the secrets behind the Spread and Rest operators with informative examples.

> **In JS, the three dots operator** `(…)` means two things:

* ***The spread operator🦶😶‍🌫️***
    
* ***The rest operator 💆‍♂️😂***
    

While their syntax is the same, but these two operators are ***not the same***.

![Master Javascript's New, Cutting-Edge Object Spread Operator | by Arnav  Aggarwal | codeburst](https://miro.medium.com/v2/resize:fit:1200/1*GLoQJzDAZ_C6G2p2FCA-hQ.png align="left")

Let's Begin👀

# **Spread Operator 😶‍🌫️🤙**

### **Overview: Spread**

In Javascript, the spread operator `...` splits array elements or object properties for easy use in new arrays or objects, enhancing code readability and efficiency.

***Hence, the name spread, i.e., “spread the elements of an array/objects in a new array/objects”.***

**Example 1: Copying an Array**

```javascript
const fruits = ['apple', 'banana', 'orange'];
const copiedFruits = [...fruits];

console.log('Original Array:', fruits);
console.log('Copied Array:', copiedFruits);
//Copies the 'fruits' array and creates a new array 'copiedFruits'.
```

**Example 2: Merging Arrays**

```javascript
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const mergedArray = [...arr1, ...arr2];

console.log('Array 1:', arr1);
console.log('Array 2:', arr2);
console.log('Merged Array:', mergedArray);
//Description: Merges two arrays 'arr1' and 'arr2' into a new array 'mergedArray'.
```

# **Rest Operator 🥳🧿**

### **Overview: Spread**

In Javascript, The Rest Operator is a collection of remaining function arguments, allowing us to handle an indefinite number of parameters as an array.

***Hence, the name spread, i.e., “the rest of the elements”.***

**So, for instance, here is the rest syntax:**

```javascript
...yourValues
```

The three dots (...) in the snippet above indicates the `rest operator`. In JS functions, `rest` gets used as a prefix of the function’s last parameter.

**Example 3: Summing Variable Arguments**

```javascript
 codefunction sum(...numbers) {
  let total = 0;
  numbers.forEach((number) => (total += number));
  return total;
}

console.log('Sum:', sum(1, 2, 3, 4, 5));
console.log('Sum:', sum(10, 20, 30));
//Description: Sums up variable number of arguments passed to the 'sum' function.
```

**Example 4: Dynamic Function Parameters**

```javascript
javascriptCopy codefunction displayInfo(name, ...skills) {
  console.log('Name:', name);
  console.log('Skills:', skills);
}

displayInfo('John', 'JavaScript', 'Python', 'HTML', 'CSS');
displayInfo('Jane', 'React', 'Node.js');
//Description: Displays the name and skills of a person using the Rest Operator to handle variable arguments.
```

# **Interactive Play Area🛝:**

Now it's your turn to wield the power of the three magical dots! Experiment with the Spread and Rest operators in the interactive code playground below:

```javascript
// Interactive code playground

// Spread Operator examples
const fruits = ['apple', 'banana', 'orange'];
const copiedFruits = [...fruits];

console.log('Original Array:', fruits);
console.log('Copied Array:', copiedFruits);

// Rest Operator examples
function sum(...numbers) {
  let total = 0;
  numbers.forEach((number) => (total += number));
  return total;
}

console.log('Sum:', sum(1, 2, 3, 4, 5));
console.log('Sum:', sum(10, 20, 30));

// Your code here

// Interactive code playground ends
```

Thus we saw that, the `Spread` syntax `“expands”` an array into its elements, while the `Rest` syntax collects multiple elements and `“condenses”` them into a single element 😄

Both the rest and spread operator might seem confusing because both of them uses a `...` syntax. So, how do we know where to use what? I remember it like this,

* ***Spread Unpacks the Elements.***
    
* ***Rest Packs the Elements,***
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689862101012/8c061572-7853-48cf-829f-6aff7ed07965.gif align="left")

# Congratulations!

You've mastered the art of the three magical dots in JavaScript.

Armed with this knowledge, you can now wield the magic of the three dots to write more efficient and concise code.

Happy coding! 🚀