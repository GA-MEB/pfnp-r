[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Programming for Non-Programmers (Remote Edition)

## "Before we begin ..."

### Schedule/Agenda

#### Day 1

| Start Time | Unit                                   | Other Notes       |
|------------|----------------------------------------|-------------------|
| 10:00 AM   | Admin and Setup                        | .                 |
| 10:30 AM   | Terminology / AMA                      | .                 |
| 11:00 PM   | Making and Styling Static Pages        | One 15-min break  |
| 12:45 PM   | Working Like a Developer               | .                 |
| 1:30 PM    | Lunch                                  | 45 mins!          |
| 2:15 PM    | JS Fundamentals and DOM Manipulation   | Two 10-min breaks |
| 4:55 PM    | Standup                                | End of Day 1      |

#### Day 2

| Start Time | Activity                                   | Other Notes      |
|------------|--------------------------------------------|------------------|
| 10:00 AM   | JS Fundamentals and DOM Manipulation, Ctd. | One 15-min break |
| 11:30 AM   | Delivering Static Pages With Node          | .                |
| 1:30 PM    | Lunch                                      | 45 mins!         |
| 2:30 PM    | Delivering Dynamic Pages With Node         | One 15-min break |
| 4:30 PM    | Serving Data from a Database               | .                |
| 4:55 PM    | Standup                                    | End of Day 2     |

### Class Expectations

There are many things that are different about taking a class online.

-   No looking over peoples' shoulders.
-   Distraction (ooh, cat pictures) literally everywhere.

But there are also many things that are the same.
You will be expected to show up on time each morning,
come back from breaks on time, and generally be focused on the class.
Additionally, you will be expected to complete any homework that's assigned.

This class is being recorded, so if you miss something, you'll be able to go
back and review it; however, these videos will not necessarily be available
until the end of each day, so please pay attention.

Also: although the class is called "Programming for Non-Programmers", we're
goign to spend most of our time focusing on one specific subset of programming,
**web development**, or building applications for the world-wide web.
Topics like computer science, embedded systems programming,
or building desktop/mobile applications, will **not** be covered.

Finally, don't stress! This is a **2-day** class, and we're covering a lot,
so don't go in expecting to have recruiters knocking on your door tomorrow.
Our intention is to give you a quick run through the highlights and essentials
of each topic, so that you'll

a. better understand how all this stuff generally works (it is called
   'Programming for Non-Programmers' after all), and

b. have a framework for learning more through further study and practice

> "The journey of a thousand miles begins with a single step..."
> -- Lao Tze

### Setup and Configuration

Before we start setting things up, you should all have signed up for accounts
with (a) Cloud9, (b) GitHub, and (c) Zoom.

If any of you had problems setting those things up, let's resolve them now.

Once all three accounts have been made, you're going to want to link your Cloud9
accounts to your GitHub accounts.

1.  Log into you GitHub account.

2.  Open a new tab, log into Cloud9 and go to your
    [settings page](https://c9.io/account/settings).

3.  Go to the 'Connected Services' tab and click the green button in the
    'GitHub' box. This should take you to a confirmation page.

4.  Click the green button that says 'Authorize Application'.

Now your GitHub and Cloud9 accounts are linked!

Finally, create two new workspaces on your Cloud9 account.
Call one `static-page`, and the other `node-app`.

### Learning Objectives

By the end of day 1, you should
(with the help of a reference, and a little time)
be able to:

-   Differentiate between the internet and the world wide web.
-   Explain the difference between 'front-end' and 'back-end'.
-   Create an HTML page by hand and load it in the browser.
-   Add CSS styling to an HTML page.
-   Read a CSS file and predict how a given element would be styled.
-   Modify a page's layout using CSS.
-   Interact with a computer using the CLI interface.
-   Use Git to save changes to a set of website files.
-   Add JavaScript code to an HTML page.
-   Write JavaScript code that reads from, and writes to, variables.
-   Compare and contrast arrays and JS objects.
-   Use the DOM to change properties of a web page.

<!--
By the end of Day 2, you should
(with the help of a reference, and a little time)
be able to:

-   Define and invoke JS functions.
-   Add an event handler to a web page.

-->

## Terminology

### Key Terms and Ideas

**The Internet** is an interconnected network (get it?) of computers
that can send messages back and forth from one computer to the other.

**The World-Wide Web** is a _service_ which is run over the internet backbone,
much like how Netflix's DVD business is a service that's built on top of the
US postal service.
A **service** is an interaction between two parties: a **client**, which makes
requests, and a **server**, which delivers on those requests.

In the case of the web, the client (usually a program called a **web browser**)
requests documents called **web pages**, and then tries to display
(or **render**) those pages for the user to see.

These web pages are served up by a **web application**, a program that runs
indefinitely and listens for requests coming in over the web.
In order to create these pages, the application uses a tool for storing large
amounts of data, called a **database**, to read and write data related to the
application's job.

In general, the part of interacting with a web application that happens in the
browser is referred to as the **front-end**, while the rest of the app is
commonly referred to as the **back-end**.

### AMA! (Ask Me Anything)

Ask me any questions you like! These questions will impact how we move through
the remaining material.
Some questions I'll be able to answer now, but for others, I'll ask you to
put them into our Zoom chat as a 'parking lot', to be answered later.

<!-- est 105 mins, including a 15 min break -->
## Making and Styling Static Pages

<!-- est 5 mins -->
### [Read: HTML](readings/html.md)

<!-- est 10 mins -->
### Demo: Make an HTML Page

<!-- est 10 mins -->
### Exercise: Make an HTML Page

In Cloud9, go to your `static-page` workspace, and at the root
(i.e the outermost level) of the filesystem, create a new
file there called `index.html`.

Copy all of the text from [cookies.txt](exercises/cookies.txt) into that file
and 'HTML-ify' it by adding the appropriate HTML tags in and around the content.

<!-- est 5 mins -->
### [Read: CSS](readings/css.md)

<!-- est 10 mins -->
### Demo: Add CSS Styling to a Page

<!-- est 10 mins -->
### Exercise: Add CSS Styling to a Page

Go back to your Cloud9 workspace from the previous exercise and create a new
directory called `stylesheets`; inside it, create a new file called
`style.css`. Then, in your HTML file, link to your CSS stylesheet.

Edit your HTML and CSS so that:

-   high-level headings (h1, h2) get colored gold (`#FFD700`), and the top-level
    heading is at least 40px tall

-   the top-level heading is in the 'impact' font

-   headings of all sub-sections get colored white (`#FFFFFF`)

-   the background of the whole page (Hint: `body`) gets set to the color
    `#D2691E`

-   every other ingredient gets colored with alternate shades of grey
    (`#C0C0C0`, `#909090`)

-   all other text gets colored light brown (`#DEB887`)

REACH: Make it so that...

-   Ingredients get backdrop that's a darker color (`#8B4513`) than
    the background when your mouse hovers over them.

-   The first letter of each step in the recipe is a little bigger than normal.

<!-- est 10 mins -->
### [Read: CSS for Layout](readings/css-layout.md)

<!-- est 15 mins -->
### Demo: CSS for Layout

<!-- est 10 mins -->
### Exercise: CSS for Layout

Go back to your recipe site, and change the layout so that

-   "INGREDIENTS" and "DIRECTIONS" sit next to each other, while "EXPERT TIPS"
    drops below

-   every ingredient and every step have 2 px of space above and below them

-   the high-level headers are offset by at least 20px from the top of the page
    and at least 50px from the left side of the page

<!-- est 45 mins -->
## Working Like a Developer

<!-- est 5 mins -->
### [Read: Use a Command Line Interface](readings/cli.md)

<!-- est 15 mins -->
### Exercise: Use a Command Line Interface

In your Cloud9 workspace, open up a terminal window -- it should say 'bash' at
the top of the tab.

Using only the terminal,

1.  create a new directory called `example-dir`
2.  create a new file called `example-1.txt` in your present directory
3.  move that new file into `example-dir`
4.  move yourself into that same directory
5.  create a new file called `example-2.txt` in your present directory
6.  rename `example-2.txt` to `example-two.txt`
7.  move back up to your parent directory
8.  recursively delete `example-dir` and all of the files it contains.

<!-- est 5 mins -->
### [Read: Save Work with Git](readings/git.md)

<!-- est 20 mins -->
### Code-Along: Save Work with Git

1.  Once you've run `git init`, run `git status` -- it should show that you have
    files with uncommitted changes.

2.  Use `git add` to add `index.html` and `style.css`.

3.  Run `git commit` to create a new commit.
    By default, this should open an in-console text editor program
    called `vi`/`vim`, where you can write your commit message.
    To start writing, type `i` to change into "INSERT" mode.
    When you're done with your message, type the `esc` key to go back to
    "COMMAND" mode, where you started. There, type `:w` to save your changes
    and then `:q` to quit.

4.  Type `git log` to see your commit history -- your most recent commit should
    be visible.

5.  Now make another two changes: delete all of the content in the `<body>` tags
    in your HTML file, and delete everything inside the CSS file (NOT the file
    itself).
    Run `git status`.

6.  Add these new changes, make a second commit (with a nice, descriptive
    message), and run `git log`. You should see two commits now!

## Programming Fundamentals

<!-- est 230 mins over two days,
including two 10-min breaks and 5-min standup -->

<!-- est 5 mins -->
### [Read: Variables and Flow Control](readings/js-vars-flow.md)

<!-- est 5 mins -->
### [Read: Add JS to Your Page](readings/js-html.md)

<!-- est 10 mins -->
### Code-Along: Variables and Flow Control

We're going to write a simple program to act as a virtual thermostat.
This thermostat will need to run for some unknown amount of time, which
suggests using a while loop. Why don't we have it stop when we exactly
reach our desired temperature?

```js
var desiredTemp = 73; // F
var actualTemp = 60; // F
while (actualTemp !== desiredTemp) {
  // do something
}
```

Suppose that when the temperature is below the desired temp, our thermostat
turns on the heat, causing it to rise by 3 degrees F. This split in our behavior
suggests using an `if` statement.

```js
var desiredTemp = 73; // F
var actualTemp = 60; // F
while (actualTemp !== desiredTemp) {
  if (actualTemp < desiredTemp) {
    console.log("Turning Heat On");
    actualTemp = actualTemp + 3;
    // A nifty shortcut for this kind of statement is `actualTemp += 3;`
  }
}
```

However, the heat should not be turned on if the temperature is above the
desired temperature -- instead, it should be turned off, and the room allowed to
cool naturally, causing temperatures to fall by 0.5 degrees F.
We could implement this with another `if`, but since we want our program to
_either_ turn the heat on or turn it off, the best approach is probably to use
`if...else`.

```js
var desiredTemp = 73; // F
var actualTemp = 60; // F
while (actualTemp !== desiredTemp) {
  if (actualTemp < desiredTemp) {
    console.log("Turning Heat On");
    actualTemp = actualTemp + 3;
    // A nifty shortcut for this kind of statement is `actualTemp += 3;`
  }
}
```

<!-- est 10 mins -->
### [Read: Arrays and Objects in JS](readings/js-arrays-objects.md)

<!-- est 20 mins -->
### Code-Along: Iterate Through Arrays

We're going to go through a very common pattern - using a 'for' loop to step
through every element in an array, and then do something with each element as it
goes by.

Suppose that we want to take an arbitrary array of numbers, and calculate the
sum.

```js
var numbers = [1, 2, 3, 4, 5, 6, 7];
var sum = 0;
```

As mentioned, one way we can approach this is by **iterating**, or doing the
same thing over and over again, as we move through the array.

Since a 'for' loop generally works by increasing its counter value (usually `i`)
by one with each run through, we can use it to successively take each different
possible index value in the array, up to an index equal to the length of the
array, minus 1. To get the length of the array, we can use a property that
arrays have called `length`.

```js
var numbers = [1, 2, 3, 4, 5, 6, 7];
var sum = 0;

//could also be i < numbers.length
for (var i = 0; i <= numbers.length - 1; i += 1) {
  // do something
}
```

Now all we need to do is do something with `numbers[i]` (which points to,
successively, `numbers[0]`, `numbers[1]`, `numbers[2]`, etc). Let's take its
value and add it to `sum`.

```js
var numbers = [1, 2, 3, 4, 5, 6, 7];
var sum = 0;

for (var i = 0; i <= numbers.length - 1; i += 1) { //could also be i < numbers.length
  sum += numbers[i];
}
```

Then, when we're finished, let's print our result.

```js
var numbers = [1, 2, 3, 4, 5, 6, 7];
var sum = 0;

for (var i = 0; i <= numbers.length - 1; i += 1) { //could also be i < numbers.length
  sum += numbers[i];
}
console.log(sum);
```

<!-- est 20 mins -->
### Exercise: Iteratively Edit Objects

Now that we've seen iteration, let's try iterating through an array of objects.
You'll see very soon why this is a useful pattern to understand.

In [`array-of-objs.js`](exercises/array-of-objs.js), you'll find some starter
code containing (naturally) an array of objects. Each object represents a
person, and has several properties including name, height, and weight.

Iterate through each object in this array; if the person's height is above 72
inches, append their name to an array (look up how you might do this) called
`taller_than_six_ft`.

REACH: Instead of an array, build a string to hold a list of names; separate
each name using commas and appropriate spaces (assume Oxford comma).

<!-- est 5 mins -->
### [Read: The DOM](readings/dom.md)

<!-- est 10 mins -->
### Code-Along: Manipulate the DOM

One note before getting started:
We can run JS code in the browser console and access the DOM that
way, but in order to actually load a JS file from our HTML, like we did with CSS
earlier today, we need to include a `<script>` tag whose `src` property is set
to the path from the HTML file to the JS code (just like we did with `href`
inside the `<link>` tag).

1.  First, let's make a file for our JS code that the page can load.
    Create a new directory called `scripts`, and inside that directory,
    create a new file called `main.js`.

2.  Next, let's fill out the HTML file we emptied earlier with some new HTML.
    Instead of a recipe page, we're going to make it a to-do list.

    ```html
    <html>
      <head>
        <link rel='stylesheet' type='text/css' href='stylesheets/style.css'>
      </head>
      <body>
        <h1> To-Do List </h1>
        <ul>
          <lh> Tasks to Complete </lh>
          <li> Buy milk </li>
          <li> Mow the lawn </li>
          <li> See the doctor </li>
        </ul>
      </body>
      <script src='https://code.jquery.com/jquery-3.1.0.js'></script>
      <script src='javascripts/main.js'></script>
    </html>
    ```

3.  Let's programatically add some styling to the top header, by increasing
    the font size to 100px.

    ```js
    $('h1').css('fontSize', '100px');
    ```

4.  Next, let's define a new class in our CSS file called 'completed'. This will
    be used to style any tasks that have already been completed.

    ```css
    .completed {
      background-color: #AAAAAA;
      text-decoration: line-through;
    }
    ```

    Just as an example, let's manually add that class to "See the doctor" item
    and see what happens. Then, let's remove it again.

5.  OK, now let's use jQuery to grab the middle two list items and add the
    `completed` class to both of those items.

    ```js
    var items = $('li');
    items.eq(1).addClass('completed');
    items.eq(2).addClass('completed');
    ```

    What do we see in the browser?

6.  Now let's actually remove the `completed` class from 'Mow the lawn';
    it looks like we may have missed a spot.

    ```js
    $('li').eq(2).removeClass('completed');
    // alternatively, $('li').eq(2).toggleClass('completed');
    ```

<!-- est 10 mins -->
### [Read: JS Functions and DOM Event Handlers](readings/js-functions-events.md)

<!-- est 15 mins -->
### Code-Along: Set Functions as Event Handlers

Let's revisit the To-Do app we were looking at earlier. We're going to add
some functionality to this app by using jQuery to respond to events and trigger
changes to the DOM. In particular, we're going to make it so that tasks can be
checked/unchecked to indicate that they've been completed.

1.  We'll start off by changing our HTML. In each `<li>`, we're going to add a
    checkbox, which will indicate whether or not an item has been completed.
    Let's also put the text content into `<span>` tags so that we can refer to
    it more easily

    ```html
    <body>
      <h1> To-Do List </h1>
      <ul>
        <lh> Tasks to Complete </lh>
        <li> <input type='checkbox'> <span> Buy milk </span> </li>
        <li> <input type='checkbox'> <span> Mow the lawn </span> </li>
        <li> <input type='checkbox'> <span> See the doctor </span> </li>
      </ul>
    </body>
    ```

2.  Next, we'll define an event-handling function to listen to changes in the
    **states** (checked/unchecked) of those check-boxes; we should be able to
    consistently trigger some behavior every time the box is checked or
    unchecked.

    ```js
    $('li > input').on('change', function(e){ // e is an object representing the event
      console.log('checked or unchecked a checkbox');
    });
    ```

3.  Finally, we'll edit the content of our event handler so that whenever the
    checkbox gets checked, the class `completed` gets added to, or removed from,
    the `<span>` element.

    ```js
    $('li > input').on('change', function(e){ // e is an object representing the event
      console.log('checked or unchecked a checkbox');
      $parent = $(e.target).parent();
      $parent.toggleClass('completed');
    });
    ```

<!-- est 20 mins -->
### Code-Along: Set Functions as Event Handlers

We're going to add a text-field form input and a button to the bottom of the
page. When the button gets clicked, the text in the input box will be added to
a new task, and the box itself will be emptied.

1.  First, let's just add a text box and a button.

    ```html
    <input placeholder='New Task Here'> <button id="create-task">   Create Task </button>
    ```

2.  Next, let's define an event handler to respond to the button click.

    ```js
    var createTask = function(){
      console.log('new task');
    };

    $('#create-task').on('click', createTask);
    ```

3.  Let's now make it so that our `createTask` handler function

    (a) reads the content of `#new-task-form-field` and stores it,

    ```js
    var createTask = function(){
      console.log('new task');
      var newTaskData = $('#new-task-form-field').val();
    };
    ```

    (b) creates a new task on the list (with the data from the input box as its
    content)

    ```js
    var createTask = function(){
      console.log('new task');
      var newTaskData = $('#new-task-form-field').val();
      $('ul').append(`<li> <input type='checkbox'> <span> ${newTaskData} </span> </li>`);
    };
    ```

    > That last thing there is called a **template string**, and it's a
    > fairly new feature of JavaScript. Whenever the pattern `${ ... }`
    > appears in a template string, JavaScript will calculate the value of
    > whatever's in the curly braces, and then replace the entire pattern with
    > that value, as part of the string.

    (c) empties the input box again

    ```js
    var createTask = function(){
      console.log('new task');
      var newTaskData = $('#new-task-form-field').val();
      $('ul').append(`<li> <input type='checkbox'> <span> ${newTaskData} </span> </li>`);
      $('#new-task-form-field').val('')
    };
    ```

4.  Finally, just for better code design, let's take that template string and
    replace it with output of a function, which we'll call `buildTemplate`.
    This will allow us build any and all template strings we might want to use
    in one place, so we won't have to worry about it anywhere else in our code.
    This idea is called **"separation of concerns"**.

    ```js
    var template = function(templateName, data) {
      if (templateName === 'new-task') {
        return `<li> <input type='checkbox'> <span> ${data} </span> </li>`
      }
    };

    var createTask = function(){
      console.log('new task');
      var newTaskData = $('#new-task-form-field').val();
      $('ul').append(template('new-task', newTaskData));
      $('#new-task-form-field').val('')
    };
    ```

Let's reflect briefly about how these responsibilities have been broken out
across the different functions:

1.  Our jQuery event handler responds to input from the user, and triggers
    `createTask` to do the actual work of creating the Task.

2.  `createTask` reads data (in this case, from a form field) and uses it to
    load a particular template string from `template` and populate it; then,
    it sends the finished HTML string back to the user as part of the UI.

3.  `template` provides a standard way of organizing and managing our template
    strings. Though there's only one now, this app is fairly simple, and it's
    quite conceivable that we might want to use other templates in the future.

This is a very common pattern, and one we'll soon see repeated on the back end.

## Delivering Static Pages with Node

<!-- est 5 mins -->
### Setup

1.  Open up a new workspace on Cloud9 called `node-app`, and build it off of the
    Node.js template.

2.  Delete the `client` directory, and the `node_modules` directory.

3.  Delete everything inside `server.js`, and replace the contents of
    `package.json` with the following:

    ```json
    {
      "name": "node-app",
      "version": "0.0.0",
      "description": "An example Node web application",
      "main": "server.js",
      "repository": "",
      "author": "",
      "license": "MIT",
      "dependencies": {
      }
    }
    ```

That's all for now; we'll do some more when we get to talking about databases.

### [Read: Server-Side JS with Node](readings/nodejs.md)

<!-- est 10 mins -->
### Code-Along : Set Up a Server Using the `http` Module

We're going to follow the pattern laid out in the reading and create a new Node
project called `node-app` which runs a simple web server.
We've already set up the basics of our app, so let's just dive into writing the
code.

1.  To start off with, we're going to want to use the [`http`](https://nodejs.org/api/http.html)
    node module, to create our server. `http` is one of the default Node
    libraries, so we don't need to download and install it. However, we do still
    need to `require` it if we want to use it.

    ```js
    var http = require('http');
    ```

2.  Next, we're going to use `http`'s `createServer` method to define a new
    HTTP server object. As part of the definition of the server, we'll pass in
    a function that tells the server how to respond to an incoming request.

    ```js
    var server = http.createServer(function(request, response){
      console.log('Hit the server!');
      console.log('request method:', request.method, 'request url:', request.url);
      response.end();
    });
    ```

    The two inputs to that function will be two objects, representing
    (respectively) the inbound request that's being handled and the new response
    that's being formulated.

3.  Launch the server by telling it to start listening to a particular port.

    ```js
    server.listen(4000);
    ```

    We can test whether or not the server is on by going to
    `localhost:4000` in a web browser and refreshing the page.
    Each time we do that, the terminal window where our server is running
    should print out some text.

4.  Finally, let's have our server respond to these requests by echoing back
    what type of request it reeived.

    ```js
    var server = http.createServer(function(request, response){
      console.log('Hit the server!');
      console.log('request method:', request.method, 'request url:', request.url);
      response.write(`Received a ${request.method} request at ${request.url}\n`);
      response.end();
    });
    ```

    That's it! We now have a fully-functioning webserver running, made up of
    fewer than 10 lines of code (1/3 of which are just printing text in the
    console).

    But wait... if we're sending back text, can we also send back HTML?

5.  Yes, yes we can. Let's write a short function which will wrap up any text
    we give it into some boilerplate HTML.

    ```js
    var htmlPage = function(content){
      return
      `<html>
        <head>
        </head>
        <body>
          ${content}
        </body>
      </html>`;
    };
    ```

    If we combine that function with our existing server setup, we can have our
    app spit back HTML instead of plain text.

    ```js
    var server = http.createServer(function(request, response){
      console.log('Hit the server!');
      console.log('request method:', request.method, 'request url:', request.url);
      var content = `<h1> Received a ${request.method} request at ${request.url} </h1>`
      response.write(htmlPage(content));
      response.end();
    });
    ```

<!-- est 20 mins -->
### Code-Along : Add Routing (with Dynamic Segments)

Being able to respond to requests is great, but it would be better if we could
be more granular, and respond differently to different requests (i.e. different
combinations of methods and URLs). That process, of parsing a requst and
determining how to respond, is called **routing**, and it's a core concern for
building a web application.

Let's start by adding some flow control to the server's controlling
function. Say that we want the HTML returned to vary based on the URL:
it should have one response for requests at `localhost:4000/my-first-page`,
one response for requests at `.../my-second-page`, and should respond with
an error message for any other URL. We could set this up by using
`if...else if...else`.

```js
var server = http.createServer(function(request, response){
  console.log('Hit the server!');
  console.log('request method:', request.method), 'request url:', request.url);
  var content = `<h1> Received a ${request.method} request at ${request.url} </h1>`;
  if (request.url === '/my-first-page') {
    content += '<h2> This is page #1. </h2>';
  } else if (request.url === '/my-second-page') {
    content += '<h2> This is page #2. </h2>';
  } else {
    content += '<h1>ERROR!!!</h1>'
  }
  response.write(htmlPage(content));
  response.end();
});
```

Now when we navigate to either URL in the browser, we see the appropriate
content, and when we navigate anwere else we see an error message.

What if, instead of having the URLs be `/my-first-page` and `/my-second-page`,
we wanted them to be `/my-pages/1` and `/my-pages/2`? We could hard-code them,
but what if we wanted to have an arbitrary number of pages? Surely we can't
hard-code all of them.

One way to do this is to use a URL _pattern_ rather than a specific fixed URL
to match with, with some parts that are just expected to vary. These sections
are called **dynamic segments**.

Knowing how to break apart the URL to identify the dynamic segments is tricky,
but we can use **Regex** to figure out if the URLs match the
target pattern. "Regex", or **regular expressions**, is a special language
designed specifically for matching patterns in text. We're not going to cover
Regex right now, but here are some great places to learn more about it:

-   [Rgex Tutorial](http://www.regular-expressions.info/tutorial.html)
-   [Regexr](http://regexr.com/)
-   [Regex Golf](http://regex.alf.nu/)

JavaScript strings all have
[a method called `.match`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/match)
which allows them to compare themselves to a regular expression
that you pass in; this method gives back an array of every instance where
the characters in the string match the regex, or returns a special value called
`null` (representing 'nothing') if it finds no matches.

The Regex pattern `/^\/my-pages\/(\d+)$/` means
"the start of the string (`^`),
followed by a slash (`\/`),
followed by 'my-pages'(`my-pages`),
followed by another slash(`\/`),
followed by a set of numbers that's at least one number long (`\d+`),
followed by the end of the string (`$`);
also, save that set of numbers in case I need it".
This pattern should only match urls like `/my-pages/1` or `/my-pages/100`,
never URLs like `/my-pages/a3`, `/my-pages-1`, etc.

Let's add this Regex to our code via the `match` method.

```js
var server = http.createServer(function(request, response){
  console.log('Hit the server!');
  console.log('request method:', request.method), 'request url:', request.url);
  var content = `<h1> Received a ${request.method} request at ${request.url} </h1>`;
  if (request.url.match(/^\/my-pages\/(\d+)$/)) {
    var matches = request.url.match(/^\/my-pages\/(\d+)$/);
    // matches should equal ['/my-pages/1'. '1'] for `/my-pages/1`
    if (matches[1] === 1) {
      content += '<h2> This is page #1. </h2>';
    } else if (matches[1] === 2) {
      content += '<h2> This is page #2. </h2>';
    }
    // this could also be written withut the conditional statements
    // as "content += `<h2> This is page #${matches[1]}. </h2>`;"
  } else {
    content += '<h1>ERROR!!!</h1>'
  }
  response.write(htmlPage(content));
  response.end();
});
```

### Exercise: Add More Routing <!-- est 25 mins -->

Now that we've set up this application, add some more routes and responses.
Make it so that you app will respong to routes of the form `/people/1`,
and respond with the name of the person in that position in the array below.

```js
['Harry', 'Bob', 'Susan', 'Lana', 'Charlie', 'Louise']
```

If any other URL is given, or if no person exists at that index, return some
sort of error message.

<!-- ## Serving Data from a Database <!-- est 25 mins -->

<!-- ### [Read: SQL Databases]() <!-- 10 mins -->

<!-- ### Code-Along : Using PostgreSQL <!-- 10 mins -->

<!-- ### Read: ORMs <!-- 5 mins -->

<!-- ### Read : NoSQL Databases <!-- 10 mins -->

## [Next Steps](readings/next-steps/md)
