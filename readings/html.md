[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Reading : HTML

**HTML** stands for "hypertext markup language". "hypertext" means text that is
'more than text', i.e. capable of linking to other HTML pages.
For the non-lawyers or editors among us, "marking up" is the process of adding
notes and other addiitonal information to an existing document.

```markdown
Four score and seven years ago our fathers brought forth on this continent,
a new nation, conceived in Liberty,
and dedicated to the proposition that all men are created equal.

Now we are engaged in a great civil war, testing whether that nation,
or any nation so conceived and so dedicated, can long endure.
We are met on a great battle-field of that war....
```

might become

```html
<html>
  <body>
    <p> Four score and seven years ago... </p>
    <p> Now we are engaged in a great civil war, ... </p>
    <!-- By the way, this thing here is called a 'comment'. -->
    <!--
      It's a way of writing extra information into a document that you don't
      want to be visible. Comments exist in many languages; this is just
      how they're written in HTML.
    -->
  </body>
</html>
```

The `html` tags show where our HTML code begins and ends. `body` shows us where
the "body" -- the visible part of our document -- starts and ends. The `p` tags
each indicate that the text inside them comprises a single paragraph. Note that
the 'closing' tag in a pair always has a `/` before its name.

HTML tags (almost) always come in pairs, and their primary purpose (at least as
of the most recent version of HTML, HTML5) is to label and classify the content
on your page into **elements**.
This makes it possible for use to add styles (CSS)
or behavior (JS) by referring to a particular element. If our content wasn't
tagged, the browser would need to read through the content of the text itself
and determine how the content should be grouped -- a VERY difficult problem.

Here are a few other common HTML tag types:

-   `h1`/`h2`/`h3`/`h4`/`h5` : Topic headings for your document.
    `h1` tags represent top-level headings, and browsers show them as the
    largest by default. Each successive tag represents a less important
    (and by default, smaller in appearance).

-   `a` : 'a' for 'anchor'. These tags are old school HTML; they create visible,
    clickable links inside your web page that load other pages and/or files.

-   `img` : An image. Simple, right? Also noteworthy is that it's one of few
    tags that _isn't_ paired.

-   `span` : An arbitrary grouping of text. By default, it adds no visible
    changes to your text.

-   `div` : An arbitrary block of space containing visible elements on a page.
    By default, it stretches all the way across the screen, but is only as tall
    as the tallest element inside of it; if nothing is inside it, it looks like
    a flat line.

-   `ol`/`ul`, `li` : Respectively, an ordered (ie. numbered) list or
    unordered (i.e. bulleted) list, and a list item which is part of that list.
