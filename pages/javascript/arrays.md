---
title: JavaScript arrays
layout: intro
---

# JavaScript Arrays
Storing javascript things in arrays


---
title: JavaScript
level: 2
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
level: 2
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
level: 2
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
level: 2
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
level: 2
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
level: 2
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
level: 2
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
level: 2
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
level: 2
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
