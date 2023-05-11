---
title: Accordion
subtitle: For hiding and showing the details
---

An accordion is just a `<details>` tag with slight variations from the default brower rendering. You can combine several of them into a unit by giving them a wrapper with the `stack` class.

<div class="stack">
<details>
  <summary>Windows system requirements</summary>
  <p>Recusandae quibusdam aut est quasi illum beatae possimus. Est labore et sunt nobis adipisci nemo et voluptatem. Voluptatem eveniet iure dolore eum ad labore consectetur.</p>
</details>
<details>
  <summary>Mac system requirements</summary>
  <p>Labore occaecati deserunt non sunt amet ex aperiam fugiat. Est voluptatem est ratione ratione reprehenderit. Consequatur quidem et velit sed.</p>
</details>
<details>
  <summary>Linux system requirements</summary>
  <p>Dolorem et totam deserunt ut quia. Commodi nam illo natus facilis provident. Consequuntur provident in fugiat. Aspernatur modi reprehenderit reiciendis quibusdam.</p>
</details>
</div>

```html
<div class="stack">
<details>
  <summary>Windows system requirements</summary>
  <p>Recusandae quibusdam aut est quasi illum beatae ...</p>
</details>
<details>
  <summary>Mac system requirements</summary>
  <p>Labore occaecati deserunt non sunt amet ex aperiam ...</p>
</details>
<details>
  <summary>Linux system requirements</summary>
  <p>Dolorem et totam deserunt ut quia. Commodi nam illo ...</p>
</details>
</div>
```
