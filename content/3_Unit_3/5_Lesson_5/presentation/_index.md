---
title: Number Methods
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Number Methods

---

* toString : this method converts a numeric value to a string
  * syntax: `.toString()`

```js
let randomNumber = 3124325454352;
console.log(randomNumber);
console.log(randomNumber.toString());
console.log((21414 + 234234).toString());
```

---

* if you look at the console, you'll see that before we converted it to a string, randomNumber was printed as a numeric value, without quotation marks.
* Remember that when numbers are concatenated to strings, they become strings themselves. So, there is no reason to use the .toString method during string to number concatenation.
* This method comes in handy when using functions or methods that require a string parameter and thus the number needs to be converted to a string.

---

* to Exponential : this method converts a numeric value to a string that contains the exponential notation of the value
  * syntax: `.toExponential(n)`

```js
let x = 3.2526;
console.log(x);
console.log(x.toExponential(2));
console.log(x.toExponential(4));
```

---

* to Fixed : this method converts a numeric value to the same numeric value with the specified number of decimal places included. This is useful when dealing with values such as money or scores.
  * syntax: `.toFixed(n)`

```js
let payCheck = 3000;
let groceries = 240.247;
let utilityBill = 139.26;
let cellPhone = 45.206;
let savings = 1000;
let spendingMoney = payCheck - groceries - utilityBill - cellPhone - savings;
console.log("This is how much money I have left: $" + spendingMoney);
console.log("But it makes more sense to round money to two decimal places, like this : $" + spendingMoney.toFixed(2));
```

---

* to Precision : this method converts a numeric value to a string with a specified length. It is essentially the same as the `.toFixed()` method, but the return type is a string. And instead of specifying the number of decimal places, we are specifying the number of characters in total, or the length of the string:
  * syntax: `.toPrecision(n)`

```js
let grade = 87.2267;
console.log("My grade is " + grade.toPrecision(4));
console.log("My grade is " + grade.toPrecision(3));
console.log("My grade is " + grade.toPrecision(2));
```

---
# Exercises


[back](..)