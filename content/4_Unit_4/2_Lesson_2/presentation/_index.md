---
title: Functions
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Function Syntax 

---

* Remember that syntax tells us how to set up(declare) and use something. The syntax for JavaScript functions is:

```js
function functionName(parameter1, parameter2){
  // function's code
}
```

* The syntax of a function has four major parts:
  * 1. The "function" keyword
  * 2. The function's name
  * 3. The function's parameters
  * 4. The code the function executes
  
---

## The "function" keyword
  * As in any declaration in JavaScript, the declaration of a function must begin with the function keyword. Just as the declaration of new variables starts with "var".
  
--- 

## The function name
  * Following the "function" keyword is the function's name. The naming conventions for functions are the same as those for variables, which we discussed in the variables section. 

---

## The function's parameters
  * Parameters are a more complex concept than the simple function keyword and function name, but they are not a difficult concept to grasp. 
  * Parameters are values that the function needs in order to perform its job.

---

* Consider a function calculating the circumference of a circle. 
* The function waits for us to give it a radius, and then calculates the circumference using the radius. 
* The function wouldn't be able to give us the value of the circumference if we did not first provide it with a value for the circle's radius. 
* Thus, the radius is a parameter for this function.

---

* The value we provide the function with that takes the place of a parameter is called an argument. 
* Providing the function with the value that takes the place of a parameter is called passing in an argument to the function.
* Parameters are found in the code the function executes, in addition to the parenthesis after the function's name.

---

* This is because the parameters act as a place holder for the different values that the function plugs in for us using the arguments we pass in. This allows functions to be reusable.
* Functions can also have no parameters, multiple parameters, and the parameters can be of different data types. 
* Functions without parameters are typically used to return an attribute of a variable, or perform tasks without changing variables, like printing the current time.

---

## The code the function executes

* Finally, the last portion of the function is the code that the function actually executes. 
* This is where the task you want the function to perform is generalized or abstracted so that the code is reusable. 
* To generalize the task the function is performing, we simply replace the changing variable(s) in the code with parameters, so that we can later pass in arguments to these parameters, and retrieve the desired result. 

---

### Example: 

* Say we have 20 circles, with the following radii: 3,7,12,5,9,42,8,60,45,21,6,9,14,27,84,32,52,37,36,15
* We want to find the circumference of all 20 circles.
* First, lets begin calculating this without the use of functions.
* The first step would be to declare our radiuses as variables. This means declaring 20 different variables, or creating an array with 20 elements.
 
```js
let radius1 = 3;
let radius2 = 7;
let radius3 = 12;
// etc, etc, etc. ....
let radius20 = 15;
```
---

* OR:
  
```js
let radii = [3, 7, 12, 5, 9, 42, 8, 60, 45, 21, 6, 9, 14, 27, 84, 32, 52, 37, 36, 15];
```

* Next we would save the circumference of each circle to a variable, or print each circumference to the console. 

```js
let circumference1 = 2 * Math.PI * radius1; // or, with use of an array, var circumference1 = 2*Math.PI*radiuses[0];
let circumference2 = 2 * Math.PI * radius2; // or, with use of an array, var circumference2 = 2*Math.PI*radiuses[1];
let circumference3 = 2 * Math.PI * radius3; // or, with use of an array, var circumference3 = 2*Math.PI*radiuses[2];
let circumference20 = 2 * Math.PI * radius20; // or, with use of an array, var circumference20 = 2*Math.PI*radiuses[19];
```

* Finally, we would print these values to the console:

```js
console.log(circumference1);
console.log(circumference2);
console.log(circumference3);
console.log(circumference20);
```

---

* This code was shortened to only four values out of the 20, and still requires more effort than the use of a function.
* Now, lets complete this task with the use of a function.
* First we will declare the function. We will name it "circumferenceCalculator" and it will take one parameter, the radius of a circle:

```js
function circumferenceCalculator(radius){
  // ...
}
```

---

* Next, we simply add the code the function will execute within the curly brackets. 
* Remember that we are generalizing the code by using parameters in place of changing variables:

```js
function circumferenceCalculator(radius) {
  console.log("My function found that the circumference of a circle with a radius of " 
    + radius + " is " + 2 * Math.PI * radius);
}
```

---

* We know from our knowledge of concatenating strings that the function will return this value: 
  * "My function found that the circumference of a circle with a radius of _____ is ____________" 
  * where the first blank is the radius we provided the function with, and the second blank is the value of the circumference that the function is calculating for us.
* Finally, to run our function, we invoke it by calling the function name and giving the function an argument for the radius. Invoking functions will be covered in depth in the next section.

---

* To calculate all of the circumferences, we can pass in the radius argument by either inputting the radius's actual value, or the variable or element storing the radius.
  
```js
// passing in the radius value directly for the first circle
circumferenceCalculator(3); 
// passing in the variable storing the radius value for the 
// second circle
circumferenceCalculator(radius2); 
// passing in the element in the radiuses array that stores the 
// radius value for the third circle (remember that it is 
// radiuses[2] because the index of an array begins at
// 0 rather than 1.)
circumferenceCalculator(radiuses[2]); 
```

---

* Now, if you check your console, you will see this printed out:
  * "My function found that the circumference of a circle with a radius of 3 is 18.84955592153876"
  * "My function found that the circumference of a circle with a radius of 7 is 43.982297150257104"
  * "My function found that the circumference of a circle with a radius of 12 is 75.39822368615503"

---

# Exercises

[back](..)