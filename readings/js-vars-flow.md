[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Reading : Variables and Flow Control

While HTML and CSS are both computer languages, they aren't, strictly speaking,
programming languages. This is because it is not possible to use these languages
to write **programs**, sets of instructions that can be executed to perform a
particular task. Although HTML and CSS allow us to determine how the browser
renders a page, they can't _do_ anything once the page is already built.

Enter JavaScript. JavaScript is a true programming language -- it allows us to
create custom sets of instructions to directly control the browser's behavior.
Additionally, thanks to a unique quirk of history, it's a language supported by
every browser; whether you're using Firefox, Chrome, or Safari,
your JS code will be able to run.

What does it mean to write a program?
Fundamentally, a program is a list of instructions that manipulate data and
guide behavior. Let's examine the first piece now. JavaScript is capable of
operating on a few different types/formats of data, but the most basic ones
are numbers (`0`, `2.4`, `-100`), text strings (`'hello world'`), and
boolean values (`true` / `false`).

For now, we're going to interact with JS through a program called a REPL -
that stands for 'READ-EVALUATE-PRINT LOOP', a description of what it does.
Once you input an **expression** containing some values, it attempts to
**evaluate**, or solve, that expression, print the result, and start all over.
In essence, it acts like a calculator: "1 + 3 =" -> "4"

```js
1 + 1 // evaluates to 2
5 - 2 // evaluates to 3
3 * 3 // evaluates to 9
```

Being able to calculate these values is not in-and-of-itself interesting.
However, we also have the ability to save results from one calculation and
reuse them in another, through a construct called **variables**.

As of v5, variables in JavaScript should be defined using the `var` keyword.

```js
var a = 1 + 1;
```

These variables can themselves be evaluated as part of an expression.

```js
var a = 1 + 1;
var b = a + 1;
```

Note that there is no ongoing relationship here between `a` and `b`;
we're just deriving a value for `b` from the _current value_ of `a`.
In fact, we could just as easily have used the same variable.

```js
var a = 1 + 1;
a = a + 1;      // the new value for `a` is the current value for `a` plus one
```

But even being able to store data isn't useful without the ability
to make _decisions_ based on that data. That's where **flow control** comes in.
Flow control is the way by which a program decides which lines of code to
execute and when.

In JavaScript, the three most fundamental methods of flow control are:

-   `if..else if..else` statements (for making decisions)
-   `while` loops (for repeating things an indeterminate number of times)
-   `for` loops (for repeating things a known, fixed number of times)

Here are some simple examples of the syntax for each type.

#### Conditionals

**if**

```js
var a = 2;
if (a > 1) {
  console.log('greater thn 1'); // print this text out in the console
}
```

**if...else**

```js
var a = 2;
if (a > 1) {
  console.log('greater thn 1'); // print this text out in the console
} else { // if a is less than or equal to 1
  console.log('not greater than 1');
}
```

**if...else if**

```js
if (a > 1) {
  console.log('greater thn 1'); // print this text out in the console
} else if (a > 0) { // if a is less than or equal to 1, but greater than zero
  console.log("at least it's better than nothing");
}
```

**if...else if...else**

```js
if (a > 1) {
  console.log('greater thn 1'); // print this text out in the console
} else if (a > 0) { // if a is less than or equal to 1, but greater than zero
  console.log("at least it's better than nothing");
} else {
  console.log('less than or equal to 0');
}
```

#### Loops

**while**

```js
var a = 1;
var b = 30;
while (a < b) { // keep running, indefinitely, until this condition becomes true
  console.log('a smaller than b');
  b = b - 10;
}
console.log('a is no longer smaller than b');
```

**for**

```js
for(var i = 0; i < 30; i = i + 1) { // counts up by 1 from 0 to 29
  console.log('This is printout ', i + 1, 'out of 30');
}
```
