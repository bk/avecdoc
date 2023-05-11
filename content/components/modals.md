---
title: Modal window
subtitle: Javascript-free lightbox component
---

A modal (or lightbox) is kind of popup window appearing seemingly atop the page, with the rest of the page overlaid with a dark, semitransparent layer. It looks like a card (since, like a card, it uses the `<article>` tag). Click the "Show modal" button below to see an example.

<p><label for="modal1" role="button" class="d-inl">Show modal</label></p>

<div class="modal">
  <input id="modal1" type="checkbox" />
  <label for="modal1" class="overlay"></label>
  <article>
    <header>
      <label for="modal1" class="close">&times;</label>
      <h4>Terrific modal</h4>
    </header>
    <p>Corrupti numquam vitae ut omnis dicta nemo ipsa sunt. Asperiores quia minima ut. Possimus quo et molestiae. Dolores qui magni sit omnis aliquam est. Voluptatem aut eveniet dolores et. Totam excepturi rerum nobis accusantium non.</p>
    <p>Architecto sint veritatis soluta asperiores eos ex minus. Eos et expedita voluptate minima. Perferendis est et praesentium autem occaecati voluptatem omnis ut. Officiis commodi quia voluptas reiciendis illum.</p>
    <footer>
      <div class="grid">
        <a role="button" href="#">Buy now!</a>
        <label for="modal1" role="button" class="bg-error">Cancel</label>
      </div>
    </footer>
  </article>
</div>

```html
<label for="modal1" role="button" class="d-inl">Show modal</label>

<div class="modal">
  <input id="modal1" type="checkbox" />
  <label for="modal1" class="overlay"></label>
  <article>
    <header>
      <label for="modal1" class="close">&times;</label>
      <h4>Terrific modal</h4>
    </header>
    <p>Corrupti numquam vitae ut omnis dicta nemo ipsa sunt...</p>
    <p>Architecto sint veritatis soluta asperiores eos ex minus...</p>
    <footer>
      <div class="grid">
        <a role="button" href="#">Buy now!</a>
        <label for="modal1" role="button" class="bg-error">Cancel</label>
      </div>
    </footer>
  </article>
</div>
```
