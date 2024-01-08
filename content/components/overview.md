# Components

None of the components below require javascript. The interactive ones (main menu, modal windows, tabs) use hidden checkboxes or radio buttons as their basis for the CSS selectors. A couple of them (main menu and modal windows) may benefit from some javascript sugar, however – primarily for being able to dismiss them using the <kbd<Esc</kbd> key.

## Cards

Cards are represented using the `<article>` tag. They have a different background and a slight border shadow, making them appear slightly raised. They are best contained in `grid` or `cols` since they lose much of their visual impact if they grow too wide.

Cards can have a footer, a header or both; these have an accented background. Images in the header are handled specially, as can be seen below.

<div class="grid-sm c2 c3-md">
  <article>
    <p>
      A barebones card, without footer, header, heading, image
      – or much of anything, really.
    </p>
  </article>
  <article>
    <header><h4>Good times</h4></header>
    <p>This card has both a header and a footer.</p>
    <footer><p class="smaller ta-c">Footering around</p></footer>
  </article>
  <article>
    <header>
      <a href="#"><img src="/img/dalle.jpg"></a>
    </header>
    <h4>With an image</h4>
    <p>This card has an image (with a link) in the header.
      Note how the image fills the header completely,
      without any padding or margins.</p>
  </article>
</div>

```html
<div class="grid-sm c2 c3-md">
  <article>
    <p>
      A barebones card, without footer, header, heading, image
      – or much of anything, really.
    </p>
  </article>
  <article>
    <header><h4>Good times</h4></header>
    <p>This card has both a header and a footer.</p>
    <footer><p class="smaller ta-c">Footering around</p></footer>
  </article>
  <article>
    <header>
      <a href="#"><img src="/img/dalle.jpg"></a>
    </header>
    <h4>With an image</h4>
    <p>This card has an image (with a link) in the header.
      Note how the image fills the header completely,
      without any padding or margins.</p>
  </article>
</div>
```

## Main menu component

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

## Modal window

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

## Tabs

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

## Hero image

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

## Admonition

An admonition is a message or reminder in the text of the page to alert the reader to something. It can contain a tip, a warning or other content. There are four types of admonitions, distinguished by their colors:

!!! note "Info"
    This is an informational message (info) which may contain a note or a tip. It is blue.

!!! warning "Warning"
    This is a warning message containing a reminder or a non-critical alert. It is orange.

!!! error "Danger"
    This is an error message or an alert about something quite dangerous. It is red.

!!! success "Success"
    This is a success message. We are happy to tell you that it is green.
    
The structure of an admonition is as follows:

```html
<div class="admonition info">
  <p class="admonition-title">Info</p>
  <p>This is an informational message ...</p>
  <p>(Any number of paragraphs may follow here...)</p>
</div>
```

An informational message is the default, so formally the type class `info` can be omitted.

A warning message has the class `caution` or `warning`. An error message has the class `error` or `danger`, and a success message the class `success`.

## Stack

<div class="cols">
<div class="cw8-sm">
A stack is a collection of elements of the same type, stacked on top of each other with the margins between them removed. It is intended for grouping elements with a visible background, such as buttons, as in this example. (See also below for an example with an accordion).
</div>
<div class="cw4-sm stack mt-0">
<button>First button</button>
<button>Second button</button>
<button>Third button</button>
</div>
</div>

```html
<div class="stack">
  <button>First button</button>
  <button>Second button</button>
  <button>Third button</button>
</div>
```

## Accordion

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

## Dropdowns

Dropdowns are also implemented as `<details>` but with a bit more special styling and with stricter requirements on the contents. The `<details>` must have `role="dropdown"` and the immediate children must be a `<summary>` and an `<ul>`, in that order. An example dropdown was shown above in the Nav menu section. Here is another example outside a `<nav>`. It looks somewhat similar to a `<select>`, which is shown on the right for comparison.

<div class="grid-sm">
  <details role="dropdown">
    <summary>Fruit dropdown</summary>
    <ul>
      <li><a href="#">Apple</a></li>
      <li><a href="#">Orange</a></li>
      <li><a href="#">Banana</a></li>
      <li><a href="#">Papaya</a></li>
      <li><a href="#">Other</a></li>
    </ul>
  </details>
  <select>
    <option selected value="1">Fruit select</option>
    <option value="2">Apple</option>
    <option value="3">Orange</option>
    <option value="4">Banana</option>
    <option value="5">Papaya</option>
    <option value="6">Other</option>
  </select>
</div>

```html
<div class="grid-sm">
  <details role="dropdown">
    <summary>Fruit dropdown</summary>
    <ul>
      <li><a href="#">Apple</a></li>
      <li><a href="#">Orange</a></li>
      ...
    </ul>
  </details>
  <select>
    <option selected value="1">Fruit select</option>
    <option value="2">Apple</option>
    <option value="3">Orange</option>
    ...
  </select>
</div>
```

As shown in the Nav example [above](#nav), dropdowns look a bit different in that context: more link-like and with tighter spacing.

A dropdown can be made to look like a button by adding `role="button"` to the `<summary>` tag. If desired, the background color of the button can then be modified by adding a class attributes (e.g. `<summary role="dropdown" class="bg-error">`). Examples (with a `d-inl` class on the `<details>` so as to constrain the buttons to content dimensions):

<div>
  <details role="dropdown" class="d-inl">
    <summary role="button">Fruity goodness</summary>
    <ul>
      <li><a href="#">Apple</a></li>
      <li><a href="#">Orange</a></li>
      <li><a href="#">Banana</a></li>
      <li><a href="#">Papaya</a></li>
      <li><a href="#">Other</a></li>
    </ul>
  </details>
  <details role="dropdown" class="d-inl">
    <summary role="button" class="bg-error">Dangerous types of fruit</summary>
    <ul>
      <li><a href="#">Apple</a></li>
      <li><a href="#">Orange</a></li>
      <li><a href="#">Banana</a></li>
      <li><a href="#">Papaya</a></li>
      <li><a href="#">Other</a></li>
    </ul>
  </details>
</div>

The list shown by the dropdown is normally placed so that its left side aligns with the left side of the `<summary>`. You can change this to the right side by adding `class="rightset"` to the `<ul>`. (The difference between the two is not visible unless the list is broader than the dropdown button, since the minimum width is the same as the button).


## Badges

A badge shows a status indicator or a number which relates to a specific (typically small) element,
often a button, a tab or a navigation item. The value for the badge is given with a `data-badge` attribute.
An empty `data-badge` leads to a badge that is a small dot.

<div class="mb-2">
<button class="badge mr-1" data-badge="917">First</button>
<button class="badge mr-1" data-badge="">Second</button>
<button class="badge" data-badge="✓">Third</button>
</div>

<div>
<a class="badge" data-badge="88" href="#">Whatever</a>
</div>

```html
<div>
  <button class="badge mr-1" data-badge="917">First</button>
  <button class="badge mr-1" data-badge="">Second</button>
  <button class="badge" data-badge="✓">Third</button>
</div>
```
