# Radio buttons

## What is this

**Purpose**: Users must choose between two or more mutually exclusive options. Radio buttons allow users to see all available choices at once and select exactly one option.

**Description**:

 - Radio buttons come in a group of two or more mutually exclusive options.
 - A radio button is either checked or unchecked.
 - There can only be one radio button checked in a group.

## Resources

### Design Patterns

* [WAI ARIA practices - Radio group example using roving tabindex](https://www.w3.org/TR/wai-aria-practices-1.1/examples/radio/radio-1/radio-1.html)
* [WAI ARIA practices - Radio group example using managed focus with aria-activedescendant](https://www.w3.org/TR/wai-aria-practices-1.1/examples/radio/radio-2/radio-2.html)
* [U.S. Web Design Standards ](https://standards.usa.gov/components/form-controls/)
* [Open Ajax Accessibility ex. 28  - Radiogroup](http://oaa-accessibility.org/example/28/)
* [Open Ajax Accessibility ex. 29 Radiogroup: aria-activedescendant](http://oaa-accessibility.org/example/29/)
* [Live demo: ARIA radio buttons by http://whatsock.com ](http://whatsock.com/tsg/Coding%20Arena/ARIA%20Radio%20Buttons/ARIA%20Radio%20Buttons/demo.htm)
* [Checkboxes and Radio Buttons by Deque](https://dequeuniversity.com/library/aria/custom-controls/sf-checkboxes-radios)

### Articles

* [The ARIA Role Matrices](http://whatsock.com/training/matrices/)
* [Toggle Buttons](https://inclusive-components.design/toggle-button/)
* [Accssible component modules: Aria Toggles, Checkboxes and Switches](http://whatsock.com/tsg/)

## Accessibility specification

Accessible radio buttons specification is defined in WAI-ARIA Authoring Practices 1.1.

See: [2.18 Radio Group](https://www.w3.org/TR/wai-aria-practices-1.1/).

## Accessibility

### Keyboard Interaction

Tabbing into the group will set focus on the currently checked radio button. If no button is currently checked, focus will move to the first button or the last depending on whether TAB or SHIFT+TAB was used to enter the group.

* **Tab and Shift+Tab: **Moves keyboard focus to the checked radio button in a radiogroup.
If no radio button is checked, focus moves to the first radio button in the group.
* **Space:**  If the radio button with focus is unchecked, it's state will be changed to checked.
* **Right**and **Down arrow:** Moves focus to next radio button in the group.
If focus is on the last radio button in the group, move focus to the first radio button.
* **Left**and **Up arrow:** Moves focus to previous radio button in the group.
If focus is on the first radio button in the group, move focus to the last radio but
* **Enter:**  Submits the form that the radio group belongs to.

### Screen reader Interaction

* Radio **must** be reachable with screen reader (even when disabled).
* Radio **must** be announced as "Radio".
* Radio label **must** be announced.
* Radio group label, if applicable, **must** be announced.
* Radio state **must** be announced (checked or unchecked).

### Mouse / Pointer Interaction

* Clicking radio **must** toggle the checked state.
* Clicking radio label **must** toggle the checked state.

### Touch Interaction

* Tapping radio **must** toggle the checked state.
* Tapping radio label **must** toggle the checked state.

ARIA markup

| **Role** | **Attributes** | **Element** | **Usage** |
| --- | --- | --- | --- |
| radiogroup | - | div | The role="radiogroup" attribute identifies the div element as a container for a group of radio buttons.The descendent radio buttons are considered part of the group.The accessible name comes the aria-labelledby attribute, which points to the element that contains the label text.The radiogroup widget does not need a tabindex value, since the ul[role"radiogroup"] element never receives keyboard focus. |
| - | aria-labelledby="[IDREF]" | div | The aria-labelledby attribute points to the element that contains the test for defining an accessible name (e.g. label) for the group of radio buttons. |
| radio | - | div | The role="radio" attribute identifies the div element as an ARIA radio button.The accessible name comes the child text content of the div element.The radio widget has a manged tabindex value, one radio button must have a tabindex="0" and the rest of the daio buttons in the group a tabindex="-1".See HYPERLINK "https://www.w3.org/TR/wai-aria-practices-1.1/" \l "kbd\_roving\_tabindex" roving tabindex for more information |
| - | tabindex="-1" | div | All radio buttons in a group that are unchecked, except for the first radio button in the case when no radio buttons are checked.[See roving tabindex for more information][7] |
| - | tabindex="0" | div | The radio button that is checked, or if no radio button is checked the first radio button in the radio group.[See roving tabindex for more information][8] |
| - | aria-checked="false" | div | Indentifies the radio button is not checked.CSS attribute selectors (e.g. [aria-checked="false"]) are used to synchronize the visual states with the value of the aria-checked attribute.The CSS :before psuedo selector and the content property is used to indicate visual state of unchecked to support high contrast setting in operating systems and browsers. |
| - | aria-checked="true" | div | Indentifies the radio button is checked.CSS attribute selectors (e.g. [aria-checked="true"]) are used to synchronize the visual states with the value of the aria-checked attribute.The CSS :before psuedo selector and the content property is used to indicate visual state of checked to support high contrast setting in operating systems and browsers. |

### Why is it important?

[...]

Utilities

### When to use

* When users need to select only one option out of a set of mutually exclusive choices.
* When the number of available options can fit onto a mobile screen.

### When to consider something else

* Consider checkboxes if users need to select more than one option or if there is only one item to select.
* Consider a dropdown if you don't have enough space to list out all available options.
* If users should be able to select zero of the options.

### Use in Joomla

* [...]

Best practices

* Users should be able to tap on or click on either the text "label" or the radio button to select or deselect an option.
* Options that are listed vertically are easier to read than those that are listed horizontally. Horizontal listings can make it difficult to tell which label pertains to which radio button.
* If you customize, make sure selections are adequately spaced for touch screens.
* Use caution if you decide to set a default value. Setting a default value can discourage users from making conscious decisions, seem pushy, or alienate users who don't fit into your assumptions. If you are unsure, leave nothing selected by default..
* Radio button labels should use sentence casing.
* Use concise labels.
* Provide an initially checked option when the field is not required and/or there is a sane default.
* Align vertically when possible.
* Align in shorter columns if there are many options.
* Ensure there is adequate spacing between adjacent fields and radio/checkbox groups.

## Code patterns for Joomla and Joomla extension

### Current
[...]

### Improved
[...]

## WCAG Reference
* **[1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-programmatic)** - Level A
* **[1.3.3 Sensory Characteristics](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-understanding)** - Level A 
* **[2.1.1 Keyboard](https://www.w3.org/WAI/WCAG20/quickref/#keyboard-operation-keyboard-operable)** - Level A
* **[4.1.2 Name, Role, Value](https://www.w3.org/WAI/WCAG20/quickref/#ensure-compat-rsv)** - Level A
