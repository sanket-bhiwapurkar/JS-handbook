# Strings

Strings are for storing text

Strings are written with quotes

## Using Quotes

A JavaScript string is zero or more characters written inside quotes.

Example

```JS
let text = "John Doe";
```

You can use single or double quotes:

Example

```JS
let carName1 = "Volvo XC60";  // Double quotes
let carName2 = 'Volvo XC60';  // Single quotes
```

Strings created with single or double quotes work the same.

There is no difference between the two.

## Quotes Inside Quotes

You can use quotes inside a string, as long as they don't match the quotes surrounding the string:

Example

```JS
let answer1 = "It's alright";
let answer2 = "He is called 'Johnny'";
let answer3 = 'He is called "Johnny"';
```

## Template Strings

String Templates

Template Strings

Template Literals

Beloved child has many names

### Back-Tics Syntax

Template Strings use back-ticks (``) rather than the quotes ("") to define a string:

Example

```JS
let text = `Hello World!`;
```

### Quotes Inside Strings

Template Strings allow both single and double quotes inside a string:

Example

```JS
let text = `He's often called "Johnny"`;
```

### Multiline Strings

Template Strings allow multiline strings:

Example

```JS
let text =
`The quick
brown fox
jumps over
the lazy dog`;
```

### Interpolation

Template String provide an easy way to interpolate variables and expressions into strings.

The method is called string interpolation.

The syntax is:

```JS
${...}
```

### Variable Substitutions

Template Strings allow variables in strings:

Example

```JS
let firstName = "John";
let lastName = "Doe";

let text = `Welcome ${firstName}, ${lastName}!`;
```

Automatic replacing of variables with real values is called string interpolation.

### Expression Substitution

Template Strings allow expressions in strings:

Example

```JS
let price = 10;
let VAT = 0.25;

let total = `Total: ${(price * (1 + VAT)).toFixed(2)}`;
```

Automatic replacing of expressions with real values is called string interpolation.

### HTML Templates

Example

```JS
let header = "Template Strings";
let tags = ["template strings", "javascript", "es6"];

let html = `<h2>${header}</h2><ul>`;
for (const x of tags) {
  html += `<li>${x}</li>`;
}

html += `</ul>`;
```

# Basic String Methods

## String Length

The length property returns the length of a string:

Example

```JS
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = text.length;
```

## Extracting String Characters

There are 4 methods for extracting string characters:

- The at(position) Method
- The charAt(position) Method
- The charCodeAt(position) Method
- Using property access [] like in arrays

### JavaScript String charAt()

The charAt() method returns the character at a specified index (position) in a string:

Example

```JS
let text = "HELLO WORLD";
let char = text.charAt(0);
```

### JavaScript String charCodeAt()

The charCodeAt() method returns the code of the character at a specified index in a string:

The method returns a UTF-16 code (an integer between 0 and 65535).

Example

```JS
let text = "HELLO WORLD";
let char = text.charCodeAt(0);
```

### JavaScript String at()

ES2022 introduced the string method at():

Examples

Get the third letter of name:

```JS
const name = "W3Schools";
let letter = name.at(2);
```

Get the third letter of name:

```JS
const name = "W3Schools";
let letter = name[2];
```

The at() method returns the character at a specified index (position) in a string.

The at() method is supported in all modern browsers since March 2022:

Note

The at() method is a new addition to JavaScript.

It allows the use of negative indexes while charAt() do not.

Now you can use myString.at(-2) instead of charAt(myString.length-2).

### Property Access [ ]

Example

```JS
let text = "HELLO WORLD";
let char = text[0];
```

Note

Property access might be a little unpredictable:

- It makes strings look like arrays (but they are not)
- If no character is found, [ ] returns undefined, while charAt() returns an empty string.
- It is read only. str[0] = "A" gives no error (but does not work!)

Example

```JS
let text = "HELLO WORLD";
text[0] = "A"; // Gives no error, but does not work
```

## Extracting String Parts

There are 3 methods for extracting a part of a string:

- slice(start, end)
- substring(start, end)
- substr(start, length)

### JavaScript String slice()

slice() extracts a part of a string and returns the extracted part in a new string.

The method takes 2 parameters: start position, and end position (end not included).

Example

Slice out a portion of a string from position 7 to position 13:

```JS
let text = "Apple, Banana, Kiwi";
let part = text.slice(7, 13);
```

Note

JavaScript counts positions from zero.

First position is 0.

Second position is 1.

Examples

If you omit the second parameter, the method will slice out the rest of the string:

```JS
let text = "Apple, Banana, Kiwi";
let part = text.slice(7);
```

If a parameter is negative, the position is counted from the end of the string:

```JS
let text = "Apple, Banana, Kiwi";
let part = text.slice(-12);
```

This example slices out a portion of a string from position -12 to position -6:

```JS
let text = "Apple, Banana, Kiwi";
let part = text.slice(-12, -6);
```

### JavaScript String substring()

substring() is similar to slice().

The difference is that start and end values less than 0 are treated as 0 in substring().

Example

```JS
let str = "Apple, Banana, Kiwi";
let part = str.substring(7, 13);
```

If you omit the second parameter, substring() will slice out the rest of the string.

### JavaScript String substr()

substr() is similar to slice().

The difference is that the second parameter specifies the length of the extracted part.

Example

```JS
let str = "Apple, Banana, Kiwi";
let part = str.substr(7, 6);
```

If you omit the second parameter, substr() will slice out the rest of the string.

Example

```JS
let str = "Apple, Banana, Kiwi";
let part = str.substr(7);
```

If the first parameter is negative, the position counts from the end of the string.

Example

```JS
let str = "Apple, Banana, Kiwi";
let part = str.substr(-4);
```

## Converting to Upper and Lower Case

A string is converted to upper case with toUpperCase():

A string is converted to lower case with toLowerCase():

### JavaScript String toUpperCase()

Example

```JS
let text1 = "Hello World!";
let text2 = text1.toUpperCase();
```

### JavaScript String toLowerCase()

Example

```JS
let text1 = "Hello World!";       // String
let text2 = text1.toLowerCase();  // text2 is text1 converted to lower
```

## String Manipulation

There are 10 methods for Manipulating string characters:

- concat()
- trim()
- trimStart()
- trimEnd()
- padStart()
- padEnd()
- repeat()
- replace()
- replaceAll()
- split()

Note

All string methods return a new string. They don't modify the original string.

Formally said:

Strings are immutable: Strings cannot be changed, only replaced.

### JavaScript String concat()

concat() joins two or more strings:

Example

```JS
let text1 = "Hello";
let text2 = "World";
let text3 = text1.concat(" ", text2);
```

The concat() method can be used instead of the plus operator. These two lines do the same:

Example

```JS
text = "Hello" + " " + "World!";
text = "Hello".concat(" ", "World!");
```

### JavaScript String trim()

The trim() method removes whitespace from both sides of a string:

Example

```JS
let text1 = "      Hello World!      ";
let text2 = text1.trim();
```

### JavaScript String trimStart()

ECMAScript 2019 added the String method trimStart() to JavaScript.

The trimStart() method works like trim(), but removes whitespace only from the start of a string.

Example

```JS
let text1 = "     Hello World!     ";
let text2 = text1.trimStart();
```

### JavaScript String trimEnd()

ECMAScript 2019 added the string method trimEnd() to JavaScript.

The trimEnd() method works like trim(), but removes whitespace only from the end of a string.

Example

```JS
let text1 = "     Hello World!     ";
let text2 = text1.trimEnd();
```

### JavaScript String padStart()

The padStart() method pads a string from the start.

It pads a string with another string (multiple times) until it reaches a given length.

Examples

Pad a string with "0" until it reaches the length 4:

```JS
let text = "5";
let padded = text.padStart(4,"0");
```

Pad a string with "x" until it reaches the length 4:

```JS
let text = "5";
let padded = text.padStart(4,"x");
```

Note

The padStart() method is a string method.

To pad a number, convert the number to a string first.

See the example below.

Example

```JS
let numb = 5;
let text = numb.toString();
let padded = text.padStart(4,"0");
```

### JavaScript String padEnd()

The padEnd() method pads a string from the end.

It pads a string with another string (multiple times) until it reaches a given length.

Examples

```JS
let text = "5";
let padded = text.padEnd(4,"0");
let text = "5";
let padded = text.padEnd(4,"x");
```

Note

The padEnd() method is a string method.

To pad a number, convert the number to a string first.

See the example below.

Example

```JS
let numb = 5;
let text = numb.toString();
let padded = text.padEnd(4,"0");
```

### JavaScript String repeat()

The repeat() method returns a string with a number of copies of a string.

The repeat() method returns a new string.

The repeat() method does not change the original string.

Examples

Create copies of a text:

```JS
let text = "Hello world!";
let result = text.repeat(2);
let text = "Hello world!";
let result = text.repeat(4);
```

### Replacing String Content

The replace() method replaces a specified value with another value in a string:

Example

```JS
let text = "Please visit Microsoft!";
let newText = text.replace("Microsoft", "W3Schools");
```

Note

The replace() method does not change the string it is called on.

The replace() method returns a new string.

The replace() method replaces only the first match

If you want to replace all matches, use a regular expression with the /g flag set. See examples below.

By default, the replace() method replaces only the first match:

Example

```JS
let text = "Please visit Microsoft and Microsoft!";
let newText = text.replace("Microsoft", "W3Schools");
```

By default, the replace() method is case sensitive. Writing MICROSOFT (with upper-case) will not work:

Example

```JS
let text = "Please visit Microsoft!";
let newText = text.replace("MICROSOFT", "W3Schools");
```

To replace case insensitive, use a regular expression with an /i flag (insensitive):

Example

```JS
let text = "Please visit Microsoft!";
let newText = text.replace(/MICROSOFT/i, "W3Schools");
```

Note

Regular expressions are written without quotes.

To replace all matches, use a regular expression with a /g flag (global match):

Example

```JS
let text = "Please visit Microsoft and Microsoft!";
let newText = text.replace(/Microsoft/g, "W3Schools");
```

### JavaScript String ReplaceAll()

In 2021, JavaScript introduced the string method replaceAll():

Example

```JS
text = text.replaceAll("Cats","Dogs");
text = text.replaceAll("cats","dogs");
```

The replaceAll() method allows you to specify a regular expression instead of a string to be replaced.

If the parameter is a regular expression, the global flag (g) must be set, otherwise a TypeError is thrown.

Example

```JS
text = text.replaceAll(/Cats/g,"Dogs");
text = text.replaceAll(/cats/g,"dogs");
Note
```

replaceAll() is an ES2021 feature.

replaceAll() does not work in Internet Explorer.

### JavaScript String split()

A string can be converted to an array with the split() method:

Example

```JS
text.split(",")    // Split on commas
text.split(" ")    // Split on spaces
text.split("|")    // Split on pipe
```

If the separator is omitted, the returned array will contain the whole string in index [0].

If the separator is "", the returned array will be an array of single characters:

Example

```JS
text.split("")
```
