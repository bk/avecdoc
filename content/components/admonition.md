---
title: Admonitions
subtitle: Messages, alerts and tips
---

An admonition is a message or reminder in the text of the page to alert the reader to something. It can contain a tip, a warning or other content. There are four types of admonitions, distinguished by their colors:

!!! note "Info"
    This is an informational message (info) which may contain a note or a tip. It is blue.


!!! warning
    This is a warning message containing a reminder or a non-critical alert. It is orange.

!!! error "Danger"
    This is an error message or an alert about something quite dangerous. It is red.

!!! success
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

