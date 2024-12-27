# Questions

- 01 What are operators in JS?
- 02 Explain differennt Operators in detail.
- 03 Explain precedence in detail.

# Operators (Mnemonics: LARA Croft DI ON BTS)

Javascript operators are used to perform different types of mathematical and logical computations.

## JavaScript Logical Operators

Logical operators are used to determine the logic between variables or values.

| Operator | Description |
| -------- | ----------- |
| &&       | logical and |
| \|       | logical or  |
| !        | logical not |

## JavaScript Arithmetic Operators

Arithmetic operators perform arithmetic on numbers (literals or variables).

| Operator | Description             |
| -------- | ----------------------- |
| -        | Addition                |
| \*       | Subtraction             |
| -        | Multiplication          |
| \*\*     | Exponentiation (ES2016) |
| /        | Division                |
| %        | Modulus (Remainder)     |
| ++       | Increment               |
| --       | Decrement               |

## Relational/Comparison Operators

Comparison operators are used in logical statements to determine equality or difference between variables or values.

| Operator | Description                       |
| -------- | --------------------------------- |
| ==       | equal to                          |
| ===      | equal value and equal type        |
| !=       | not equal                         |
| !==      | not equal value or not equal type |
| >        | greater than                      |
| <        | less than                         |
| >=       | greater than or equal to          |
| <=       | less than or equal to             |
| ?:       | ternary operator                  |

## Assignment Operators

The Simple Assignment Operator assigns a value to a variable.

```JS
let x = 10;
```

| Operator | Example   | Same As      |
| -------- | --------- | ------------ |
| =        | x = y     | x = y        |
| +=       | x += y    | x = x + y    |
| -=       | x -= y    | x = x - y    |
| \*=      | x \*= y   | x = x \* y   |
| /=       | x /= y    | x = x / y    |
| %=       | x %= y    | x = x % y    |
| \*\*=    | x \*\*= y | x = x \*\* y |

[See More](https://www.w3schools.com/js/js_assignment.asp)

## Bitwise Operators

| Operator | Name                  | Description                                                                                              |
| -------- | --------------------- | -------------------------------------------------------------------------------------------------------- |
| &        | AND                   | Sets each bit to 1 if both bits are 1                                                                    |
| \|       | OR                    | Sets each bit to 1 if one of two bits is 1                                                               |
| ^        | XOR                   | Sets each bit to 1 if only one of two bits is 1                                                          |
| ~        | NOT                   | Inverts all the bits                                                                                     |
| <<       | Zero fill left shift  | Shifts left by pushing zeros in from the right and let the leftmost bits fall off                        |
| >>       | Signed right shift    | Shifts right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off |
| >>>      | Zero fill right shift | Shifts right by pushing zeros in from the left, and let the rightmost bits fall off                      |

| Operation | Result | Same as      | Result |
| --------- | ------ | ------------ | ------ |
| 5 & 1     | 1      | 0101 & 0001  | 0001   |
| 5 \| 1    | 5      | 0101 \| 0001 | 0101   |
| ~ 5       | 10     | ~0101        | 1010   |
| 5 << 1    | 10     | 0101 << 1    | 1010   |
| 5 ^ 1     | 4      | 0101 ^ 0001  | 0100   |
| 5 >> 1    | 2      | 0101 >> 1    | 0010   |
| 5 >>> 1   | 2      | 0101 >>> 1   | 0010   |

[See more](https://www.w3schools.com/js/js_bitwise.asp)

## Conditional (Ternary) Operator

JavaScript also contains a conditional operator that assigns a value to a variable based on some condition.

```JS
let voteable = (age < 18) ? "Too young":"Old enough";
```

If the variable age is a value below 18, the value of the variable voteable will be "Too young", otherwise the value of voteable will be "Old enough".

## The Optional Chaining Operator (?.)

The ?. operator returns undefined if an object is undefined or null (instead of throwing an error).

```JS
// Create an object:
const car = {type:"Fiat", model:"500", color:"white"};
// Ask for car name:
document.getElementById("demo").innerHTML = car?.name;

```

## The Nullish Coalescing Operator (??)

The ?? operator returns the first argument if it is not nullish (null or undefined).

Otherwise it returns the second argument.

```JS
let name = null;
let text = "missing";
let result = name ?? text;
```

## Type Operators

| Operator   | Description                                                |
| ---------- | ---------------------------------------------------------- |
| typeof     | Returns the type of a variable                             |
| instanceof | Returns true if an object is an instance of an object type |

| typeof                | result                 |
| --------------------- | ---------------------- |
| typeof "John"         | // Returns "string"    |
| typeof ("John"+"Doe") | // Returns "string"    |
| typeof 3.14           | // Returns "number"    |
| typeof (33 + 66)      | // Returns "number"    |
| typeof NaN            | // Returns "number"    |
| typeof 1234n          | // Returns "bigint"    |
| typeof true           | // Returns "boolean"   |
| typeof false          | // Returns "boolean"   |
| typeof {name:'John'}  | // Returns "object"    |
| typeof [1,2,3,4]      | // Returns "object"    |
| typeof {}             | // Returns "object"    |
| typeof []             | // Returns "object"    |
| typeof new Object()   | // Returns "object"    |
| typeof new Array()    | // Returns "object"    |
| typeof new Date()     | // Returns "object"    |
| typeof new Set()      | // Returns "object"    |
| typeof new Map()      | // Returns "object"    |
| typeof function () {} | // Returns "function"  |
| typeof x              | // Returns "undefined" |
| typeof null           | // Returns "object"    |

The instanceof operator returns true if an object is an instance of a specified object type:

```JS
// Create a Date
const time = new Date();

(time instanceof Date);
```

```JS
// Create an Array
const fruits = ["apples", "bananas", "oranges"];

(fruits instanceof Array);
```

```JS
// Create a Map
const fruits = new Map([
  ["apples", 500],
  ["bananas", 300],
  ["oranges", 200]
]);

(fruits instanceof Map);
```

```JS
// Create a Set
const fruits = new Set(["apples", "bananas", "oranges"]);

(fruits instanceof Set);
```

## Comparing Different Types

Comparing data of different types may give unexpected results.

When comparing a string with a number, JavaScript will convert the string to a number when doing the comparison. An empty string converts to 0. A non-numeric string converts to NaN which is always false.

| Case        | Value |
| ----------- | ----- |
| 2 < 12      | true  |
| 2 < "12"    | true  |
| 2 < "John"  | false |
| 2 > "John"  | false |
| 2 == "John" | false |
| "2" < "12"  | false |
| "2" > "12"  | true  |
| "2" == "12" | false |

When comparing two strings, "2" will be greater than "12", because (alphabetically) 1 is less than 2.

```JS
To secure a proper result, variables should be converted to the proper type before comparison:
age = Number(age);
if (isNaN(age)) {
  voteable = "Input is not a number";
} else {
  voteable = (age < 18) ? "Too young" : "Old enough";
}
```

## Delete, in, spread operator

# Precedence

[See](https://www.w3schools.com/js/js_precedence.asp)
