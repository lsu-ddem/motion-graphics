---
title: Javascript intro
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# JavaScript 

* a popular and powerful scripting language used to write programs and make web pages dynamic.
* JavaScript is able to make web pages dynamic by allowing us to program interactions with users and elements of web pages.
* Eventually we will get to interacting and manipulating web pages from our JavaScript code, but first we'll start with the basics.

--- 

# Code comments 


* Different programming languages have different syntaxes for comments.
* JavaScript (or JS)'s syntax is two forward slashes per typed line: //
  
```
// What you're reading now is called a comment. "//"
```

```
/*
  This is an example of a multi-line comment
  it does not depend upon the beginning of the current line
  containing "//"
*/
```

---

Now try in a blank <a href="http://codepen.io/pen" target="_blank">Codepen</a>

--- 

# Syntax 

* those comments looked different, this is known as syntax
* syntax simply means the rules or guidelines for doing something in a language, in our case a programming language.

--- 

# Declaring variables 

* Variables are the used in programming the same way they are used in math: as storage containers for some kind of data, kinda like a placeholder.
* Creating and storing a variable is called "declaring" a variable.

---

# Declaring variables 

To declare a new variable, you need at least 2 things.

1. the JavaScript keyword `var`, `let`, or `const` 
which specifies that you are assigning a new variable
2. a name for the variable (called an identifier) 
that adheres to naming rules discussed in the next segment

---

# Variables 

* The reason a variable needs at least 2 components is because 
variables can be created without being assigned to a value yet.
* Whenever we declare variables without assigning them to a value, their value is automatically "undefined." For example:

```
let myVariable;
let weeklyIncome; 
```
--- 

# Assigning Variables

* if we tried to print the value of either of these two variables, we would see "undefined" in the console
* If we know the value we want to set a variable to when we are creating it, we can simply declare a new variable and set it equal to this value
(this is called "assigning" the variable to a value), like so:

```
let year = 2018;
let placeHolder = "This is an example of a variable.";
```
--- 

* If we had declared a variable without assigning its value (an undefined variable), and now we know what we would like to set the variable equal to,
we can simply call the variable name and set it equal to that value, like so:

```
myVariable = "random words!";
weeklyIncome = 700;
```

* We do not need to use the "var" keyword again because we have already declared that myVariable and weeklyIncome 
  
--- 

# Console.log

* To check that these variables now store the new values, we can print them to the console.
* The `console` is used in programming for troubleshooting, finding bugs, keeping code organized, and ensuring accuracy.
* To view the console on codepen, simply click the console button in the bottom left corner

--- 

# Console.log

* If you are not on codepen's website, you can view the console by right clicking the webpage and clicking 'inspect' or 'inspect element' and selecting the console tab:
* this is also useful when in codepen's `debug` mode, which you might have to use sometimes to fix certain errors

---

# Console.log

* To print text to the console, we place it in the quotation marks of the console print statement:
  
```
console.log("Hello, Patrick");
```

* We can print our variables to check that they print the new values we assigned them:

```
console.log(myVariable);
console.log(weeklyIncome);
```

--- 

# Reassign variables 

* We can reassign the value of a variable as many times as we would like:

```
myVariable = "this is assigned to a new value";
myVariable = "now it's assigned to an even newer value";
```

*  We can even assign the value of a variable to that of another variable like so:

```
weeklyIncome = myVariable;
```
---

# Let keywords

* we have been using var to define variables, but `let` is newer
* use let instead of var always 
* you will see var in older code so it's good to know it what it is
  
--- 

# TLDR: 

## "var" == bad "let" == good use "let"

```
if (true) {
  let newVar = "newVar only exists in the context of this codeblock";
}
```

--- 

<!-- //////////////////////////// *** Write about organization and syntax ***/////////////////////////////////// -->
# Coding style

* Your coding style is the way you format and structure the code you write.
* Clean code is important because it makes it easier to read your code, not only for you but for others viewing your code(teacher) or working on your code after you(group work)
* Clean code also allows us to troubleshoot more easily because we can pinpoint problem areas. This is harder to do with unorganized or 'spaghetti' code

---

# conventions

* Use "camelCase" for naming variables(covered more in depth in the next section). camelCase is the practice of keeping the first word lowercase, and the rest of the words begin with an uppercase letter.
   
      ```  
      Ex: camelCase, javaScript, myExample
      ```

---

# Conventions -- cont

* Put spaces before and after operators (+, -, *, /, %, etc) and put a space after commas. This helps with readability.
      Ex: 

      ```    
     let price = 200 + (5 - 27) / 30; 
      ```
  * Codepen will do this autuomatically for you if you click on `Tidy JS` 

---

# Exercises

1. open a new Code Pen
2. CTRL + C the exercise, CTRL + V into the new Pen that you just created
3. Name your work something meaningful, then save (CTRL + S)
4. under the problem, provide a solution
5. repeat until problems <= 0
6. smile, you're done, either move on to the next part or wait for your teachers instructions

