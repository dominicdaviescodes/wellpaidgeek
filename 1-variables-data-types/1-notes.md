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