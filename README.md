# backend (node.js)

- [Node.js doc](https://nodejs.org/en/docs)
- [Express.js doc](https://expressjs.com/en/starter/installing.html)
- [MongoDB doc](https://www.mongodb.com/docs/atlas/)
- [Mongoose doc](https://mongoosejs.com/docs/guide.html)
---

##  Node.JS
- Node.js allows you to run JavaScript on the server
- Node.js is an open-source. cross platform. JS runtime environment.
- It is not a language. 
- It is not a framework.
- It is built on the V8 JavaScript engine used by Google Chrome


#### What Can Node.js Do?
- Node.js can generate dynamic page content
- Node.js can create, open, read, write, delete, and close files on the server
- Node.js can collect form data
- Node.js can add, delete, modify data in your database

#### Download Node.js
- The official Node.js website has installation instructions for Node.js: [node.js](https://nodejs.org)
- If you want to make sure node.js is installed, Type this command in the command screen 
```sh
  node -v
```

#### Browser vs Node.js
- Node.js and a browser are both software environments used to execute JavaScript code.
- Node.js supports both the <b> commonJS </b> and <b>ES module</b> systems 
- Browser we are Starting to see teh <b>ES module </b>standard being implemented
- Node.js is designed for server-side JavaScript programming,
- browser is designed for client-side web application development and content rendering.
- In the browser, we don't have all the nice APIs that node.js provides through its modules.
- In node.js, we don't have the <b>document </b>, <b>window</b> and all the other objects that are provided by the browser.

#### Module 
- A module is an encapsulated and reusable chunk of code that has its own context.
- In node.js, each file is treated as a separate module.

#### Types of modules:
1. Local modules:
    - modules that we create in our application
2. Built-in modules:
    - modules that Node.JS ships with out of the box.
3. third Party modules:
    - modules written by other developers that we can use in our application.