---
title: CSS variables
subtitle: Settings for colors, fonts and layout
---

## Colors

These variables are defined by the theme. Their specific value depends on whether the light or the dark variety of the theme is active.

- `--accent`: Accent color, used for links.
- `--accent-bg`: Accent background.
- `--bg`: Main background color.
- `--box-shadow`: Box shadow setting (for cards).
- `--border`: Border color.
- `--button-text`: Color of text in buttons.
- `--card-bg`: Background of cards.
- `--code`: Text color for inline `<code>` elements.
- `--code-bg`: Background for inline `<code>` elements.
- `--contrast-bg`: Alternative accent background, contrasting more clearly with `--bg`.
- `--disabled`: Color for disabled buttons.
- `--error`: Color for admonition of type `error`; generally red.
- `--info`: Color for admonition of type `info`; generally blue.
- `--marked`: Background for `<mark>` elements.
- `--mark-text`: Text color for `<mark>` elements.
- `--preformatted`: Background for code blocks.
- `--success`: Color for admonition of type `success`; generally green.
- `--text`: Main text color.
- `--text-heading`: Color for headings.
- `--text-light`: Muted text color.
- `--text-vivid`: Color for vivid text; lighter text in dark themes and darker in light themes.
- `--warning`:  Color for admonition of type `warning`; generally orange.

Themes may in some cases also affect the font settings, but those variables are listed below rather than here.

## Breakpoints

- `--bp-xs`: 480px; wide mobile phone or small tablet above this point, ordinary mobile below it.
- `--bp-sm`: 768px; tablet in portrait mode.
- `--bp-md`: 960px; tablet in landscape mode or small laptop/desktop.
- `--bp-lg`: 1280px; laptop/desktop.
- `--bp-xl`: 1600px; laptop/desktop with large screen.

!!! danger "Read-only breakpoints"
    `@media` queries cannot be based on CSS variables, so these values are **for reference only**. If they are changed after loading the stylesheet, it will probably have unfortunate side effects, as some calculations are based upon them.

## Font settings

The basic font families are in the following variables

- `--mono-font`: Monospaced typeface.
- `--sans-font`: Sans-serif typeface.
- `--serif-font`: Serif typeface.
- `--main-font`: The main body text font; generally identical to either `--sans-font` or `--serif-font`.

The heading typeface may or may not be different from the `--main-font`:

- `--heading-font`: Typeface for headings. Generally the same as `--sans-font`.
- `--heading-weight`: The font-weight for headings. The default is `bold`.

There are several variables for font size:

- `--font-size`: Base size of body text.
- `--h1-size`: Size for H1 headings.
- `--h2-size`: Size for H2 headings.
- `--h3-size`: Size for H3 headings.
- `--h4-size`: Size for H4 headings.
- `--h5-size`: Size for H5 headings.
- `--h6-size`: Size for H6 headings.

## Layout

- `--container-fixed-margin`: Minimum margin for content in main/container in `fixed` mode. The default is 25px.
- `--container-width`: The width for content in main/container in normal mode (when there is room). The default is 54rem.
- `--container-max-width`: Maximum width for content in main/container in normal or `fluid` mode. The default is 92%.

## Grid/column

- `--column-gap`: Gap between columns in a grid or column container; 2 × `--spacing` by default (i.e. 20px in most cases).
- `--row-gap`: Gap between rows in a grid or column conainer; 2 × `--spacing` by default (i.e. 20px in most cases).
- `--grid-min-col-width`: Minimum width of items in a grid; set by default to 60px in mobile and 120px otherwise.

## Other

- `--spacing`: The basic spacing unit, affecting most of the padding and margin settings, as well as few others. Set to 0.625rem by default, which corresponds to 10px for most people.
- `--border-radius`: The border-radius for rounded corners. This is set to half of `--spacing` by default, i.e. generally 5px.

