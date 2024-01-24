---
title: Tree
subtitle: A tree-like list with toggleable subitems
---

An unordered list with the class `tree` styles `<details>` such that it becomes easy to represent tree-like navigation structures with collapsible subitems.

<div class="p-1 mb-2 bg-accent d-inl">
<ul class="tree sans mt-0 mb-0">
  <li>Plain item</li>
  <li>
    Item with fixed subitems
    <ul>
      <li>subitem 1</li>
      <li>subitem 2</li>
    </ul>
  </li>
  <li>
    <details open>
      <summary>Toggleable item, open by default</summary>
      <ul>
        <li>Normal subitem</li>
        <li>
          <details>
            <summary>Toggleable item</summary>
            <ul>
              <li>subsubitem 1</li>
              <li>subsubitem 2</li>
            </ul>
          </details>
        </li>
      </ul>
    </details>
  </li>
</ul>
</div>

```html
<ul class="tree">
  <li>Plain item</li>
  <li>
    Item with fixed subitems
    <ul>
      <li>subitem 1</li>
      <li>subitem 2</li>
    </ul>
  </li>
  <li>
    <details open>
      <summary>Toggleable item, open by default</summary>
      <ul>
        <li>Normal subitem</li>
        <li>
          <details>
            <summary>Toggleable item</summary>
            <ul>
              <li>subsubitem 1</li>
              <li>subsubitem 2</li>
            </ul>
          </details>
        </li>
      </ul>
    </details>
  </li>
</ul>
```
