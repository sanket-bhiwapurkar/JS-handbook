# Loops

Loops can execute a block of code a number of times. Loops are handy, if you want to run the same code over and over again, each time with a different value. Often this is the case when working with arrays:

Instead of writing:

```JS
text += cars[0] + "<br>";
text += cars[1] + "<br>";
text += cars[2] + "<br>";
text += cars[3] + "<br>";
text += cars[4] + "<br>";
text += cars[5] + "<br>";
```

You can write:

```JS
for (let i = 0; i < cars.length; i++) {
  text += cars[i] + "<br>";
}
```

JavaScript supports different kinds of loops:

- while - loops through a block of code while a specified condition is true
- do/while - also loops through a block of code while a specified condition is true
- for - loops through a block of code a number of times
- for/in - loops through the properties of an object
- for/of - loops through the values of an iterable object

## The While Loop

The while loop loops through a block of code as long as a specified condition is true.

Syntax

```JS
while (condition) {
  // code block to be executed
}
```

Example

In the following example, the code in the loop will run, over and over again, as long as a variable (i) is less than 10:

Example

```JS
let text = "";
let i = 0;
while (i < 10) {
  text += "The number is " + i;
  i++;
}
```

```bash
The number is 0
The number is 1
The number is 2
The number is 3
The number is 4
The number is 5
The number is 6
The number is 7
The number is 8
The number is 9
```

If you forget to increase the variable used in the condition, the loop will never end. This will crash your browser.

## The Do While Loop

The do while loop is a variant of the while loop. This loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.

Syntax

```JS
do {
  // code block to be executed
}
while (condition);
```

Example

The example below uses a do while loop. The loop will always be executed at least once, even if the condition is false, because the code block is executed before the condition is tested:

Example

```JS
let text = ""
let i = 10;
do {
  text += "The number is " + i;
  i++;
}
while (i < 10);
```

```bash
The number is 0
```

Whereas, while loop won't be executed

```JS
let text = "";
let i = 10;
while (i < 10) {
  text += "<br>The number is " + i;
  i++;
}
```

```bash
// no output
```

## The For Loop

The for statement creates a loop with 3 optional expressions:

```JS
for (expression 1; expression 2; expression 3) {
  // code block to be executed
}
```

Expression 1 is executed (one time) before the execution of the code block.

Expression 2 defines the condition for executing the code block.

Expression 3 is executed (every time) after the code block has been executed.

Example

```JS
for (let i = 0; i < 5; i++) {
text += "The number is " + i + "<br>";
}
```

From the example above, you can read:

Expression 1 sets a variable before the loop starts (let i = 0).

Expression 2 defines the condition for the loop to run (i must be less than 5).

Expression 3 increases a value (i++) each time the code block in the loop has been executed.

### Expression 1

Normally you will use expression 1 to initialize the variable used in the loop (let i = 0).

This is not always the case. JavaScript doesn't care. Expression 1 is optional.

You can initiate many values in expression 1 (separated by comma):

Example

```JS
for (let i = 0, len = cars.length, text = ""; i < len; i++) {
  text += cars[i] + "<br>";
}
```

And you can omit expression 1 (like when your values are set before the loop starts):

Example

```JS
let i = 2;
let len = cars.length;
let text = "";
for (; i < len; i++) {
  text += cars[i] + "<br>";
}
```

### Expression 2

Often expression 2 is used to evaluate the condition of the initial variable.

This is not always the case. JavaScript doesn't care. Expression 2 is also optional.

If expression 2 returns true, the loop will start over again. If it returns false, the loop will end.

If you omit expression 2, you must provide a break inside the loop. Otherwise the loop will never end. This will crash your browser. Read about breaks in a later chapter of this tutorial.

### Expression 3

Often expression 3 increments the value of the initial variable.

This is not always the case. JavaScript doesn't care. Expression 3 is optional.

Expression 3 can do anything like negative increment (i--), positive increment (i = i + 15), or anything else.

Expression 3 can also be omitted (like when you increment your values inside the loop):

Example

```JS
let i = 0;
let len = cars.length;
let text = "";
for (; i < len; ) {
text += cars[i] + "<br>";
i++;
}
```

### Loop Scope

Using var in a loop:

Example

```JS
var i = 5;

for (var i = 0; i < 10; i++) {
  // some code
}

// Here i is 10
```

Using let in a loop:

Example

```JS
let i = 5;

for (let i = 0; i < 10; i++) {
  // some code
}

// Here i is 5
```

In the first example, using var, the variable declared in the loop redeclares the variable outside the loop.

In the second example, using let, the variable declared in the loop does not redeclare the variable outside the loop.

When let is used to declare the i variable in a loop, the i variable will only be visible within the loop.

Using const in a loop will throw an error

## The For In Loop

The JavaScript for in statement loops through the properties of an Object:

Syntax

```JS
for (key in object) {
  // code block to be executed
}
```

Example

```JS
const person = {fname:"John", lname:"Doe", age:25};

let text = "";
for (let x in person) {
  text += person[x];
}

```

Example Explained

- The for in loop iterates over a person object
- Each iteration returns a key (x)
- The key is used to access the value of the key
- The value of the key is person[x]

Do not use for in over an Array if the index order is important.

The index order is implementation-dependent, and array values may not be accessed in the order you expect.

It is better to use a for loop, a for of loop, or Array.forEach() when the order is important.

## The For Of Loop

The JavaScript for of statement loops through the values of an iterable object.

It lets you loop over iterable data structures such as Arrays, Strings, Maps, NodeLists, and more:

Syntax

```JS
for (variable of iterable) {
  // code block to be executed
}
```

variable - For every iteration the value of the next property is assigned to the variable. Variable can be declared with const, let, or var.

iterable - An object that has iterable properties.

### Looping over an Array

Example

```JS
const cars = ["BMW", "Volvo", "Mini"];

let text = "";
for (let x of cars) {
  text += x;
}
```

### Looping over a String

Example

```JS
let language = "JavaScript";

let text = "";
for (let x of language) {
text += x;
}
```
