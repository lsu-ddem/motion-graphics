---
title: String Operators
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# String Operators

* JavaScript's string operators are used to attach strings to one another, or to attach variables to strings.
* String operators each have a symbol known as the operator that is used to perform the operation

---

* Concatenation : concatenate is another word for add. Concatenating two strings simply means adding or attatching them to one another.
  * Operator: `+` 

```js
x = "My name is ";
y = "Hulk Hogan, ";
z = "Brothur";
const sentence = x + y + z;
```

### Q : What is the value of the variable sentence?

#### Note that this operator (+) is also used for numerical addition. 

---

* You may ask how you are supposed to specify that you are adding strings instead of numbers, and the answer is that you do not have to. 
* If any value you are adding is a string, the compiler automatically uses the + operator to concatenate values to the string, even if they are numbers. The result is a string. 
* For example:

```js
var cents = 93;
var sentenceWithNumbers = "I have " + 16 + 
  " dollars and " + cents + " cents.";
console.log(sentenceWithNumbers);
```

---

* Note that between each value or variable added, another addition sign needs to be used to concatenate the entire string. 
* It is good practice to pay attention to where spaces should be inserted so that the sentence's formatting is not confusing and bunched together when the string is printed out.
* Typically if you are printing a string and then a new variable or string, you want to make sure there is a space included at the end of the first string, or the beginning of the second. 

---

* Concatenate-Equals : assigning a variable to its original value plus some specified value concatenated to it
  * Operator: `+=`

```js
x = "My name is ";
y = "Hulk Hogan,";
z = "Brothur";
var sentence = x + y + z;
x += y + z;
```

### Q : What is the value of variable x? Is this equal to the value of sentence?

---
# Exercise 

[back](..)