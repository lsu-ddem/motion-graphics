---
title: Assignment Operators
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Assignment Operators 

---

* JavaScript's assignment operators are used to assign variables to different values. 
* Assignment operators each have a symbol known as the operator that is used to perform the operation.
* Equals: used to assign a variable to a value
  * Operator: `=`
  
```js
let example = 5;
let name = "Alex";
name = example;
```

### Q : What is the value of the variable named "name"?

---

* Plus-Equals: assigning a variable to its original value plus some specified value
  * Operator: `+=` 
  * shorthand for `x = x + number`

```js         
x = 5;
y = 30;
x += 10;
x += y;
y += x;
```

### Q : What is the value of variable y?

---

* Minus-Equals : assigning a variable to its original value minus some specified value
  * Operator: `-=` 
  * shorthand for `x = x - number`

```js
x = 50;
y = 23;
x -= 12;
x -= y;
y -= x;
```

### Q : What is the value of variable y?

---

* Times-Equals : assigning a variable to its original value times some specified value
  * Operator: `*= `
  * shorthand for `x = x * number`

```js
x = 13;
y = 9;
x *= 3;
x *= y;
y *= x;
```

### Q : What is the value of variable y?

---

* Divide-Equals : assigning a variable to its original value divided by some specified value
  * Operator: `/= `
  * `x = x / number`
  * less common

```js
x = 348;
y = 24;
x /= 58;
y /= x;
```

### Q : What is the value of variable y?

---
 
* Modulus-Equals : assigning a variable to its original value modulus some specified value
  * Operator: `%=` 
  * also rarely used 

```js
x = 49;
y = 17;
x %= 12;
y %= x;
```

### Q: What is the value of variable y?

---
# Exercise 

[back](..)