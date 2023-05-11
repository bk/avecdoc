---
title: Hero
subtitle: The ubiquitous hero image component
---

A hero image is a large (often full-screen) dark background image with text on top, appearing at the top of the page or near it.

There is not much to a hero image. Give a `<div>` or other block element the `hero` class. You must set the background image on that div yourself in a stylesheet or via the `style` attribute. If the image is not dark enough, you can add a dark gradient to the background as well, like so:

```css
background-image:
    linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url(/img/hero.jpg);
```

By default the size of the hero div depends on the content, although it has a minimum height of 400px. The following classes modify how the hero block behaves:

- `full-height`: Ensure a height of at least the screen height.
- `half-height`: Ensure a height of at least half the screen height.
- `center-content`: The text in the hero block will be centered both vertically and horizontally.

As a rule, the text on top of the hero div should be light in color. You must see to this yourself. The `dark-theme` class may be helpful, as well as such utility classes as `text-brigt`

If the hero image is inside `<main>` you should add the `full` class to the block to ensure that it covers the full screen width.
