---
title: JSON Syntax
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# JSON Syntax 

* JSON is often used to communicated between web browsers and servers
* it is always sent as text, AKA a string
* the JavaScript method `JSON.parse()` exists to parse the data from strings into JavaScript
  making the translation from JSON text to useable JavaScript data easier for us
  
--- 

# Parse Method 

* The JSON.parse() method can be used on any JSON data you want to convert to JS, whether it was received from a server, or it was stored in the JS code.
* The first requirement of the parse method is that the JSON data must be wrapped in a string by placing single quotes around the entirety of the data

---
# Example 

* For example, say we declare a new JSON object on the next line like so:

``` 
let studentJSON = 
  { "firstName" : "Millie", "lastName" : "Brown", "grade" : 10 };
```
* If we tried to use the parse method on studentJSON as it is, and then print the last name attribute, nothing will be printed to the console :

```
let studentJS = JSON.parse(studentJSON);
console.log(studentJS.lastName);
```
---

# Example 

* The parameter of the JSON.parse() method must be a string 

```
studentJSON = 
  '{"firstName" : "Millie", "lastName" : "Brown", "grade" : 10}';
```

* Reassigning the value of studentJSON to the string of JSON data now allows us to successfully implement the parse method:

```
let student = JSON.parse(studentJSON);
console.log(student.firstName);
```

---

# JS to JSON

* Remember that JSON is useful for exchanging data from AND to a web server.
* In the event that we want to convert JS data and SEND JSON data to a web server, we essentially perform the opposite action of the JSON.parse method
* Fortunately, there is also a method that makes this task easy for us, called Stringify.

---

# Stringify Method

* Declare a new variable to store the string returned by the Stringify method:

```js
let newString;
```

* Set the new variable equal to the Stringify method with the JavaScript object passed in as a parameter:

```
newString = JSON.stringify(student);
```

---

# Exceptions

* The string is now ready to be sent to a server, which will read the JSON text
* exceptions: 
  * Remember that JSON does not support `functions, dates, or undefined values`. 
  * if it has a date, function, or undefined value, JSON will alter the object according to the unsupported data type.

---

# dates & functions 

* Dates are simply converted to a string. Let's look at an example:
  
```
let obj = { name: "John", today: new Date(), city : "New York" };
let myJSON = JSON.stringify(obj);
console.log(myJSON);
```
* Functions are removed from the object entirely unless the return value of a function is converted to a string before the stringify method is implemented

--- 

# Looping

* How do we loop over the data? 
* Looping is extremely useful when working with larger JSON data sets; for example when populating a table of the JSON data instead of having to manually enter each cell
* Looping through JSON data is something that will look familiar, as it just uses a simple for-in loop
  
--- 

# For-in loop 

* used to loop through the properties of an object; in this case, we're looping through the properties of a JSON object
* For JSON data, we can loop through and print each key like so:
  
```
television = { "brand":"Samsung", "model":"QF Series", "make":"QN82Q6FNAFXZA", "price":2999};
for (key in television) {
  console.log(key);
}
``` 

---

# for-in

* Note that the iterator, key, can be named anything. It could be i, x, etc. The name is irrelevant
* To loop through the JSON data and retrieve the values of the key:value pairs, we use bracket notation like so:
  
```
for (key in television) {
    console.log(television[key]);
}
```

---

# Nesting
  
* Sometimes you want to store a JSON object within a JSON object.
* For example, if we're making a list of our friends and their respective attributes, such as hair color, eye color, age, name, etc. all of these keys typically require one value
  
---

# Nesting 

* we use nesting for more complex data, such as pets 
  
```
friend = {
  "name":"Kate",
  "age":21,
  "hairColor": "Blonde",
  "eyeColor": "Brown",
  "pets": {
    "bird": "Mack",
    "iguana": "Beemer",
    "cat": "Ozzy",
    "hamster": "Retsuko"
  }
}
```

---

# Nesting

* Nested JSON data is simply accessed using dot or bracket notation like so:

```
console.log(friend.pets.hamster);
```

* or:

```
let pet2 = friend.pets["iguana"];
console.log(pet2);
```

---

# Exercises 

[back](..)





