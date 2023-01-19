---
layout: intro
title: HTML tables
level: 1
---

# HTML Tables

Marking up HTML Tables



---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

Consists of one `<table>` element and one or more `<tr>`, `<th>`, and `<td>` elements inside `<thead>` and `<tbody>` elements.


```html
<table>
  <thead>
    <tr>
      <th>Month</th>
      <th>OC Transpo Ridership</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>300000</td>
    </tr>
  </tbody>
</table>
```

<div class="text-sm">

[\<table> - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)

</div>

<!-- 

Slide notes: 

* Although HTML allows it, you should only have one <h1> on the page

-->

---
layout: two-cols-header
title: Semantic elements
level: 2
---

# Tables
Used when you need to display tabular data

::left::

```html
<table>
  <thead>
    <tr>
      <th>Month</th>
      <th>OC Transpo Ridership</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>300000</td>
    </tr>
     <tr>
      <td>February</td>
      <td>320000</td>
    </tr>
    ...
  </tbody>
</table>
```

::right::

<table>
  <thead>
    <tr>
      <th><strong>Month</strong></th>
      <th><strong>OC Transpo Ridership</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>300000</td>
    </tr>
    <tr>
      <td>February</td>
      <td>320000</td>
    </tr>
    <tr>
      <td>March</td>
      <td>330000</td>
    </tr>
    <tr>
      <td>April</td>
      <td>340000</td>
    </tr>
    <tr>
      <td>May</td>
      <td>290000</td>
    </tr>
    <tr>
      <td>June</td>
      <td>250000</td>
    </tr>
  </tbody>
</table>


---
title: Tables
level: 2
---

# Tables
Used when you need to display tabular data

Other table elements include `<caption>`, `<colgroup>`, `<tfoot>`. Since these elements aren't used very frequently we don't cover them here.

While beyond the scope of this course, for more complex tables, you may run into `rowspan` and `colspan` attributes. These attributes help you layout tables that have a high degree of complexity. 
