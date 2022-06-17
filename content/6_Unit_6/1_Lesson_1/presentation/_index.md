---
title: Loops
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Loops 

---

* Loops are used in programming to save time and effort, both in terms of the time and energy the programmer has to put in, and the efficiency of the program itself
* Loops repeat the same block of code until a specified condition is met, typically using or plugging in a different value each time
* Loops can be used to accomplish a variety of tasks, such as iterating through an array, etc. etc.

---

## For Loops 

* As we visit each type of loop, you'll notice that they have very literal names
* For loops have the name 'for loop' because code is executed for as many iterations as specified
* An iteration is one complete loop. We make for loops execute for a specified number of iterations by declaring an iterator


---


{{% section %}}

* The keyword for, followed by parenthesis and a pair of curly brackets
  * The parenthesis contain the three statements for loops require
  * The curly brackets contain the code to be executed during each iteration of the loop

---

{{% slide content="slides.forloop" %}}

{{% /section %}}


---

{{% section %}}

* Statement 1/Iterator
  * Statement 1 is code that initializes the iterator for the for loop.
  * The iterator is our counting variable. It counts how many times we have looped through the for loop, so that the program knows when to stop looping.
  * The iterator will typically start at 0, unless we are working with arrays or something in which we want to start at a different index. 
  * Statement 1 is executed before the loop begins executing


---

{{% slide content="slides.forloop" %}}

{{% /section %}}

---
{{% section %}}

* Statement 2/Condition
  * Statement 2 is a condition that the loop tests before beginning the next loop
  * The condition tests the iterator against some other value
  * Say, for example, we wanted to loop through the for loop 5 times. The iterator would start at 0, and the condition would test if the iterator is less than 5.
  * As long as the condition evaluates to true, the loop will execute


---

{{% slide content="slides.forloop" %}}

{{% /section %}}

---

{{% section %}}

* Statement 3/Increment
  * Statement 3 is the final portion of the statements within the loop's parenthesis
  * Statement 3 is executed after the loop executes, and updates the iterator to signify that another loop has been completed
  * The iterator will typically be increased or decreased by 1, but it is not limited to changing the value by 1

* Between each of the three statements, you must place a semicolon

---

{{% slide content="slides.forloop" %}}

{{% /section %}}

---

* Example : The following for loop will loop 4 times and print the value of i to the console each time:

```js
for (i = 0; i < 4; i++) {
  console.log("i is currently equal to " + i);
}
```

---

* In this for loop, 
* Statement 1 is i = 0, meaning the loop will start with the iterator, i, at 0;
* Statement 2 is i < 4, meaning the loop will execute as long as i is less than 4
* Statement 3 is i++, meaning after each loop, the value of i will be increased by 1.

---

* In the beginning of working with loops, it's really useful to walk through each iteration of a loop by hand with pen and paper, to understand how the loop is working
* On paper, for each iteration, you can record the value of the iteration variable, whether the condition is true, and the value of the iterator after it has been incremented/decremented/altered

--- 

* For example, I would write something like this on paper to walk myself through the forloop on line 68:
  
Loop 1: 

```js
i = 0
i < 4 = true
i++ = 1
// Will the loop execute again? Yes
```

Loop 2:

```js
i = 1
i < 4 = true
i++ = 2
// Will the loop execute again? Yes
```

---

Loop 3:

```js
i = 2
i < 4 = true
i++ = 3
// Will the loop execute again? Yes
```

Loop 4:

```js
i = 3
i < 4 = true
i++ = 4
// Will the loop execute again? No, because the condition i < 4 
// is no longer true after i was last incremented
```

---

* Loops can be used to accomplish more than simply printing things over and over. 
* Loops can be used in any scenario where we would otherwise have to write many lines of similar code or lines performing the same task, but with altered values

---

* For example, the next for loop will loop through the array 'cities' and capitalize each element

```js
let cities = ['baton rouge', 'new orleans', 'san antonio', 'miami', 
  'portland', 'san francisco', 'las vegas'];
console.log(cities);
```

* By setting the condition to i less than the length of the cities array, we ensure that the for loop iterates through each array element 

---

* Remember that the length of an array is the number of elements within the array
* Additionally, remember that array indexes begin at 0, and we initialized our iterator, i, to be 0 in the beginning of the for loop. 
* Do not get confused at the fact that there are 7 elements within the array, but the condition is proven false whenever i is equal to 7. This is because i begins at 0.

---

```js
for (i = 0; i < cities.length; i++) {
  // here, we are using the iterator to access the element in the array according to which loop we are on.
  // if you are writing out the loop to better understand it, ensure that you understand the code within the loop is changing each iteration, from  cities[0] = cities[0].toUpperCase();, to cities[1] = cities[1].toUpperCase();, and so on
  cities[i] = cities[i].toUpperCase();
  console.log(cities[i]);
}
```

---

* To better understand how much our efficiency is increased by using loops, compare the forloop on line 117 to the alternative code below. Both perform the same actions, but the forloop is much quicker, both for us to program and for the computer to execute:

---

```js
cities[0] = cities[0].toUpperCase();
console.log(cities[0]);

cities[1] = cities[1].toUpperCase();
console.log(cities[1]);

cities[2] = cities[2].toUpperCase();
console.log(cities[2]);

cities[3] = cities[3].toUpperCase();
console.log(cities[3]);

cities[4] = cities[4].toUpperCase();
console.log(cities[4]);

cities[5] = cities[5].toUpperCase();
console.log(cities[5]);

cities[6] = cities[6].toUpperCase();
console.log(cities[6]);
```

---

* If you declare the variable used as the loop's iterator outside of the loop's declaration, you can omit statement 1, like so:

```
let j = 0;
for (; j < 5; j++) {
  console.log(j);
}
```

---

* Additionally, if the iterator is incremented/decremented/altered inside of the loop's code, statement 3 can be omitted from the loop's parenthesis aswell:

```js
for (i = 0; i < 10;) {
  if (i < 5) {
    console.log(i + " is smaller than 5");
  }
  i++;
}
```

---

## For-In Loops 

* Whereas forloops repeat a block of code a specified number of times, a for-in loop loops through the properties of an object
* The code within the loop is executed once per each of the object's properties
* For-in loops have two required parameters: var and object, where var is the property and object is the object name

---

* For-in loops behave similarly to forloops looping through arrays, but instead of looping through elements of an array, we are looping through properties of an object
* To visit each of the properties in an object, we would program our for-in loop like so:

---

```js
let chinchilla = {
  name: "Pushki",
  age: 4,
  color: "gray",
  fluffLevel: "maximum capacity"
};

// Notice that the contents of the loop's parenthesis is much 
// different than a typical for loop
// The parenthesis tell the loop to loop through each property 
// in the object 'chinchilla'

for (property in chinchilla) {
  console.log(chinchilla[property]);
}
```

---

* We can also include a specifier to loop through the properties of an object, whether it be let, const, or var; however this is not necessary, as you can see on line 185
* The following three for-in loops will produce the same output as the loop on line 185:

```js
for (var prop in chinchilla) {
  console.log(chinchilla[prop]);
}
for (const prop in chinchilla) {
  console.log(chinchilla[prop]);
}

for (let prop in chinchilla) {
  console.log(chinchilla[prop]);
}
```

---

## For-Each 

* The last forloop related topic worth mentioning is the concept of for-each
* Foreach is used to visit each element within an array.
* We've written for loops that visit each element in array previously, so the code below will show the conversion of a regular for loop to a foreach statement:

---

```js
let inventory = ['muffins', 'rolls', 'pastries'];
let popularItems = [];

for (i = 0; i < inventory.length; i++) {
  popularItems.push(inventory[i]);
  console.log("New popular item added: " + popularItems[i]);
}
```

* The code above is copying the contents of the inventory array to the popular items array. The code below performs the same task using the foreach method:

---

* first we clear the popularItems array so the elements aren't duplicated

```js
popularItems = [];
// next we use a forEach statement to push and print the elements
inventory.forEach(function (element) {
  popularItems.push(element);
  console.log("New popular item added: " + element);
});
```

---

# Exercises

[back](..)