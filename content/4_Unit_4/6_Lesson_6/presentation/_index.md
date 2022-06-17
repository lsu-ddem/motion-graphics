---
title: Writing Methods
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Writing Methods

---

* As mentioned earlier, objects can have methods that we can invoke to perform some kind of function or action on the object
* Methods are stored as an object property, but are programmed by defining a new function to assign the property to
* To look at a few examples, we will use the employee object below:
  
---

* The employee object will represent an employee of our imaginary company, Katie Johnson. 
* This object stores the information for employee Katie Johnson, with properties for her name, ID, phone number, address, hourly wage, and number of hours worked this week.
* The last property of the employee object will be the method called "printEmployeeInfo"

---
  
* The printEmployeeInfo method declares a new function that returns the employee ID and full name in a formatted order
* You'll notice that the method uses a new keyword we haven't worked with yet, "this"
* When used in an object method, the 'this' keyword refers to the object in context. 
* On line 30, this.firstName is equivalent to saying employee.firstName:

---

```js
let employee = {
  firstName: "Katie",
  lastName: "Johnson",
  employeeID: 295025,
  phone: 4560001234,
  address: "42 Wallaby Way",
  wage: 13.50,
  hoursWorked: 25,
  printEmployeeInfo: function () {
    return "Employee #" + this.employeeID + " : " + this.firstName + " " + this.lastName;
  }
};

console.log(employee.printEmployeeInfo());
```

---
   
* Next, lets add a method to the employee object that calculates their weekly pay
* This method will be called "paycheck" and will return the product of the employee object's wage property and the employee object's hoursWorked property:

```js
employee.paycheck = function () {
  return "$" + (this.wage * this.hoursWorked);
}
```

---

* Now, we can invoke the paycheck method like so:

```js
let income = employee.paycheck();
console.log(income);
```

* or: 

```js
console.log("Employee #" + employee.employeeID + " worked " 
  + employee.hoursWorked + " hours this week and earned " 
  + employee.paycheck());
```

---

* Try updating the hoursWorked property to a number greater than 25, and invoking the paycheck method again:

```js
employee.hoursWorked = 40;
console.log("Employee #" + employee.employeeID + " worked " +
  employee.hoursWorked + " hours this week and earned " + 
  employee.paycheck());
```

* Finally, lets write an employee contact information method.
  
---

* The method will be named "contact" and will print the information to the console in this order: 
* Employee #ID - Last Name, First Name , Phone: (###)-###-#### , Address: __________

```js
employee.contact = function () {
  return "Employee #" + this.employeeID + " - " + this.lastName + 
  ", " + this.firstName + " , Phone: (" + 
  this.phone.toString().slice(0, 3) + ")-" + this.phone.toString().slice(3, 6) + 
  "-" + this.phone.toString().slice(6, 10) + " , Address: " + this.address;
}
console.log(employee.contact());
```

---

# Exercises

[back](..)