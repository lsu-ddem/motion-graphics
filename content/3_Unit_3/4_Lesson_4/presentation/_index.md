---
title: String Methods
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# String Methods

---

## String Length
* syntax: `.length`

```js
let longestWord = "pneumonoultramicroscopicsilicovolcanoconiosis";
console.log(longestWord.length);

let sentence = "The longest word in the English language is " + longestWord;
console.log(sentence.length);
``` 

---

* Finding the first occurrence of text within a string
  * syntax: .indexOf("")

```js
let repeating = "Dogs are the best. Dogs are the best. Dogs are the best.";
let index = repeating.indexOf("best");
console.log("The word best first shows up at index " + index);

let carmen = "Where in the world is Carmen San Diego?";
console.log("I found her! She's at index " + carmen.indexOf("Carmen San Diego"));
```

---

* we can also include a second parameter that tells the program to find the instance of the text after a specific index, like so:

```js
console.log("The word best shows up next at index " + 
  repeating.indexOf("best", index));
console.log("The word best shows up last at index " + 
  repeating.indexOf("best", 14));
```
---

* Finding the last occurrence of text within a string
  * syntax: .lastIndexOf("")

```js
repeating = "Dogs are the best. Dogs are the best. Dogs are the best.";
console.log("The word best last shows up at index " + 
  repeating.lastIndexOf("best"));

let waldo = "Lorem ipsum dolor sit amet, where's waldo consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Where's waldo ut enim ad minim veniam, quis nostrud exercitation ullamco laboris where's waldo nisi ut aliquip ex ea commodo where's waldo consequat."
console.log("Waldo was last seen at index " + 
  waldo.lastIndexOf("where's waldo"));
```

* Just as we did for the `indexOf()` method, we can also include a second parameter that specifies the starting index, like so:

```js
console.log("Waldo was last seen at index " + 
  waldo.lastIndexOf("where's waldo", 25));
```

---

* Searching a string to see if text is in it, and returning the index if it is. 
  * If the text is not in the string, the return value is -1.
  * syntax: `.search("")`

```js
let alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
console.log(alphabet.search("K"));
console.log(alphabet.search("m"))

let randomStuff = "I can't find my purse anywhere, is it in this string?";
if (randomStuff.search("purse") != -1) {
  console.log("I found your purse! It was at index " + 
    randomStuff.search("purse"));
} else {
  console.log("No your purse wasn't in that string :( ");
}
```

---

* The next method deals with "cutting out" a portion of a string by specifying the start and end index of what we want to cut out. Three methods achieve this: `slice, substring, and substr`. These achieve the same results, so we will only review `slice`.
* If you'd like to see examples of the other two methods, `substring` and `substr`, visit: https://www.w3schools.com/js/js_string_methods.asp
* To find the start and end index, you can use the methods above, or simply count the characters. Each character in a string, including spaces, is one index. Remember that indexes begin at 0, not 1.

---

* Slice
  * syntax: `.slice(start, end)`

```js
repeating = "Dogs are the best. Dogs are 100% the best. Dogs are the best.";
let percentOfBestDogs = repeating.slice(19, 42);
console.log(percentOfBestDogs);

let cut = "Cut my life into pizzas, dis is my last resort";
console.log(cut.slice(0, 23));
```

---

* Replacing content in a string. The replace method returns a new string with the changed values instead of altering the original string
* syntax: `.replace("old", "new")`

```js
let theTruth = "Dogs are the best.";
let betterDogs = repeating.replace("best", "all time greatest");
console.log(betterDogs);
```

---

* In the situation that we have multiple instances of the word being replaced, and we want to replace *all* of them, follow this syntax:
* Remove the quotation marks from the "old" string and place a forward slash (/) before and after the phrase
* After the last forward slash, include the letter 'g'. This tells JS to alter all instances of the phrase within the slashes.

```js
theTruth = "Dogs are the best. Dogs are 100% the best. Dogs are the best.";
console.log(theTruth.replace(/best/g, "greatest"));
```

---

* Converting string to uppercase
* syntax: `.toUpperCase()`

```js
let small = "i want to be in uppercase :( ";
console.log(small.toUpperCase());
```

---

* Converting string to lowercase
* syntax: `.toLowerCase()`

```js
let large = "I WANT TO BE IN LOWERCASE :( ";
console.log(large.toLowerCase());
```

---

* Convert a string into an array
* This is the final string method we will cover. This method is extremely handy when you are dealing with a file or list of data, such as a class roster that you need to place into an array, and doing so manually would take a long time.
* Strings are split by the specified character within the quotations of the `split` method:

```js
let names = "Bob, Barb, Max, Daniel, Katie, Marie, Elle, Jack, Chloe, Smith, Jane";
let classRoster = names.split(", ");
console.log("The fifth student on the roster is " + classRoster[4]);
console.log("The seventh student on the roster is " + classRoster[6]);
console.log("The last student on the roster is " + classRoster[10]);
```

---

* Note that strings can be split by whatever you need them to be split by.
* If your string is a list of values separated by spaces, you simply put a space within the quotes:
  
```js
let values = "12 13 14 15 16 17 18 19";
let arrayOfValues = values.split(" ");
console.log(arrayOfValues[3]);
```

---
# Exercises


[back](..)