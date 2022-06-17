---
title: READING JSON WITH FETCH API
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Reading JSON with Fetch API  

---

* In the last section we covered how to read JSON data from an online source using an XMLHTTPRequest
* Fortunately, there exists a much more convenient JavaScript API to achieve the same goal, Fetch API
* Fetch API is essentially a more powerful and flexible version of what XMLHTTPRequests does

---

* As the name entails, Fetch API provides an interface for 'fetching' resources 
* The fetch method has a single mandatory parameter, which is the URL of the resource we want to access or 'fetch'
* The fetch method returns something called a Promise, which is the response of the request we sent (whether or not it was successful)

---

* A Promise also contains various information about the request and response, such as headers and the HTTP status, but we won't be concerned with this data for now
* After the response is retrieved, we can specify what the code should do by programming the .then() method, which is much like programming the .onload function for an XMLHTTPRequest.

---

* Before we can program what we want to do with the data returned, we have to actually extract the data from the Promise we recieve back
* To extract the content from the HTTP Response, we format the response of the fetch to a specified type, as we were required to do when we were using an XMLHTTPRequest.
* After extracting the data from the response, we use the then() method to achieve multiple things, whereas we had to use different methods when working with XMLHTTPRequests.

---

* When working with XMLHTTPRequests, we had to specify the response type after declaring a new XMLHTTPRequest, which we set to json (red.responseType = 'json';)
* Then we used the .onload() method to write a function that told our program what we wanted to do with the JSON data we got back from the request.
* Fetch API uses the same method to achieve both of these tasks.
The .then() method is used in Fetch API to specify the response type of the promise, and also to program what we want to do with the data

---

* To format the data we get back into a specific data type, the then() method takes the response of the fetch (which is a promise) as a parameter, 
and passes the promise it into a function which extracts the data (removing the extra information such as headers, http status, etc) and parses it into the * specified data type
* Data can be extracted from a promise and returned in the following formats: 
* .arrayBuffer() , .blob() , .json() , .text() , and .formData() 

---

* Since we're working with JSON, we can specify that we want the data transformed into JSON like so:
* we'll use our simple library JSON data from the sections before to walk through our first fetch example, then we'll practice with larger data sets:

---

```js
fetch('https://api.myjson.com/bins/12j3gg?')
  // remember that the first step is using the fetch method to 
  // 'fetch' the url we want to access.
  // remember we will implement the .then() twice: once to 
  // specify the return type of the data, to format it into 
  // JSON, and the second time to program what we want to do 
  // with the formatted data our first .then() method contains 
  // a shorthand JavaScript function that parses the response into JSON
  .then(res => res.json())

  // The next then() method is where we actually work with the JSON data we extracted. 
  // The second .then() takes the response of the first then method as a parameter
  // Here we can do whatever we please with the JSON data, such as printing it 
  // to the console, saving it to arrays or variables, displaying it in HTML, etc.
  .then((out) => {
    // This is another arrow function, it is the exact equivalent of saying .then(function(out){ })
    // Here we're simply saying to print the output of the response that was parsed into JSON to the console
    console.log('Output: ', out);
    // If you look at the console, you'll see that our entire myLibrary object was printed to the console as a JSON object
  }).catch(err => console.error(err));
```

---

* this shorthand function:  

```js
.then(res => res.json()) 
```

* is the exact same as the longer version below:

```js
.then(function(res){
        return res.json();
}
```

---

* example with no comments

```js
fetch('https://api.myjson.com/bins/12j3gg?')
  .then(res => res.json())
  .then((out) => {
    console.log('Output: ', out);
  }).catch(err => console.error(err));
```

---

* Just like that, we've obtained and printed our JSON library using Fetch API within just 5 short lines
* Fetch API can be more convenient and easier to use than XMLHTTPRequests.
* Unfortunately, like all good things, Internet Explorer is behind on updating their browser to support Fetch API.

---

* So in the event that you're implementing Fetch API in a scenario where old people are using Internet Explorer, its better to default to using XMLHTTPRequests
* Now lets look at working with the data we get in return in more detail than just printing the entire JSON to the console 
*  Lets write a script to print the titles of all of the books within our library and the authors name in this format: 'Title by Author' :

---

```js
fetch('https://api.myjson.com/bins/12j3gg?')
  .then(res => res.json())
  .then(out => {
    // Each line before this one should be familiar to you;
    // line 89 fetches the JSON data storing our library
    // line 90 parses the response object into JSON
    // and finally line 91 creates a shorthand function for the response from the fetch, 
    // The next few lines are the contents of the function handling the JSON data parsed from the response from the fetch
    console.log("Books in my Library:");
    // this for loop loops through the object within the myLibrary object (remember that there are multiple objects within the myLibrary object to represent our books)
    for (let i = 0; i < out.myLibrary.length; i++) {
      // the loop iterates as many times as there are objects(aka for as many books as there are) within myLibrary by setting the condition to the length of the myLibrary object
      console.log(out.myLibrary[i].title + " by " 
        + out.myLibrary[i].author);
      // we then simply print the title and author of each book by accessing the title and author keys of the current object the loop is on using dot notation
    }
  })
```

---
  
* Before we use Fetch API with actual JSON data, lets practice the library scenario with your own JSON data
* First, you'll need to create your own JSON data representing your library of books.
* There are many methods to go about creating a JSON file or hosting the JSON file online
* For example, http://myjson.com/ is convenient to use, but since you already have experience with codepen, you can just store JSON data in a new pen

---

* To store JSON data in a codepen to be used from another script later on, first create a new pen in a new tab
* Next, simply write the JSON data in the JavaScript section of the codepen editor, heres an example : https://codepen.io/lsuddem/pen/pGNzQy
* To reference the JSON data in a Fetch or XMLHTTPRequest, simply set the url parameter to the url of the pen and add '.js' to the end of the link 
* So if the pen storing my library is https://codepen.io/lsuddem/pen/pGNzQy, I can fetch the JSON data by using https://codepen.io/lsuddem/pen/pGNzQy.js as the url

---

## Try it! 
* First create your pen containing the JSON data representing your own library, or just some of your favorite books. 
 * Include at least 5 books, with key:value pairs for their Title, Author, Rating (on scale of 0-5), and anything else you wish to include
* In the space below, create a new fetch using the url to your own JSON data

---

* parse the response from the fetch into JSON and loop through your data, printing it to the console in this format:
 * Books in my library: (or "My favorite books:")
 * Title by Author : i star rating ; where i is the rating you gave the book in the JSON data 

---


* After you've successfully printed your books to the console, lets practice using Fetch API with some real data
* Many web services and APIs often use JSON to format data that is available to the public. 
* For example, many local governments are working towards transparency by providing easily accessible data to the public in the form of open data websites, such as https://data.brla.gov/

---
  
* According to Forbes, as of 2019 there are over 90 cities with such open data portals, including Austin, Chicago, Dallas, Las Vegas, NYC, Memphis, etc. : https://www.forbes.com/sites/metabrown/2018/04/29/city-governments-making-public-data-easier-to-get-90-municipal-open-data-portals/#6969d3c5a0d7
* For this section, I'll use Baton Rouge's open data, but it would be good practice to try fetching and manipulating JSON data from other cities' open data portals afterwards
* So far we've become experts at fetching JSON data and printing specific key:value pairs from the response we receive
  
--- 

* Next we'll gain experience working with larger data sets and doing more with the data  
* Let's say you currently live in Baton Rouge, but you're considering moving to another city.
* You really like the food in Baton Rouge, however, so you're reluctant about leaving the city, but the crime in Baton Rouge is a main factor driving you to move elsewhere

---

* Before you look at other cities and their crime statistics, you first decide to do some quick calculations regarding the crime in Baton Rouge
* You visit Baton Rouge's open data resource, https://data.brla.gov, and view the different categories of crime within Public Safety (https://data.brla.gov/Public-Safety/Baton-Rouge-Crime-Incidents/fabb-cnnu)
  
---

* Looking at a visualization of the data, you see that crimes are categorized into 12 main classifications: crimes related to theft, narcoticts, battery, criminal damage to property, vehicle burglary, assault, residential burglary, firearm, non-residential burglary, individual robbery, nuisance, and other 
* Let's say, for whatever reason, the crimes you're most concerned with include residential burglary, firearm, individual robbery, and narcotics. Perhaps you're immune to the other types of crimes, who knows. But these 4 crimes, you just can't stand to be around.

---

* From the large set of crime data provided by data.brla.gov, lets tally each of the crimes recorded pertaining to these 4 specified categories, and print the totals of each type of crime committed in Baton Rouge to the console:
* first we'll create a new fetch to the JSON data representing the record of crimes in Baton Rouge

---

```js
fetch("https://data.brla.gov/resource/5rji-ddnu.json")
  // next we parse the response from the fetch into JSON 
  .then(res => res.json())
  // now we program the counting of each of the 4 types of crimes we're concerned with
  .then((out) => {
    // the next four lines simply declare the variables that will store the totals for each of the types of crimes
    let totalResidentialBurglary = 0;
    let totalFirearm = 0;
    let totalIndivRobbery = 0;
    let totalNarcotics = 0;
    // the for loop on the next line loops through the output of the parsed JSON data
    for (let i = 0; i < out.length; i++) {

      // the next few if statements check if the current object's crime key:value pair matches that of the four types of crimes we're concerned with in this scenario
      // because the data set stores the crime types in capital letters, the types have to be in caps when we check if the crime is equal to any of the four types, because lowercase letters do not equate to capital letters, like so:

      if (out[i].crime == "RESIDENTIAL BURGLARY")
        totalResidentialBurglary++;
      if (out[i].crime == "FIREARM")
        totalFirearm++;
      if (out[i].crime == "INDIVIDUAL ROBBERY")
        totalIndivRobbery++;
      if (out[i].crime == "NARCOTICS")
        totalNarcotics++;
    }
    // now we'll print the tallied counts to the console 
    console.log("Total Residential Burglary Crimes Committed : " + totalResidentialBurglary);
    console.log("Total Firearm Crimes Committed : " + totalFirearm);
    console.log("Total Individual Robbery Crimes Committed : " + totalIndivRobbery);
    console.log("Total Narcotics Crimes Committed : " + totalResidentialBurglary);

    // looking at the console, you can see the totals for each of the categories of crime
  })
```

---

* Lets say that living in Baton Rouge your entire life has made you somewhat unphased when you see the totaled numbers for the four types of crimes, and these results don't necessarily persuade you to move
* You decide, instead, that if the total number of crimes on your street exceeds 30, you'll consider moving to another town
* You live on a street called Government, so in your new fetch you're going to tally all of the crimes that occurred on government street like so:

---

```js
fetch("https://data.brla.gov/resource/5rji-ddnu.json")
  .then(res => res.json())
  .then((out) => {
    let totalCrimeCount = 0;
    for (let i = 0; i < out.length; i++) {
      // the data set inludes a key specifically for the street name (st_name), as well as a key for the entire address
      if (out[i].st_name == "GOVERNMENT")
        totalCrimeCount++;
    }
    console.log("There were " + totalCrimeCount + " crimes documented on government street in 2018 ");
  })
```

---

* Okay, as of now the crime count is only at a mere 14 offenses, so you decide you'll stick around and keep eating southern food for a while longer.
*  Thats the gist of Fetch API!

---

# Excercise 

[back](..)