---
title: JavaScript functions
layout: intro
---

# JavaScript Functions
Defining functions


---
title: JavaScript
level: 2
---

# We often want to repeat procedures
Functions

* Functions consist of three items:
* The function keyword and the name of the function
* The parameters that are passed into the function, seperated by commas
* The code block that executes enclosed in curly braces

```js

function canVisitVegas(age) {
    let allowed = null; 
    
    if (age >= 21) {
        allowed = true;
    } else {
        allowed = false; 
    }
    return allowed
}

console.log(canVisitVegas(25)); // true

```


---
title: JavaScript
level: 2
---

# Local variables
Functions

* Function variables are "scoped", so local variables won't be available outside the function 
* In the example below, when we try to read `allowed` JavaScript will throw an error

```js

function canVisitVegas(age) {
  let allowed = null; 
    
  if (age >= 21) {
    allowed = true;
  } else {
    allowed = false; 
  }
  return allowed
}

console.log(allowed); // Error!

```



---
title: JavaScript
level: 2
---

# Outer variables
Functions

* Variables declared outside of a function (in the direct parent) are made available to the function 
* In the example below, 

```js

let age = 21;

function canVisitVegas() {
    let allowed = null;
    
    if (age >= 21) {
        
        allowed = true;
    } else {
        allowed = false; 
    }
    return allowed
}

console.log(canVisitVegas()); // true!

```



---
title: JavaScript
level: 2
class: "border-l-36 border-green-600"
---

# Now you try! 
Basics

* Open your JavaScript file and copy this code 
* There is an outer variable called `age` (21) and an inner variable called `age` (16)
* Try to guess which `age` variable will be used and what the output will be in the console

```js
let age = 21;

function canVisitVegas() {
  let age = 16
  let allowed = null;

  if (age >= 21) {
    allowed = true;
  } else {
    allowed = false; 
  }
  return allowed
}

console.log(canVisitVegas()); // ????
```



---
title: JavaScript
level: 2
---

# A word about Global Variables
Functions

* Variables declared outside of a function are called "global" variables and given a global scope 
* This means that they are visible from any function, which is considered bad practice 
* Now that you know this, a much better practice is to put all of your logic and variables inside a function 

