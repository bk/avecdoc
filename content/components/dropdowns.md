---
title: Dropdowns
subtitle: Perfect for navigation
---

Like accordions, dropdowns are also implemented as `<details>` but with a bit more special styling and with stricter requirements on the contents. The `<details>` must have `role="dropdown"` and the immediate children must be a `<summary>` and an `<ul>`, in that order. An example dropdown was shown above in the Nav menu section. Here is another example outside a `<nav>`. It looks somewhat similar to a `<select>`, which is shown on the right for comparison.

<div class="grid-sm">
  <details role="dropdown">
    <summary>Fruit dropdown</summary>
    <ul>
      <li><a href="#">Apple</a></li>
      <li><a href="#">Orange</a></li>
      <li><a href="#">Banana</a></li>
      <li><a href="#">Papaya</a></li>
      <li><a href="#">Other</a></li>
    </ul>
  </details>
  <select>
    <option selected value="1">Fruit select</option>
    <option value="2">Apple</option>
    <option value="3">Orange</option>
    <option value="4">Banana</option>
    <option value="5">Papaya</option>
    <option value="6">Other</option>
  </select>
</div>

```html
<div class="grid-sm">
  <details role="dropdown">
    <summary>Fruit dropdown</summary>
    <ul>
      <li><a href="#">Apple</a></li>
      <li><a href="#">Orange</a></li>
      ...
    </ul>
  </details>
  <select>
    <option selected value="1">Fruit select</option>
    <option value="2">Apple</option>
    <option value="3">Orange</option>
    ...
  </select>
</div>
```

As shown in the Nav example [above](#nav), dropdowns look a bit different in that context: more link-like and with tighter spacing.

A dropdown can be made to look like a button by adding `role="button"` to the `<summary>` tag. If desired, the background color of the button can then be modified by adding a class attributes (e.g. `<summary role="dropdown" class="bg-error">`). Examples (with a `d-inl` class on the `<details>` so as to constrain the buttons to content dimensions):

<div>
  <details role="dropdown" class="d-inl">
    <summary role="button">Fruity goodness</summary>
    <ul>
      <li><a href="#">Apple</a></li>
      <li><a href="#">Orange</a></li>
      <li><a href="#">Banana</a></li>
      <li><a href="#">Papaya</a></li>
      <li><a href="#">Other</a></li>
    </ul>
  </details>
  <details role="dropdown" class="d-inl">
    <summary role="button" class="bg-error">Dangerous types of fruit</summary>
    <ul>
      <li><a href="#">Apple</a></li>
      <li><a href="#">Orange</a></li>
      <li><a href="#">Banana</a></li>
      <li><a href="#">Papaya</a></li>
      <li><a href="#">Other</a></li>
    </ul>
  </details>
</div>

The list shown by the dropdown is normally placed so that its left side aligns with the left side of the `<summary>`. You can change this to the right side by adding `class="rightset"` to the `<ul>`. (The difference between the two is not visible unless the list is broader than the dropdown button, since the minimum width is the same as the button).

