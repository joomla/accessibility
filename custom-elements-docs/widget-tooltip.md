# Tooltips [draft]

## What is this

**Purpose**: Users need additional, potentially optional, information on demand.

**Description**: A tooltip is a contextual popup that displays a description for an element. The tooltip typically becomes visible in response to a mouse hover, or after the owning element receives keyboard focus.

## Resources

### Design Patterns

* [WAI ARIA practices - Work on this design pattern is in progress and tracked on Github](https://github.com/w3c/aria-practices/issues/128)
* [Accessible jQuery-ui Components](http://hanshillen.github.io/jqtest/?tabid=tooltip)
* [Bootstrap – ](http://getbootstrap.com/components/)
* [Open Ajax Accessibility ex. 39  - Tooltip](http://oaa-accessibility.org/example/39/) 
* [Open Ajax Accessibility ex. 40 - Tooltip: ARIA CSS selectors](http://oaa-accessibility.org/example/40/)
* [Live demo: Simple Tooltip by http://whatsock.com](http://whatsock.com/tsg/Coding%20Arena/Tooltips/Tooltip%20(Internal%20Content)/demo.htm)
* [PaulJAdam's Modern Web Accessibility Demos](http://pauljadam.com/demos/)
* [jQuery API documentation](http://api.jqueryui.com/tooltip/)
* [Tooltip Dialog by Deque ](https://dequeuniversity.com/library/aria/popups-dialogs/sf-tooltip-dialog)
* [Frend - A collective](https://frend.co/components/tooltip/)
* [ghosh - microtip](https://github.com/ghosh/microtip)

### Articles

* [The ARIA Role Matrices](http://whatsock.com/training/matrices/)
* [Building a fully-accessible help tooltip](https://www.sarasoueidan.com/blog/accessible-tooltips/)
* [How can I make Twitter Bootstrap tooltips accessible?](https://stackoverflow.com/questions/19290384/how-can-i-make-twitter-bootstrap-tooltips-accessible)
* [Thread: best tooltip markup and behavior?](http://webaim.org/discussion/mail_thread?thread=5041)

### Accessibility specification
Accessible tooltips specification is defined in WAI-ARIA Authoring Practices 1.1.

[See: 2.23 Tooltip.](https://www.w3.org/TR/wai-aria-practices-1.1/)

## Accessibility

### Keyboard Interaction

Tooltip can be navigated with the following shortcuts:

* **Tab**: When a form control receives focus a tooltip appears. The tooltip is hidden when the control loses focus.
* **Escape**: Closes tooltip. Once dismissed, mouse hover will display the tooltip as if the control does not have focus.

**Behavior**:

* Host **must** be keyboard focusable.
* Overlay **must** appear after short delay when host receives focus.
* Focus **must** move from host to first focusable control in overlay.
* Overlay **must** disappear when focus leaves flyout.
* Focus should not move to overlay element itself, only it's focusable children.
* The show and hide delays of a overlay may vary depending on the need, but the default is 200ms to show and 0ms to hide
* Tooltips cannot be interacted with.

### Screenreader

* Assistive technology that supports tooltip role will announce the overlay content after a short delay. This delay is configurable in most screen readers.
* Reading order must flow directly from host into overlay.

### Mouse

* Overlay must appear after short delay whenever host receives mouseover. Overlay must disappear when neither the host or overlay have mouseover.

### Touch

* Many touch devices do not support hover interactions!

## ARIA markup

| **Role** | **States, and Properties** | **HTML tag** | - |
| --- | --- | --- | --- |
| **tooltip** | - | - | Element that serves as the tooltip container |
| - | **aria- describedby** | - | The element that triggers the tooltip references the tooltip element with aria-describedby. |

### Notes:

An element that includes role="tooltip" should not be focusable.

Instead, aria-describedby must be set on the triggering element so that it references the ID of the container element that includes role="tooltip".

The triggering element may consist of any active element or interactive widget type that is focusable and includes a valid role.

If the triggering element does not consist of a native active element, it must be made keyboard accessible.

When the mouse moves over the triggering element, or when the triggering element receives focus, the Tooltip should be rendered.

When the mouse moves away from the triggering element, or when the triggering element loses focus, the Tooltip should be removed or hidden.

If the aria-describedby attribute is programmatically changed on the triggering element while it still has focus, a description\_changed event will fire so that assistive technologies can convey the new Tooltip information appropriately.

### Why is it important?

[...]

## Usability

### When to use

* Tooltips can be attached to any element. When you hover the element with your mouse, the title attribute is displayed in a little box next to the element, just like a native tooltip.
* Tooltips are also useful for form elements, to show some additional information in the context of each field.

### Use in Joomla

* Backend Joomla - contextual help; this is very important for administrators with disabilities.
* Frontend: Contextual Help in Contact Form.

## Guidance

* Tooltips are attached to an element and appear when the element is hovered over
* The show and hide delays of a tooltip may vary depending on the need, but the default is 200ms to show and 0ms to hide
* Tooltips cannot be interacted with.


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


