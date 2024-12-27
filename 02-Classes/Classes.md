# Questions

- 01 What are classes in JS?
- 02 How to create class in JS
- 03 How to use class in JS
- 04 Explain class properties and methods.
- 05 Explain the constructor method.
- 06 Explain 'use strict' in class.
- 07 What is inheritance?
- 08 Explain class inheritance with detail syntax.
- 09 what in super()?
- 10 Explain getters and setters in class.
- 11 Explain Hoisting in class.
- 12 Explain JS static methods in detail. When to use Static methods. 


# Classes

In JavaScript, classes are a blueprint for creating objects with shared properties and methods. They provide a more structured and object-oriented way to define and work with objects compared to the traditional approach using functions and prototypes.

Classes of Functions

## Classes vs Functions (Old Syntax)

Before classes were introduced in ES6, JavaScript used constructor functions and prototypes to create objects. Classes are essentially syntactical sugar over the old prototype-based inheritance.

```JS
function Car(make, model) {
  this.make = make;
  this.model = model;
}

Car.prototype.displayInfo = function() {
  console.log(`Car: ${this.make} ${this.model}`);
};

const myCar = new Car('Honda', 'Civic');
myCar.displayInfo(); // Output: Car: Honda Civic

```

See W3 Javascript:
[Class Intro](https://www.w3schools.com/js/js_class_intro.asp)
[Class Inheritance](https://www.w3schools.com/js/js_class_inheritance.asp)
[Class Static](https://www.w3schools.com/js/js_class_static.asp)
