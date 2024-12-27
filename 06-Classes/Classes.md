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
