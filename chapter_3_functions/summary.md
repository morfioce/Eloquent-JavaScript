## Summary

This chapter taught you how to write your own functions. The function keyword, when used as an expression, can create a function value. When used as a statement, it can be used to declare a variable and give it a function as its value.

<strong>Create a function value f</strong>
```javascript
var f = function(a) {
  console.log(a + 2);
};
```

<strong>Declare g to be a function</strong>
```javascript
function g(a, b) {
  return a * b * 3.5;
}
```

A key aspect in understanding functions is understanding local scopes. Parameters and variables declared inside a function are local to the function, re-created every time the function is called, and not visible from the outside. Functions declared inside another function have access to the outer function’s local scope.

Separating the tasks your program performs into different functions is helpful. You won’t have to repeat yourself as much, and functions can make a program more readable by grouping code into conceptual chunks, in the same way that chapters and sections help organize regular text.