---
title: Functions
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Functions

---

* Functions are blocks of code that are programmed to perform specific actions/a specific task. 
* Functions are designed to be reusable because they save time and make programming easier. 
* Functions are similar to formulas in mathematics. 

---

* You may remember doing tedious math problems in which you had to plug values into the same formula over and over and over again, and record the answer, such as finding the circumference of a number of different circles.
* Functions eliminate the tedious portion of using formulas by taking the values we want to plug into a formula, plugging them in for us, and giving us the result. 
* Functions are not solely used for repeated use of a formula, however. Functions have essentially no limitations on their use, meaning you can program a function to do whatever you please. 

---

* We can have a function that returns sentences in pig latin, a function that calculates how many seconds you've been alive, a function that creates new objects or edits an array, the possibilities are endless.

* After we learn about functions, we will be able to create a button like the one below. Try clicking the button to see what happens.

```js
function helloUser(){
  let page = document.querySelector('#place');
  let adjectives = ["Magical!!! 🦄✨💫" , "Fun!!! 🦄✨💫" , "Handy dandy!!! 🦄✨💫"];
  let word = Math.floor(Math.random() * 3);
  page.innerHTML = "Functions are " + adjectives[word];
}
```

---

## See the function in action

[back](..)