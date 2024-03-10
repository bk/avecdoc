---
title: Chip
subtitle: For tags and similar entities
---

Chips (also known as "pills") are used for tags and similar entities. They can
also be used as the basis for more elaborate widgets which include images or
icons (e.g. a widget representing a user with an avatar image).

A chip is formed by assigning the `chip` class to an inline element, often an
`<a>` or a `<span>`.

<a href="#" class="chip">#sometag</a>
<a href="#" class="chip"><img src="/img/dalle.jpg" class="borad-round" style="aspect-ratio:1;margin-right:3px"> John Smith, jr.</a>
<span class="chip">Dismiss me <a href="#" class="close">×</a></span>

```
<a href="#" class="chip">sometag</a>
<a href="#" class="chip"><img src="/img/dalle.jpg" class="borad-round" style="aspect-ratio:1;margin-right:3px"> John Smith, jr.</a>
<span class="chip">Dismiss me <a href="#" class="close">×</a></span>
```
