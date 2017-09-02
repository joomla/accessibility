# Dialog (Modal)
## What is this
**Purpose**:

A Dialog enables the user to get information or handle a form and enter data, without leaving the primary window. A Dialog starts when the user activates a button or a Link which acts as button.

For accessibility this link or button should inform the user that it opens a Modal Dialog.

**Description**:

Dialogs are most often used to prompt the user to enter or respond to information.

A dialog that is designed to interrupt workflow is usually modal. ****Windows under a modal dialog are inert. That is, users cannot interact with content outside an active dialog window. Inert content outside an active dialog is typically visually obscured or dimmed so it is difficult to discern, and in some implementations, attempts to interact with the inert content cause the dialog to close.

Modal Dialogs are only usable when JS is enabled.

## Accessibility
### Accessibility specification

Accessible dialog is defined in WAI-ARIA Authoring Practices 1.1.

* See: [2.9 Dialog (Modal)](https://www.w3.org/TR/wai-aria-practices-1.1/#dialog_modal)
* See about role ddialog: [WAI-ARIA 1.1.](https://www.w3.org/TR/2016/CR-wai-aria-1.1-20161027/#dialog)

### Small Screens

To make the content easier to read when displayed on small screens, the dialog fills 100% of the screen. Completely covering the background window also hides background movement that occurs on some mobile devices when scrolling content inside the dialog and

Modal Windows are difficult not only for blind but for unexperienced users.

Inexperienced users who do not understand the principle of overlaying windows try to close the modal by closing the tab itself and therefore the whole application. This may cause the loss of a input in a form.

### Keyboard Interaction

**Open Dialog**

When a dialog opens, focus placement depends on the nature and size of the content.

* In all circumstances, focus moves at open event to an element contained in the dialog.
* Unless a condition where doing otherwise is advisable, focus is initially set on the first focusable element.
* If content is large enough that focusing the first interactive element could cause the beginning of content to scroll out of view, it is advisable to add tabindex="-1" to a static element at the top of the dialog, such as the dialog title or first paragraph, and initially focus that element.
* If a dialog contains the final step in a process that is not easily reversible, such as deleting data or completing a financial transaction, it may be advisable to set focus on the least destructive action, especially if undoing the action is difficult or impossible. Alert Dialog Pattern is often employed in such circumstances.
* If a dialog is limited to interactions that either provide additional information or continue processing, it may be advisable to set focus to the element that is likely to be most frequently used, such as an OK or Continue button.
* If there is a long modal window possible (i.e. a list to select an entry) it is good practice, to set a cancel-button also on the top of the window. This prevents the user - also the user with mouse - to scroll down.
* Give the user an information how he can quit the Modal, this helps also inexperienced users who do not understand the principle of the overlaying window.

**Work in Dialog**

Modal dialogs contain their tab sequence. That is, Tab and Shift + Tab do not move focus outside the dialog. However, unlike most non-modal dialogs, modal dialogs do not provide means for moving keyboard focus outside the dialog window without closing the dialog. (Important

In the following description, the term tabbable element refers to any element with a tabindex value of zero or greater. Note that values greater than 0 are strongly discouraged.)

* The tab sequence of all dialogs must include a visible element with role button that closes the dialog, such as a close icon or cancel button. It is recommended that the dismiss button is over the fold if the modal window becomes larger.
* When a dialog opens, focus moves to an element inside the dialog. See notes below regarding initial focus placement.
**Tab**:
* Moves focus to the next tabbable element inside the dialog.
* If focus is on the last tabbable element inside the dialog, moves focus to the first tabbable element inside the dialog.
**Shift + Tab**:
* Moves focus to the previous tabbable element inside the dialog.
* If focus is on the first tabbable element inside the dialog, moves focus to the last tabbable element inside the dialog.
**Escape**: Closes the dialog.

**Close Dialog**

When a dialog closes, focus returns to the element that invoked the dialog unless either:
* The invoking element no longer exists. Then, focus is set on another element that provides logical work flow.
* The work flow design includes the following conditions that can occasionally make focusing a different element a more logical choice:
* It is very unlikely users need to immediately re-invoke the dialog.
* The task completed in the dialog is directly related to a subsequent step in the work flow.

For example, a grid has an associated toolbar with a button for adding rows. the Add Rows button opens a dialog that prompts for the number of rows. After the dialog closes, focus is placed in the first cell of the first new row.

### Screenreader Interaction

[... ]

### Mouse Interaction

[... ]

### Touch Interaction

[... ]

## ARIA markup

* The element that serves as the dialog container has a role="dialog". 
* All elements required to operate the dialog are descendants of the element that has role dialog.
* The dialog container element has aria-modal="true". 
* The dialog has either:
  * A value set for the aria-labelledby property that refers to a visible dialog title.
  * A label specified by aria-label.
* Optionally, the aria-describedby property is set on the element with the dialog role to indicate which element or elements in the dialog contain content that describes the primary purpose or message of the dialog. Specifying descriptive elements enables screen readers to announce the description along with the dialog title and initially focused element when the dialog opens.

* **aria-labelledby="IDREF"**: Gives the dialog an accessible name by referring to the element that provides the dialog title. 
* **aria-describedby="IDREF"**: Gives the dialog an accessible description by referring to the dialog content that describes the primary message or purpose of the dialog. Used in three of the four dialogs included in the example. See the above accessibility features section for an explanation.
* **aria-modal="true"**: Tells assistive technologies that the windows underneath the current dialog are not available for interaction (inert).

## Usability

Modal windows are difficult not only for blind but for unexperienced users.

Inexperienced users who do not understand the principle of overlaying windows try to close the modal by closing the tab itself and therefore the whole application. This may cause the loss of a input in a form.

### When to use

* If content should be hidden when the window is open.
* If content or form is dynamically created depending on what the user has entered before

### When to consider something else

* If the modal contains a form, the user cannot print it if he wants to have a copy of his input. This is only important if a dialog contains a form, for example for a booking / reservation. If this is important, find another solution (Or a solution for printing only the content of the modal). This is a general problem of modal dialogs, no topic for accessibility.

### Use in Joomla

* Backend: The Batch Functionality in com_menu
* JFormField: Users - com_content, com_contact
* JFormField: Categories - com_content, com_contact
* Media manager
* Color picker
* Calendar

* Nearly all 3rd party components use this technique.

## Code patterns for Joomla and Joomla extension

### Current

**In 3.7.x Layout for modals, backend and frontend**

* [Github/Joomla/joomla-cms/layouts/joomla/modal/](https://github.com/joomla/joomla-cms/tree/staging/layouts/joomla/modal)

By tabbing you cannot come to the cancel button.

**Batch features in backend**: 

As for example com_banners:

Joomla Components use the 

```php
JHtml::_('behavior.modal');
```
See: administrator/components/com_banners/views/banners/tmpl/default.php

https://github.com/joomla/joomla-cms/blob/3.8-dev/libraries/cms/html/bootstrap.php#L254

### Improved

In Joomla V 4.0 use [Bootstrap v4](https://v4-alpha.getbootstrap.com/components/modal/) class="modal" especially:

"Be sure to add role="dialog" and aria-labelledby="...", referencing the modal title, to .modal, and role="document" to the .modal-dialog itself. Additionally, you may give a description of your modal dialog with aria-describedby on.modal."


## Resources

### Design Patterns

* [WAI ARIA Practices 1.1 - dialog](https://www.w3.org/TR/wai-aria-practices-1.1/examples/dialog-modal/dialog.html)
* [W3C using ARIA role=dialog](https://www.w3.org/WAI/GL/wiki/Using_Aria_role%3Ddialog_to_implement_a_modal_dialog_box)
* [Bootstrap (v4) Modal](https://v4-alpha.getbootstrap.com/components/modal/)
* [Accessible jQuery-ui Components (Dialog Widget)](https://hanshillen.github.io/jqtest/)
* [Open Ajax Accessibility ex. 2](http://oaa-accessibility.org/example/2/)
* [Mozilla Org Accessibility ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_dialog_role)
* [harvard.edu Keyboard Interaction](https://accessibility.huit.harvard.edu/support-keyboard-interaction)
* [Making an accessible dialog box by ENZOnline](https://www.nczonline.net/blog/2013/02/12/making-an-accessible-dialog-box/) 
* [Modal Dialog - Code Library of Accessibility Examples by Deque](https://dequeuniversity.com/library/aria/popups-dialogs/sf-modal-dialog)

### Articles
* [How to Build WAI-ARIA Modal Alert Dialogs: A11y Support Series](https://www.deque.com/blog/aria-modal-alert-dialogs-a11y-support-series-part-2/)
* [Creating An Accessible Modal Dialog](https://bitsofco.de/accessible-modal-dialog/)
* [jQuery simple and accessible modal window, using ARIA](https://a11y.nicolas-hoffmann.net/modal/)
* [The Incredible Accessible Modal Window](https://www.npmjs.com/package/accessible-modal-dialog)

## Notes

There are different types of dialogs which overlay the primary window.

* **Lightboxes** - Overlay the primary window but the main window can be reached by the user. An interaction with the primary window closes the lightbox. In general used for presenting images.
* **Modal Dialogs** - The user cannot interact with the underlying (main) window until he closes the Modal. In general, dialogs contain forms with input fields.
* **Messages**: Overlaying windows which do not contain input fields, and in general do not make the main window inert.
* **Alerts**: Overlaying windows which may require an (.. Bestätigung durch den user)
* Popovers, Tooltips

This document is on modal dialog windows.
