---
title: Main menu component
subtitle: A simple, javascript-free navigation menu
---

The main menu must be inside a `<nav>` in order to function as intended.
Click on the menu symbol on the right in the navbar below to see how it works.

<div class="demo">
<nav>
<div><!-- for pushing the menu right --></div>
<div>
  <input id="main-menu-demo" type="checkbox" class="show-menu">
  <label for="main-menu-demo" class="burger pr-1">
    <span class="menu-icon"></span>
  </label>
  <div class="menu has-close">
    <label for="main-menu-demo" class="close">&times;</label>
    <h4>Menu</h4>
    <ul>
    <li><a href="#">Frontpage</a></li>
    <li><a href="#">Tempora velit</a></li>
    <li><a href="#">Illa laborum ipsa</a></li>
    <li><a href="#">Eaque voluptates</a></li>
    </ul>
  </div>
</div>
</nav>
</div>

```html
<nav>
<div><!-- for pushing the menu right --></div>
<div>
  <input id="main-menu-demo" type="checkbox" class="show-menu">
  <label for="main-menu-demo" class="burger pr-1">
    <span class="menu-icon"></span>
  </label>
  <div class="menu has-close">
    <label for="main-menu-demo" class="close">&times;</label>
    <h4>Menu</h4>
    <ul>
    <li><a href="#">Frontpage</a></li>
    <li><a href="#">Tempora velit</a></li>
    <li><a href="#">Illa laborum ipsa</a></li>
    <li><a href="#">Eaque voluptates</a></li>
    </ul>
  </div>
</div>
</nav>
```

This menu widget is not responsive by itself. In order to distinguish between the menu available to mobile visitors and the navigation seen by those using laptops or desktops, you can use the visibility utility classes described later (`seen-*` and its companions).
