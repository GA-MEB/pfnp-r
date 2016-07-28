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

<!-- est 20 mins -->
### Exercise: Variables and Flow Control

Write a little script that raises 2 to a power specified by a variable called
`power`, and prints out the final result.
There's more than one way to solve this.

<!-- est 10 mins -->
### Demo: Arrays and Objects in JS

In addition to basic data types like strings and numbers, JavaScript also has
two data types for managing _collections of things_, called **arrays** and
**objects**. An array is an ordered list of things (any kind of thing) where any
item on the list can be accessed via its **index**
(i.e. its position in the list).

```js
var array = [ 'a', 'b', 'c', 'd', 'e'];
// index vals: 0    1    2    3    4
// don't ask why it starts at 0; it just does.
```

The syntax for doing this involves using square braces (`[]`).

```js
console.log(array[2]); // prints out 'c'
array[2] = 'z';
console.log(array[2]); // prints out 'z'
```

JavaScript Objects (also sometimes called dictionaries, hashes,
or associative arrays), are collections of **keys** and **values**,
where values can be any type of data, and keys are _strings_ used to look up
thos values (much like how items in an array are looked up by their index).

```js
var obj = {
  'keyOne': 'z', // note that quotes for the keys are optional
  'keyTwo': 'a'
};
```

Note that there is no inherant order to these pairs of keys and values; in this
particular case, sorting by key would leave values _un_sorted, and vice versa.

To access items in a JS object, you can use the same square bracket notation as
arrays.

```js
console.log(obj['keyOne']); // prints 'z'
obj['keyOne'] = 'A';
console.log(obj['keyOne']); // prints 'A'
```

However, it's much more common to use 'dot syntax' for doing those things.

```js
console.log(obj.keyOne); // prints 'z'
obj.keyOne = 'A';
console.log(obj.keyOne); // prints 'A'
```

When written this way, it's common to refer to `keyOne` and `keyTwo` as
"properties" of the object.

<!-- est 10 mins -->
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

Let's fill out the HTML file we emptied earlier with some new HTML.
Instead of a website page, we're going to make it a to-do list.

```html
<h1> To-Do </h1>

<ul>
  <lh> Tasks to Complete </lh>
  <li> Buy milk </li>
  <li> Mow the lawn </li>
  <li> See the doctor </li>
</ul>
```

1. Let's programatically add some styling to the top header, by increasing
   the font size to 100px.

   ```js
   document.getElementsByTagName('h1')[0].style.fontSize = '100px';
   ```

2.  Next, let's define a new class in our CSS file called

<!-- END DAY 1 -->
<!-- ### Exercise: Manipulate the DOM <!-- est 20 mins -->

<!-- ### Demo: Define and Invoke Functions <!-- est 10 mins -->

<!-- ### Exercise: Define and Invoke Functions <!-- est 20 mins -->

<!-- ### Code-Along: Set Functions as Event Handlers <!-- est 15 mins -->

<!-- ### Exercise: Set Functions as Event Handlers <!-- est 20 mins -->

<!--
## Delivering Static Pages with Node <!-- -->

<!-- ### Read: Node.js -->

<!-- ### Code-Along: Initialize a New Node Project <!-- est 5 mins -->

<!-- ### Code-Along: Set Up a Server Using the `http` Module
<!-- est 15 mins -->

<!-- ### Exercise: Set Up a Server Using the `http` Module <!-- est 20 mins -->

<!-- ### Code-Along: Add Routing and Control to Your App <!-- est 20 mins -->

<!-- ### Exercise: Add Routing and Control to Your App <!-- est 25 mins -->

<!--
## Delivering Dynamic Pages with Node <!-- est 120 mins -->

<!-- ### Code-Along: Make Template Strings <!-- est 10 mins -->

<!-- ### Code-Along: Serve Template Strings <!-- est 15 mins -->

<!-- ### Exercise: Add 'View' Templates to Your App <!-- est 20 mins -->

<!-- ### Exercise: Do It All Again! <!-- est 20mins -->

<!--
## Serving Data from a Database <!-- est 25 mins -->

<!-- ### Read and Code: SQL Databases <!-- 10 mins -->

<!-- ### Read and Code: NoSQL Databases <!-- 10 mins -->

<!-- ### Read: ORMs <!-- 5 mins -->
