---
title: Function Returns
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Function Returns
 
---

* As mentioned earlier, functions end with a return statement
* A return statement must begin with the keyword 'return'
* Whatever follows the return keyword is what is literally "returned" to us as a result of running the function
* We can place variables, equations, strings, concatenations, etc. as the return value for a function
* Unlike other popular languages, JavaScript does not require us to specify the type of data that is being returned

---

* I will provide a few examples of different types of functions and returns, so that you see the different possibilities for return statements, and gain greater understanding of functions:
* 1. Future Age Calculator
  * This function simply returns the age the user will be in the year provided by the user.
  * The function calculates the future age by subtracting the future year from the current year, and adding that value to the user's current age:
  * We return this equation on line 26, meaning that when we invoke the function, it will give us the result of the equation on line 26.

---

```js
let myAge = 20;
let futureYear = 2060;
console.log("I'm " + myAge + " now, but in " + futureYear + " I'll be " + futureAge(myAge, futureYear));

myAge = 32;
futureYear = 2047;
console.log("I'm " + myAge + " now, but in " + futureYear + " I'll be " + futureAge(myAge, futureYear));

function futureAge(currentAge, futureYear) {
  let now = new Date();
  let thisYear = now.getFullYear();
  return currentAge + (futureYear - thisYear);
}
```

---

* 2. Random Pet Generator
  * The next type of return we're going to look at is returning new objects or properties of new objects
  * This next function randomly selects different elements from different arrays and assigns these values to the property of a new pet object
  * We return the randomly selected properties of the new pet object to the user. 
  * The function's return statement prints the randomly selected properties of the object to the console in a specified format.

---

```js
console.log(petGenerator());

function petGenerator() {

  let petNames = ['Charlie', 'Max', 'Bella', 'Fluffi', 'Petunia', 'Bloo', 'Sushi'];
  let animalTypes = ['bird', 'cat', 'dog', 'horse', 'tiger', 'chinchilla', 'bunny'];
  let animalColors = ['tan', 'black and white', 'spotted', 'striped', 'red-orange', 'rainbow', 'brown'];

  let randomNumber = Math.floor(Math.random() * 7);

  let newPet = {
    name: petNames[randomNumber],
    type: animalTypes[randomNumber],
    color: animalColors[randomNumber]
  };

  return "Your new pet is a " + newPet.color + " " + newPet.type + " named " + newPet.name + "!";
}

```

---

* 3. Different Return Possibilities:
  * This example is a fully functioning state sales tax calculator for all 50 states.
  * The taxCalculator function takes two parameters: the price of the product and the state to calculate the sales tax for
  * The return value not only depends on the arguments, but also whether or not we are able to calculate the product price with sales tax. Events that would prevent us from doing so include the state not having sales tax, or the user passing in an invalid argument for the state parameter.

---

* We have to account for these possibilities, so we will program 3 possible return statements.
* To invoke this function, we simply declare a new variable equal to the functions invocation, or just print it to the console, like so:

[back to codepen to see this larger example](..)

---

# Exercises

[back](..)