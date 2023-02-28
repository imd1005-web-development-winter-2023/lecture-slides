---
title: JavaScript
layout: intro
---

# JavaScript
The programming language everyone loves and absolutely hates



---
title: JavaScript
level: 2
---

# How to run JavaScript code
JavaScript basics

Running code in the `head` tag. Meh. 

```html
<html>
  <head>
    ...
    <script>
      /* 
        This is a multiline 
        JavaScript comment 
      */

      // And this is a single line comment
      console.log("Hello World");
    
    </script>
  </head>
  ...
</html
```



---
title: JavaScript
level: 2
---

# How to run JavaScript code
JavaScript basics

Running code in the `body` tag. Better. 

```html
<html>
  ...
  <body>
    ...
    <script>
      /* 
        This is a multiline 
        JavaScript comment 
      */

      // And this is a single line comment
      console.log("Hello World");
    
    </script>
  </body>
</html
```




---
title: JavaScript
level: 2
---

# How to run JavaScript code
JavaScript basics

Running code in the `body` from a seperate `js` file. Best. 

```html
<html>
  ...
  <body>
    ...
    <script src="javascript.js"></script>
  </body>
</html
```




---
title: JavaScript
level: 2
---

# Working with variables
JavaScript basics

There are three ways to declare a variable `var`, `let`, and `const`.

```html
<script>

  /* NEVER USE VAR */ 
  var myFirstVariable = "Hello";

   /* Then we have let */ 
  let mySecondVariable = "World";
  
  /* And finally we have const */ 
  const myConstVariable = true;

</script>
```




---
title: JavaScript
level: 2
---

# Statements
JavaScript basics

A statement is an instruction written in javascript code that the browser interprets and then does a thing. 

**Always put in semi-colons at the end of a line of code**. 

JavaScript is loosely typed and may work without them but you will get unexpected behaviour. 

```html
<script>

  let age = 300;

</script>
```


---
title: JavaScript
level: 2
---

# Code blocks
JavaScript basics

Code blocks are sections of code bound by a `{` and a `}`

**Never put a semi-colon at the end of a code block, they don't need them**. 

```html
<script>

  let age = 300;

  if (age > 50) {
    console.log("Damn that's old");
  }

  /* Note: there isn't a semi-colon at the end of line 7 */

</script>
```

---
title: JavaScript
level: 2
---

# Naming conventions
JavaScript basics

The hardest thing to do in development, apart from everything, is to name your variables. 

There are three different naming conventions `pascal case`, `camel case`, and `snake case`. 

(Note: there is a fourth - `kebab-case` but that doesn't work in JavaScript)

```html
<script>

  // Camel case 
  let numTodoItems = 41;

  // Pascal case 
  let NumTodoItems = 44;

  // Snake case 
  let num_todo_items = 32; 

</script>
```



---
title: JavaScript
layout: center
level: 2
---

# The most important line of code in JavaScript:

```html
<script>

  // This is the border: 1px solid red; of JavaScript 
  console.log(numTodoItems);

</script>
```


---
title: JavaScript
level: 2
---

# Now you try! 
JavaScript basics

* Create an HTML page
* Add a script element to the bottom of the page
* Add the following code to your page 
* Open up the inspector tools in your browser 
* View the console output

```html
<script>

  // Declare a variable
  let message = "Hello World";

  // Console log the contents of the variable 
  console.log(message);

</script>
```



---
title: JavaScript
level: 2
---

# So many Variables 
JavaScript basics

* String 
* Number 
* BigInt
* Boolean
* Null 
* Undefined
* Object 
* Symbol



---
title: JavaScript
level: 2
---

# String
JavaScript basics

String type is used to store textual data, or a sequence of characters.

```html
<script>

  // this is a string 
  // note the quotation marks around the value
  let message = "Hello World";

</script>
```


---
title: JavaScript
level: 2
---

# Number
JavaScript basics

This is the largest numerical value that can be stored in  a `number` 9007199254740991. 

If you think your app will need to store a bigger number, than you should use a `BigInt`.

```html
<script>

  // this is a number
  let numberOfElephants = 9007199254740991;

</script>
```


---
title: JavaScript
level: 2
---

# BigInt
JavaScript basics

This is the largest numerical value that can be stored in  a `number` 9007199254740991. 

If you think your app will need to store a bigger number, than you should use a `BigInt`.

```html
<script>

  // this is how we use a BigInt
  let numberOfElephants = BigInt(9007199254740992);

</script>
```



---
title: JavaScript
level: 2
---

# Boolean
JavaScript basics

Booleans can be set to `true` or `false`. 

```html
<script>

  // this is a boolean
  let isElephantPresent = false;

</script>
```



---
title: JavaScript
level: 2
---

# Null
JavaScript basics

This is an assigned value that means nothing, nada. 

We generally use this value to setup a variable and flag that nothing is set in the variable yet. 

```html
<script>

  // this is a null value
  let numElephants = null;

</script>
```



---
title: JavaScript
level: 2
---

# Undefined
JavaScript basics

This is state of a variable before a value is set to that variable

```html
<script>

  // Whoops - declared a variable but didn't set it to anything
  let numElephants;

  console.log(numElephants); // this will return undefined 

</script>
```



---
title: JavaScript
level: 2
---

# Objects
JavaScript basics

Objects in JavaScript are a basic building block and almost everything in JavaScript is an object.

We generally use objects to collect a bunch of data and keep it together. 

The following is a really simple example of an object, though they can get very complex. 

```html
<script>

  // Declare an empty object
  const elephant = {
    name: "Jimbo",
    age: 200,
    isMarried: false,
  };

  // Access a property using the dot notation
  console.log(elephant.name)

</script>
```


---
title: JavaScript
level: 2
---

# Now you try! 
JavaScript basics

* In the page you had open before 
* Type this code in to your page and check out the console messages

```html
<script>

  // Declare an age variable 
  let wage = 33; 

  // Declare another value 
  let bonus = 22;

  // Manipulate the age by adding 10 to it 
  wage = wage + bonus; 

  // Console log the contents of the variable 
  console.log("The updated wage is set to", wage);

</script>
```


---
title: JavaScript
level: 2
---

# Now you try! 
JavaScript basics

* In the page you had open before 
* Let's try adding two strings together
* Type this code in to your page and check out the console messages

```html
<script>

  // Declare the start of message
  let beginMessage = "Hello how are"; 

  // Declare the end of the message
  let endMessage = "you doing?";

  // Add both of the strings and display using the console log
  console.log(beginMessage + endMessage);

  // How would you add a space to seperate the two messages?

</script>
```


---
title: JavaScript
level: 2
---

# Now you try! 
JavaScript basics

* In the page you had open before 
* Define a `const` called `boilingPoint` and set it to `100`
* 
* Type this code in to your page and check out the console messages

```html
<script>

  // Declare a const and set it to 100

  // Try to assign the const a new value
  boilingPoint = 105;
 
  // Add both of the strings and display using the console log
  console.log("The boiling point is:" , boilingPoint);

</script>
```


---
title: JavaScript
---

# Now you try! 
JavaScript basics

* Okay this one is sneaky
* In the page you had open before 
* Define a `string` called `quote`
* Set the value of the string to be `You had me at "Hello"` (note the included double quotation marks)
* Console log the `quote` variable

```html
<script>

  // Declare a const and set it to - You had me at "Hello"
  const quote = ; // ADD CODE HERE
 
  // Add then display using the console log
  console.log(quote);

</script>
```



---
title: JavaScript
---

# Now you try! 
JavaScript basics

* Let's practice using a simple object
* Create an object named `product` 
* Add the following properties to the object 
  * `price` set to `4.99`
  * `name` set to `Nacho Cheese Doritos`
  * `isInStock` set to `true`
* Console log the `product` variable

```html
<script>

  // Declare a const and set it to - You had me at "Hello"
  const product = {}; // ADD CODE HERE
 
  // Add then display using the console log
  console.log(product);

</script>
```


---
title: JavaScript
---

# Template literals 

Backticks can help us do awesome things with strings

```html
<script>

  // Declare a const called price and set it
  const price = 4.99; 

  // Declare a const called quantity and set it
  const quantity = 7 
 
  // Add then display using the console log
  console.log(`You can buy ${quantity} elephants for ${price * quantity}`);

</script>
```



---
title: JavaScript
---

# Now you try! 
JavaScript basics

* Let's practice using a template literal 
* I've created three variables that you will need to reference
* Using template literals and the console log, display the following by referencing the three variables 
* `My phone number is (613) 825-6849`

```html
<script>

  // Declare some attributes 
  let areaCode = 613;
  let telephonePrefix = 825;
  let lineNumber = 6849;
 
  // Use a string template literal 
  // to display: "My phone number is (613) 825-6849"
  console.log(`ADD_YOUR_CODE_HERE`);

</script>
```




---
title: JavaScript
---

# Arrays in JavaScript
JavaScript basics

* Up until now we've seen primitive data types dealing with single values
* Arrays are collection objects where we can put a bunch of items into an array

```html
<script>

  // Declare an empty array 
  let myEmptyArray = [];

  // Declare an array with some values 
  let myFavouriteColoursArray = ["purple", "blue", "hotpink", "green", "yellow"];

  // Declare an array of a bunch of things
  let myMixedArray = ["blue", 55, false, "green"];
 
  // Output the arrays 
  console.log(myEmptyArray);
  console.log(myFavouriteColoursArray);
  console.log(myMixedArray);

</script>
```


---
title: JavaScript
---

# Arrays in JavaScript
JavaScript basics

* You can also use the `new Array()` and `Array()` function declerations to create arrays, though I would skip using them. 

```html
<script>

  // Declare an empty array 
  let myEmptyArray = new Array(); // the same as []

  // Declare an array with some values 
  let myFavouriteColoursArray = new Array("purple", "blue", "hotpink", "green", "yellow");

  // Declare an array of a bunch of things
  let myMixedArray = Array("blue", 55, false, "green");
 
  // Output the arrays 
  console.log(myEmptyArray);
  console.log(myFavouriteColoursArray);
  console.log(myMixedArray);

</script>
```



---
title: JavaScript
---

# Array Index
JavaScript basics

* Every item in an array is indexed
* The index counting starts at 0 (zero)
* This means that the first item is at index 0, the second item is at index 1, and so on

```html
<script>

  // Declare an array with some values 
  let myFavouriteColoursArray = ["purple", "blue", "hotpink", "green", "yellow"];
 
  // Output the arrays 
  console.log(myFavouriteColoursArray[0]);
  console.log(myFavouriteColoursArray[1]);
  console.log(myFavouriteColoursArray[2]);
  console.log(myFavouriteColoursArray[3]);
  console.log(myFavouriteColoursArray[4]);

</script>
```



---
title: JavaScript
---

# Now you try! 
JavaScript basics

* Add seven (7) numbers to the `myLotteryNumbers` array
* Run the code and see what the output

```html
<script>

  // Declare an array with your seven values
  let myLotteryNumbers = []; // ADD CODE HERE
 
  // Output the array
  console.log('The winning numbers are ', myLotteryNumbers);

</script>
```


---
title: JavaScript
---

# Now you try! 
JavaScript basics

* Continuing from where you left off, you should have 7 numbers in an array
* Add `10` to the first value in the array 
* Add `100` to the last value in the array 
* Multiply by `* 3` the third value in the array 
* Run the code and see what the output is

```html
<script>
  // Declare an array with your seven values
  let myLotteryNumbers = [];

  // Modify the first value in the array by adding 10 to it
  // Modify the last value in the array by adding 100 to it 
  // Modify the third value in the array by multiply it by 3
 
  // Output the array
  console.log('The modified numbers are ', myLotteryNumbers);
</script>
```



---
title: JavaScript
---

# Our first peak into properties and methods
JavaScript basics

* Since an `array` is a JavaScript Object, it comes with a number of `properties` and `methods` that we can use 
* For example, we can use the `push()` method to add items to an array

```html
<script>

  // Declare an empty array 
  let myFavouriteColours = [];

  myFavouriteColours.push("purple");

  myFavouriteColours.push("green");

  // Output the array
  console.log('The modified numbers are ', myLotteryNumbers);

</script>
```



---
title: JavaScript
---

# Our first peak into properties and methods
JavaScript basics

* We can also use the `.length` property to tell us how many items are in the array

```html
<script>

  // Declare an empty array 
  let myFavouriteColours = [];

  myFavouriteColours.push("purple");
  myFavouriteColours.push("green");

  // Output the array
  console.log('The amount of items in the array are ', myFavouriteColours.length);

</script>
```



---
title: JavaScript
---

# Const and arrays
JavaScript basics

* We can set an `array` as a `const` variable and JavaScript will allow us to change the items inside the array but JavaScript won't let reassign the variable.

```html
<script>

  // Declare const array
  const myFavouriteColours = ["purple", "green", "blue"];

  // Adding an item works
  myFavouriteColours.push("gold");
  
  // Output the array
  console.log('The amount of items in the array are now ', myFavouriteColours.length);

  myFavouriteColours = ["hotpink", "orange"]; // This won't work

</script>
```



---
title: JavaScript
---

# There's also a reverse method 
JavaScript basics

* We can use the `reverse` method to reverse the order of the items in the array

```html
<script>

  // Declare const array
  const myLotteryNumbers = [1, 22, 34, 56, 83, 59, 23];

  // Output the array
  console.log("Original: ", myLotteryNumbers);

  // Reverse method
  myLotteryNumbers.reverse();
  
  // Output the array
  console.log("After reverse: ", myLotteryNumbers);

</script>
```
