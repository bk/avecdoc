---
title: Basic typography
subtitle: Basic appearance of common elements
---

## Body text

The user's base font size is left unchanged. For most people, it is 16px.

The font size for body text is set to 1.125rem by default, which accordingly means 18px in most cases.

The font size of most text elements is set in rems (if it its size is changed from the body text size at all).

Spacing units (margins and padding) are rem-based as well.

The theme determines if the default font is a serif or a sans-serif. The default theme sets the text font to serif but the font of headings to sans-serif. For more on themes, see later in this document.

## Headings

The sizes of headings are as follows by default:

- H1 is about 2.616rem or 42px (again, assuming a base font size of 16px).
- H2 is about 1.992rem or 32px.
- H3 is about 1.549rem or 25px.
- H4 is about 1.273rem or 20px.
- H5 is 1.125 rem or 18px.
- H6 is 1rem or 16px.

Headings can be grouped in `<hgroup>`, normally containing a heading and a subheading of a lower level (although other block elements, such as `<p>`, may also be used). This reduces the size of the subordinate heading and renders it in a muted color.

```html
<hgroup>
  <h2>The Roman Empire</h2>
  <h3>Its rise, decline and fall</h3>
</hgroup>
```

## Links and buttons

<div>
  <a href="#">This is a normal link</a>
  <button>This is a plain button</button>
  <a href="#" role="button">A button-like link</a>
  <a href="#" class="text">A link with the .text class</a>
</div>

You make links (and some other elements) look like buttons by adding `role="button"`.
See also the page on [forms](../forms/).

## Inline formatting

- **bold**, *italic*, <u>underlined</u>
- Sub<sub>script</sub> and super<sup>script</sup>.
- <mark>Highlighted</mark> (using `<mark>`)
- Inline code: `<code>`.
- Keyboard commands like <kbd>Ctrl-K</kbd>: `<kbd>Ctrl-K</kbd>`.

## Lists

Not much has been done to modify the default appearance of lists.

Bulleted list with one level of nesting:

- List item of first level
- Second list item
    - Sublist starts here
    - and continues here
    - until we reach the third item
- We now return to the first level.

Numbered list:

1. item one
2. item two
3. item three

Definition lists:

<dl>
<dt>First term</dt>
<dd>Definition of term 1</dd>
<dt>Second term</dt>
<dd>Definition of term 2</dd>
</dl>

## Blockquote

The source/author can be given with `<cite>` if desired.

> Laudantium nisi molestiae facere ullam. Eos eius fuga et optio nulla explicabo totam. Corrupti culpa vero tempore. Consectetur sint ut consequatur. Nam quae voluptatum optio vel.
> <cite>– Marcus Tullius Cicero</cite>

## Code block

A code block is `<pre>`, often with `<code>` immediately inside. As an example, the preferred structure for an HTML document using AvecCSS:

```html
<!DOCTYPE html>
<html>
  <head>...</head>
  <body>
    <header>...</header>
    <main>...</main>
    <footer>...</footer>
  </body>
</html>
```

