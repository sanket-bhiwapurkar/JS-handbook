# Keywords/Reserved Words

JavaScript statements often start with a keyword to identify the JavaScript action to be performed. JavaScript keywords are reserved words. Reserved words cannot be used as names for variables.

Here is a list of some of the keywords:

| Keyword  | Description                                                   |
| -------- | ------------------------------------------------------------- |
| var      | Declares a variable                                           |
| let      | Declares a block variable                                     |
| if       | Marks a block of statements to be executed on a condition     |
| switch   | Marks a block of statements to be executed in different cases |
| for      | Marks a block of statements to be executed in a loop          |
| function | Declares a function                                           |
| return   | Exits a function                                              |
| try      | Implements error handling to a block of statements            |

Our [Reserved Words Reference](https://www.w3schools.com/js/js_reserved.asp) lists all JavaScript keywords.

# JavaScript Identifiers

All JavaScript variables must be identified with unique names.

These unique names are called identifiers.

Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume).

The general rules for constructing names for variables (unique identifiers) are:

- Names can contain letters, digits, underscores, and dollar signs.
- Names must begin with a letter.
- Names can also begin with $ and \_.
- Names are case sensitive (y and Y are different variables).
- Reserved words (like JavaScript keywords) cannot be used as names.

### JavaScript is Case Sensitive

All JavaScript identifiers are case sensitive.

The variables lastName and lastname, are two different variables:

```JS
let lastname, lastName;
lastName = "Doe";
lastname = "Peterson";
```

JavaScript does not interpret LET or Let as the keyword let.

### JavaScript Dollar Sign $

Since JavaScript treats a dollar sign as a letter, identifiers containing $ are valid variable names:

```JS
let $ = "Hello World";
let $$$ = 2;
let $myMoney = 5;
```

Using the dollar sign is not very common in JavaScript, but professional programmers often use it as an alias for the main function in a JavaScript library.

### JavaScript Underscore (\_)

Since JavaScript treats underscore as a letter, identifiers containing \_ are valid variable names:

```JS
let _lastName = "Johnson";
let _x = 2;
let _100 = 5;
```

Using the underscore is not very common in JavaScript, but a convention among professional programmers is to use it as an alias for "private (hidden)" variables.
