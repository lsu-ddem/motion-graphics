---
title: Conditional Operators
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Conditional Operators

---

* JavaScript's conditional operator can be used as a shorthand for conditional statements(these are covered in a later lesson). 
* The conditional operator assigns a value to a variable according to the result of a specified condition. 
* The conditional operator has a specified syntax(way of writing/coding) instead of an assigned operator key.

---

## Conditional 

* used to test the relationship between a variable's value and another variable's value, using the comparison operators
  * Syntax: `variablename = (condition) ? value1:value2`
         
```js
let time = 1800; //this is 8pm in military time
let currentSky = (time >= 1650) ? "dark":"light";
time = 700;//this is 7am military time
currentSky = (time <= 1650) ? "light":"dark";
```

###  Q : What is the result of the comparison the last line (light or dark)?

---

# Logical Operators 

---

* JavaScript's logical operators are used to determine whether an entire statement/condition is true or false depending on the operation and values involved. 
* These can be used to assign boolean values to variables or to determine the next course of action in conditional statements.
* The logical operators have symbols known as the operators that are used to perform the operations

--- 

## And 
* if the values on both sides of the operand are true, then the operation returns true. If one is false, the operation returns false. If both are false, the operantion returns false. 
  * Operator: `&&`

```js
x = 20;
y = 30;
j = 19;
z = (x > 10) && (y < 50); // returns true
```

---

## Or 
* if one or more values are true, the entire statement returns true. Only if both sides of the operand are false does the entire statement return true
  *  Operator: `||` 

```js
x = 20;
y = 30;
z = (x > 10) || (y < 15); // returns true because the left side is true, even though the right side is false
```

---

## Not

* the not operator returns the opposite of the value it is operating on.
  * Operator: ! 

```
x = false;
y = true;
z = !x; //returns true
z = !y; //returns false
```    

---
# Exercises

[back](..)