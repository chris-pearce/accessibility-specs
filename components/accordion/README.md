# Accordion




## Description

> An accordion component is a collection of expandable panels associated with a common outer container. Panels consist of a header and an associated content region or panel. The primary use of an Accordion is to present multiple sections of content on a single page without scrolling, where all of the sections are peers in the application or object hierarchy. The general look is similar to a tree where each root tree node is an expandable accordion header. The user navigates and makes the contents of each panel visible (or not) by interacting with the Accordion Header.
<br>
—<http://www.w3.org/TR/wai-aria-practices/#accordion>




## Terminology

- **Container**—the containing element wrapping all accordion items.
- **Trigger**—the accordion item label and control that expands and collapses its corresponding **Target**.
- **Target**—the containing element wrapping the content associated with the **Trigger**.



## Markup

**No JavaScript**

```html
<x class="js-accordion">
  <x class="js-accordion-trigger">[...]</x>
  <x class="js-accordion-target">[...]</x>
</x>
```

**With JavaScript**

```html
<x class="js-accordion" role="tablist" aria-multiselectable="true">
  <x class="js-accordion-trigger [is-expanded]" id="[accordion-trigger-x]" aria-controls="[id-of-'js-accordion-trigger']" aria-selected="[true/false]" aria-expanded="[true/false]" tabindex="[-1/0]" role="tab">[...]</x>
  <x class="js-accordion-target [is-expanded]" id="[accordion-target-x]" aria-labelledby="[id-of-'js-accordion-target']" aria-hidden="[true/false]" role="tabpanel">[...]</x>
</x>
```

- `[is-expanded]` is the state hook that is toggled according to the expanded or collapsed state of the accordion item, by default and when collapsed the hook isn't applied, when expanded then append `is-expanded` to both the **Trigger** and **Target** elements.
- ARIA attributes having the values 'true' or 'false' are toggled according to the expanded or collapsed state of the accordion item:
  - **Trigger:** `aria-selected` and `aria-expanded` by default and when collapsed is 'false', when expanded is 'true'.
  - **Target:** `aria-hidden` by default and when collapsed is 'true', when expanded is 'false'.
- The `id` attributes where the "x" is concerned should equal '1' then increment by 1 for each accordion item **Trigger** and **Target** elements e.g. 
  - Item 1: `id="accordion-trigger-1"` / `id="accordion-target-1"`
  - Item 2: `id="accordion-trigger-2"` / `id="accordion-target-2"`
  - Item 3: `id="accordion-trigger-3"` / `id="accordion-target-3"`
- The `tabindex` attribute for the **Trigger** element by default and when collapsed is `tabindex="-1"`, when expanded is `tabindex="0"`.




## Keyboard interaction

The accordion takes up one tab stop in the tab order. It can be navigated with the following shortcuts:

- Up or Left Arrow: move focus to the previous **Trigger**
- Down or Right Arrow: move focus to the next **Trigger**
- Space and Enter key: expand the currently focused **Trigger**
- Home: move focus to the first **Trigger**
- End: move focus to the last **Trigger**

The kitchen sink: [Keyboard interaction](http://www.w3.org/TR/wai-aria-practices/#accordion).




## No JavaScript

[TODO]




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

[TODO]
