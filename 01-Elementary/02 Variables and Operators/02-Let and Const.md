## Using let

The value of a Variable declared with let can be updated

The let keyword was introduced in ES6 (2015)

Variables declared with let have Block Scope

Variables declared with let must be Declared before use

Variables declared with let cannot be Redeclared in the same scope

```JS
let x = 5;
let y = 6;
let z = x + y;
```

Only use let if you can't use const

## Using const

The const keyword was introduced in ES6 (2015)

Variables defined with const have Block Scope

Variables defined with const cannot be Redeclared in the same scope

Variables defined with const cannot be Reassigned

must be assigned a value when they are declared

```JS
const PI = 3.141592653589793;
PI = 3.14;      // This will give an error
PI = PI + 10;   // This will also give an error
```

### Must be Assigned

JavaScript const variables must be assigned a value when they are declared:

```JS
//Correct
const PI = 3.141592653589793;

//Incorrect
const PI;
PI = 3.14159265359;
```

### When to use JavaScript const?

Always declare a variable with const when you know that the value should not be changed.

Use const when you declare:

- A new Array
- A new Object
- A new Function
- A new RegExp

### Constant Objects and Arrays

The keyword const is a little misleading.

It does not define a constant value. It defines a constant reference to a value.

Because of this you can NOT:

- Reassign a constant value
- Reassign a constant array
- Reassign a constant object

  But you CAN:

- Change the elements of constant array
- Change the properties of constant object

### Constant Arrays

You can change the elements of a constant array:

```JS
// You can create a constant array:
const cars = ["Saab", "Volvo", "BMW"];

// You can change an element:
cars[0] = "Toyota";

// You can add an element:
cars.push("Audi");
```

But you can NOT reassign the array:

```JS
 const cars = ["Saab", "Volvo", "BMW"];

cars = ["Toyota", "Volvo", "Audi"];    // ERROR
```

### Constant Objects

You can change the properties of a constant object:

```JS
// You can create a const object:
const car = {type:"Fiat", model:"500", color:"white"};

// You can change a property:
car.color = "red";

// You can add a property:
car.owner = "Johnson";
```

But you can NOT reassign the object:

```JS
 const car = {type:"Fiat", model:"500", color:"white"};

car = {type:"Volvo", model:"EX60", color:"red"};    // ERROR
```
