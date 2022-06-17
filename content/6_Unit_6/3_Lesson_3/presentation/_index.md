---
title: Nested Loops
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Nested Loops 

---

* You may recall the idea of nesting from the lesson on conditional statements. 
* Nesting simply means placing something within another instance of the same type.
* With nested conditional statements, we wrote an if statement that had an if or if-else statement within it.

---

* The same idea applies to all loops.
* We can nest for loops inside of for loops, while loops inside of while loops, do while loops inside of do while loops, etc.
* We can also nest any loop type within a loop of a different type. For example, placing a while loop inside of a forloop, or a for loop inside of a do-while loop.

---

* We are also able to place conditional statements within loops, and vice versa
* The purpose of nesting is to execute code depending on further conditions.

---

* For example, imagine you just woke up and are getting dressed for the day. 
    * What do you take into consideration when you're getting dressed? 
    * You probably take a look at the weather to know how best to dress
    * If its cold, you bundle up. If its warm, you put on shorts and a shirt.
    
---
  
  * But what other factors alter our outfit of the day? What about if the weather app tells us its raining today? 
  * Does this change your outfit of choice? You might choose to wear rain boots or a rain jacket instead or in addition to your original choices.

--- 

  * First, our outfit was dependent on the temperature outside. Then we considered the weather. Our outfit was then dependent on further conditions. 
  * Therefore, if we were to see this scenario programmed via conditional statements or perhaps using loops, there would be nesting at some point to include a test for the weather, since this factor can alter the outfit we choose.

---

* Lets model this scenario using nested conditional statements, which we have had practice with before:

```js
let temperature = 75;
let weather = "rainy";
if (temperature < 45) {
  if (weather == "sunny") {
    let clothes = "warm clothes with a hat or some sunglasses";
  } else if (weather == "rainy") {
    let clothes = "warm, dry clothes with a rain jacket or rain boots";
  } else {
    let clothes = "bundle up in warm clothes";
  }
} else if (temperature < 65) {
  if (weather == "sunny") {
    let clothes = "layered clothes with a hat or some sunglasses";
  } else if (weather == "rainy") {
    let clothes = "layered clothes clothes with a rain jacket or rain boots";
  } else {
    let clothes = "wear layered clothes to adapt to the chilly and warm parts of the day";
  }
} else {
  if (weather == "sunny") {
    let clothes = "light & breathable clothes with a hat or some sunglasses";
  } else if (weather == "rainy") {
    let clothes = "light & breathable clothes with a rain jacket or rain boots";
  } else {
    let clothes = "wear light & breathable clothes because it is hawt outside";
  }
}
```

---

* We've had plenty of practice with nested conditional statements, so lets start looking at nested loops:
* Nested for loops can be used to accomplish a variety of goals. One of the most common uses for nested for loops is accessing elements within 2D arrays 

---

* Consider the following 2D array "breakfasts", created by declaring arrays within an array:

```js
var breakfasts = [
  // each of these arrays are elements of the breakfasts array, 
  // though they are arrays with elements themselves.
  ["biscuits", "sausage"],
  ["pancakes", "syrup"],
  ["kolache", "jelly"]
];
```

* Using a single for loop, we can access the second element in each array. The second elements include sausage, syrup, and jelly.

---

* We can accomplish this pretty easily by specifying that the element we want to access is the second element in each array, like so: 

```js
for (let i = 0; i < breakfasts.length; i++) {
  // the element is accessed by accessing the i-th element of the 
  // breakfasts array, which we know is an array itself, so we 
  // specify which element of this array we want to access:
  // remember that the second element of an array has an index of 1 
  console.log(breakfasts[i][1]);
}
```

* Checking the console, you'll see that the second elements were printed out

---

* What about scenarios in which there are multiple elements in a 2D array and we want to traverse through all of them, instead of accessing a single element? 

* In this instance, we implement nested for loops:

```js
var newBreakfasts = [
  ["biscuits", "sausage", "OJ", "cheese grits", "grapes"],
  ["pancakes", "syrup", "strawberries", "apple juice", "ham"],
  ["kolache", "jelly", "bacon", "mango", "chocolate milk"]
];
```

---

* Using the same methodology as the forloop on line 38 would only result in the second element within each array being printed.

* We want to print each item related to each breakfast, however, so we will implement a nested for loop like so:

```js
for (let i = 0; i < newBreakfasts.length; i++) {
  // this line is simply printing "Breakfast Option N: " to the 
  // console to keep the print statements organized
  console.log("Breakfast Option " + (i + 1) + " : ")
  // pay special attention to the second for loop's statement 2. 
  // It says it will loop as long as j is less than the length 
  // of the array ***located at element i***
  for (let j = 0; j < newBreakfasts[i].length; j++) {
    console.log(newBreakfasts[i][j]);
  }
}
```

---

* For loops are the best loop to iterate through arrays of one or more dimensions, but the same concept of nested loops applies to other types of loops as well
* Below is an example of nested while loops:
* The loops are printing 99 through 00 to the console, one by one 

---

* The first while loop executes WHILE the statement "tens is greater than or equal to 0" is TRUE. 
* Looking at the declaration of the tens variable on line 136, we see that tens is initialized to 9. This means that the outer loop will loop 10 times total
* The second while loop executes WHILE the statement "ones is greater than or equal to 0" is TRUE. 

---

* On line 74, we initialized ones to equal 9. We place this withIN the first while loop because of the fact that the second while loop is decrementing the ones variable.
* If we failed to place "ones = 9" within the first while loop, the ones variable would not be reset to 9 after having printed the ten values, and the rest of the values would not be printed. 

---

* Nested while loop example:

```js
let tens = 9;
let ones;
while (tens >= 0) {
  ones = 9;
  while (ones >= 0) {
    console.log(tens + "" + ones);
    // here we ensure to decrement the ones variable so that we 
    // are not caught in an infinite loop
    ones--;
  }
  // here we ensure to decrement the tens variable so that we 
  // are not caught in an infinite loop
  tens--;
}
```

---

* Below are a few examples of different nested loops:
* Do while: 

```js
do {
  let count = 10;
  console.log("doin the first thing");
  do {
    count--;
    console.log("doin the second thing within the first thing");
  } while ((count + 1) > 2);
} while (count > 0);
```

---

# Exercises

[back](..)