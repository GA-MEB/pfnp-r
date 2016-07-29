[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Reading : Server-Side JS with Node

The history of JavaScript is rather noteworthy.

In the early 90s, Sun Microsystems had just come out with a popular programming
language called **Java**, which was groundbreaking in that it could be used to
write programs for a wide variety of different types of chips
('write once, run anywhere'). Because Java was becoming so popular, it began to
be used in lots of applications, including powering small mini-applications
(or "app-lets") that loaded inside web pages.

In the summer of 1995, Netscape Communications Corp hired an engineer named
Brendan Eich to to build them a new language which resembled Java to run in
their new web browsing program, Netscape Navigator. This language, 'JavaScript',
would soon be running on millions and millions of computers around the world,
buoyed by the success of Netscape. JavaScript soon became the de facto language
of programming on the web. Eich himself would go to head the Mozilla project,
Netscape's big open source initiative, which ultimately survived Netscape and
continues to be very influential.

However, JavaScript itself still had a lot of problems. Eich had developed the
language in only **ten days**, in order to meet a production deadline, and it
still had lots of bugs and quirks. This led to most programmers not taking it
very seriously as a language, and even though the language would improve with
time, JavaScript was mostly relegated to _only_ being used on the web.

This changed in 2009 in a big way with the release of [**Node.js**](https://nodejs.org/),
an open-source, cross-platform system developed by Ryan Dahl for running
JavaScript outside of the browser. Node was built on top of Google's V8
JavaScript engine, so it could run JS code just like a browser (including the
handling of asynchronous events). Soon after Node's release, a
**package management system** called `npm` was released; this provided a
standard way for managing 3rd-party JS libraries that an app might need.

Once you have Node installed on your system, setting up a new Node project is
fairly straightforward. Simply create a new directory to hold your project,
and then run `npm init` inside that directory. This will create a
**manifest file** (which holds a list of all of your project's dependencies)
called `package.json`, and make a new sub-directory called `node_modules` where
those dependencies can be downloaded. The purpose of the manifest file is to
allow people to download the dependencies separately, by running the command
`npm install` in the root directory of your project.

To add another Node module as a dependency to your project, run
`npm install ` + the module's name + ` --save` in the root directory;
this will not only download the module you want, it will also add that module
to `package.json` so that anyone else who uses your project will know to
download it too. When you want to call upon one of these dependencies in your
JavaScript code, just use the global `require` function to load the module.
`require` will run the module in question, and if the module lists a particular
object as an **export** of that module, the `require` function will return that
value.

```js
// Here's an example of requiring and using a node module as a dependency.
// The API documentation for fs is at https://nodejs.org/api/fs.html
var fs = require('fs');

fs.readFile('someFile.csv', function(err, data){
  if (err) throw err;
  console.log(data);
})
```

To actually launch your Node application, just type `node` followed by a path
to your main JS file (which should generally sit in the root directory of your
Node project).
