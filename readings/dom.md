[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Reading : The DOM

OK, it's time you learned the the truth. When you heard earlier that we were
grabbing HTML elements and manipulating them, this was actually a lie (albeit, a
useful lie). In fact, what we were doing was manipulating _programmatic objects_
_**representing** HTML elements_. The browser uses all of these objects to keep
track of all of the data associated with a page.

Every browser today provides a JavaScript interface for interacting with this
'document-object model', or DOM. To access the top-level object, you can simply
type `document` in your JS, and you'll have it.

To grab and manipulate the object (or object**s**) associated with a set of
elements, we can call `document.getElementsByTagName(/* tag name */)` or
`document.getElementsByClassName(/* class name */)`, or even
`document.querySelector(/* CSS selector */)` if we want to get fancy.

Each of those will give us back an array of JS objects -- specifically,
DOM elements -- which we can then manipulate like any other array of objects.

A full list of the properties available on a JS DOM object can be found
[here](https://developer.mozilla.org/en-US/docs/Web/API/Element),
but the ones you're most likely to use are the `.innerhtml`
(for changing the inside of an element), `.children` (to grab a list of elements
inside a given element), and `.style`
(to modify [CSS styling](http://www.w3schools.com/cssref) for that element).

One last note before getting started:
We can run JS code in the browser console and access the DOM that
way, but in order to actually load a JS file from our HTML, like we did with CSS
earlier today, we need to include a `<script>` tag whose `src` property is set
to the path from the HTML file to the JS code (just like we did with `href`
inside the `<link>` tag).
