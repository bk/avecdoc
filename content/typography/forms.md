---
title: Forms
subtitle: Appearance of form elements
---

Buttons have been seen [previously](../basics/). Form elements are kept simple. Here is an example form containing some of them:

<form>
<div class="grid-sm">
 <p>
  <label>Fruit</label>
  <select>
    <option selected="selected" value="1">--please select--</option>
	<option value="2">Apple</option>
    <option value="3">Orange</option>
    <option value="4">Banana</option>
    <option value="5">Papaya</option>
    <option value="6">Other</option>
	</select>
 </p>
 <p>
  <label>Name</label>
  <input type="text" name="name" required>
 </p>
</div>
<div class="grid-sm">
 <p>
  <label>Email</label>
  <input type="email" name="email" required>
 </p>
 <p>
  <label>Phone</label>
  <input type="text" name="phone">
 </p>
</div>
<div class="cols">
 <p class="cw3-sm">
  <label>Widget type:</label>
  <label><input checked name="type" type="radio" value="a"> Recusandae</label>
  <label><input name="type" type="radio" value="b"> Blanditis</label>
  <label><input name="type" type="radio" value="c"> Excepturi</label>
 </p>
 <p class="cw9-sm">
  <label>Message</label>
  <textarea rows="6"></textarea>
 </p>
</div>
 <p>
  <label>
  <input type="checkbox" id="checkbox" value="terms">
  I agree to the <a href="#">terms and conditions</a>
  </label>
 </p>

  <button>Send</button>
  <button type="reset" class="bg-error">Reset</button>
  <button disabled="disabled">Disabled</button>
</form>

One thing to note here is that the reset button has a `bg-error` class so as to make it red, and most elements have been placed into a grid or into columns using the `grid` and `cols` classes. Both of these will be discussed later.

