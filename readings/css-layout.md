[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Reading : CSS for Layout

In addition to setting the values of colors and fonts, CSS can also be used to
specify how pieces of your page are laid out.

The most basic system for this is called the **box model**.
Essentially, it treats every element on your page as a box, with predefined
dimensions (margin, padding, border) that can be specified to organize space.
If we were to analogize it to having a [picture in a frame](http://www.ikea.com/PIAimages/0313893_PE513763_S5.JPG),

-   `border` would be the thickness of the frame.

-   `padding` would be the dimensions of the matte around the picture -- how far
    the picture is offset from the _interior of the frame_.

-   `margin` would be the distance that the _outside of the frame_ would be
    offset from things around the picture, such as the floor or other paintings.

However this is still fairly limiting. Although we can establish some space
around elements, they still can only line up from top to bottom. Why is that?

The reason is that there are actually two categories of HTML elements:
**block** elements and **inline** elements. Inline elements are elements that
exist interspersed with text; since text wraps to the size of its container,
these elements also wrap. `span` is the most basic member of this group.
Block elements, in contrast, represent things that take up space on the page,
such as paragraphs or images. These elements do not wrap, and instead only stack
vertically.

There are ways to change this behavior.
For instance, every element has a property called `display`,
which determines how the browser displays a particular element.
By setting this property to either `inline` or `block`, respectively,
block elements can be made to wrap and inline elements can be made to stack.
Elements can even be made to disappear by setting this property to `none`.

Another approach, built on top of the first, uses two properties called `float`
and `clear`. This system allows you to not only treat a bunch of elements as
inline elements, it also allows you to indicate when any given element
_and all subsequent elements_ should drop down.

If four `div` elements are floated to the left, they will be
arranged like so:

```markdown
|[ 1 ] [ 2 ] [ 3 ] [ 4 ]     (more space)
```

These elements will wrap as space allows.

> Note: They will also no longer keep open any `div` elements that contain them;
> if you aren't careful, this can cause divs' heights to suddenly drop to 0.

However, if we were to set the `clear` property of the second `div` to `left`,
it would drop down below the first `div`, as would all subsequent divs
(which would otherwise continue to wrap).

```markdown
|[ 1 ]
|[ 2 ] [ 3 ] [ 4 ]     (more space)
```

If you think of floated elements as words in a set of text,
'clearing' an element makes a new line and puts that element at the beginning
of the line.

Floating to the right is the same but in the opposite direction (kind of like
writing in a right-to-left language, like hebrew or japanese).

```markdown
(more space)    [ 4 ] [ 3 ] [ 2 ] [ 1 ]|
```

`clear:left` breaks up `float:left`,
while `clear:right` breaks up `float:right`,
and `clear:both` will break up either.
