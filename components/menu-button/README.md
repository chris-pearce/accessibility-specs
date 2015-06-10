# Menu Button




## Description

>> A menu button is a push button that is used to invoke a menu. It appears as a normal button typically with a downward pointing arrow or triangle as a visual cue that it triggers the display of a menu.

>> Menu buttons are used in situations where authors want to provide a single menu without having to construct a complete menu bar.

>> When presenting the menu, ensure that it is completely visible on screen.
<br>
—<http://www.w3.org/TR/wai-aria-practices/#menubutton>




## Terminology

- **Container**—the containing element wrapping the menu button and the menu itself.
- **Trigger**—the menu button that invokes the menu.
- **Target**—the menu itself.



## Markup

**No JavaScript**

```html
<div class="js-menu-button">
  <a class="js-menu-button-trigger" href="[id-of-'js-accordion-target']" aria-haspopup="true">[...]</a>
  <div class="js-menu-button-target" id="menu-button-target-1">
    <ul role="menu">
      <li role="presentation">
        <a href="[url]" role="menuitem">[...]</a>
      </li>
      <li role="presentation">
        <a href="[url]" role="menuitem">[...]</a>
      </li>
      [...]
    </ul>
  </div>
</div>
```

**With JavaScript**

```html
<div class="js-menu-button [is-visible]">
  <a class="js-menu-button-trigger [is-visible]" href="[id-of-'js-menu-button-target']" aria-expanded="[true/false]" role="button">[...]</a>
  <div class="js-menu-button-target [is-visible]" aria-hidden="[true/false]" id="menu-button-target-x">
    <ul role="menu">
      <li role="presentation">
        <a href="[url]" role="menuitem" tabindex="-1">[...]</a>
      </li>
      <li role="presentation">
        <a href="[url]" role="menuitem" tabindex="-1">[...]</a>
      </li>
      [...]
    </ul>
  </div>
</div>
```

- `[is-visible]` is the state hook that is toggled according to the **Target** being visible or hidden, by default and when hidden the hook isn't applied, when visible append `is-visible` to the **Container**, **Trigger**, and **Target** elements.
- ARIA attributes having the values 'true' or 'false' are toggled according to the visible or hidden state of the **Target**:
  - **Trigger:** `aria-expanded` by default—and when **Target** is hidden—is 'false', when expanded is 'true'.
  - **Target:** `aria-hidden` by default and when visible is 'true', when expanded is 'false'.
- The `id` attribute on the **Target** element where the "x" is concerned should equal '1' then increment by 1 for each **Target** element e.g. 
  - Menu button **Target** 1: `id="menu-button-target-1"`
  - Menu button **Target** 2: `id="menu-button-target-2"`
  - Menu button **Target** 3: `id="menu-button-target-3"`

**N.B.** if the menu is for navigational purposes then do not apply the following ARIA roles:

- `role="menu"`
- `role="menuitem"`
- `role="presentation"`


## Keyboard interaction

The menu button can be navigated with the following keyboard shortcuts:

- Space or Enter key: with focus on the **Trigger** pressing Space or Enter will toggle the display of the **Target** whilst focus remains on the **Trigger**
- Down Arrow key: 
  - With focus on the **Trigger** and no **Target** visible, pressing Down Arrow key will make the **Target** visible and move focus into the **Target** and onto the first **Target** item. 
  - With focus on the **Trigger** and the **Target** visible, pressing Down Arrow key will move focus into the **Target** onto the first menu item.
- Up and Down Arrow keys: with focus on the **Target**, the Up and Down Arrow keys move focus within the **Target** items, "wrapping" at the top and bottom.
- Escape key: with focus on the **Target**, pressing Escape key closes the menu and returns focus to the **Trigger**.
- Tab key: 
  - With focus on the **Trigger** pressing the Tab key will take the user to the next tab focusable item on the page.
  - With focus on the **Target**, pressing the Tab key will take the user to the next tab focusable item on the page.




## No JavaScript

If JavaScript is disabled then the component will still work by using the CSS `:target` selector to open the drop down menu as the **Trigger** and **Target** are connected via the `id` of the **Target** by the **Trigger** referencing that `id` in its `href` value. 

To close the **Target** this link is provided at the bottom of the **Target** which is only visible to users with JavaScript disabled:

```html
<li role="presentation" class="u-hide-if-js-is-on">
  <a href="#">[X] close menu</a>
</li>
```




## Checklist

<table>
<tbody>
<tr>
<th scope="col" style="text-align: left;">Consideration</th>
<th scope="col" style="text-align: left;">Description</th>
<th scope="col" style="text-align: left;">Yes/No/N.A.</th>
</tr>
<tr>
<th scope="row">Focusable</th>
<td>Can you get to the control via the keyboard? 
<br>Refer to <a href="http://www.w3.org/WAI/PF/aria-practices/#kbd_focus">Providing Keyboard Focus</a></td>
<td></td>
</tr>
<tr>
<th scope="row">Operable</th>
<td>Can you use the control with the keyboard?
<br>Refer to <a href="http://www.w3.org/WAI/PF/aria-practices/#keyboard">Keyboard Navigation</a></td>
<td></td>
</tr>
<tr>
<th scope="row">Expected operation</th>
<td>Can you use the standard keys for the control type to operate it. 
<br>Refer to <a href="http://www.w3.org/WAI/PF/aria-practices/#aria_ex"><abbr title="Accessible Rich Internet Applications">ARIA</abbr> Widget Design Patterns</a></td>
<td></td>
</tr>
<tr>
<th scope="row">Clear indication of focus</th>
<td>Can you easily see it when the control has focus?
<br>Refer to <a href="http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-focus-visible.html">Visible Focus</a> (WCAG2)</td>
<td></td>
</tr>
<tr>
<th scope="row">Label</th>
<td>The control has a text label that is exposed as an <a href="http://www.w3.org/TR/wai-aria/terms#def_accessible_name">accessible name</a> in <a href="http://rawgit.com/w3c/aria/master/html-aam/html-aam.html#introduction-accessibility-apis">accessibility APIs</a></td>
<td></td>
</tr>
<tr>
<th scope="row">Role</th>
<td>The control has an appropriate role exposed in <a href="http://rawgit.com/w3c/aria/master/html-aam/html-aam.html#introduction-accessibility-apis">accessibility APIs</a></td>
<td></td>
</tr>
<tr>
<th scope="row">States and properties</th>
<td>The control has any UI states and properties that it has exposed in <a href="http://rawgit.com/w3c/aria/master/html-aam/html-aam.html#introduction-accessibility-apis">accessibility APIs</a></td>
<td></td>
</tr>
<tr>
<th scope="row">Color contrast</th>
<td> The control label/description/icon is perceivable/usable for low vision users (Use a <a href="http://www.paciellogroup.com/resources/contrastanalyser/">color contrast checker</a>.)</td>
<td></td>
</tr>
<tr>
<th scope="row">High contrast mode</th>
<td>The control is perceivable/usable when High Contrast Mode is enabled (e.g. <a href="http://www.paciellogroup.com/blog/2010/01/high-contrast-proof-css-sprites/">Windows HC mode</a>)</td>
<td></td>
</tr>
</tbody>
</table>




## Examples

- http://simplyaccessible.com/about/
- http://davidtheclark.github.io/react-aria-menubutton/
- http://mpnkhan.github.io/BootStrapExamples/a11yfixes/bs.html
