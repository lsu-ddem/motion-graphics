---
title: Math Methods
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Math Methods

---

* The JavaScript Math object has a lot of useful methods that are worth mentioning.
* To use the Math methods, we don't have to construct a new Math object.
* All we do is include the Math object name, and then invoke the method, such as:

```js
let roundUp = Math.round(9.8); 
// here we invoked the round method. This would round 9.8 to 10.
```

---

* There are a few constants loaded into the JS Math object's properties.
* A few of these include:
  * 1. PI : `Math.PI`
  * 2. Euler's constant : `Math.E`
  * 3. Natural log base 10: `Math.LN10`
* More : https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math

---

* The Math object also has many methods, but we will only cover the ones you will likely use most
* If you'd like to see a full list of the Math object's methods, go to https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math

---

* 1. Exponents:
  * Syntax: `Math.pow(x,y)` where x is the base and y is the exponent 

```js 
let value = Math.pow(5, 2);
let newValue = Math.pow(value, 2);
```

---

* 2. Random:
  * Syntax: `Math.random()` 
  * When `Math.random()` is used without any arguments, it returns a random value between 0 and 1:

```js 
console.log("Here is a random number " + Math.random());
```

* However, we can specify the values we want the random number to be within range of using the next method:

---

* 3. Floor:
  * Syntax: `Math.floor()` 
  * `Math.floor()` is used to return the largest whole number that is less than or equal to a specified value. We use this method to get a random whole number within a specific range of numbers, such as 1-10:

```js 
let randomNum = Math.floor((Math.random() * 10) + 1);
console.log(randomNum);
```

---

* the syntax of using .floor with .random is: 
* `Math.floor((Math.random * maxRangeValue) + minRangeValue)`

```js
console.log("A new random number between 1 and 10 is " + 
  Math.floor((Math.random() * 10) + 1));
console.log("Another random number between 1 and 10 is " + 
  Math.floor((Math.random() * 10) + 1));
```

---

* 4. Round:
  * Syntax: `Math.round(x)` rounds the value x to the nearest whole number

```js
let roundMeUp = Math.round(5.7);
let roundMeDown = Math.round(7.3);
```

---

* 5. Exponential Function:
  * Syntax: `Math.exp(x)` raises E to the x power

```js
let raised = Math.exp(5);
```

---

* 6. Absolute Value:
  * Syntax: `Math.abs(x)` returns the absolute value of the variable or value in parenthesis

```js
let positive = Math.abs(-24343525);
let negative = -24124214;
let absoluteVal = Math.abs(negative / 2);
```

---

* 7. Square Root:
  * Syntax: `Math.sqrt(x) `returns the square root of the value or variable in parenthesis

```js
let sqrt = Math.sqrt(25);
sqrt = Math.pow(sqrt, 2);
console.log(Math.sqrt(sqrt));
```

---

* 8. Trigonometric Functions:
  * Syntax: 
    * Sin : `Math.sin(x)`
    * Tan : `Math.tan(x)`
    * Cos : `Math.cos(x)`
    * Arcsin : `Math.asin(x)`
    * Arctan : `Math.atan(x)`
    * Arccos : `Math.acos(x)`

---

* Though there are a number of methods for the Math object that we didn't cover, you likely won't need to use them as a beginner programmer. Still, you can read about them here: 
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math
* and:
* https://www.w3schools.com/js/js_math.asp

---
# Exercises


[back](..)