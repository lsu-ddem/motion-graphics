---
title: Event Invoked Functions
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Event Invoked Functions

---


* JavaScript is typically used in coordination with HTML. Because of this, events that occur within or to HTML elements can trigger the invocation of a JavaScript function. 
* HTML is the language used for developing and designing web pages. I've provided a brief overview of HTML in the HTML tab of this codepen so you have a greater understanding of how we use events to trigger a JavaScript function to run.


---

* In this case, consider an event to be any action, property, or change that can be tested for, such as when something on a web page is clicked or hovered over. Events work the same way logically that they do in real life. Say, for example, if you were to insert your house key into your front door. On the event that you turn your key to unlock it, your door will become unlocked. If we were to replicate this event through programming, we would run a function that would probably be called unlockDoor() on the event that a key is inserted and turned.

---

* There are numerous different types of events that can happen to an HTML element that triggers the invocation of a JavaScript function, such as:
    * `onClick` : when a user clicks an element
    * `onLoad` : when the webpage finishes loading
    * `onMouseOver` : when a user hovers over an element
    * etc! Resources: https://www.w3schools.com/js/js_events.asp , https://www.w3schools.com/jsref/dom_obj_event.asp

---

* `onClick` is the main event we will focus on. 
* `onClick` is an HTML attribute that runs a specified JavaScript function whenever the element is clicked. 
* You may first think of a button when you're thinking of putting this event to use, but the onClick event can be applied to any HTML element. 

---

* The onClick attribute allows us to execute a JavaScript function when the element with the attribute is clicked. The onClick attribute logically works with buttons, but any element can be given an onClick attribute that executes a function, including a paragraph or image.
* We have already coded the onClick attribute in our HTML on the button element, so now we need to declare the eraseContent() function. This function does not need to take any parameters.

---

[see codepen for longer code examples](..)

---

# Exercises

[back](..)