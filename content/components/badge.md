---
title: Badges
subtitle: For showing a small status indicator for UI elements such as buttons
---

A badge shows a status indicator or a number which relates to a specific (typically small) element,
often a button, a tab or a navigation item. The value for the badge is given with a `data-badge` attribute.
An empty `data-badge` leads to a badge that is a small dot.

<div class="mb-2">
<button class="badge mr-1" data-badge="917">First</button>
<button class="badge mr-1" data-badge="">Second</button>
<button class="badge" data-badge="✓">Third</button>
</div>

It may be necessary to ensure extra spacing around the element that the badge is attached to in order to prevent it from obscuring something in the surroundings.


```html
<div>
  <button class="badge mr-1" data-badge="917">First</button>
  <button class="badge mr-1" data-badge="">Second</button>
  <button class="badge" data-badge="✓">Third</button>
</div>
```
