---
title: While Loops
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# While Loops 

---

* While loops, like for loops, have a very literal name. 
* They are called while loops because they execute the same block of code *while* a provided condition is true
* While loops have a simpler syntax than for loops. All we have to include is the while keyword, and place the condition for the loop within parenthesis:

```js
while (condition) {
  code to execute
}
```

---

* The syntax of a while loop is similar to a for loop, but with statement1 and statement3 omitted, leaving just the condition
* You can also compare the syntax of a while loop to an if-statement, the only real difference is that the while loop repeats itself until its condition is no longer true
* While loops have a simpler syntax than for loops, but they are a more dangerous form of loop for beginner programmers

---

* The reason while loops can be dangerous, especially for beginners, is because it is much easier to get stuck in an infinite loop using a while loop than it is using a forloop
* An infinite loop is the worst of the worst. They are caused by an error on the programmers part that led the while loop's condition to never result to false
* Infinite loops will literally execute forever, and have to be forcibly stopped either by the programmer forcing the program to stop running, or the compiler recognizing the infinite loop and terminating the program

---

* To avoid infinite loops, always ensure that the condition for your while loop will eventually be false. This is done by changing some variable used in the condition with each iteration
* This is the same concept as updating your iterator in a for loop, so that you can continue through the loop and eventually reach the loop's limit of iterations
 
---

* For example, the while loop below would turn into an infinite loop

```js 
let pies = 5;
let customers = 4;
while (pies >= customers) {
  console.log("We have enough pies for our " + customers 
    + "customers!");
}
```
---

* If you're extremely curious and want to break this page by removing the comments on lines 18 and 24 to make the infinite loop run, fight the urge to do so.
* The window will just be annoyingly slow for a while and codepen will eventually print [CodePen]: An infinite loop (or a loop taking too long) was detected, so we stopped its execution. Sorry!" to the console, so it isn't worth it
* The while loop on line 23 turned into an infinite loop because we didn't update the value of pies during each iteration

---

* If we never update the value of pies, the condition (pies >= customers) will never change, and will always be true, resulting in an infinite loop.
* We can turn the infinite loop into a functioning while loop by updating the pies variable within the loop's code

```js
let pies = 5;
let customers = 4;
while (pies >= customers) {
  console.log("We have enough pies for our " + customers + " customers!");
  pies--;
}
```

* Now, the while loop will make 2 loops before its condition is proven false and it stops executing.
  
---

* Now that you know what not to do with while loops, here is what you should use them for:
* While loops are used to repeat the same block of code repeatedly, just like for loops. So what is the difference?
* For loops are useful when we need to make a specific number of iterations *and* the code within the loop changes depending on what number iteration we are currently on
  * For example, using for loops to traverse through an array. We use the iterator variable to access the current element within the array

---

* While loops are simpler in that they aren't counting the number of loops they are making, they are simply executing the same code until they are told not to(which is done by the condition eventually resulting in false)
* Since while loops aren't counting the number of iterations they make, we choose to use for loops in situations in which the iteration count is relevant or important, such as arrays.

---

* Ex 1: The loop below "cuts" wood into 1000 sheets of paper per each log of wood. The loop executes 'while' we have wood to cut. When the wood variable is 0, there is no more wood to cut, and the loop terminates because the condition is proven false.

```js
let wood = 5;
let paper = 0;
while (wood > 0) {
  paper += 1000;
  wood--;
}
console.log("The paper factory made " + paper + " sheets of paper.");
```

---

* Ex 2: The function below uses a while loop to ask a user for their login credentials and breaks after the correct credentials are put in or the incorrect credentials are entered more than two times:
  * Invoke the function logIn and enter the login credentials when prompted: 
  * the login is "barbie" and the password is "confidentialBarbieBidniz"

---

```js 
logIn();

function logIn() {
  let login = "";
  let password = "";
  while ((login == "") && (password == "")) {
    login = prompt("Please enter login:");
    if (login == "barbie") {
      password = prompt("Please enter password:");
      if (password == "confidentialBarbieBidniz") {
        alert("Successfully logged " + login + " in!");
        console.log(login + " has been logged in.");
      } else {
        password = prompt("Incorrect password, please try again:");
      }
    } else {
      login = prompt("Incorrect login, please try again:");
    }
  }
}
```

---
      
# Do-While Loops

---

* The next type of loop is the do-while loop
* Do-while loops differ from while-loops in that the code to execute is executed first, and then the condition for the loop is checked.
* If the condition is false, the loop will stop executing, but no matter what a do-while loop will always execute at least once.
    
---

* While loops, however, check the condition first, and only execute the loop's code if the condition is true.     
* Because the order of a do-while loop is reversed, the syntax is somewhat reversed too:

```js
loopNumber = 0;
do {
  console.log("Testing do-while loop");
  loopNumber--;
} while (loopNumber > 0);
```

* If you check the console, you'll see that "Testing do-while loop" is printed once, even though the loop's condition says to loop while the variable loopNumber is greater than 0. 

---

* In a typical while loop, nothing would have been printed to the console because the condition is false. 
* However, since do-while loops execute once no matter the result of the condition afterwards, the statement was printed to the console.
* Do-while loops should be used over while loops when you want to make sure that the code is executed at least one time
    
---

* Below is the wood-paper example from the while loop section translated into a do-while loop:

```js
let wood1 = 5;
let paper1 = 0;
// The do segment of this do-while loop will execute the first time 
// no matter the result of the condition, but each iteration after 
// the first is dependent upon the condition resulting in true:
do {
  paper1 += 1000;
  wood1--;
} while (wood1 > 0);
console.log("The paper factory made " + paper1 + 
  " sheets of paper.");
```

---

* In this example, apple pie is printed once before checking the condition, but each iteration afterwards only executes and prints apple pie if the condition is true

```js
let apples = 3;
do {
  console.log("apple pie");
  apples--;
} while (apples > 0);
```

---

# Exercises

[back](..)