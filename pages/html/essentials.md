---
layout: intro
title: HTML
level: 1
---

# HTML Essentials

Everything you need to know about Hypertext Markup Language

---
title: So what is HTML
level: 2
---

# So what is HTML
The basics

HTML is a markup language we use to define the structure of the content of our web pages. 

We use tags to define the content's purpose and give an element semantic meaning.

For example, the following text: 

```html
Buster is hungry 
```

If we wanted to identify that line as a paragraph of text, we would write the following: 

```html
<p>Buster is hungry</p>
```

`<p>` refers to the HTML tag, and "Buster is hungry" refers to the content within the tag.

<!-- 

Slide notes: 

-->


---
title: Anatomy of an HTML Element
level: 2
---

# Some common terms to understand
The basics

```html
<p class="text-red">Buster is hungry</p>
```


* open tag `<p>`— the part to an element that defines where this type of content starts
* close tag `</p>`— the part of an element that defines where this type of content ends
* attribute `class="text-red"`— a piece of metadata that isn’t usually visible in the browser but defines extra information about the element
* element — the combination of an open tag, the content, and a close tag

<!-- 

Slide notes: 

-->


---
title: Anatomy of an HTML Element
level: 2
---

# A note about nesting 
The basics

You can put elements inside other elements. This is referred to as nesting. We also sometimes refer to these elements as having a parent-child relationship. 

Keep in mind that the elements have to be nested properly. 

```html
<p class="text-red">Buster is <strong>very</strong> hungry</p>
```

The element above will work fine.


```html
<p class="text-red">Buster is <strong>very hungry</p></strong>
```

The element above is not structured properly because the `<p>` tag is closed before the `<strong>` tag. 


<!-- 

Slide notes: 

-->


---
title: HTML Document
level: 2
---

# HTML Document
The basics

Here is what the code for an empty basic HTML document looks like: 

```html
<!DOCTYPE html>
<html lang="en-ca"> <!-- Sets the language to Canadian English -->
<head>
  <meta charset="utf-8">
  <title>Title of the page</title>
</head>
<body>
    <!-- This is a comment - it will not appear on your web page-->
</body>
</html>
```

<!-- 

Slide notes: 

-->


---
title: Headings
level: 2
---

# Headings
The elements

Heading elements allow you to specify what content on your page is a heading or sub heading.

```html
<!-- 6 heading levels: -->
<h1>Earth</h1>
  <h2>North America</h2>
    <h3>Canada</h3>
      <h4>Ontario</h4>
        <h5>Toronto</h5>
        <h5>Ottawa</h5>
          <h6>Nepean</h6>
          <h6>Kanata</h6>
    <h3>United States</h3>
      <h4>California</h4>
      <h4>New York</h4>
  <h2>Africa</h2>
    <h3>Egypt</h3>
      <h4>Cairo</h4>
        <h5>Cairo</h5>
    <h3>Nigeria</h3>
    <h3>Kenya</h3>
```

<!-- 

Slide notes: 

* Although HTML allows it, you should only have one <h1> on the page

-->



---
title: Paragraphs
level: 2
---

# Paragraphs
The elements

Paragraph tag for, you guessed it, paragraphs of text.

```html
<p>Meatloaf andouille bacon alcatra short ribs. Salami meatball spare ribs,
     shankle ribeye burgdoggen bacon pork. Beef andouille pig biltong.</p>

<p>Drumstick andouille boudin, shankle jowl pork chop chuck picanha
     short loin pork loin kevin chicken fatback.</p>
```

<!-- 

Slide notes: 

-->


---
title: Paragraphs
level: 2
---

# Lists
The elements

There are three types of lists that can be marked up. 

`<ul>` Unordered lists - for when the order of the items in the list don't matter, such as a list of things to buy at the grocery store 

```html
<ul>
    <li>Milk</li>
    <li>Eggs</li>
    <li>Chips</li>
    <li>Bananas</li>
</ul>
```

<!-- 

Slide notes: 

-->


---
title: Lists
level: 2
---

# Lists
The elements

There are three types of lists that can be marked up. 

`<dl>` Ordered lists - for when the order of the items is important, like instructions in a recipe

```html
<ol>
    <li>Add Milk</li>
    <li>Beat the eggs and add to the milk</li>
    <li>Smash the bananas and set aside</li>
</ol>
```

<!-- 

Slide notes: 

-->


---
title: Paragraphs
level: 2
---

# Lists
The elements

There are three types of lists that can be marked up. 

`<dl>` Description lists - for defining data and value pairs

```html
<dl>
    <dt>Length</dt>
    <dd>12 metres</dd>

    <dt>Mass</dt>
    <dd>5.4 metric tons</dd>
</dl>
```

<!-- 

Slide notes: 

-->



---
title: Paragraphs
level: 2
---

# Links
The elements

Links are the key to the whole web! Here's how to make a link. 

First identify the text that you want to make a link.

```html
<p>Buster likes to go the groomer name <a>Martin</a></p>
```

Then add an `href` attribute to the `<a>` tag. 

```html
<p>Buster likes to go the groomer name <a href="">Martin</a></p>
```

Finally, add the web address to the `href` attribute 

```html
<p>Buster likes to go the groomer name <a href="https://martin.cutshair.com">Martin</a></p>
```

<!-- 

Slide notes: 

-->


---
title: Images
level: 2
---

# Images
The elements

Images in websites are not embedded in the website, but linked to by the HTML document.

Images need two attributes to specify extra details about the image: the location of the image and the alternative content.

```html
<img src="buster.jpg" alt="Photo of Buster">
```

<!-- 

Slide notes: 

-->

---
layout: center
title: Exercise 01
level: 2
---

[Exercise 01](https://github.com/imd1005-web-development-winter-2023/exercise-html-01/)

