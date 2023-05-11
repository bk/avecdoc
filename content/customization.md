---
title: Themes and customization
subtitle: Dark mode, color themes – and extending AvecCSS
---

## Light and dark mode

AvecCSS defines colors for both light and dark mode and supports automatic switching between them depending on the OS (or browser) preference setting.

The page author can also specify the mode explicitly using the `light-theme` or `dark-theme` CSS classes. This may apply to the whole page or to a section of it. For instance, you can use light mode for the main body of the page but dark mode for the header and footer like this:

```html
<html class="light-theme">
  <head>...</head>
  <body>
    <header class="dark-theme">...</header>
    <main>...</main>
    <footer class="dark-theme">...</footer>
  </body>
</html>
```

A more agnostic way of accomplishing much the same thing is to use the `reverse-theme` class. This switches to whichever color mode is not the default one for the page. In other words, if no theme is set and the user prefers dark mode, it will switch to light mode; and if `light-theme` has been applied to the `<html>` or `<body>` element or the user has no explicit preference, it will switch to dark mode.

```html
<html>
  <head>...</head>
  <body>
    <header class="reverse-theme">...</header>
    <main>...</main>
    <footer class="reverse-theme">...</footer>
  </body>
</html>
```

In this example, if the user prefers dark mode then the header and footer will be light while the main section will be dark. Otherwise, the header and footer will be dark and the rest of the page light.

## Color themes

A theme is implemented as a set of SCSS variables defining the colors to use in both light and dark mode. There are currently 6 themes.

- Default
- Gruvbox
- One: 
- Pico
- Plain
- Selenized

The themes are exported to separate CSS files which can be loaded after the main AvecCSS file. For instance, in order to switch to Selenized, you would do this:

```html
<link rel="stylesheet" href="/css/avec.css">
<link rel="stylesheet" href="/css/avec.selenized-theme.css">
```

## Customizing AvecCSS

- A lot of customization can be done by modifying the CSS variables used by AvecCSS.

- You can modify the CSS classes and rules in AvecCSS by overriding them in your own CSS file.

- Similarly, if you want to create your own color theme theme without touching SCSS, it is quite easy to modify one of the theme files and save it under a new name.

- If you need to customize AvecCSS beyond this, the best way is to clone the project and change the SCSS source.
