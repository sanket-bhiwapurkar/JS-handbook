# Functions

A JavaScript function is a block of code designed to perform a particular task.

A JavaScript function is executed when "something" invokes it (calls it).

## Function Declarations Syntax

A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().

Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).

The parentheses may include parameter names separated by commas:

(parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: {}

```JS
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
```

```JS
function myFunction(a, b) {
  return a * b;
}
```

Function parameters are listed inside the parentheses () in the function definition.

Function arguments are the values received by the function when it is invoked.

Inside the function, the arguments (the parameters) behave as local variables.

## Function Expressions

A JavaScript function can also be defined using an expression.

A function expression can be stored in a variable:

Example

```JS
const x = function (a, b) {return a \* b};
```

After a function expression has been stored in a variable, the variable can be used as a function:

Example

```JS
const x = function (a, b) {return a \* b};
let z = x(4, 3);
```

The function above is actually an anonymous function (a function without a name).

Functions stored in variables do not need function names. They are always invoked (called) using the variable name.

The function above ends with a semicolon because it is a part of an executable statement.

## The Function() Constructor

As you have seen in the previous examples, JavaScript functions are defined with the function keyword.

Functions can also be defined with a built-in JavaScript function constructor called Function().

Example

```JS
const myFunction = new Function("a", "b", "return a * b");

let x = myFunction(4, 3);

```

You actually don't have to use the function constructor. The example above is the same as writing:

Example

```JS
const myFunction = function (a, b) {return a \* b};

let x = myFunction(4, 3);
```

## Arrow Functions

Arrow functions allows a short syntax for writing function expressions.

You don't need the function keyword, the return keyword, and the curly brackets.

Example

```JS
// ES5
var x = function(x, y) {
  return x * y;
}

// ES6
const x = (x, y) => x * y;
```

Arrow functions do not have their own this. They are not well suited for defining object methods.

Arrow functions are not hoisted. They must be defined before they are used.

Using const is safer than using var, because a function expression is always constant value.

You can only omit the return keyword and the curly brackets if the function is a single statement. Because of this, it might be a good habit to always keep them:

Example

```JS
hello = (val) => "Hello " + val;
```

In fact, if you have only one parameter, you can skip the parentheses as well:

```JS
hello = val => "Hello " + val;
```

Arrow functions are not supported in IE11 or earlier.

## Self-Invoking Functions

Function expressions can be made "self-invoking".

A self-invoking expression is invoked (started) automatically, without being called.

Function expressions will execute automatically if the expression is followed by ().

You cannot self-invoke a function declaration.

You have to add parentheses around the function to indicate that it is a function expression:
Example

```JS
(function () {
  let x = "Hello!!";  // I will invoke myself
})();
```

The function above is actually an anonymous self-invoking function (function without name).

## Functions Can Be Used as Values

JavaScript functions can be used as values:

Example

```JS
function myFunction(a, b) {
  return a * b;
}

let x = myFunction(4, 3);
```

JavaScript functions can be used in expressions:

Example

```JS
function myFunction(a, b) {
  return a * b;
}

let x = myFunction(4, 3) * 2;
```

## Functions are Objects

The typeof operator in JavaScript returns "function" for functions.

But, JavaScript functions can best be described as objects.

JavaScript functions have both properties and methods.

The arguments.length property returns the number of arguments received when the function was invoked:

Example

```JS
function myFunction(a, b) {
  return arguments.length;
}
```

The toString() method returns the function as a string:

Example

```JS
function myFunction(a, b) {
  return a * b;
}

let text = myFunction.toString();
```

A function defined as the property of an object, is called a method to the object.

A function designed to create new objects, is called an object constructor.

## Hoisting

Hoisting applies to variable declarations and to function declarations.

Because of Hoisting, JavaScript functions can be called before they are declared:

```JS
myFunction(5);

function myFunction(y) {
return y \* y;
}
```

Functions defined using an expression are not hoisted. They must be defined before they are used.

Arrow functions are not hoisted. They must be defined before they are used.
