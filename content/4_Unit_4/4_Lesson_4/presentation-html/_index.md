---
title: HTML Overview
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# overview of HTML

---

* This will not be too detailed of an overview of HTML, as we are only discussing its use with JavaScript and invoking JavaScript functions.  
* HTML stands for Hyper Text Markup Language 
* HTML allows us to create our own websites by writing code in a way that can be read by a browser and translated into the images and designs you see on web pages. 

---

* All text, images, etc. present on a website are there because they were coded into the website's HTML. 
* Good websites make use of at least 3 languages: HTML for structure, CSS for design, and JavaScript for interactability/making web pages dynamic. 
* HTML is responsible for laying out the structure of the site. 

---

* An actual HTML file contains the following lines of code that you won't see present in HTML code on codepen, and that is because codepen allows us to begin at the body tag of the HTML: 

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>My First Heading</h1>
    <p>My first paragraph.</p>
  </body>
</html>
```

---
* If you were to copy the previous code, open up a txt file on your computer, paste the code into the text file and save the file as "index.html", you will be able to double click the file and open it in a web browser, where you will see the two sentences "My First Heading" and "My first paragraph.". 
 * Codepen makes this task easier by rendering our HTML in the white space below. 

---

* Once we add our first element, you will see it display in the white space. 

* This white space is the equivalent to a website, what you would see when you opened this HTML file.

* You don't need to concern yourself with memorizing or being able to completely understand, or even reproduce that sample code. 


---


* Content is placed onto a web page by placing elements within the page's HTML. 
* There are a variety of elements with different uses, such as headings, paragraphs, sections, images, videos, tables, etc. all with their own unique start and end tags. 
* All HTML elements begin with a start tag and end with an end tag. 
* Any content that the element will hold goes between these two tags. 

---

* A start tag consists of the element's tagname, wrapped in carats <___> , while an end tag has a forward slash before the tagname </___>, as you can see on the body element: <body> </body> . 
* Most often, an element's tag name will be predictable, such as the body element's tagname simply being 'body'. 
* However, some elements' tagnames are shortened, such as heading 1, heading 2, heading 3, heading 4, and heading 5 simply being reduced to h1, h2, h3, h4, and h5. 

---

* You can check that you are using the correct tagname for an element simply by googling "HTML 5 __(element)__ tagname"
* It is important to always remember to include a closing/end tag for an element at the correct position. 
* HTML elements can be nested within each other, so misplacing or forgetting an ending tag can cause errors in the format and appearance of your website, with elements accidentally being placed inside of one another or ending up in the wrong place entirely. 

---


*  The first element we will dissect is the body element. 

  * The body element contains all of the content that is visible on the web page. 

  * All of the content containing paragraphs, text, images, etc. are placed within elements that are all nested within the start and end body tag. 

  * Anything placed outside of the body element will not be visibly rendered on the page, so it is important to make sure all of your content is within the body tags. 


---

* The next line of code contains our body's start tag. 
     * Any content we want to display on our web page will be placed before the body's end tag. 
     * These elements will be nested within the body tag. 
     * To keep our code organized and so that the nesting is easy to see, we will indent each element's starting tag within the body element. 
     * If an element within the body also has nested elements, these elements will have two indentions 
     * (you can consider 1 tab = 1 indention, or 4 spaces = 1 indentation)   

---

```html
<body>
  <div id="textArea"> 
    <p class = "field1">
      This paragraph is in the first div and has the class "field1".
    </p>
    <p class = "field2">
      This paragraph is in the first div and has the class "field2".
    </p>
  </div>
  <div id="blankArea"> 
    <p class = "field1">
      This paragraph is in the second div and has the class "field1"
    </p>
    <p class = "field2">
      This paragraph is in the second div and has the class "field2"
    </p>
  </div>
  ...
```

---
* Above there are 2 div elements. A div is an element used to specify a division or section on our web page.
    * Within the div element's start tag, you can see the id attribute.
    * HTML elements can be given attributes in their start tag that can be used in HTML, CSS, and JavaScript.
    * There are a number of different attributes we can give HTML elements, from style attributes, event attributes, identifier attributes, etc. 
    * The id attribute is how we will be able to access the HTML element from our JavaScript code.

---  

* We do not need to go in depth into editing HTML with JavaScript, but we do need to be familiar with two main concepts.
  * Attributes, and
  * querySelector

---

* Any attribute of an HTML element can be retrieved using JavaScript. 
* We can also manipulate attributes of an HTML element via Javascript, but first we have to select the HTML element *through* JavaScript.
* The attribute on our div's start tag, the id attribute, is an identifier. We use the id attribute to give our element a unique name that will be used to call upon that element and select it for editing or manipulation in CSS or JavaScript. 

---

* We use the id attribute to select the element by using the HTML Dom methods.
* We have already discussed JavaScript objects and using their methods. HTML Dom methods are used in JavaScript to select and edit elements from within JavaScript.

---


* There are a few different methods we can use:
* `document.querySelector("")`
  * querySelector() is used to access the first element matching the attribute provided within the quotations. 
  * The attribute within the quotations must be a CSS selector. A CSS selector literally lets us *select* the element we want to work with.
  * There are a number of CSS selectors, which can be found here: https://www.w3schools.com/cssref/css_selectors.asp
  * We are going to focus on using querySelector with the` element, ID, and Class attributes` 

---

* `Element`: in our JavaScript code, we would access the div from line 44 by saying 

```js
var textArea = document.querySelector("div");
```

* this would make the variable textArea reference the first div element in the HTML. If there were another div after the first, the textArea variable would only reference the first div.
* we use 'document' so that we can access the methods associated with the JavaScript document object, such as `.querySelector("")`

---

* `ID`: in our JavaScript code, we would access the div from line 44 by its ID attribute, by saying:

```js
var textArea = document.querySelector("#textArea");
```

* this would make the variable textArea reference the div element in the HTML with the id "textArea". Even if there were divs before or after that div, only the textArea div is referenced.
* The ID attribute is used to single out and give an element an explicitly unique identifier.

---

* `Class`: in our JavaScript code, we would access the paragraphs from both line 45 and 49 by their class attribute, by saying:

```js
var textArea = document.querySelector(".field1");
```

* this would make the variable textArea reference ALL paragraph elements with the class attribute "field1", so both of the paragraphs with the class field1 in both divs will be selected.
* The class attribute is used to apply the same code to multiple elements at once, unlike the id attribute which ensures only one element is being edited.

---
       
[html exercise](..)