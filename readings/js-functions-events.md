[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Reading : JS Functions and DOM Event Handlers

By this point, you've seen things like `$('li')` or `console.log('text')`,
but you haven't yet been filled in about what these are. In those two examples,
both `$` and `console.log` are a special type of data called a **function**.

Functions are a type of data that store JavaScript code, run it later
using a set of inputs provided at the time, and spit back some kind of result.

Here's how we might define a function.

```js
var addOne = function(inputNumber) {
  return inputNumber + 1;
};
```

`addOne` is now a function; when it runs, `addOne` takes a number
(which it refers to as 'inputNumber'), adds `1` to it, and gives back
(or 'returns') this new value. By returning that value, we can take the output
from that function and use it in different situations.

To run the `addOne` function with an input value of 4, simply write `addOne(4)`.
This expression is completely interchangeable with the output value it produces,
so writing `addOne(0) * 2` is exactly the same as writing `1 * 2`.

Functions (and their equivalents in other languages) are a **very** important
part of writing software.

1.  Functions allow code to be reused, so that the same problem doesn't need
    to be solved twice.

2.  Building simple functions, and using them to create more complex ones, is
    one way that a complex problem can be broken up into several smaller,
    less complex problems that can be tackled separately.

3.  Functions can be **modular** in that two functions which produce the same
    results are usually interchangeable,
    _even if they work in completely different ways_.

4.  Functions can be turned into **methods** by attaching them to objects;
    not only does this offer a nice way to model something's _behaviors_ as well
    as its _attributes_, it also means that the function's behavior can be tied
    to the values of that specific object's properties.

    ```js
    var person = {
      name: 'Matt',
      greet: function(){
        console.log(`Hi! My name is ${this.name}.`)
      }
    };
    person.greet(); // => 'Hi! My name is Matt.'
    ```

## Event Handlers

One very big role that functions can play in the context of a web page or web
application is acting as **event handlers**. When certain types of events
(such as a mouse click, or hovering over a location) happen, the browser is able
to respond by running a predefined, event-specific function to properly handle
that event.

Just for perspective, here are some of the types of events that event handlers
can respond to:

-   a mouse click

-   the mouse button switching from an 'up' position to a 'down' position (or
    vice versa)

-   the mouse moving into, or out of, a particular space on the screen

-   the user entering (loading) or leaving (unloading) a page

-   a change in the value of an input field

-   entering a particular key in the keyboard

More complete lists can be found
[here](http://www.w3schools.com/jsref/dom_obj_event.asp) and
[here](https://developer.mozilla.org/en-US/docs/Web/Events).
You can also define custom events and trigger them as part of your code.

To add an event handler in jQuery, you'll want to use the `.on` method of some
jQuery object. For instance, if we wanted to run the function `printText` every
time someone clicked the button with id 'click-me', we simply write

```js
var printText = function(){
  console.log("HERE'S SOME TEXT!");
};
$('#click-me').on('click', printText);
```

Alternatively, if we wanted, we could define that function right inside the
`on` method call; this approach could make sense if we were not planning to
reuse our handler code for something else.

```js
$('#click-me').on('click', function(){
  console.log("HERE'S SOME TEXT!");
});
```
