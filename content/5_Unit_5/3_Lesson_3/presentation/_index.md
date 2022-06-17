---
title: JS Data Types
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Data Types

* You may have noticed in the first two sections that we declare new variables in the same way no matter what we set them equal to, by using the let keyword and giving the variable a name.
* JavaScript has `dynamic variables`. This is what allows us to declare all variables in the same way, and what allows us to reset a variable that may have stored a number before, to storing a string of text.

--- 

#  Numbers

  - Other programming languages typically specify the use between variables that store integers, which are whole numbers, and variables that store doubles, which are numbers with fractions or decimals.
  - JavaScript has dynamic variables, however, so there is no need to specify whether a variable is storing an integer or decimal/double. 

--- 

# Number Example 

* To create a variable that stores a numeric value, we simply declare a new variable to that value.
  
```
let myNumber = 45678930;
let shoppingBill = 45.89;
let myAge = 20;
let numberOfPetsIOwn = 4;
```

---
# Strings

* Strings are variables that store text. Variables that store strings are set equal to the string in quotation marks, whether it be a sentence, paragraph, or a single word. Examples:

```
let myString = "This is my string.";

let myParagraph = "This is my paragraph. It isn't about anything yet, it just exists to you some examples of a string. This paragraph could be as long or as short as I want ibe. But, I am out of sentences, so I'll cut it short.";

let name = "Bob Ross";
let firstName = "Leslie";
let lastName = "Knope";
```

---

# Booleans

* Booleans are variables that store a `true` or `false` value. The variables are identified with a name, and set to either `true` or `false`. 
* Booleans are important and useful variables, as they are used in conditional and logical statements, which we will visit later. Examples:

```
let myBoolean = false;
let pizzaIsGross = false;
let pizzaIsYum = true;
```

---

# Arrays

* Arrays are variables that store a collection of data. They are used to store multiple values within one variable. 
* The following syntax will declare an empty array with an unspecified size. Remember that the value of unassigned variables, including unassigned arrays, is undefined.

```  
let myEmptyArray = [];
```

---

* Arrays are declared by assigning the variable to data enclosed in brackets and separated by commas. 
* Arrays can store any data type and combinations of different data types. Ex:

```
let myArray = ["my", "JavaScript", "Array"];
let testScores = ["Jane", 80, "Matt", 76, "Kate", 90, "Rachel", 98, "Bartholomew", 85];
```

----

* If necessary, the declaration of an array can span across multiple lines, such as:

```
let sameTestScores = [
   "Jane", 80, 
   "Matt", 76, 
   "Kate", 90, 
   "Rachel", 98, 
   "Bartholomew", 85
];

let animals = [
   "dogs",
   "cats",
   "chinchillas"
];
```

---

* An element is single value or input in the array. The array named animals contains 3 elements: the strings `dogs, cats, and chinchillas`. 
* Each element has an index within the array. An element's index tells us where it is located in the collection of data.
* Array indexes begin at position 0. The first element in an array, then, has an index of 0. The second element is at index 1, the third is at index 2, and so on.

--- 

* To access data stored in arrays, we have to specify the index of the element we want to obtain. 
* Ex: I want to obtain the second element within the array named animals. The second element in this array is the string "cats". 
* The first element is at index 0, so we know the second element is at index 1. We would access the element at index 1 like so:
  
```
animals[1];
```

---

* Elements can be accessed by specifying their index within an array and can be assigned to a new value. Ex:

```
animals[1] = "polar bears";
```

* The array named animals would still contain 3 elements, but instead of dogs, cats, and chinchillas, the array now contains dogs, polar bears, and chinchillas.

--- 

* To print an element to the console, we simply place the statement accessing the element within the console.log print statement:
  
```
console.log(animals[1]);
```

* We can print multiple values in one print statement by adding a space in between the values, like so:
Note that the operator "+" is NOT adding the three values in the traditional sense. Rather, it is joining the two strings together, with a space in the middle.

```
console.log(animals[1] + " " + animals[2]);
```

<!-- --- -->

* Or we could print the entire animals array:

```        
console.log(animals);
```

---

## Question: 
### How would we use indexes to access values in the array named "testScores" for Kate and Bartholomew only? 


---

# Initialize array 

* Sometimes the content of an array needs to be added in later, and we want to create an empty array. 

```
let emptyArray = [];
```

* If we know what size our array is going to be, we can declare an empty array of a fixed size like so:

```js
let finalExamScores = new Array(30); 
// the variable finalExamScores is now assigned to a new array with 30 empty (undefined) elements. 
// this is usually not necessary 
```
---

# Objects

* An object is a collection of properties, and a property is an association between a name (or key) and a value.
* Objects are essentially used to store multiple values within one container.
* These values are referred to as properties of the object

--- 

* To understand properties, think of your dream car. Describe the car to yourself. You'll probably mention the color, make, model, etc. These are properties of the car.
* Cars are not the only things with properties, however. For example, describe yourself or your friend. You'll probably mention name, hair color, eye color, favorite show, favorite animal, etc.
* Objects allow us to create a variable in our program with which we can store all of these properties. 

---

* So, we can make an object that represents ourself, our friend, our dream car, or anything else, and store the properties in it.
* The value of a property can be any data type, meaning the 'year' property of a car can store a numeric value, while the 'model' property stores a string value
* We assign properties to objects in name:value pairs, either during the construction of an object, or after an object has been created

---

* First, we will look at declaring an empty object, and adding properties after an object has been created.
* An empty object is an object that does not yet have any properties assigned to it. Remember that we can always add properties to an object later on.
* To declare a new object without any properties, we say:

```
let myFirstObject = {};
```       

---

* We created our empty object, named myFirstObject. Now we want to add properties so that the object is no longer empty:
* To add a property to an object, we first have to **access** the object that we will be adding the property to. 
* We access an object by calling the object name, then we access the property of the object

---

* We can access an object's property two ways:  
        
* Dot Notation. Ex: objectName.propertyName  
   * Dot Notation uses a dot/period between the object name and property name to access or declare that property

* Bracket Notation. Ex:objectName["propertyName"]
  * Bracket Notation uses a pair of brackets after the object name, with the property name placed inside of the brackets in quotation marks

---

* Dot Notation is more often used because it is easier to read and is more efficient, as we have to type less characters than we would using bracket notation; however the two are interchangeable
* Adding a property to an object is similar to declaring a new variable, but we access the object and property and assign it a value, instead of assigning a value to a new variable using "let newProperty = ___"

```
objectName.propertyName = "someValue";
// or
objectName.propertyName = 12345;
```

---

* Adding a new property with dot notation:
  
```
myFirstObject.myFirstProperty = "this is my first object's first property";
```

* Adding a new property with bracket notation:
  
```
myFirstObject["mySecondProperty"] = "this is my first object's second property";

```

* Remember that properties can be any data type, and objects can have multiple properties of different data types
  
---

* Dot and bracket notation are also used to access a property that we want to edit the value of, like so:

```            
myFirstObject["myFirstProperty"] = "The value of this property has changed to this sentence!";
```

```
myFirstObject.mySecondProperty = "this property has a new value, too!!";
// Check the console to see that the values changed:
console.log("New values: " + myFirstObject.myFirstProperty + 
  " and " + myFirstObject.mySecondProperty);
```
---

* We can also create objects and assign their properties on the same line, or across multiple lines as we can do with arrays:
  * When we create a new object and assign properties at the same time
  * we set the new object equal to its properties using the following syntax

```
let newObject = {propertyOne:"valueOne", propertyTwo:"valueTwo", propertyThree:"valueThree"};
```

---

* Make sure that the properties are inside of the curly brackets, the property name is followed by a colon(:), and that the property:value pairs are separated by commas:

```js
let newCar = {make:"Honda", model:"Civic", color:"Gray"};
```

* on the line above, the newCar object is given 3 properties: make, model, and color.
* we can print these properties to the console like so:

```js
console.log(newCar.make);
console.log(newCar.model);
```

---

* Just as we were able to add and alter properties we added to an empty object, we can also alter the value of these properties after they are assigned, and add new ones:

```js
newCar.color = "Red";
newCar.year = "2018";

console.log("My car is a " + newCar.color + ", " + newCar.year + " "+ newCar.make + " " + newCar.model);
```

* Objects also have methods, which are functions that are programmed as properties of that object. We will discuss the use and creation of methods in a later segment.

---

# Exercise 

[back](..)