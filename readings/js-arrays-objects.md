[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Reading : Arrays and Objects in JavaScript

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
