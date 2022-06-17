---
title: Array Methods
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Array Methods 

---

* to String : Arrays also have a `.toString()` method, and just like we can create arrays from a string, we can create a string from an array. The string contains the elements of the array separated by commas
  * syntax: `.toString()`

```js
var colors = ['Red', 'Orange', 'Yellow', 'Green', 'Blue', 'Indigo', 'Violet'];
console.log("The colors that makeup the rainbow are " + colors.toString());
```

---

* Join : Similar to the toString() method, the join method creates a string from an array, but allows us to specify a different separator than the comma:
  * syntax: `.join()`

```js
colors = ['Red', 'Orange', 'Yellow', 'Green', 'Blue', 'Indigo', 'Violet'];
console.log("The colors that makeup the rainbow are " + colors.join(" and "));
```

---

* push : `push` is a method that allows us to 'push' a new element into an array. The element is added at the last index.
  * syntax: `.push()`

```js
colors = ['Red', 'Orange', 'Yellow', 'Green', 'Blue', 'Indigo', 'Violet'];
colors.push('White');
colors.push('Black');
console.log("New colors were added to the list : " + colors[7] + " and " + colors[8]);
```

---

* shift : `shift` is a method that allows us to remove the first element of an array. The element is completely removed from the array, not just accessed. This means that the rest of the elements shift up one position/index. The element is returned to us and is no longer in the array.
* `syntax: `.shift()`

```js
console.log("The first color in the list is : " + colors.shift());
console.log("We removed Red from the list, so now the colors are " + colors.toString());
```

---

* unshift : `unshift` is a method that inserts a new element at the beginning of an array, and increases the rest of the elements' indexes by 1
  * syntax: `.unshift()`

```js
console.log("I'm adding red back to the list now... ");
colors.unshift("Red");
console.log("Now the colors are back to normal : " + colors.toString());
```

---

* sort : sort is a method that sorts the elements of an array alphabetically
  * syntax: `.sort()`

```js
var letters = ['P', 'M', 'E', 'T', 'N', 'X', 'J', 'I'];
console.log("Letters unsorted: " + letters.toString());
console.log("Letters sorted: " + letters.sort().toString());
```

---

* reverse : `reverse` is a method that reverses the order of the elements within an array
  * syntax: `.reverse()`

```js
var order = ['First', 'Second', 'Third', 'Fourth', 'Fifth'];
console.log("Original order: " + order.toString());
console.log("Reversed order: " + order.reverse().toString());
```


---
# Exercises


[back](..)