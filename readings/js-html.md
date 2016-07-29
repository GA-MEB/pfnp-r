[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Reading : Adding JS to Your Webpage

OK, so you can write some basic JS code. How do you get it to load with your
page?

As it turns out, the process is very similar to how CSS gets loaded.
For your page to load JS code, you need to add a pair of `<script>` tags into
your page.

Once you have the tags in your page, you have two options. Either

1.  Write JavaScript code in the HTML file itself, between the two `<script>`
    tags,

    ```html
    <script>
      var a = 1;
      var b = 2;
      console.log(a + b);
    </script>
    ```

    or

2.  Have the first `<script>` tag reference another file contianing JS code,
    using its `src` (source) property.

    ```html
    <script src="scripts/main.js"></script>
    ```

    ```js
    // scripts/main.js
    var a = 1;
    var b = 2;
    console.log(a + b);
    ```

In both cases, the JS code will get loaded by the browser when it reaches the
`<script>` tag, so for now, we'll want those tags to live at the bottom of the
body -- that way they never try to reference an element that hasn't loaded yet.
There are tricks we can use in our JS to make it so that the location doesn't
matter, but we might not get to them today.
