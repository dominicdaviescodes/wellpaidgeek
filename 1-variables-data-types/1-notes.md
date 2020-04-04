## What is a variable? 

we must first declare a variable and assign a value to it.

```javascript
  var firstname = 'Dominic';
  var lastName = ('Davies');
  console.log(firstname);
  console.log(lastName);

```

Exercise #1

create a variable and reasign a value to it.

```javascript
  var name = 'Dominic';
  name = ('Bob');
  console.log(name);

```

## The different data types in JavaScript

We categorize the values which can be held in variables. We need different data types to model different things.

* string
  * var username = ' ';
  * var email = 'test@example.com'
  * now standard to use single quotes for strings in js
* number
  * holds numerical values. JS has 1 number type (floating point) can have decimals like 1.35
  * var a = -1;
  * var average = 1.98;
* boolean
  * must be either true or false. another way to say yes/no is true/false
  * var javaScriptIsAwesome = true;
  * var pythonIsAwesome = false;
* objects
  * good for grouping together variables and functionality in a way that makes sense
  * holds various variables of different types, only need one variable (person) to hold them all
  * all variables below could be written separately but they belong to the same person
  * can have nested objects like address, below.
```javascript
  var person = {
    firstName: 'Tom',
    lastname: 'Jones',
    age: 87,
    address: {
      line1: '1 high street',
      city: 'Cardiff',
      countryId: 51,
    },
  };
```
* undefined
  * a variable that has'nt been declared or assigned a value YET.
  * var country;  // has been declared with no value
```javascript
var person = {
  firstName: 'Tom',
  lastname: 'Jones',
  age: 87,
  address: {
    line1: '1 high street',
    city: 'Cardiff',
    countryId: 51,
  },
};

console.log(person.age);  // returns 87
console.log(person.country); // returns undefined
```
* Null
  * represents an empty value
  * confusing. 
  * has been declared with with a value but the value is currently empty
  * good for if you have optional entries like age, users can enter their age: 37, or decide not to which will leave age:null
```javascript
var nothing = null;
var animal = 'hippo';
animal = null;
```
* typeof before a variable lets you know the data type.

** Basic Maths

We type expressions in the console then the console evaluates the expression.

```javascript
10 * 10 // when combined like this numbers and operators become an expression

100 // when evaluated that expression produces a number value, here it's 100
```

```javascript
var a = 5;
var b = 7;

var result = (a + b);
console.log(result);

// returns 12
```
JS has a maths library built in
Math is a built-in object that has properties and methods for mathematical constants and functions.


```javascript
var min = Math.min(3,8,2);
var max = Math.max(3,8,2,9);
console.log('Min', min);
console.log('Max', max);

// Min 2.  min gives us smallest from list of numbers
// Max 9.  max gives us largest from list of numbers
```

we can use expressions anywhere we can use values

```javascript
console.log('Min', Math.min(3, 8, 2));
console.log('Max', Math.max(3, 8, 2, 9));

// Min 2
// Max 9

```
### Return nearest whole number
ceil (round up) and floor (round down) 

```javascript
console.log('Ceil 2.2', Math.ceil(2.2));
console.log('Ceil 3.9', Math.ceil(3.9));

// Ceil 2.2 3
// Ceil 3.9 4
```

```javascript
console.log('Floor 0.9', Math.floor(0.9));
console.log('Floor 9.9', Math.floor(9.9));

// Floor 0.9 0
// Floor 9.9 9
```

### Exercise
* find smallest number and round down
* find largest number and round up
  * 0.9
  * 4.8
  * 1.5
```javascript
console.log('Min', Math.floor(Math.min(0.9, 4.8, 1.5)));  // 0
console.log('Max', Math.ceil(Math.max(0.9, 4.8, 1.5)));  // 5
```
Instructors answer
```javascript
var min = Math.min(0.9, 4.8, 1.5);
console.log(Math.floor(min));

var max = Math.max(0.9, 4.8, 1.5);
console.log(Math.ceil(max));
```

## Math.random() 
The Math.random() function returns a floating-point, pseudo-random number in the range 0 to less than 1 (inclusive of 0, but not 1) (0 to 0.9999999 etc...) with approximately uniform distribution over that range — which you can then scale to your desired range. The implementation selects the initial seed to the random number generation algorithm; it cannot be chosen or reset by the user.

#### Get a random number between 0 - 10 (0 to 9.9999999999) not inclusive of 10
we multiply Math.random() * 10
we will want a whole number rounded down (you don't want 10)

```javascript

var randomNumber = Math.random() * 10;
console.log(Math.floor(randomNumber));

// or 

console.log(Math.floor(Math.random() * 10));

```



