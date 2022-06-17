---
title: Naming Variables
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Naming Variables 

* Remember that we declare a new variable by typing the let keyword and then assigning a name to the variable. 
* A variable's name is also known as an identifier.

```
let blank;
```

---

# Rule 1

* Names must begin with a letter, an underscore, or a dollar sign $ (best coding practice starts names with a lowercase letter). 
* The letter of the first word in an identifier should always be lowercase, and the first word of any proceeding words should be uppercase. 

```
// This practice is called camelcase. Ex: 
// myVariable, placeHolder, camelCase
```

---

# CamelCase?

![yes](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ef/CamelCase.svg/368px-CamelCase.svg.png)

---

# Rule 2

* Names are case sensitive. If you declare a variable with the identifier `myVariable`, it cannot be accessed by saying `myvariable` or `myVARIABLE`

--- 

# Rule 3

* Reserved words cannot be used as names. 
* There are a few words used in JS that perform specific actions, such as the let keyword that tells the computer we are declaring a new variable
* Reserved words include JavaScript keywords, and all of the words included here: http://www.javascripter.net/faq/reserved.htm

--- 

# Reserved words example 

```
            let monthlyRent = 600;
            let carNote$ = 300;
            let home_address = "789 Super Fun Ln.";
            let businessAddress2 = "326 City Rd.";
            let lunchTotal$ = 11.49;
```

* notice the different types of data assigned
  
---

# Exercise 

* Declare new variables and convert the following phrases to an appropriate variable name, using camelCasing and other naming conventions:

1. annual income
2. bills to be paid
3. number of vacation days left
4. week one
5. week two
6. week six 