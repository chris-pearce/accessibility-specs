# Accessibility specifications for UI components

*This is a living document.*

**NOTE**

- `x` equals any element in markup blocks.
- The following conventions are used for DOM hooks:
  - [State hooks](https://github.com/chris-pearce/css-guidelines#state-hooks)
  - [JS hooks](https://github.com/chris-pearce/css-guidelines#javascript-hooks)

---

## Accordion

### Description

>> An accordion component is a collection of expandable panels associated with a common outer container. Panels consist of a header and an associated content region or panel. The primary use of an Accordion is to present multiple sections of content on a single page without scrolling, where all of the sections are peers in the application or object hierarchy. The general look is similar to a tree where each root tree node is an expandable accordion header. The user navigates and makes the contents of each panel visible (or not) by interacting with the Accordion Header.
<br>
—<http://www.w3.org/TR/wai-aria-practices/#accordion>

### Terminology

- **Container:** the containing element wrapping all accordion items.
- **Trigger:** the accordion item label and control that expands and collapses its corresponding **Target**.
- **Target:** the containing element wrapping the content associated with the **Trigger**.

### Markup

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

- `[is-expanded]` the state hook that is toggled according to the expanded or collapsed state of the **Trigger** and **Target** elements.
- `id` attribute, "x" = 1 then increment by 1 for each **Trigger** and **Target** e.g. `id="accordion-trigger-1"`, `id="accordion-target-1"`.
- `tabindex="[-1/0]"`, default is `tabindex="-1"`, when **Target** is expanded change to `tabindex="0"`.

### Keyboard interaction

The accordion takes up one tab stop in the tab order. It can be navigated with the following shortcuts:

- Up or Left Arrow: move focus to the previous **Trigger**
- Down or Right Arrow: move focus to the next **Trigger**
- Space and Enter key: expand the currently focused **Trigger**
- Home: move focus to the first **Trigger**
- End: move focus to the last **Trigger**

The kitchen sink: [Keyboard interaction](http://www.w3.org/TR/wai-aria-practices/#accordion).

### No JavaScript

[TODO]
  
