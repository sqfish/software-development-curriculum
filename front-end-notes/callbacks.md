## Callbacks

> A reference to executable code, or a piece of executable code, that is passed as an argument to other code. The callback function is then called (or executed) inside of a containing function.
> Callback functions have access to the containing function's scope, so they can access the containing functions' variables, and even the variables from the global scope.
> Can be used to handle when the status of an asynchronous operation is updated.

```js
function someAction(x, y, someCallback) {
    return someCallback(x, y);
}

function calcProduct(x, y) {
    return x * y;
}

function calcSum(x, y) {
    return x + y;
}

alert(someAction(5, 15, calcProduct));

alert(someAction(5, 15, calcSum));
```