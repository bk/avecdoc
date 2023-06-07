---
title: Layout
subtitle: Default page layout, grids and columns
---

## Breakpoints

Some of the layout features are dependent upon the defined breakpoints, which are the following:

- AvecCSS is mobile-first. Accordingly, there is no named breakpoint for mobile phones in portrait mode.
- `xs`: wide mobile or small tablet, 480px and up. Rarely used.
- `sm`: portrait tablet, 768px and up.
- `md`: landscape tablet or small laptop/desktop, 960px and up.
- `lg`: intermediate laptop/desktop, 1280px and up.
- `xl`: wide laptop/desktop, 1600px and up.

## Basics: `<main>` or `.container`

By default, block level elements immediately inside the `<body>` have a width of 55rem (normally equal to 880px) or 92%, whichever is smaller. This means that if you add AvecCSS to a random HTML document you are likely to at least get something readable.

To use AvecCSS properly, however, you should either have the document structure indicated in the code block above (with `<main>` inside `<body>`), or a `<div>` inside `<body>` with the CSS class `container`.

By default, the immediate children of the container follow the same rule, i.e. keep to a width of at most 55rem or 92%, whichever is smaller. You can add the following classes to the container to change this:

- `items-fluid`: Children keep to 92% regardless of screen width.
- `items-fixed`: Children keep to a fixed width for each breakpoint interval from `sm` to `lg` upwards. Below this the width is fluid. The widths are: 718px for `sm` and up, 910px for `md` and up, 1230px for `lg` and up.
- `items-max-md`: When added to `items-fluid` or `items-fixed`, sets the maximum width of each immediate child to the fixed width associated with `md`, i.e. 910px.
- `items-max-lg`: When added to `items-fluid`, sets the maximum width of each immediate child to the fixed with associated with `lg`, i.e. 1230px.
- `items-max-xl`: When added to `items-fixed`, expands the maximum width of children from 1230px to 1500px (which is the width associated with the `xl` breakpoint). When added to `items-fluid`, sets the maximum width to 1500px.

A child element can always override the setting imposed by the container by specifying the following classes:

- `fluid`: The item takes up `92%` of the available space, regardless of screen width.
- `fixed`: The item has a fixed width for each breakpoint as indicated above.
- `full`: The item takes up all the available horizontal space, breaking out of the container ("full-bleed").
- `max-md`, `max-lg`, `max-xl`: Add this to `fixed` to specify a maximum width, or use it to override an `items-max-XX` setting in the container.
- `normal`: Behave as if the container had not specified any `items-*` class.

## Header and nav

### Header

The main `<header>` (i.e. a `<header>` which is an immediate child of `<body>`) gets an accented background and a bottom-border.

### Nav

A horizontal navigation bar, `<nav>`, is typically at the top of the header. The children of `<nav>` are spaced equally and the underlining of links is removed.

Here is a simple but not atypical `<nav>`:

<div class="demo">
<nav>
  <ul>
    <li><strong><a href="/">AvecCSS</a></strong></li>
  </ul>
  <ul>
    <li><a href="/products/">Products</a></li>
    <li><a href="/blog/">Blog</a></li>
    <li>
      <details role="dropdown">
        <summary>Dropdown</summary>
        <ul>
          <li><a href="#">Dicta maiores</a></li>
          <li><a href="#">Laboriosam</a></li>
          <li><a href="#">Quibusdam quod</a></li>
          <li><a href="#">Nihil obstat</a></li>
        </ul>
      </details>
    </li>
    <li><a href="/mission/">Our mission</a></li>
  </ul>
</nav>
</div>

```
<nav>
  <ul>
    <li><strong><a href="/"><strong>AvecCSS</a></strong></li>
  </ul>
  <ul>
    <li><a href="/products/">Products</a></li>
    <li><a href="/blog/">Blog</a></li>
    <li>
      <details role="dropdown">
        <summary>Dropdown</summary>
        <ul>
          <li><a href="#">Dicta maiores</a></li>
          ...
        </ul>
      </details>
    </li>
    <li><a href="/mission/">Our mission</a></li>
  </ul>
</nav>
```

You would often have a "hamburger menu" at the top right of the main `<nav>`, at least in mobile and sometimes in all screen sizes. This is easily done using AvecCSS; see the page on the [menu component](/components/menu/)

For more on the Dropdown widget, see [here](/components/dropdowns/).

## Footer

The footer is full-width by default and separated from the body with a top border. It has a smaller font.

## Grids, columns, flex

Despite its small size, AvecCSS provides three different methods for arranging arbitrary page elements into a structured layout.

### Grid

Give a containing element the class `grid` to make its children fill a grid where each of them takes up equal horizontal space. When that cannot be done without making each of them narrower than a certain minimum (120px by default), then the next item will wrap to the next line. Example:

<div class="grid mb-2">
  <div class="demo">1</div>
  <div class="demo">2</div>
  <div class="demo">3</div>
  <div class="demo">4</div>
  <div class="demo">5</div>
  <div class="demo">6</div>
  <div class="demo">7</div>
  <div class="demo">8</div>
  <div class="demo">9</div>
  <div class="demo">10</div>
  <div class="demo">11</div>
</div>

```html
<div class="grid">
  <div class="demo">1</div>
  <div class="demo">2</div>
  <div class="demo">3</div>
  <div class="demo">4</div>
  <div class="demo">5</div>
  <div class="demo">6</div>
  <div class="demo">7</div>
  <div class="demo">8</div>
  <div class="demo">9</div>
  <div class="demo">10</div>
  <div class="demo">11</div>
</div>
```

Grids are normally for breakpoint `md` and up. You can use the class `grid-sm` for `sm` and up or `grid-xs` for all screen sizes. (The default minimum width below `sm` is 60px rather than 120px).

The items are separated by a column or row gap (normally 20px). You can get rid of this with the class `nogap`.

You can affect the minimum width of the children by adding classes to the grid container indicating the desired number of "columns" for each breakpoint:

- `c2` to `c12`: "I want this number of columns by default". (Below `sm` only `c2` to `c4` work; below `md` only `c2` to `c6` work. This assumes, of course, that `grid-xs` or `grid-sm` have been used).
- `cN-XX` where `N` is a number between 2 and 12 and `N` is a breakpoint name (`sm`, `md`, `lg` or `xl`): "I want this number of columns from this breakpoint and up". (When the breakpoint is `sm`, `N` cannot be above 6, and of course either `grid-xs` or `grid-sm` must have been used).

This should be 2 columns in mobile, 3 in `sm`, 4 in `md`, 5 in `lg` and 6 in `xl`:

<div class="grid-xs c2 c3-sm c4-md c5-lg c6-xl mb-2">
  <div class="demo">1</div>
  <div class="demo">2</div>
  <div class="demo">3</div>
  <div class="demo">4</div>
  <div class="demo">5</div>
  <div class="demo">6</div>
  <div class="demo">7</div>
</div>

```html
<div class="grid-xs c2 c3-sm c4-md c5-lg c6-xl">
  <div class="demo">1</div>
  <div class="demo">2</div>
  <div class="demo">3</div>
  <div class="demo">4</div>
  <div class="demo">5</div>
  <div class="demo">6</div>
  <div class="demo">7</div>
</div>
```

### Columns

Because `grid` items are always the same size it is not appropriate for defining layouts in the usual sense. The `cols` class, however, provides a more traditional 12-column based layout system.

By default, each item takes up all 12 columns, meaning that they each have to specify their own width as described below. This default can be changed by adding the following classes to the columns container:

- `col-twelfth`, `col-sixth`, `col-fourth`, `col-third`, `col-half`: The default width for each item becomes 1, 2, 3, 4 or 6 of the 12 columns available, respectively. Add `-sm`, `-md`, `-lg` or `xl` to these class names to apply the effect to that breakpoint and above.
- `no-gap`, `no-colgap`, `no-rowgap`: Get rid of the gaps between children. Add breakpoint names if desired to make this effect responsive.

The columns themselves, i.e. the immediate children of the column container can set the following classes to affect their own width and placement. Breakpoint names can be appended to each of these if desired (e.g. `cw6-sm`):

- `cw1` to `cw12` indicates the width of the item in columns.
- `cs1` to `cs12`: indicates at which column it should start.
- `cr2` to `cr6`: indicates how many rows this item should span. (Subsequent items appear beside it for the indicated number of rows provided they are not too wide or explicitly set to start at a conflicting column).
- `ord-1` to `ord-12`, as well as `ord-first`, `ord-last` and `ord-none`: Affects where this column items appears in the order of display. (In practice, `ord-none` would only be used in a responsive variant, in a context such as `ord-last ord-none-md`).

An example of a moderately complex layout implemented with these building blocks:

<div class="cols col-fourth mb-2">
  <div class="demo">cw3 by default</div>
  <div class="demo cw5">explicitly cw5</div>
  <div class="demo cw2">cw2</div>
  <div class="demo cw2">cw2</div>
  <div class="demo cw6 cr3">cw6 spanning 3 rows</div>
  <div class="demo">default</div>
  <div class="demo">default</div>
  <div class="demo cw6">cw6</div>
  <div class="demo cw12 ord-last">Full-width and moved to end using .ord-last</div>
  <div class="demo cs10">Jumping to col 10</div>
  <div class="demo cw10 cs2">10-wide, starting at col 2</div>
</div>

```html
<div class="full cols col-fourth">
  <div class="demo">cw3 by default</div>
  <div class="demo cw5">explicitly cw5</div>
  <div class="demo cw2">cw2</div>
  <div class="demo cw2">cw2</div>
  <div class="demo cw6 cr3">cw6 spanning 3 rows</div>
  <div class="demo">default</div>
  <div class="demo">default</div>
  <div class="demo cw6">cw6</div>
  <div class="demo cw12 ord-last">Full-width and moved to end using .ord-last</div>
  <div class="demo cs10">Jumping to col 10</div>
  <div class="demo cw10 cs2">10-wide, starting at col 2</div>
</div>
```

### Flex

A third possibility is to build up your own layout using `display: flex` (normally via the `.d-flex` utility class) along with helper classes made available by AvecCSS. This is not as rigid as the above options but does require some knownledge of CSS.

Here is a simple example that might represent a rather unstructured collection of differently-sized thumbnails:

<div class="d-flex f-jc-center f-alit-center f-wrap">
  <div class="demo m-1" style="width:150px; height: 200px"></div>
  <div class="demo m-1" style="width:170px; height: 120px"></div>
  <div class="demo m-1" style="width:160px; height: 210px"></div>
  <div class="demo m-1" style="width:150px; height: 150px"></div>
  <div class="demo m-1" style="width:160px; height: 210px"></div>
  <div class="demo m-1" style="width:150px; height: 200px"></div>
  <div class="demo m-1" style="width:160px; height: 210px"></div>
  <div class="demo m-1" style="width:150px; height: 150px"></div>
  <div class="demo m-1" style="width:170px; height: 120px"></div>
</div>

```html
<div class="d-flex f-jc-center f-alit-center f-wrap">
  <div class="demo m-1" style="width:150px; height: 200px"></div>
  <div class="demo m-1" style="width:170px; height: 120px"></div>
  <div class="demo m-1" style="width:160px; height: 210px"></div>
  <div class="demo m-1" style="width:150px; height: 150px"></div>
  <div class="demo m-1" style="width:160px; height: 210px"></div>
  <div class="demo m-1" style="width:150px; height: 200px"></div>
  <div class="demo m-1" style="width:160px; height: 210px"></div>
  <div class="demo m-1" style="width:150px; height: 150px"></div>
  <div class="demo m-1" style="width:170px; height: 120px"></div>
</div>
```

Another example emulating the effect of `grid-xs c2 c3-sm c4-md c5-lg`, similar to one of the grid examples seen above:

<div class="d-flex f-wrap m-neg-1 fc-00a">
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
</div>

```html
<div class="d-flex f-wrap m-neg-1 fc-00a">
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
  <div class="w50 w33-sm w25-md w20-lg"><div class="demo">item</div></div>
</div>
```

The flex helper classes are as follows:

- On the flex container (`.d-flex` or similar): 
  - `.f-dir-row`, `f-dir-col`: flex-direction.
  - `.f-wrap`, `f-nowrap`: flex-wrap.
  - `.f-jc-{start|end|center|between|around|evenly}`: justify-content.
  - `.f-alit-{start|end|center|base|stretch}`: align-items.
- On the flex container but (also or only) affecting the immediate children:
  - `.m-neg-{1|2}`: sets negative margin on the container but also the
    corresponding padding on the children.
  - `.fc-{0|1}{0|1}{0|a}`: Sets the `flex` shorthand property on the children
    (grow, shrink, basis).
- On the children:
  - `.grow-{0|1|2|3}`: flex-grow.
  - `.basis-{a|0|fill}`: set flex-basis to `auto`, `0` or `100%`, respectively.
  - `.als-{start|end|center|base|stretch}`: align-self.
