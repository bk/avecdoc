---
title: Animations
subtitle: Helper classes for simple animations
---

## hover-grow

The `hover-grow` class enlarges the applied element slightly when hovering over it with the mouse.

<button class="hover-grow">Hover me!</button>

```html
<button class="hover-grow">Hover me!</button>
```

## Bounce and fade-in

These classes have a visual effect when the page is loaded or when they are applied to an element after having been absent (using javascript).

In the following examples the effect is demonstrated by applying the class to the admonition containing each link.

<script>
function anim(id, cls) {
  el = document.getElementById(id);
  el.classList.remove(cls);
  el.classList.add(cls);
}
</script>


<div class="admonition info" id="ex1">
  <p class="admonition-title">Bounce</p>
  <p><a href="javascript:anim('ex1', 'bounce')">Click here</a> to see the effect of the <code>bounce</code> class.</p>
</div>

```html
<div class="admonition info bounce">
  <p class="admonition-title">Bounce</p>
  <p><a href="#">Click here</a> to see the effect of the <code>bounce</code> class.</p>
</div>
```

<div class="admonition neutral" id="ex2">
  <p class="admonition-title">Bounce in</p>
  <p><a href="javascript:anim('ex2', 'bounce-in')">Click here</a> to see the effect of the <code>bounce-in</code> class.</p>
</div>

<div class="admonition success" id="ex3">
  <p class="admonition-title">Fade in</p>
  <p><a href="javascript:anim('ex3', 'fade-in')">Click here</a> to see the effect of the <code>fade-in</code> class.</p>
</div>


<div class="admonition danger" id="ex4">
  <p class="admonition-title">Fade in from the left</p>
  <p><a href="javascript:anim('ex4', 'fade-in-left')">Click here</a> to see the effect of the <code>fade-in-left</code> class.</p>
</div>

<div class="admonition warning" id="ex5">
  <p class="admonition-title">Fade in from the right</p>
  <p><a href="javascript:anim('ex5', 'fade-in-right')">Click here</a> to see the effect of the <code>fade-in-right</code> class.</p>
</div>

## Pulse

The `pulse` class shows an infinite pulsating opacity effect. This is mainly useful for placeholder content shown while the real content is being loaded from the server.

<div class="admonition neutral pulse">
  <p class="admonition-title">Please wait</p>
  <p>Your information will be shown here... eventually.</p>
</div>
