## Callbacks

A reference to executable code, or a piece of executable code, that is passed as an argument to other code. The callback function is then called (or executed) inside of a containing function. A callback function has access to the containing function's scope, so they can access the containing function's variables and parameters, and even the variables from the global scope.

```js
function fullName(firstName, lastName, callback){
  console.log("My name is " + firstName + " " + lastName);
  callback(lastName);
}

var greeting = function(ln){
  console.log('Welcome Mr. ' + ln);
};

fullName("Jackie", "Chan", greeting);
```

The callback function can be an existing function (see example above) or an anonymous function that is created when the containing function is called (see example below).

```js
function fullName(firstName, lastName, callback){
  console.log("My name is " + firstName + " " + lastName);
  callback(lastName);
}

fullName("Jackie", "Chan", function(ln){
  console.log('Welcome Mr. ' + ln);
});
```

Callbacks are just functions that get executed at some later time. The key to understanding callbacks is to realize that they are used when you don't know **when** some async operation will complete, but you do know **where** the operation will complete — the last line of the asyncronous function!

### References
* [Understanding Callback Functions in Javascript](http://recurial.com/programming/understanding-callback-functions-in-javascript/)
* [Callbacks](https://github.com/maxogden/art-of-node#callbacks) by Max Ogden
* [Callback Functions in Javascript](http://www.impressivewebs.com/callback-functions-javascript/) by Louis Lazaris