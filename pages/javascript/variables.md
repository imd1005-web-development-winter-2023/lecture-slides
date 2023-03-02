---
title: JavaScript variables
layout: intro
---

# JavaScript Variables
Learning about primitives, object literals, and variables

---
title: JavaScript
level: 2
---

# Working with variables
Variables

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

# So many Variables 
Variables

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
Variables

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
JavaScript variables

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
Variables

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
Variables

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
Variables

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
Variables

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
Variables

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
Variables

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
Variables

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
Variables

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
level: 2
---

# Now you try! 
Variables

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
level: 2
---

# Now you try! 
Variables

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
level: 2
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
level: 2
---

# Now you try! 
Variables

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

