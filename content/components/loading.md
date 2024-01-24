---
title: Loading
subtitle: A spinner indicating that an operation is in progress
---

Add an `aria-busy="true"` attribute to an element in order to indicate that an
operation is in progress (such as loading data from the server backend).

<div class="grid">
  <button aria-busy="true" class="m-0 p-1">Please wait...</button>
  <article aria-busy="true" class="m-0 p-1"></article>
  <p class="m-0 p-1"><a href="#" aria-busy="true">Loading...</a></p>
</div>

Note that a link or button with an active loader cannot be clicked upon.

```html
<div class="grid">
  <button aria-busy="true" class="m-0 p-1">
    Please wait...
  </button>
  <article aria-busy="true" class="m-0 p-1"></article>
  <p class="m-0 p-1">
    <a href="#" aria-busy="true">Loading...</a>
  </p>
</div>
```


