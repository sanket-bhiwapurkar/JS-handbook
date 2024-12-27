# Questions

- 01 What are conditional statements and why they are used?
- 02 Name all the conditional Statements.
- 03 Explain all the conditional Statements in detail.
- 04 What is Common Code Blocks in switch statement.

# Conditional Statements

Very often when you write code, you want to perform different actions for different decisions.

Conditional statements are used to perform different actions based on different conditions.

In JavaScript we have the following conditional statements:

- Use `if` to specify a block of code to be executed, if a specified condition is true
- Use `else` to specify a block of code to be executed, if the same condition is false
- Use `else if` to specify a new condition to test, if the first condition is false
- Use `switch to` specify many alternative blocks of code to be executed

## The if Statement

Use the if statement to specify a block of JavaScript code to be executed if a condition is true.

Syntax:

```JS
if (condition) {
  //  block of code to be executed if the condition is true
}
```

Note that if is in lowercase letters. Uppercase letters (If or IF) will generate a JavaScript error.

```JS
if (hour < 18) {
  greeting = "Good day";
}
```

```Bash
Good day
```

## The else Statement

Use the else statement to specify a block of code to be executed if the condition is false.

```JS
if (condition) {
  //  block of code to be executed if the condition is true
} else {
  //  block of code to be executed if the condition is false
}
```

Example

If the hour is less than 18, create a "Good day" greeting, otherwise "Good evening":

```JS
if (hour < 18) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
```

```JS
Good day
```

## The else if Statement

Use the else if statement to specify a new condition if the first condition is false.

Syntax

```JS
if (condition1) {
  //  block of code to be executed if condition1 is true
} else if (condition2) {
  //  block of code to be executed if the condition1 is false and condition2 is true
} else {
  //  block of code to be executed if the condition1 is false and condition2 is false
}
```

Example

If time is less than 10:00, create a "Good morning" greeting, if not, but time is less than 20:00, create a "Good day" greeting, otherwise a "Good evening":

```JS
if (time < 10) {
  greeting = "Good morning";
} else if (time < 20) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
```

```Bash
Good morning
```

## Switch Statement

The switch statement is used to perform different actions based on different conditions. The JavaScript Switch Statement

We use the switch statement to select one of many code blocks to be executed.

Syntax

```JS
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

### Switching Details

This is how it works:

- The switch expression is evaluated once.
- The value of the expression is compared with the values of each case.
- If there is a match, the associated block of code is executed.
- If multiple cases matches a case value, the first case is selected.
- If there is no match, the default code block is executed.
- If no default label is found, the program continues to the statement(s) after the switch.

Example

The getDay() method returns the weekday as a number between 0 and 6. (Sunday=0, Monday=1, Tuesday=2 ..)

This example uses the weekday number to calculate the weekday name:

```JS
switch (new Date().getDay()) {
case 0:
day = "Sunday";
break;
case 1:
day = "Monday";
break;
case 2:
day = "Tuesday";
break;
case 3:
day = "Wednesday";
break;
case 4:
day = "Thursday";
break;
case 5:
day = "Friday";
break;
case 6:
day = "Saturday";
}
```

```bash
Thursday
```

### The break Keyword

When JavaScript reaches a break keyword, it breaks out of the switch block.

This will stop the execution inside the switch block.

It is not necessary to break the last case in a switch block. The block breaks (ends) there anyway.

**Note**: If you omit the break statement, the next case will be executed even if the evaluation does not match the case.

### The default Keyword

The default keyword specifies the code to run if there is no case match:
Example

The getDay() method returns the weekday as a number between 0 and 6.

If today is neither Saturday (6) nor Sunday (0), write a default message:

```JS
switch (new Date().getDay()) {
  case 6:
    text = "Today is Saturday";
    break;
  case 0:
    text = "Today is Sunday";
    break;
  default:
    text = "Looking forward to the Weekend";
}
```

```JS
Looking forward to the Weekend
```

The default case does not have to be the last case in a switch block:

Example

```JS
switch (new Date().getDay()) {
  default:
    text = "Looking forward to the Weekend";
    break;
  case 6:
    text = "Today is Saturday";
    break;
  case 0:
    text = "Today is Sunday";
}
```

If default is not the last case in the switch block, remember to end the default case with a break.

### Common Code Blocks

Sometimes you will want different switch cases to use the same code.

In this example case 4 and 5 share the same code block, and 0 and 6 share another code block:

Example

```JS
switch (new Date().getDay()) {
  case 4:
  case 5:
    text = "Soon it is Weekend";
    break;
  case 0:
  case 6:
    text = "It is Weekend";
    break;
  default:
    text = "Looking forward to the Weekend";
}
```

### Strict Comparison

Switch cases use strict comparison (===).

The values must be of the same type to match.

A strict comparison can only be true if the operands are of the same type.

In this example there will be no match for x:

```JS
Example
let x = "0";
switch (x) {
  case 0:
    text = "Off";
    break;
  case 1:
    text = "On";
    break;
  default:
    text = "No value found";
}
```
