---
title: Date Object and Methods
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Date Object and Methods

---

# Date Object 

---

* A useful object in the JavaScript library is the Date object. 
* We now know the difference between primitive and reference types, and we know that JavaScript treats primitive types as objects(aka reference types) when using methods.
* A date object, however, needs to be declared for us to work with dates.

---

* We declare a date object by simply saying:

```js
let today = new Date();
```

* Setting the variable equal to new Date(); constructs a new date object that the today variable is a reference to.

---

* There may be an instance in which you wish to create a date object that does not represent the current time. In this case, we can construct date objects like so:
* within the parenthesis, we place: `(Year, Month, Day, Hour, Minute, Seconds, and Milliseconds)`
* we do not have to provide all of these parameters, however. 

---

* For example, we can provide only the year, month, and day, like so:

```js
let myBirthday = new Date(1997, 7, 29);
```

* Now we can apply the many date methods to our date object, 'today'.

---

# Date Methods

---


* getFullYear : this method returns the year of the date object in a 4 digit format
  * syntax: `.getFullYear()`

```js
today = new Date();
console.log("The current year is " + today.getFullYear());

myBirthday = new Date(1997, 7, 29);
console.log("I was born in " + myBirthday.getFullYear());
```

---

* 2. getMonth : this method returns the month of the date object as a number. Months begin at 0, meaning January = 0 while December = 12
  * syntax: `.getMonth()`


```js
today = new Date();
console.log("The current month is " + today.getMonth());
```

---

* instances like the print statement above allow us to program our own solutions. If I wanted to print the word form of the month, such as January, we could use an array, if-else statements, or a switch statement:

```js
let months = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'];
let currentMonth = today.getMonth();
console.log("The current month is " + months[currentMonth]);
```

---

* 3. getDate : this method returns the day of the date object as a number from 0-31(out of the month)
  * syntax: `.getDate()`

```js
today = new Date();
console.log("Today is " + today.getMonth() + " / " + today.getDate());
```

---

* 4. getDay : this method returns the day of the date object as a number from 0-6 (as a weekday)
  * syntax: `.getDay()`

```js
today = new Date();
let days = ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
console.log("Today is " + days[today.getDay()]);
```

---

* 5. getHours : this method returns the hours of the date object as a number from 0-23
  * syntax: `.getHours()`

```js
today = new Date();
console.log("The current hour is " + today.getHours());
```

---

* 6. getMinutes : this method returns the minutes of the date object as a number from 0-59
  * syntax: `.getMinutes()`

```js
today = new Date();
console.log("The current minute is " + today.getMinutes());
```

---

* 7. getSeconds : this method returns the seconds of the date object as a number from 0-59
  * syntax: `.getSeconds()`

```js
today = new Date();
console.log("The current second is " + today.getSeconds());
console.log("The time is now " + today.getHours() + " : " + today.getMinutes());
```


---
# Exercises


[back](..)