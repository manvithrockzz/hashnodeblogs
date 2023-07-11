---
title: "The Magic of  WTemplate Engines😍"
datePublished: Tue Jul 11 2023 16:18:31 GMT+0000 (Coordinated Universal Time)
cuid: cljyhy8tn000708l29hn3h0w8
slug: the-magic-of-wtemplate-engines
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689092253723/b85188eb-c013-48f2-ba6a-b10ce1236f65.png
tags: express, web-development, backend, expressjs-cilb5apda0066e053g7td7q24, template-engine

---

When you're building a backend application🥲 in Node.js and need to send `HTML` back to clients, then you must find a way to **“mix-in”** or **interpolate** the processed data into the HTML files you are sending. For simple "data interpolation and testing purposes", one way🚀 to do this is by `concatenating HTML strings with data or using the template strings in JavaScript`.

If you're aiming to develop applications with extensive💪 HTML code and dynamic content, there's a better approach: <mark>Template Engines</mark>, Interesting right??

# What is Template Engine?

In the modern world🌍, interactions and experiences have become more personalized and engaging. Nowadays, almost everyone can access the internet, and many web applications are designed to be dynamic.

Take Instagram, for example. When you and I log in, we see different news feeds. The overall structure of the page remains the same, with posts displayed in a sequential order and usernames placed above them. However, the specific content varies for each user.📸✨

This customization is achieved😎 through the use of a template engine. The template for the news feed is initially defined, and then, based on the current user and the database query, the template is filled with relevant content.

We can use template engines in both the backend and front end😃. If we use a template engine in the backend to generate the HTML, we call that **Server-Side Rendering (SSR),** If we use a template engine in the frontend to generate the HTML, we refer to it as **Client-Side Rendering (CSR).**

# Look how it works 👇

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689090150336/c6a431e0-2af5-45bb-888d-b4830c0fedf6.png align="center")

**A template engine works very simply🔥:** you create a template and, with the appropriate syntax, pass variables into it. Then, at the appropriate route to render📈 the template, you assign values to the variables declared in your template file. These are compiled in real time as the template gets rendered.

One☝️ essential feature of `template engines` are that they **allow us to create reusable components called partials**, which can be reused in other files. This helps prevent `code duplication` and `makes changes easier to implement`😯.

> ***There are several template engines available today, and the more popular ones include Pug (fka Jade), Handlebars, EJS, Mustache, Swig, and others.***

Now that we understand what templating engines are, let us now take a look at some **benefits**. Of course, you must have guessed a few, but let me throw some light on those you probably didn’t 😊.

# **Advantages of Using Template Engines**

Obviously😁, there are benefits involved in using templating engines is the reason why it is so **widely used by developers**. Below👇 I have listed out quite a few:

1. Better (Faster) Performance.
    
2. Creating an HTML template with minimal code.
    
3. Enhances developer productivity.
    
4. Improves readability, usability, and maintainability of applications.
    
5. Maximizes client-side data processing.
    
6. Easy reuse of templates on multiple pages.
    

**Okay😮‍💨, so we’re done with understanding the basics of template engines**.

# **How to install template engines with the Express JS**

in Three steps:

```javascript

npm i ejs ---> Install EJS
npm i mustache --->Install Mustache
npm i pug --->Install Pug
```

**And Many More🙈**

# **Integrating Express template engines**

To integrate a template engine into your Express application, you can do it with just a few lines of code:

📂 Specify the directory where your template files are located using `app.set('views', './views')`. By default, Express looks for a directory named "views" in your application's root directory.

🖥️ Set the template engine you want to use by calling `app.set('view engine', 'ejs')`, where 'ejs' can be replaced with the name of your preferred template engine (e.g., 'pug', 'handlebars').

🚀 Here's an example:

```javascript
const express = require('express');
const app = express();

app.set('views', './views');
app.set('view engine', 'ejs');

// ...define your routes and other middleware...

app.listen(3000, () => {
  console.log('Server started on port 3000');
});
```

Please make sure to install the necessary dependencies for the chosen template engine, such as "ejs" in this case, using `npm install ejs`.

# **Conclusion 🤗**

📝 In this article, we discovered templating engines, explored their advantages, and learned how to install them. ✨ That's a concise and comprehensive introduction! ✅

And its a wrap, If you enjoyed learning and find it useful please do like and share so that, it reaches others as well 🤝

### Thanks for reading 😃

See you in my next Blog article, Take care!!  
**Happy Learning😃**