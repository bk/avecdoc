---
title: Utility classes
subtitle: Generic classes that often make custom CSS unneccesary
---

## Spacing

Margins and spacing are indicated with classnames following the pattern `<prefix><direction>-<unit>`, where `<prefix>` is either `m` for margin or `p` for padding, `direction` is either empty or one of `t`, `r`, `b` or `l` (for top, right, bottom and left, respectively); whereas `<unit>` is either a number between 0 and 5, the word `half`, or `a` for `auto` (`a` is for `m` only).

The numbers (as well as `half`) indicate how many spacing units to apply. By default, the spacing unit is 0.625rem (i.e. 10px).

For instance, `ml-a mr-a mb-2 p-half` means horizontal centering, a bottom margin of 20px and a padding of 5px (unless the base font size or the `--spacing` css variable have been changed).

There is currently no support for responsive spacing (i.e. spacing for specific screen widths).

## Visibility

A collection of classes with the pattern `seen-<m><s><d>` where `<m>`, `<s>` and `<d>` are either 1 (for visible) or 0 (for invisible) control in which breakpoints the element with the class can be seen. The breakpoints are the following: `<m>` is mobile (i.e. the `xs` and below), `<s>` is tablet and small desktop, i.e. the `sm` and `md` breakpoint range, and `<d>` is `lg` and up. For instance, `seen-100` means that the element with this class should only be visible in mobile.

If you use a `seen-*` class on an inline element you must add the `inl` class as well so as to indicate that it is inline. Similarly, if you use it on a table, you need to add the `tbl` class as well.

The class `hidden` is an alias for `seen-000`, and `shown` is an alias for `seen-111`.

You can also hide something in a specific brekapoint range with `hidden-md`, `hidden-sm`, `hidden-lg` and `hidden-lg`. These can be combined with `seen-*` in order to make an element visible only at a specific breakpoint as follows:

- mobile only (anything below `sm`) = `seen-100`
- sm-only = `seen-010 hidden-md`
- md-only = `seen-010 hidden-sm`
- lg-only = `seen-001 hidden-xl`
- xl-only = `seen-001 hidden-lg`

## Display

There are three base classes for setting `display` values: `.d-block`, `.d-inl` (which sets `inline-block`), and `.d-flex`. There are also responsive versions of these (such as `.d-flex-sm`) for the breakpoints `sm`, `md`, `lg` and `xl`. Currently there are no special classes for other values of `display`, such as `none`, `table`, `table-cell` and so on (except in combination with the `seen-*` utilities as described above).

## Border and border-radius

A class following the pattern `b<direction>-<amount>` affects the borders of the element to which it is applied. Here `<direction>` is either `t`, `r`, `b`, or `l` (for each of the four sides), or `a` (for all sides); whereas `<amount>` is either 0, 1, 2 or 4, which indicates the number of pixels.

The class `borad` applies the border-radius in the `--border-radius` CSS variable (5px by default).

The class `borad-0` sets the border-radius to 0.

The class `borad-round` applies a border-radius of 50%, making square elements look circular.

## Width

The width of an element can be set with a class following the pattern `w<amount>`, where `<amount>` is one of 0, 10, 20, 25, 33, 40, 50, 66, 75, 80, or 100. These numbers stand for the percentage of the available space. (Here, 33 actually means 33.333333%, and 66 66.666666%, but the other percentages are exact).

The widths can be made responsive by appending a breakpoint postfix. For instance, `w100 w50-sm w33-lg` means 100% width in mobile, 50% width in tablet and small desktop and 1/3 width in normal desktops/laptops.

The class `wa` sets width to `auto`. Breakpoint postfixes can be appended to this as well.

## Fonts

### Font family

The classes `sans`, `serif` and `mono` set the font-family for their targets to the configured values of the CSS variables `--sans-font`, `--serif-font` and `--mono-font`, respectively.

### Font size

The classes `larger` and `smaller` apply the relative font size keywords `larger` and `smaller` to the given element and its descendants. The effect may differ slightly between browsers. Commonly `smaller` means 83.33% and `larger` 120% of the base font size.

## Color and background

Foreground or text color can be set with the following classes: `text-vivid`, `text-accent`, `text-muted`, `text-reverse`, `text-success`, `text-warning`, `text-error`, `text-info`, `text-normal`.

Background color can be set with the following classes: `bg-accent`, `bg-contrast`, `bg-marked`, `bg-reverse`, `bg-success`, `bg-warning`, `bg-error`, `bg-info`, `bg-normal`, `bg-card`.

For buttons and button-like elements, an outline style can be turned on by adding the class `outline`. The foreground and border color on such buttons can be controlled with the additional classes `success`, `error`, `warning`, `info`, or `plain`. (The last of these gives the button the default text foreground color).

The colors which are applied are from the active theme. They are registered in CSS variables which mostly have names similar to the class names.

## Alignment

The classes `ta-l`, `ta-r` and `ta-c` set text-align to left, right or center, respectively.

Th classes `fl-r` and `fl-r` apply `float: right` and `float: left`, respectively. To this you may add `cl-r` or `cl-l` for `clear: right` and `clear: left`, respectively. The parent of a floated child may benefit from the `clearfix` class.


## X-scroll

Add the class `x-scroll` to a wrapper to allow content inside the wrapper to scroll horizontally if needed. This is mainly useful for large tables so as to make them accessible in mobile: `<div class="x-scroll"><table>...</table></div>`.

