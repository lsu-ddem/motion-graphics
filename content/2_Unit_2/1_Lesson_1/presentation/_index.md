---
title: JS Operators
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Javascript Operators

---

* Operators are used in programming to assign new values, compare values, test values, update values, perform arithmetic on values, etc.
* operators are used to manipulate variables in a number of ways. 
* So far, we've only really dealt with the default assignment operator, `=`, like when we say:

```js    
var usingAssignmentOperator = "<-- Thats the common assignment operator";
```
---
* In total, there are seven categories of operators in JavaScript. 
* These include operators for 
  * arithmetic operations, 
  * assignments, 
  * string operations, 
  * comparisons, 
  * logical operations, 
  * conditional operations, and other types of operators that are worth mentioning.
   
---

# Arithmetic Operators 

---

* JavaScript's arithmetic operators are used to perform arithmetic in your code. 
* Arithmetic operators each have a symbol known as the operator that is used to perform the operation.
* Addition : adding two values or variables together
  * Operator: **+** 
  
  ```js       
  let sum = 5 + 7000;
  let x, y;
  x = 20;
  y = 30;
  let z = x + y + 400; 
  ```

* Q : What is the value of variable z?

---

* Subtracting : subtracting one value or variable from another
  * Operator: - 
  
  ```js
  let minus = 300 - 87;
  let a, b;
  a = 83;
  b = 65;
  let c =  a - b; 
  ```
* Q : What is the value of variable c?

---

* Multiplication : multiplying multiple values or variables together
  * Operator: *

```js
  let product = 75 * 39;
  let j, k;
  j = 14;
  k = 92;
  let l = j * k * .5; 
```
* Q : What is the value of variable l?

---

* Division : dividing one or more values or variables by another
  * Operator: /

```js
let quotient = 5016 / 6;
let q, w;
q = 46;
w = 138;
let p = (w / q) / 3; 
```
* When there are multiple operations on a single line, the answer is calculated in the order of PEMDAS 
* Q : What is the value of variable p?

---

* Modulus : retrieving the remainder of one or more values or variables being divided by another
  * Operator: %

```js
let modulus = 33%15; 
// the value of modulus would be 3, 
// because 32 goes into 15 twice, with left over.
let h = 46;
let i = 13;
let g = h % i;  
```
* Q : What is the value of variable g?

---

* Increment : increasing the value of a variable by 1 (adding 1)
  * Operator: ++

```js
let someValue = 10;
someValue++;
let newValue = someValue++;
```
* Q : What is the value of the variable named newValue?

---

* Decrement : decreasing the value of a variable by 1 (subtracting 1)
  * Operator: --

```js
// Examples:
let someOtherValue = 90;
someOtherValue--;
let anotherNewValue = someOtherValue--;
```

* Q : What is the value of the variable named anotherNewValue?

---

* The operators can be used on fixed values, such as:
  
```js
let adding = 5 + 5;
let subtracting = 10 - 5;
let dividing = 40 / 5;
let multiplying = 80 * 3;
let modulus = 20 % 8;
```

* Arithmetic operators can also be used on variables:
  
```js
let number = 50;
let newAdding =  adding + number;
let newSubtracting = subtracting - number;
let newDividing = number / dividing;
let newMultiplying = multiplying * number;
let newModulus = number % modulus;
```

---

* The operators can even be used with a mix of fixed values and variables:

```js
newAdding =  adding + 30;
newSubtracting = subtracting - 23;
newDividing = 5 / dividing;
newMultiplying = multiplying * 7;
newModulus = 24 % modulus;
```

---

# Exercise 

[back](..)