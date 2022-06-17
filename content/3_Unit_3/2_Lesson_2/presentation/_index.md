---
title: Switch Statements
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---


# Switch statements 

---

* The final type of conditional statement is the switch statement. 
* Switch statements are used to "switch" among a number of conditions called cases, instead of including tons of else if statements. 
* The cases compare the value of the tested variable/value to the value attributed to the case.
* Once the correct value is found, the code in that case is executed.
* If no cases match the tested value, the switch statement executes the "default case" 
  
---

## Examples:

* This first switch statement will test different conditions to see what today is, in terms of the name of the day.
* The switch statement will do this by utilizing a JavaScript date object, which will be covered in a later segment.
* The variables 'today' and 'day' get the current date from the JavaScript Date object. Objects are covered in a later segment.

---

* On line 35, the value of the day is returned to us in a numeric format, with 0 representing Sunday, 1 representing Monday, and so on.
* We use a switch statement instead of 7 if, else if, else statements to determine what day it is:
* The variable day is compared to the values of each case. When the value is matched, the day is printed. 

---

* We always include a default statement in switch statements in case of an error on our part, or in case none of the cases evaluate as true. 
* The default case also helps with troubleshooting instead of not having any output when something goes wrong.

---

```js
// today is a variable storing a new JavaScript Date object. 
let today = new Date;
// day is a variable storing the numeric value for today's day out of the week
let day = today.getDay();

// Pay attention to the syntax of the switch statement. First, begin with the keyword switch() with the tested variable within the parenthesis:
// The switch statement's cases go inside of the curly brackets:

switch (day) {
  // The first case on the next line contains the code to execute in the case that day is equal to 0. This is the equivalent of testing " if(day == 0) "
  case 0:
    // if this case is true, the day is Sunday. We print this to the console.
    console.log("It's Sunday");
    // It is important to include a break statement at the end of each case in a switch statement, so that the program stops checking each condition after the case has evaluated as true, and the switch statement is exited
    // Ensuring that the program does not continue to check the rest of the cases improves the program's efficiency 
    break;
    // the next line is the equivalent of testing " if(day == 1) "
  case 1:
    console.log("It's Monday");
    break;
  case 2:
    console.log("It's Tuesday");
    break;
  case 3:
    console.log("It's Wednesday");
    break;
  case 4:
    console.log("It's Thursday");
    break;
  case 5:
    console.log("It's Friday");
    break;
  case 6:
    console.log("It's Saturday");
    break;
    // the default case is simply declared by saying default: rather than case ___: 
  default:
    console.log("It's today");
}
```

---

* We can also program switch statements that check more complex conditions
* To do so, we set the variable the switch statement is checking to "true". 
* Now, we can set the conditions for the cases to more complex conditions, such as the cases below: 

---
* This switch example determines the letter grade of a test score out of 100

```js     
let testScore = 73;

// Note that we use 'true' in place of the tested variable, and incorporate the testScore variable in the case conditions
switch (true) {
  case testScore >= 90:
    console.log(testScore + " / 100 : A");
    break;
  case testScore >= 80:
    console.log(testScore + " / 100 : B");
    break;
  case testScore >= 70:
    console.log(testScore + " / 100 : C");
    break;
  case testScore >= 60:
    console.log(testScore + " / 100 : D");
    break;
  case testScore >= 70:
    console.log(testScore + " / 100 : F");
    break;
  default:
    console.log("Score is too low to even have a grade");
}
```

---
# Exercises


[back](..)