---
title: Intro to JSON
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Intro to JSON

* JSON stands for JavaScript Object Notation.
* JSON is a data format that stores information in key:value pairs, just like a JavaScript Object does
* In other words, JSON is a specific syntax of JavaScript that is used to serialize certain data types
  
---

# JSON Uses

* JSON is commonly used to store and exchange data between a server and web application or browser.
  
![client/server](https://upload.wikimedia.org/wikipedia/commons/c/c9/Client-server-model.svg)

--- 

# JSON USES

* For example, when you visit a website and login with your username and password, you're submitting data to a server that checks your login credentials and either logs you into the website, or tells you the login information was incorrect.
* In order for the browser and server to communicate and actually log you in or send an error message, the information you entered must be submitted to the server. This is where JSON becomes useful.
  
---

# JSON

* JSON may be stored in its own file with the file extension .json, or put directly into code when it is stored as a string  
* Because JSON uses JavaScript notation, any JavaScript object can be converted into JSON and sent to a server.
* Likewise, a server can return JSON data to us, and the JSON data can be converted to JavaScript objects and used as such.

--- 

# Structure

* JSON syntax is derived from JavaScript object syntax.
* Remember that JavaScript objects are stored in key:value pairs (if you need a refresher on objects, review lesson 1.3 JS Data Types)
* JSON syntax also requires that data is stored in name:value (AKA key:value) pairs.

--- 

# Structure

* These syntax rules are similar to the syntax rules for JavaScript objects, however there are a few notable differences: 
  * JSON name/value pairs both have to be wrapped in double quotation marks (" "). This rule excludes number values, booleans, and null. 

ex:    
```
{"species":"cat"}, {"age": 21}  JS object: {species: "cat"} or {species: 'cat'}, {age: 21}
```

---
# Structure 

* A JSON object has to be stored in a variable as a string, which is then parsed into JS.
* The JSON object is stored in a string by placing the entirety of the JSON data within a pair of single quotes: ' ' 
* For example, here is JSON data storing student info: 
  
```
{ "firstName" : "Millie", "lastName" : "Brown", "grade" : 10 }
```

---

# JSON diffs

* A JavaScript object can contain attributes of practically any data type, including a date or a function, as we practiced in earlier lessons
* JSON objects, however, cannot have attributes that are of the following types: 
      - functions
      - dates
      - undefined
  
---

# JSON DIFFS

* Which means that JSON objects `can` have attributes of the following data types:
    - strings
    - numbers
    - other JSON objects
    - arrays
    - booleans
    - null
  
---
      
# Accessing JSON

* Dot Notation: values of the JSON object can be obtained by specifying the objectName.keyName like so:

```
dogObj = {"breed":"poodle", "name":"Moxie", "age": 3, "likes":"fluffy toys"};

console.log(dogObj.breed);
console.log(dogObj.name);
console.log(dogObj.name + " is a " + dogObj.age + " year old " + dogObj.breed);
```

---

#  Accessing JSON
* Bracket Notation: values of the JSON object can be obtained by specifying the objectName["keyName"] like so:

```
catObj = {"breed":"Siamese", "name":"ChiChi", "age": 2, "likes":"napping"};
console.log(catObj["breed"]);
console.log(catObj["name"]);
console.log(catObj["name"] + " is a " + catObj["age"] + " year old " + catObj["breed"] + "cat");
```

---

# Modifying JSON

* Dot and Bracket notation are also used to modify values of the JSON object:
  * Dot notation modification:
  
```
catObj.age = 2.5;
console.log(catObj.age);
```

--- 

# Modifying JSON

* Bracket notation modification:

```
dogObj["likes"] = "tennis balls";
console.log(dogObj["likes"]);
```

* this is useful if your key is a number
  
---

# Resources

* JSON Documentation
  * https://www.json.org/
  * https://www.w3schools.com/js/js_json_intro.asp
  * https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON


* What is JSON and Why Would I Use It?
https://stackoverflow.com/questions/383692/what-is-json-and-why-would-i-use-it

--- 

# Exercises 

[back](../)