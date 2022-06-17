---
title: Conditional Statements
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Conditional Statements 

---

* Conditional Statements use operators to test different expressions, and execute code according to the outcome of the expressions.
  * If statements, 
  * Else statements, 
  * Else if statements, and 
  * switch statements.
* Conditional statements can be nested within each other, so that another expression can be tested after one has been proven true or false, to determine the next course of action for the program.

---

## If statements 

* If statements are pretty self explanatory. The statement tests "if" a condition within the parenthesis is true. 
* If the condition is true, the code is executed. Like so:

```js
if (5 < 6){
  console.log("Our first if statement!");
}
```

---

* The expression within the parenthesis is the condition being tested. 
* All of the conventions for using conditional and logical operators remain true when we use them in if statements.

```js
let name = "Bob";
if (name === "Bob"){
  console.log("Hiiiii Bob!");
}
```

```js
x = 20;
y = 30;
if ((x > 10) && (y < 50)) {
  console.log("True!");
}
```

---

## Else statements 

* Else statements follow if statements and/or else-if statements(covered next). 
* Else statements are literally saying "if that condition was not true, execute this code" 

```js
let name = "Todd";
if (name === "Lisa Frank") {
  console.log("Hiiiii, Lisa Frank!");
} else {
  console.log("Hiiii, " + name);
}
```

---

## More examples:
```js
let money = 241352315;
if (money > 10000000000) {
  console.log("Wow you're rich.");
} else {
  console.log("You're still pretty rich but not *that* rich.");
}
```

---
```js
let nightTime = false;
let morningTime = true;

if (morningTime || nightTime) {
  console.log("We used the or operator and it was truuuuu");
} else {
  console.log("We used the or operator and it was faaaalse");
}

if (morningTime && nightTime) {
  console.log("We used the and operator and it was truuuuu");
} else {
  console.log("We used the and operator and it was faaaalse");
}

if (morningTime) {
  console.log("Goooood morning");
} else {
  console.log("It isn't morning");
}

if (nightTime) {
  console.log("Goooood night");
} else {
  console.log("It isn't night");
}
```

---

## Else-if statements 

* Else-if statements are used in between if statements and else statements to test for an extra condition before running the "else code".
* In other words, if the if statement proves false, the next expression evaluated will be the else if, which will test for a new condition. 
* If the else if is also false, the next else if expression is evaluated, or the else code is executed.

---

* We can have multiple else if statements before the final else statement

```js
let name1 = "Todd";
let name2 = "Katy";
let name3 = "Max";
if (name1 == "Katy") {
  console.log("Hiiiii, Katy!");
} else if (name1 == "Max") {
  console.log("Hiiiii, Max!");
} else {
  console.log("Hiiii, " + name1);
}
```

* What will be printed?
  
---

```js
if (morningTime) {
  console.log("Goooood morning");
} else if (nightTime) {
  console.log("Goooood night");
} else {
  console.log("What time is it?!?!");
}
```

* Running the code at this point, "Gooood morning" would be printed to the console. If we update the values of the variables and run the expressions again, we will see a new value printed to the console:

---

```js
morningTime = false;
nightTime = true;
if (morningTime) {
    console.log("Goooood morning");
} else if (nightTime) {
    console.log("Goooood night");
} else {
    console.log("What time is it?!?!");
}
```

* Now, "Gooood night" will be printed to the console. Finally, we will change the values of the variable so that we arrive at the else statement:

---

```js
nightTime = false;
if (morningTime) {
  console.log("Goooood morning");
} else if (nightTime) {
  console.log("Goooood night");
} else {
  console.log("What time is it?!?!");
}
```

---

* As mentioned, conditional statements can be nested within each other. For example:

```js
let color = "purple";
if (color == "red") {
  console.log(color);
} else if (color == "purple") {
  if (5 > 6) {
    console.log("First nested if-statement was true");
  } else {
    console.log("First nested if-statement was false");
  }
}
```

---
# Exercises

* to get the length of a string: 
  
```js
let string = 'helloooo'
console.log(string.length) // 8 
```

[back](..)