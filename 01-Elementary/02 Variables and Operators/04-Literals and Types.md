# Literals

In JavaScript, **literals** are fixed values that are written directly in the code. They represent data values that are assigned to variables or used in expressions without needing any calculation or computation. Literals can be of various types, and each type has its specific syntax.
Eg: 42, "Hello", true, null, `world ${box}`, etc.

## Types of Literals in JavaScript:

1. **Number Literals**:

   - These represent numeric values and can be integers or floating-point numbers.
   - **Examples**:
     ```javascript
     let a = 42; // Integer literal
     let b = 3.14; // Floating-point literal
     let c = 0xff; // Hexadecimal literal (255 in decimal)
     let d = 1e3; // Exponential notation (1000)
     ```

2. **String Literals**:

   - These represent a sequence of characters enclosed in either single quotes (`'`), double quotes (`"`), or backticks (`` ` ``) for template literals.
   - **Examples**:
     ```javascript
     let str1 = "Hello, World!"; // Single-quoted string literal
     let str2 = "JavaScript"; // Double-quoted string literal
     let str3 = `Template Literal`; // Template literal
     ```
   - **Template Literals** (enclosed in backticks) allow for string interpolation, which is inserting variables or expressions inside a string:
     ```javascript
     let name = "Alice";
     let greeting = `Hello, ${name}!`; // Result: "Hello, Alice!"
     ```

3. **Boolean Literals**:

   - JavaScript has two boolean literals: `true` and `false`, which represent the two possible values of a boolean.
   - **Example**:
     ```javascript
     let isActive = true; // Boolean literal
     let isCompleted = false; // Boolean literal
     ```

4. **Null Literal**:

   - The `null` literal represents the absence of any value or object.
   - **Example**:
     ```javascript
     let data = null; // Null literal
     ```

5. **Object Literals**:

   - An object literal is a comma-separated list of key-value pairs (properties) enclosed in curly braces `{}`.
   - **Example**:
     ```javascript
     let person = { name: "John", age: 30, job: "developer" };
     ```
   - This creates an object with properties `name`, `age`, and `job`.

6. **Array Literals**:

   - An array literal is a list of values enclosed in square brackets `[]`.
   - **Example**:
     ```javascript
     let numbers = [1, 2, 3, 4, 5]; // Array literal
     ```

7. **Regular Expression Literals**:

   - Regular expression literals are used to define a pattern for pattern matching in strings. They are written between forward slashes (`/`).
   - **Example**:
     ```javascript
     let regex = /abc/; // Regular expression literal
     ```

8. **Function Literals** (Function Expressions):
   - A function literal (or anonymous function expression) defines a function without a name and can be assigned to a variable or passed around as an argument.
   - **Example**:
     ```javascript
     let sum = function (a, b) {
       return a + b;
     }; // Function literal
     ```

## Are literals and values same?

In JavaScript, **literals** and **values** are closely related, but they are not exactly the same. Here's how they differ:

### **Values**:

- A **value** is the actual data or information represented by a variable or expression in the program.
- Values are the real data that a program works with, whether they come from literals, variables, expressions, or other sources.
- A value can be a **literal**, but it can also come from calculations or function results.

### **Literals**:

- A **literal** is a specific representation of a value written directly in the code.
- It refers to the syntax or notation used to define a value directly in the code without needing any computation.

### Example:

```javascript
let x = 42; // `42` is a literal, and `x` holds the value 42.
let y = 2 + 3; // `2 + 3` is an expression that evaluates to the value 5, but 5 is a value, not a literal.
```

# Data Types

JavaScript has 8 Datatypes:

- String
- Number
- Bigint
- Boolean
- Undefined
- Null
- Symbol
- Object
- The Object Datatype

The object data type can contain both built-in objects, and user defined objects:

Built-in object types can be:

objects, arrays, dates, maps, sets, intarrays, floatarrays, promises, and more.

In JavaScript, there are two main categories of data types: **primitive types** and **reference types**. They differ in how they are stored, accessed, and manipulated in memory.

### **1. Primitive Types**:

Primitive types are basic data types that hold **single values**. These values are **immutable**, meaning they cannot be altered once they are created. When a primitive value is assigned to a new variable or passed to a function, **a copy** of the value is created.

#### Characteristics of Primitive Types:

- **Immutable**: Once created, the value of a primitive type cannot be changed (though you can assign a new value to the variable).
- **Stored by value**: When you assign a primitive value to another variable, it creates a copy of the value, not a reference to the original value.
- **Simple**: They are the simplest types, representing a single value.

#### Examples of Primitive Types:

1. **String**: Represents sequences of characters.
   ```javascript
   let str = "Hello";
   ```
2. **Number**: Represents numeric values, both integer and floating-point numbers.
   ```javascript
   let num = 42;
   let num2 = 42.35;
   ```
3. **Boolean**: Represents `true` or `false`.
   ```javascript
   let isActive = true;
   ```
4. **Undefined**: Represents a variable that has been declared but not assigned a value.
   ```javascript
   let x;
   console.log(x); // undefined
   ```
5. **Null**: Represents an intentional absence of value or object.
   ```javascript
   let y = null;
   ```
6. **Symbol** (ES6): Represents a unique, immutable value often used as property keys in objects.
   ```javascript
   const id = Symbol("id");
   ```
7. **BigInt** (ES11): Represents large integers beyond the limit of `Number`.
   ```javascript
   const bigNum = 1234567890123456789012345678901234567890n;
   ```

#### Example:

```javascript
let a = 10;
let b = a; // b is a copy of a
a = 20;
console.log(a); // 20
console.log(b); // 10
```

In this example, `a` is changed to 20, but `b` remains 10 because `b` was a copy of the original value of `a`.

---

### **2. Reference Types**:

Reference types are more complex data types that can hold **multiple values**. They are **mutable**, meaning their values can be changed after creation. When you assign a reference type to a new variable or pass it to a function, **a reference to the original object** is passed, not a copy.

#### Characteristics of Reference Types:

- **Mutable**: The values of reference types can be modified.
- **Stored by reference**: When you assign a reference type to another variable, both variables point to the same object in memory. Modifying one will affect the other.
- **More complex**: Reference types can represent collections of data, like arrays, objects, and functions.

#### Examples of Reference Types:

1. **Object**: Represents collections of key-value pairs.
   ```javascript
   let obj = { name: "Alice", age: 30 };
   ```
2. **Array**: A special type of object that represents an ordered list of values.
   ```javascript
   let arr = [1, 2, 3];
   ```
3. **Function**: Functions are also considered reference types.
   ```javascript
   function greet() {
     console.log("Hello!");
   }
   ```

#### Example:

```javascript
let obj1 = { name: "Alice" };
let obj2 = obj1; // obj2 references the same object as obj1
obj1.name = "Bob";
console.log(obj1.name); // 'Bob'
console.log(obj2.name); // 'Bob' (both refer to the same object)
```

In this example, both `obj1` and `obj2` point to the same object in memory. Changing `obj1` also affects `obj2`, because they reference the same object.

---

### **Key Differences Between Primitive Types and Reference Types**:

| Feature                  | **Primitive Types**                                           | **Reference Types**                                                            |
| ------------------------ | ------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Memory Storage**       | Stored by value (copy of the value).                          | Stored by reference (pointers to the same object).                             |
| **Mutability**           | Immutable (cannot be changed directly).                       | Mutable (values can be changed).                                               |
| **Assignment**           | When assigned to a new variable, a copy of the value is made. | When assigned to a new variable, both variables refer to the same object.      |
| **Example Types**        | String, Number, Boolean, Null, Undefined, Symbol, BigInt      | Object, Array, Function                                                        |
| **Passing to Functions** | Passing a primitive value passes a copy of the value.         | Passing a reference type passes the reference, so changes affect the original. |
| **Equality Comparison**  | Two primitive values are equal if they have the same value.   | Two reference values are equal if they refer to the same object.               |

---

### Example: Difference in Behavior

#### Primitive Types:

```javascript
let a = 10;
let b = a; // Copy of a is assigned to b
a = 20;

console.log(a); // 20
console.log(b); // 10 (b still holds the original value)
```

#### Reference Types:

```javascript
let obj1 = { name: "Alice" };
let obj2 = obj1; // obj2 is a reference to obj1
obj1.name = "Bob";

console.log(obj1.name); // 'Bob'
console.log(obj2.name); // 'Bob' (obj2 is pointing to the same object as obj1)
```
