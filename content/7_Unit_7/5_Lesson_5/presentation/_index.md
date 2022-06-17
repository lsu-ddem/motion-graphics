---
title: JSON and HTML
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# JSON Data Scraping / HTML  

---

* So far we've had tons of practice obtaining JSON data using XMLHTTPRequests or Fetch API, and applying the data we received to real life scenarios,
* Such as when we found all of the subdivisions under a specific number of lots in the last section, or determined which street was safest according to crime data.
* We're going to continue putting JSON to use for real life scenarios, however now we want to start displaying the data we obtain and calculate in a more practical way.

---

* Up until this point we've only printed our results and calculations to the console
* Now we're going to begin inserting the data we retrieve and work with into HTML to get a better visual representation of the data,
* and to display the data in a way that is useful and provides information to us or someone else.

---

* When you take raw data in the form that we've been working with, for example the large set of data containing crime reports, and present it in a way that provides insight or context regarding the data, you transform the data into information. 
* This is a basic principle of statistics. In short, data and information are different. 

---

* **Data** - facts or figures from which conclusions can be drawn
* **Information** - data that has been classified/organized/recorded/interpreted in a manner such that meaning of the data emerges.
* This is essentially what we are achieving by presenting the data we work with visually using HTML to present a clear meaning of the data.

---

* First we'll cover a simple example inserting JSON data we retrieved from an outside source into our HTML:
* Lets create an HTML element for our data to be contained within. If you go to the HTML tab, you'll see an H1 holding the text ' New Residential Buildings in 2019'
* followed by an empty h2 with the class "blank". We want to store the number of new residential buildings built in Baton Rouge in 2019 in this h2.

---

* First we'll declare a variable, fillInTheBlank, to store the h2 element so that we can update its contents with the JSON data in the function of our fetch
* Next we'll have to actually obtain the number of new buildings, which we can achieve by creating a new fetch to the JSON data provided by Open Data BR:
 
---

```js
let fillInTheBlank = document.querySelector(".blank");
// visit the json data provided by open data BR and 
// interpret the data being provided
// each JSON object is a new building. Each building contains 
// information regarding the date their permits were issued to 
// build, and the number of permits required to build it.
fetch("https://data.brla.gov/resource/rd5e-2zhz.json")
  // parsing the promise output into JSON
  .then(res => res.json())
  .then((output) => {
    // the variable newBuildings is going to store the total number 
    // of residential buildings built in 2019
    let newBuildings = 0;
    for (let i = 0; i < output.length; i++) {
      // for each object in the JSON data, if the first 4 characters
      // of the date value match 2019, the counter increases because 
      // it was/will be built in 2019
      if (output[i].issueddate.substring(0, 4) == "2019")
        newBuildings++;
    }
    // after the loop finishes iterating through the data, we update
    //  the content of the h2 element to be the total number of new 
    // buildings in 2019
    // this value will update and be shown on the rendered web page 
    // in the result pane
    fillInTheBlank.innerHTML = newBuildings + " new buildings";
  })
```

---

* Now that we've seen how to insert JSON data into HTML, we can do more complex things:
* If you were to show someone the json data representing the residential buildings per year (https://data.brla.gov/resource/rd5e-2zhz.json) without any context whatsoever,
* not even saying "hey this is data about residential buildings", just showing them the JSON data and nothing else, they'd probably be completely lost, right?

---

* However, if you organized the data in a way that allows them to understand the data and what it means and represents, they would be easily informed just by looking at your organization of the data.
* We'll practice the method of turning data into information by populating a table with the JSON data to provide information about the number of new residential buildings in Baton Rouge per year, from 2014 to 2019.

---

* First lets remove the h2 we worked with earlier and update the title (in the h1) to be "New Residential Buildings in Baton Rouge 2014 - 2019"

```js
let title = document.querySelector("h1");
title.innerHTML = " 🏘 New Residential Buildings in Baton Rouge 2014 - 2019";
// now we'll remove the h2 from the page 
fillInTheBlank.style.display = "none";
```

---

* Now that the title is updated and we've removed the h2, we're ready to get started with our table!
* First we'll create the empty table in our HTML
* If you look in the HTML pane, you will see that we created a table with the class "container", and established the 4 table headers that indicate what the columns of the table represe

---

* As you can see, the table contains 4 columns. One for the Year, Number of new buildings that year, total number of permits obtained that year, and the average number of permits per buildin
* Each row we insert into the table from our JS code will represent a year from the dataset, from 2014 to 20
* We created the table body, but the rest of the creation of the table will be handled in our JavaScript code rather than our HTML.

---

* The function handling the JSON data and inserting it into our HTML is longer than functions we've placed within our fetch before, 
* so in this case, we've passed the function called 'calculate' into our second .then() method,
* which passes the output of the promise from the fetch request that was parsed into JSON into the calculate function

---

```js
fetch("https://data.brla.gov/resource/rd5e-2zhz.json")
  // parsing the promise output into JSON:
  .then(res => res.json())
  // passing the parsed JSON data into the calculate function:
  .then(calculate)
```

---

## the calculate function
* based on the table headers we've already established, we know we need to extract or calculate data for the following:
* year, number of buildings per year, and number of permits per year
* the average number of permits per building can be calculated using the two values we extract from the JSON data

---

[go see the calculate function](..)

---

# Excercise 

[back](..)