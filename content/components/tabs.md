---
title: Tabs
subtitle: Simple tab boxes with up to eight tabs
---

A tab box can have up to eight tabs. The structure is rather strict. Inside a wrapper with the `tabs` class, there is first at the front a series of radio button elements and labels representing the tabs (they must be arranged as pairs with the radio button immediately in front of its label). After that the tab panes themselves follow; they must have a `pane` class and appear in the same order as the corresponding tabs. One of the tabs must be `checked`. Here is an example:

<div class="tabs">
  <input type="radio" name="tabgroup" id="tab1" checked>
  <label for="tab1">Animi</label>
  <input type="radio" name="tabgroup" id="tab2">
  <label for="tab2">Perspiciatis</label>
  <input type="radio" name="tabgroup" id="tab3">
  <label for="tab3">Voluptas</label>
  <div class="pane"><p>Tab pane 1. Dignissimos ullam architecto beatae rem. Harum voluptatem exercitationem unde accusamus delectus. Accusantium labore et qui et hic delectus. Consectetur sunt qui quia voluptatem quia et ex doloribus. Nesciunt dolorum et eligendi necessitatibus est ut in modi. Dolorem commodi maiores velit.</p></div>
  <div class="pane"><p>Tab pane 2. Aut et non pariatur doloremque officiis eos neque quos. Quo natus porro itaque quis ut veniam. Dolorum et mollitia incidunt dignissimos voluptate ullam labore qui. A quos quaerat temporibus. Amet excepturi quia libero. Blanditiis vitae aut illum.</p></div>
  <div class="pane"><p>Tab pane 3.  Quisquam aut officiis sequi nostrum. Rerum debitis culpa dolor sunt recusandae et possimus. Voluptatibus qui omnis non eos praesentium et.</p></div>
</div>

```html
<div class="tabs">
  <input type="radio" name="tabgroup" id="tab1" checked>
  <label for="tab1">Animi</label>
  <input type="radio" name="tabgroup" id="tab2">
  <label for="tab2">Perspiciatis</label>
  <input type="radio" name="tabgroup" id="tab3">
  <label for="tab3">Voluptas</label>
  <div class="pane"><p>Tab pane 1. Dignissimos ullam architecto beatae...</p></div>
  <div class="pane"><p>Tab pane 2. Aut et non pariatur doloremque officiis...</p></div>
  <div class="pane"><p>Tab pane 3.  Quisquam aut officiis sequi nostrum...</div>
</div>
```
