---
title: Bitwise Operators
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Bitwise Operators 

---

* JavaScript's bitwise operators are used to perform bitwise operations on values to determine relationships similar to logical operations, such as AND, OR, NOT, etc.
* The difference between bitwise operators and logical operators, then, is that bitwise operators are used on numeric values only. 
* When a bitwise operator is used, numeric values using the operator are converted to their 32 bit values.

---

* A bit is the smallest possible unit of (computer) data. A bit can only be one of two binary values: 0 or 1.
* 8 bits make up one single byte.
* Knowledge of binary is not required to program with JavaScript, so we will not go into detail on the conversion of a numeric value to its binary value. This conversion is done 'behind the scenes' by the computer anyways.
* You will probably not use bitwise operators too frequently

---

### Bitwise operations result in True or False, like logical operators. 

### If you'd like to read more about bitwise operators, visit the documentation: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_Operators 
     
---

# Other Types of Operators 

* JavaScript has a few additional operators that can be convenient, and are worth mentioning. You likely would not use these as frequently as the other operators already discussed.

---

* Type Of : The type of operator returns the data type of a specified variable, object, function, etc.
  * Operator: typeof
  * useful for making sure you are receiving the correct type of data, reducing bugs 

```js
let car = "Honda";
typeof car; //this line returns "string" because the value of car is a string
let x, y;
let equation = x + 5 / (6 * y) + 17;
typeof equation; //this line returns "number" because the value of car is a string
typeof car === typeof equation // false
```

---

Delete : The delete operator deletes a property from an object
  * Operator: delete
  * i have never seen this used

```js
let pet = {name:"Macy", species:"Dog", age:5, attribute:"fluffy"};
delete pet.age;   // removes the age property from the pet object
```

---

* In : The in operator checks to see if a specified property is in a specified object(objects are covered in the next lesson). If the object does contain the property, the operation returns true. Otherwise, it returns false.
  * Operator: in

```js
pet = {name:"Macy", species:"Dog", age:5, attribute:"fluffy"};
"name" in pet;   // returns true because the pet object has a property called "name"
```

---
# Exercises

[back](..)