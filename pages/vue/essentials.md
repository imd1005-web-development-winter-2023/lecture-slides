---
title: Vue.JS essentials
layout: intro
---

# Vue.JS essentials
The Progressive JavaScript Framework


---
title: Vue.JS essentials
level: 2
layout: two-cols-header
---

# Learning Vue.JS 
Vue.JS essentials

::left::

* Getting Started
* Creating reactive variables
* Declarative Rendering
* Attribute binding
* Conditional rendering
* List rendering 
* Event handling

::right::


* Class and style binding
* Computed property
* Watchers
* Components
* Props
* Emits


<!-- 

    Slide notes: 

-->


---
title: Vue.JS essentials
level: 2
---

# Getting Started
Vue.JS essentials

We need to setup a project with an HTML, CSS, and JavaScript file. 

HTML head: 

```html
<!-- Add the following script to the head -->
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
```

HTML body:

```html
<!-- Add the following to the body -->
<body>
    <!-- Vue.JS app boundary -->
    <div id="app">

    </div>
    <script src="./main.js"></script>
</body>
```

<!-- 

    Slide notes: 

-->



---
title: Vue.JS essentials
level: 2
---

# Getting Started
Vue.JS essentials

We now add our Vue.JS code that declares and mounts our app. As long as we don't have any console log errors we should be ready to code our Vue.JS app.

JavaScript: 

```js
// Get an instance of the createApp Vue object
const { createApp, ref } = Vue;

// This is where our app logic will go - in the createApp method
const app = createApp({
  setup() {
    
  },
});

// Finally, we mount our app to our web page
app.mount("#app");
```


<!-- 

    Slide notes: 

-->


---
title: Vue.JS essentials
level: 2
---

# Creating reactive variables
Vue.JS essentials

The core feature of Vue is rendering reactive state. 

This means that we can create a reactive variable in our app code, and then display that variable in our app template.

Everytime our reactive variable changes in value, Vue will automatically update where ever it is being used in our app template. 

There are two ways we can declare reactive values, with `ref()` and with `reactive()`. 

Details on `reactive()` and `ref()` are discussed in [Guide - Reactivity Fundamentals](https://vuejs.org/guide/essentials/reactivity-fundamentals.html).

<!-- 

    Slide notes: 

-->

---
title: Vue.JS essentials
level: 2
---

# Creating reactive variables
Vue.JS essentials

When we create a `ref()`, after initialisation we use the `.value` property to change the value of the reactive variable

```js
setup() {
    // create a reactive variable using ref
    const message = ref("Hello world");

    console.log(message.value) // "Hello world"

    message.value = "Not hello world anymore"
    
    // expose to the template
    return {
        message,
    };
},
```

<!-- 

    Slide notes: 

-->



---
title: Vue.JS essentials
level: 2
---

# Creating reactive variables
Vue.JS essentials

When we create a `reactive()`, after initialisation we can modify the variable without the need for the `.value` property

```js
setup() {
    // create a reactive variable using reactive
    const counter = reactive(
        { count: 0 }
    );
    const message = ref("Hello world");
    console.log(counter.count); // 0
    console.log(message.value); // "Hello world"
    
    // expose to the template
    return {
        counter,
        message,
    };
},
```

<!-- 

    Slide notes: 

-->



---
title: Vue.JS essentials
level: 2
---

# Declarative Rendering
Vue.JS essentials

We can render the reactive variables we just created using the moustache syntax. 

```html
<h1>{{ message }}</h1>
<p>Counter is {{ counter.count }}</p>
```

<!-- 

    Slide notes: 

-->


---
title: Vue.JS essentials
level: 2
---

# Attribute binding
Vue.JS essentials

We actually can't use moustache systax everywhere in our template. If we want to dynamically change attributes we need to use a slightly different syntax. We use the `v-bind` directive. 

Template: 
```html 
<div v-bind:id="dynamicID"></div>
```

JavaScript:
```js
setup() {
    // create a reactive variable using reactive
    const dynamicID = ref("myID");
    // expose to the template
    return {
        dynamicID,
    };
},
```

<!-- 

    Slide notes: 

-->



---
title: Vue.JS essentials
level: 2
---

# Attribute binding
Vue.JS essentials

We can also use the shorthand and remove the text for the `v-bind` directive and it will still work (note we still need the colon before the `id`) 

Template: 
```html 
<div :id="dynamicID"></div>
```


<!-- 

    Slide notes: 

-->


---
title: Vue.JS essentials
level: 2
---

# Attribute binding
Vue.JS essentials

In addition to `id`s, we can also bind `src` and `alt` attributes for an image.

Template: 
```html 
<img v-bind:src="imgSrc" v-bind:alt="imgAlt" />
```

JavaScript:
```js
setup() {
    // create a reactive variable using reactive
    const imgSrc = ref("./image/chuck-norris.png");
    const imgAlt = ref("Picture of Chuck Norris");
    // expose to the template
    return {
        imgSrc,
        imgAlt,
    };
},
```

<!-- 

    Slide notes: 

-->


---
title: Vue.JS essentials
level: 2
---

# Conditional rendering
Vue.JS essentials

Vue makes it really easy for us to show and hide elements on a page based on a reactive variable. 

And as an added awesome bonus, if our reactive variable changes, then Vue will automatically rerender the page so that the correct elements are hidden and shown.

More details on `v-if`: [Guide - Conditional Rendering](https://vuejs.org/guide/essentials/conditional.html)

<!-- 

    Slide notes: 

-->




---
title: Vue.JS essentials
level: 2
---

# Conditional rendering
Vue.JS essentials

Vue uses the `v-if` and `v-else` directives for conditional rendering. If `isAwesome` is `true`, then we show the first `<p>` tag. If however `isAwesome` is false, then the second `<p>` tag is shown.

```html
<p v-if="isAwesome">Everything is Awesome!</p>
<p v-else>On no, something isn't awesome</p>
```

<!-- 

    Slide notes: 

-->



---
title: Vue.JS essentials
level: 2
---

# Conditional rendering
Vue.JS essentials

And here is our app code where we declare `isAwesome` and set it to `true`. If it was `false` then the second paragraph would be shown.

JavaScript:
```js
setup() {
    // create a reactive variable using reactive
    const isAwesome = ref(true);
    // expose to the template
    return {
        isAwesome,
    };
},
```

<!-- 

    Slide notes: 

-->


---
title: Vue.JS essentials
level: 2
---

# List rendering 
Vue.JS essentials

The `v-for` directive allows us to quickly and easily render lists that are based on an array.

To render a list we must provide a special `:key` attribute.

More details on v-for: [Guide - List Rendering](https://vuejs.org/guide/essentials/list.html)

```html
<ul>
    <li v-for="todo in todos" :key="todo.id">
        {{ todo.text }}
    </li>
</ul>
```

<!-- 

    Slide notes: 

-->



---
title: Vue.JS essentials
level: 2
---

# List rendering 
Vue.JS essentials

And here is the reactive array declared and exposed to the template.

```js
setup() {
    // create a reactive variable using reactive
    const todos = ref([
        { id: 0, text: "Buy Milk" , done: false },
        { id: 1, text: "Pick up dry cleaning" , done: false },
        { id: 2, text: "Put air in tires" , done: false },
        { id: 3, text: "Get coffee" , done: false }
    ]);
    // expose to the template
    return {
        todos,
    };
},
```

<!-- 

    Slide notes: 

-->

---
title: Vue.JS essentials
level: 2
---

# Event handling
Vue.JS essentials

We can listen to DOM events using the `v-on` directive. 

There is also a shorthand syntax that uses the `@` symbol. 

We don't have to add any event listeners manually, Vue takes care of that for us.

```html
<!-- On button press, the increment function will fire -->
<button v-on:click="increment">{{ count }}</button>

<!-- On button press, the increment function will fire - shorthand -->
<button @click="increment">{{ count }}</button>

<!-- On form submit the default browser behaviour is prevented and the onSubmit function will run -->
<form @submit.prevent="onSubmit">
    ...
</form>
```

<!-- 

    Slide notes: 

-->



---
title: Vue.JS essentials
level: 2
---

# Event handling
Vue.JS essentials

```js
setup() {
    // create a reactive variable using ref
    const count = ref(0);
    
    function increment() {
        count.value++;
    }

    function onSubmit() {
        ...
    }

    // expose to the template
    return {
        count,
        increment,
        onSubmit,
    };
},
```

<!-- 

    Slide notes: 

-->


---
title: Vue.JS essentials
level: 2
---

# Class and style binding
Vue.JS essentials

We can also bind classes to our template elements. 

In the code below we are using the `v-bind` syntax to add a class to our `div`. If the `isActive` class is true (or evaluates to true) then the `active` class will be added to the element. 

If `isActive` is false, then the `active` class won't be added. 

```html
<!-- With v-bind directive -->
<div v-bind:class="{ active: isActive }">Hello world</div>

<!-- Shorthand -->
<div :class="{ error: isError }">Hello world</div>

<!-- You can also use both the class and dynamic class attributes together -->
<div class="todo" v-bind:class="{ active : isActive }">...</div>
```

<!-- 

    Slide notes: 

-->



---
title: Vue.JS essentials
level: 2
---

# Event handling
Vue.JS essentials

And here is how we would setup the reactive variables from the previous example.

```js
setup() {
    // create a reactive variable using ref
    const isActive = ref(false);
    const isError = ref(false);

    // expose to the template
    return {
        isActive,
        isError,
    };
},
```

<!-- 

    Slide notes: 

-->

---
title: Vue.JS essentials
level: 2
---

# Computed property
Vue.JS essentials

<!-- 

    Slide notes: 

-->



---
title: Vue.JS essentials
level: 2
---

# Watchers
Vue.JS essentials

<!-- 

    Slide notes: 

-->




---
title: Vue.JS essentials
level: 2
---

# Components
Vue.JS essentials

<!-- 

    Slide notes: 

-->




---
title: Vue.JS essentials
level: 2
---

# Props
Vue.JS essentials

<!-- 

    Slide notes: 

-->




---
title: Vue.JS essentials
level: 2
---

# Emits
Vue.JS essentials

<!-- 

    Slide notes: 

-->