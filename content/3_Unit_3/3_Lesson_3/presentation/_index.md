---
title: Using JS Objects and Methods
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Using JS Objects and Methods 

---

* In lesson 1.3 discussing data types, we learned how to create objects in JavaScript.
* Remember that objects store multiple values within one variable, and their values are attributed to their "properties"
* We can obtain the value of an object's property by typing the objectName.objectProperty

---

* There is a difference between typical variables and objects that we have not yet discussed, and that is the difference between primitive values and reference values.
* Primitive values are simply values stored to variables without creating new objects.
* You weren't aware, but for all of the types of variables we have created so far, there was a way for us to declare those variables as objects. 

---

* If we were to have declared the variables as objects, they would be of the reference type instead of primitive.
* For example, lets simply declare a new variable that stores a string of text:
  
```js
let primitiveWords = "Have a really great day, like maybe even the best day ever, because why not.";
```

* The variable 'primitiveWords' is a string primitive. 

---

* JavaScript identifies six data types as primitive: **undefined, null, boolean, number, string, and symbol**.
* That means the following variables are also primitive types:

```js
let year = 2018;
let snowyOutside = false;
let randomVariable;
let placeHolder = null;
```


---

*  Now lets create the reference type equivalent of the primitive variable 'words':

```js
let referenceWords = new String("Have a really great day, like maybe even the best day ever, because why not.");
```

*  the variable referenceWords is a String Object.
* The purpose of learning about the difference between primitive and reference types is to understand the use of JavaScript methods.

---

* JavaScript methods exist for the different objects in the JavaScript library.
* An object's method is essentially a function that was programmed as a property of that object, and therefore we can invoke the function similarly to how we retrieve any property of an object: objectName.objectMethod()
* We have not yet covered functions, so we will not learn about writing object methods until the next section.

---

* Instead, this lesson focuses on using the objects methods already built into the JavaScript library.
* Lets start with the String Object and its methods:
* As you saw, we can create a reference type variable that stores a string object.

---

* On this object, we can use the methods created for JavaScript String Objects, such as:
    * .length : returns the length of a string
    * .indexOf("word") : returns the index of the first occurrence of the specified text within quotes
    * .slice(start, end) : splits a string into two strings, the new string containing the text within the start and end indexes 

---

* For example:
  
```js
console.log(referenceWords.length); // this prints 76 to the console
console.log(referenceWords.indexOf("great")); // this prints 14 to the console
console.log(referenceWords.indexOf("why")); // this prints 68 to the console
```

* However, if I try to use these methods with the primitiveWords variable....

```js
console.log(primitiveWords.length); // this prints 76 to the console
console.log(primitiveWords.indexOf("great")); // this prints 14 to the console
console.log(primitiveWords.indexOf("why")); // this prints 68 to the console
```

* The methods still work even though primitiveWords is a primitive type!!!

---

* This is because, whenever these methods are invoked, JavaScript treats primitive values as objects in order to use the many methods in the JS library.
* This means that we can apply the JavaScript methods for most objects to their primitive equivalent.
* We will now cover a few different methods and objects from JavaScript's library


---
# Exercises


[back](..)