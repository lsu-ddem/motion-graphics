---
title: READING JSON WITH XMLHTTPREQUEST
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Reading JSON with XMLHTTPRequests 

---

# JSON files 

* JSON can be much more complex than what we've seen so far, handling 100s of objects
* now we will use JSON files instead of JSON objects written into our JS code 
* .json files wrap the entirety of the JSON content within a pair of curly brackets { } as you will see
* .json files also almost always contain multiple objects, but the syntax for this is something we've already seen, so don't get intimidated.
  
---

# JSON files 

* why store everything in one file? 
  * JSON is extremely useful for presenting data in an organized, clean format that is easy for both humans and machines to read
  
---
# Example 

* books in our personal library 
  * Instead of having 30 or so individual variables storing the data, we can organize the data in a JSON file by placing them within an array
  *  Each element of the array is a JSON object itself, and the elements are separated by commas, just like a JavaScript array
* notice the square and curly brackets 
  
---

# Example 

* Example of using JSON to organize a personal library: https://api.myjson.com/bins/12j3gg?pretty=1
* You can see the data organized in an easily readable format, representing our library of 3 books
* We can now bring this file into our projects using XMLHTTPRequest

---

# XMLHTTPRequest

* XMLHTTPRequest ( XHR for short ) is an API in the form of an object.
* XHR objects are used to communicate back and forth with servers. 
* XML(which is a language) is in the name, but XMLHTTPRequests can be used with any language, which is why we can use them when working with JSON files
  
--- 

# XMLHTTPRequest

* declare a new variable and set it equal to XMLHTTPRequest()  
* declare a JavaScript constant variable storing the URL of our JSON data 

```  
const url = "https://api.myjson.com/bins/12j3gg?pretty=1";
```
---

* Next we declare another constant named 'request' which creates a new XMLHttpRequest object

```
const request = new XMLHttpRequest();
```

* The line above, the declaration of the request constant, created a new XMLHttpRequest object.
* The XMLHttpRequest object allows us to easily request data from a server
    
---

* Next we'll specify the response type of our request by using the responseType method, of which the default response type is text:

```js
request.responseType = 'json';
// Now our response type is set to JSON.
```

* now we try to submit the request
* The HttpRequest is literally a request to a server
  * our browser asking another machine somewhere else in the world for something.
  * Whether that something is getting data, sending data, etc. 

---

# HTTP Methods 

*  GET
   *  Requests using GET as the method should only retrieve data 
* POST 
  * Requests using POST as the method are **sending** information to that location, either new or updated information
  * The sending and reception of the information often causes a change in state on the server
    
--- 

* PUT
  * Requests using PUT as the method are sending information to a location, but this information completely replaces what information was held prior
  * In other words, PUT can be used to update information already being shared/stored, but it can also be used to store new information

* DELETE
  * Requests using DELETE as the method are deleting the specified resource


---

* The other 5 HTTP methods include HEAD, CONNECT, and TRACE, OPTIONS, and PATCH which you caread about here: 
  * https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods
      

---
# Open 

* Next, we need to open the XMLHTTPRequest object we created by using the .open() method, and specifying which HTTP Request method we want to use:

```js
request.open('GET', url, true);
```

* The .open() method initializes a new or existing request
   
---

* The method takes up to 5 parameters, and as little as 2 parameters.
* The 2 parameters required no matter what include the HTTP Request method type wrapped in quotation marks, and the url of the JSON data:

```   
XMLHttpRequest.open(method, url)
```

---

* The 3rd optional parameter is a boolean that defaults to **true**, which specifies whether or not to execute the operation asynchronously. 
* The async parameter defaults to true because sending the request asynchronously allows for our JavaScript code to continue working;
* Instead of having to wait for a response from the server, the JS code can continue to execute other scripts while waiting, and handle the response some time after the response is ready to be handled

---

* Setting this parameter to false would send the request synchronously, forcing us to wait for a response to gain back control and continue executing scripts or working
* The 4th and 5th optional parameters are for a user and password, which are used for authentification, but again are optional.
  
---

# Onload 

* onload method is called when an XMLHTTPRequest transaction is successfully completed
* The method is set equal to a function that will be executed when the request is completed successfully
* Within the function, we tell our code what to do with the data we get back from the request, which is stored in request.response

---
# onload example

```js
request.onload = function () {
    // first we want to check that the response to the request 
    // is ready for us to work with the data it returned
    // We do this by checking if the status of the request 
    // is equal to 200, which is the ready status like so:
    if (request.status == 200){
      // if the response is ready for us to work with, the following code will execute:
      let jsonData = request.response; // this line stores the JSON data from the response to local variable
      console.log(jsonData);
    }
  //close the if statement and the function curly brackets
  };
// Finally, we send the request off by using the .send method() : 
request.send();
```

* now check out the console! 
  
---

# Full Example

[codepen](https://codepen.io/lsuddem/pen/zVajgB?editors=0010)

---

# Excercise 

[back](..)