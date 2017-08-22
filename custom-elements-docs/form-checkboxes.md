# Checkboxes

## What is this

**Purpose**: Users need to specify which option(s) from a set are applicable/valid/true based on a label

**Description**:

* A set of checkboxes are used when a user is able to select none, one, or multiple options
* A single checkbox is used when a user is able to select or not select an option
* When clicked, a checkbox's state toggles between unchecked and checked
* Checkboxes can have an indeterminate state that is set based on external interactions (e.g., indicating that some but not all items in a collection are selected)
* Checkbox labels should use sentence casing
* Use concise labels
* Align vertically when possible
* Align in shorter columns if there are many options
* The selected state of a checkbox should ideally indicate something 'positive' and may require the rephrasing of the label (e.g., Send me weekly reminders, vs. Do not send me weekly reminders)
* Ensure there is adequate spacing between adjacent fields and radio/checkbox groups

## Resources

### Design Patterns

* [WAI ARIA practices - two state ](https://www.w3.org/TR/wai-aria-practices-1.1/examples/checkbox/checkbox-1/checkbox-1.html)
* [WAI ARIA practices - mixed state ](https://www.w3.org/TR/wai-aria-practices-1.1/examples/checkbox/checkbox-2/checkbox-2.html)
* [Accessible jQuery-ui Components ](http://access.aol.com/aegis/)
* [U.S. Web Design Standards ](https://standards.usa.gov/components/form-controls/)
* [Open Ajax Accessibility ex. 8 Checkbox group using ARIA CSS selectors for visual state ](http://oaa-accessibility.org/example/8/)
* [Open Ajax Accessibility ex. 5 Checkboxes using IMG elements for visual state..](http://oaa-accessibility.org/example/5/)
* [Checkboxes and Radio Buttons by Deque](https://dequeuniversity.com/library/aria/custom-controls/sf-checkboxes-radios)

### Accessibility specification

Accessible checkbox specification is defined in WAI-ARIA Authoring Practices 1.1.

See: [2.7 Checkbox](https://www.w3.org/TR/wai-aria-practices-1.1/).

## Accessibility

### Keyboard Interaction

Checkbox can be navigated with the following shortcuts:

* **Tab**: Moves keyboard focus to the checkbox.
* **Space**: Toggle check checkbox between checked and unchecked..

**Behavior**

* When the checkbox is unchecked, all the controlled checkboxes will be unchecked.
* When the checkbox is mixed, all the controlled checkboxes will return to the last state the user selected for that particular checkbox or the default state when the page was loaded.
* When the checkbox is checked, all the controlled checkboxes will be checked.
* Checkbox **must** be keyboard focusable (unless disabled).
* If checkbox has keyboard focus, pressing SPACEBAR **must** toggle the checked state.
* If checkbox has keyboard focus, pressing ENTER key **must** submit the form.
* If checkbox has keyboard focus, pressing TAB key or SHIFT-TAB key combo moves keyboard focus to next or previous interactive element on page respectively.

### Screenreader Interaction

* Checkbox **must** be reachable with screen reader (even when disabled).
* Checkbox **must** be announced as "checkbox".
* Checkbox label **must** be announced.
* Checkbox group label, if applicable, **must** be announced.
* Checkbox state **must** be announced.

### Mouse / Pointer Interaction

* Clicking checkbox **must** toggle the checked state.
* Clicking checkbox label **must** toggle the checked state.

### Touch Interaction

* Taping checkbox **must** toggle the checked state.
* Taping checkbox label **must** toggle the checked state.

## ARIA markup

| Role | Attribute | Element | Usage |
| --- | --- | --- | --- |
| checkbox | - | div | The role="checkbox" attribute identifies the div element as a ARIA checkbox.The accessible name comes the child text content of the div[role="checkbox"] element.The checkbox widget needs a tabindex="0" value. |
| - | tabindex="0" | div | The div["checkbox"] is identified as an ineractive element and is added to the tab order of the page by setting the tabindex="0". |
| - | aria-checked="false" | div | Indentifies the checkbox button as unchecked.CSS attribute selectors (e.g. [aria-checked="false"]) are used to synchronize the visual states with the value of the aria-checked attribute.The CSS :before psuedo selector and the content property are used to indcate visual state of "unchecked" to support high contrast setting in operating systems and browsers. |
| - | aria-checked="true" | div | Indentifies the checkbox as checked.CSS attribute selectors (e.g. [aria-checked="true"]) are used to synchronize the visual states with the value of the aria-checked attribute.The CSS :before psuedo selector and the content property are used to indcate visual state of "checked" to support high contrast setting in operating systems and browsers. |

### Markup in the mixed state

| **Role** | **Attribute** | **Element** | **Usage** |
| --- | --- | --- | --- |
| checkbox | - | div | The role="checkbox" attribute identifies the div element as a ARIA checkbox.The accessible name comes the child text content of the div[role="checkbox"] element.The checkbox widget needs a tabindex="0" value. |
| - | tabindex="0" | div | The div["checkbox"] is identified as an interactive element and is added to the tab order of the page by setting the tabindex="0". |
| - | aria-controls="[IDREFS]" | div | A list of IDREFs identifies which checkboxes are controlled by the mixed checkbox. |
| - | aria-checked="false" | div | Indentifies the checkbox button as not unchecked.This state reflects that all the controlled checkboxes are unchecked.CSS attribute selectors (e.g. [aria-checked="false"]) are used to synchronize the visual states with the value of the aria-checked attribute.The CSS :before psuedo selector and the content property are used to indcate visual state of "unchecked" to support high contrast setting in operating systems and browsers. |
| - | aria-checked="true" | div | Indentifies the checkbox as checked.This state reflects that all the controlled checkboxes are checked.CSS attribute selectors (e.g. [aria-checked="true"]) are used to synchronize the visual states with the value of the aria-checked attribute.The CSS :before psuedo selector and the content property are used to indcate visual state of "checked" to support high contrast setting in operating systems and browsers. |
| - | aria-checked="mixed" | div | Indentifies the checkbox as mixed.This state reflects that some of controlled checkboxes are all checked and some are not checked.CSS attribute selectors (e.g. [aria-checked="mixed"]) are used to synchronize the visual states with the value of the aria-checked attribute.The CSS :before psuedo selector and the content property are used to indcate visual state of "mixed" to support high contrast setting in operating systems and browsers. |

### Why is it important?
[...]

## Utilities
### When to use

* When a user can select any number of choices from a set list.
* When a user needs to choose "yes" or "no" on only one option (use a stand-alone checkbox). For example, to toggle a setting on or off.
* When users need to see all the available options at a glance.

### When to consider something different

* If there are too many options to display on a mobile screen.
* If a user can only select one option from a list (use radio buttons instead).

### Use in Joomla
* [...]

## Best practices
* Surround a related set of checkboxes with a <fieldset>. The <legend> provides context for the grouping. Do not use fieldset and legend for a single check.
* The custom checkboxes here are accessible to screen readers because the default checkboxes are moved off-screen with position: absolute; left: -999em.
* Each input should have a semantic id attribute, and its corresponding label should have the same value in it's for attribute.
* The title attribute can replace <label>.
* Users should be able to tap on or click on either the text label or the checkbox to select or deselect an option.
* List options vertically if possible; horizontal listings can make it difficult to tell which label pertains to which checkbox.
* Avoid using negative language in labels as they can be counterintuitive. For example, "I want to receive a promotional email" instead of "I don't want to receive promotional email."
* If you customize, make sure selections are adequately spaced for touch screens.

## Code patterns for Joomla and Joomla extension

### Current
[...]

### Improved
[...]

## WCAG Reference
4.1.2 Name, Role, Value and 1.3.1, 1.3.3, 2.1.1

## Resources
* [The ARIA Role Matrices](http://whatsock.com/training/matrices/)
* [Toggle Buttons](https://inclusive-components.design/toggle-button/)
* [Accssible component modules: Aria Toggles, Checkboxes and Switches](http://whatsock.com/tsg/)
