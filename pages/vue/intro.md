---
title: Intro to Vue.JS
layout: intro
---

# Vue.JS
The Progressive JavaScript Framework


---
title: Vue.JS logo
level: 2
layout: center
---

<svg class="logo" viewBox="0 0 128 128" width="300" height="300"><path fill="#42b883" d="M78.8,10L64,35.4L49.2,10H0l64,110l64-110C128,10,78.8,10,78.8,10z" data-v-7b849662=""></path><path fill="#35495e" d="M78.8,10L64,35.4L49.2,10H25.6L64,76l38.4-66H78.8z"></path></svg>

<p class="text-center"><a href="https://vuejs.org" rel="external" target="_blank">Vue.JS</a></p>


---
title: What is Vue.JS 
level: 2
layout: image-right
image: /images/slides/vue/intro/group.jpg
---

# What is Vue.JS 
Build web interfaces quickly and easily

Vue (pronounced /vjuː/, like **view**) is a JavaScript framework for building user interfaces. 

It builds on top of standard HTML, CSS, and JavaScript and provides a declarative and component-based programming model that helps you efficiently develop user interfaces, be they simple or complex.

Source: [What is Vue?](https://vuejs.org/guide/introduction.html#what-is-vue)

<!-- 

    Slide notes: 

    Credit: 

    Photo by RealToughCandy.com: https://www.pexels.com/photo/road-man-people-woman-11035366/

    Photo by cottonbro studio: https://www.pexels.com/photo/group-of-people-in-front-of-a-laptop-7437488/

-->



---
title: What is Vue.JS 
level: 2
---

# Why I love Vue.JS
Build web interfaces quickly and easily

Today we're lucky to have so many different JavaScript frameworks that we could invest our time in learning (Angular, React, SolidJS, etc.), and all options are valuable for your career development. 

While all frameworks have their pros and cons, the reason I keep coming back to Vue.JS: 

* ultra fast render times and is the most performant (though admittedly the gap is closing)
* great [developer documentation](https://vuejs.org/guide/introduction.html)
* is easier to pick up than other JS frameworks
* builds off your existing knowledge of HTML, CSS, and JavaScript
* lots of tutorials, articles, youtube videos to help you along the way
* growing collection of plugins (but not as big as React)

<!-- 

    Slide notes: 

    Credit: 

    Photo by RealToughCandy.com: https://www.pexels.com/photo/road-man-people-woman-11035366/

    Photo by cottonbro studio: https://www.pexels.com/photo/group-of-people-in-front-of-a-laptop-7437488/

-->

---
title: VueJS
level: 2
---

# A super simple Vue.JS app
Build web interfaces quickly and easily

We're going to setup a super simple Vue.JS app to jump right into the code.

In the future we'll look into `node` and `vite` and modern build tools that used to build production Vue.JS apps. 

**Step 1**: Add the reference to the Vue.JS javascript files to your web page

```html
<html>
  <head>
    ...
    <!-- We can use the Vue.JS library directly from a Content Delivery Network (CDN)-->
    <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

  </head>
  ...
</html>
```

<!-- 

    Slide notes: 

    Credit: 

    https://vuejs.org/guide/quick-start.html#using-vue-from-cdn

-->



---
title: VueJS
level: 2
---

# A super simple Vue.JS app
Build web interfaces quickly and easily

We need to define the visual template that our Vue.JS app will read and load into. A common pattern is to use a `<div>` with an `id` called `app`, but you can set it to any valid selector.  

**Step 2**: Create a div with an id that our app can load into on the page. We'll just put in an `<h1>` in for now. 

```html
<html>
  ...
  <body>
    <main>
    
      <!-- Vue.JS app boundary -->  
      <div id="app">
        <h1>Hello World!</h1>
      </div>
    
    </main>
  </body>
</html>
```

<!-- 

    Slide notes: 

    Credit: 

    https://vuejs.org/guide/quick-start.html#using-vue-from-cdn

-->



---
title: VueJS
level: 2
---

# A super simple Vue.JS app
Build web interfaces quickly and easily

In a seperate JavaScript file, we're going to add all of our app logic, so let's add a reference to that file in our HTML page. 

**Step 3**: Add a `<script>` at the bottom of our page to load our Vue.JS app code

```html
<html>
  ...
  <body>
    ...

    <!-- Import and mount our Vue.JS App -->
    <script src="./main.js"></script>

  </body>
</html>
```

<!-- 

    Slide notes: 

    Credit: 

    https://vuejs.org/guide/quick-start.html#using-vue-from-cdn

-->



---
title: VueJS
level: 2
---

# A super simple Vue.JS app
Build web interfaces quickly and easily

We use the `createApp` method to setup our app logic (right now it's just an empty app). We then have to mount our app to our page using the `mount` method to tell Vue.JS to run our app.  

**Step 4**: Setup some boilerplate code to create and mount a Vue.JS app in our `#app` `<div>`

```js
// main.js 

// Get an instance of the createApp Vue object
const { createApp } = Vue;

// This is where our app logic will go - in the createApp method
const app = createApp({});

// Finally, we mount our app to our web page
app.mount("#app");

```

<!-- 

    Slide notes: 

    Credit: 

    https://vuejs.org/guide/quick-start.html#using-vue-from-cdn

-->



---
title: VueJS
level: 2
---

# A super simple Vue.JS app
Build web interfaces quickly and easily

In a `setup()` function, we're going to create a reactive object in Vue.JS using the `ref()` method and `return` it so we can use it in our app template code.

**Step 5**: Use `ref()` to create a reactive object and return it

```js
// main.js 
const { createApp, ref } = Vue; // Get an instance of the createApp and ref from the Vue object
const app = createApp({
  setup() {
    // component logic
    const message = ref("Hello world");
    // expose to the template
    return {
      message,
    };
  },
});
app.mount("#app"); // Finally, we mount our app to our web page
```

<!-- 

    Slide notes: 

    Credit: 

    https://vuejs.org/guide/quick-start.html#using-vue-from-cdn

-->


---
title: VueJS
level: 2
---

# A super simple Vue.JS app
Build web interfaces quickly and easily

Now we can update our app template to display the `message` instead of the hard coded text

**Step 6**: Update our template to use our reactive `message` variable in the template

```html
<body>
  <main>

    <!-- Vue.JS app boundary -->  
    <div id="app">
      <!-- "moustache" template to reference exposed Vue.JS reactive objects -->
      <h1>{{ message }}</h1>
      <!-- You can also run JavaScript expressions inside the template expressions -->
      <p>{{ message.split('').reverse().join('') }}</p>
    </div>

  </main>
</body>
```

<!-- 

    Slide notes: 

    Credit: 

    https://vuejs.org/guide/quick-start.html#using-vue-from-cdn

-->



---
title: VueJS
level: 2
---

# A super simple Vue.JS app
Build web interfaces quickly and easily

Now let's add a reactive counter to our web app

**Step 7**: Use `ref()` to create another reactive object and return it

```js
// main.js 
const { createApp, ref } = Vue; // Get an instance of the createApp and ref from the Vue object
const app = createApp({
  setup() {
    // component logic
    const message = ref("Hello world");
    const counter = ref(0);
    // expose to the template
    return {
      message,
      counter,
    };
  },
});
app.mount("#app"); // Finally, we mount our app to our web page
```

<!-- 

    Slide notes: 

    Credit: 

    https://vuejs.org/guide/quick-start.html#using-vue-from-cdn

-->



---
title: VueJS
level: 2
---

# A super simple Vue.JS app
Build web interfaces quickly and easily

Now we can add the `counter` reactive object to our template

**Step 8**: Update our template to use our reactive `counter` variable in the template

```html
<body>
  <main>

    <!-- Vue.JS app boundary -->  
    <div id="app">
      <!-- "moustache" template to reference exposed Vue.JS reactive objects -->
      <h1>{{ message }}</h1>
      <!-- Display our counter variable (automatically converted to a string) -->
      <p>Our counter {{ counter }}</p>
    </div>

  </main>
</body>
```

<!-- 

    Slide notes: 

    Credit: 

    https://vuejs.org/guide/quick-start.html#using-vue-from-cdn

-->


---
title: That's the basics
level: 2
layout: image-right
image: /images/slides/vue/intro/vue-logo.jpg
---

# That's the intro 
Where to go for more information 

* [Official Vue.JS website](https://vuejs.org)
* [Official Vue.JS documentation](https://vuejs.org/guide/introduction.html)
* [Basic Vue.JS Tutorial](https://vuejs.org/tutorial/#step-1)
* [Free Vue School Courses](https://vueschool.io/courses?filter=free-courses)
* [Free Vue Mastery Intro Course](https://www.vuemastery.com/courses/intro-to-vue-3/intro-to-vue3)
* [The documentary](https://www.youtube.com/watch?v=OrxmtDw4pVI)

<!-- 

    Slide notes: 

    Credit: 

    Photo by RealToughCandy.com: https://www.pexels.com/photo/road-man-people-woman-11035366/

    Photo by cottonbro studio: https://www.pexels.com/photo/group-of-people-in-front-of-a-laptop-7437488/

-->