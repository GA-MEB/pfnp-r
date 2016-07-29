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
inside a given element), `.style` (to directly modify
[CSS styling](http://www.w3schools.com/cssref) for that element), and
[`.classList`](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList)
(for adding and removing CSS classes).

## jQuery

In the field, you'll often see people using a JavaScript **library**
(a published collection of code) called [**jQuery**](http://jquery.com/)
for manipulating the DOM.

| Vanilla JS Syntax                                      | Rough jQuery Equivalent                            |
|--------------------------------------------------------|----------------------------------------------------|
| `document.getElementsByTagName('li')`                  | `$('li')`                                          |
| `document.getElementsByClassName('my-class')`          | `$('.my-class')`                                   |
| `document.getElementById('submit-form')`               | `$('#submit-form')`                                |
| `someJsDomElement.innerHTML = '<p> New text </p>'`     | `$someJqueryObject.html('<p> New text </p>')`      |
| `someJsDomElement.innerHTML += '<p> New text </p>'`    | `$someJqueryObject.append('<p> New text </p>')`    |
| `someJsDomElement.classList.add('class-to-add')`       | `$someJqueryObject.addClass('class-to-add')`       |
| `someJsDomElement.classList.remove('class-to-remove')` | `$someJqueryObject.removeClass('class-to-remove')` |
| `someJsDomElement.style.color`                         | `$someJqueryObject.css('color')`                   |
| `someJsDomElement.style.color = '#FF0000'`             | `$someJqueryObject.css('color', '#FF0000')`        |

> 'ID' is another type of property, like classes, that can be used to identify
> DOM elements. However, unlike classes, an element can only have one ID, and an
> ID can only refer to one element. In terms of specificity, ID rules beat even
> class rules; nevertheless, it is more common to see IDs used with JavaScript
> than CSS, because (a) with JS, the uniqueness of an ID helps to avoid
> incorrect behavior, and (b) with CSS, you're often in the position of wanting
> to use styles in multiple places.
> **TL;DR** : Use classes for styling; use IDs for working with JS.

As you can see, the jQuery commands tend to be shorter, and this has the nice
effect of making code easer to read (a _very_ good thing -- code that's easy
to read and understand is usually code that's easy to maintain and update).

They also all use an existing standard, CSS selectors, as their default
system for looking up elements; though the ordinary JS DOM supports that through
`document.querySelector`, it's still a clunkier interface than jQuery.
And on top of all of that, jQuery doesn't just give back an array of elements --
it gives back a special jQuery object, which provides additional helpful
properties and pre-programmed behaviors that make working with the collection
rather easy.

However, many developers dislike jQuery because they feel that it's too complex
a library, and tries to do too many things (DOM manipulation, event handling
animations, and more).
It also runs more slowly slower than plain-old-vanilla JavaScript,
[as certain snarky devs like to point out](http://vanilla-js.com/),
and it's less well supported by older web browsers.

Since jQuery is an external library, you need to either downloaded it from
the [official jQuery website](http://jquery.com/), or link to a hosted copy of
the code through a [**content delivery network**](https://code.jquery.com/),
or **CDN**. The advantage to using a CDN is that you don't need to
download anything, but the downside is that you'll only be able to access
the library when your internet is working...

To load jQuery into your page so that you can use it in your own code,
create another pair of `<script>` tags
**above the tags that load your own JS code**,
and set `src` to whatever location (CDN or local) jQuery is at.

The full documentation for jQuery is available online [here](http://api.jquery.com).
