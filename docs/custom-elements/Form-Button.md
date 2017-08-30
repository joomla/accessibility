# Button
## What is this

**Purpose**: User need input a command with one of the following possible action: submit form, reset form or action defined by JavaScript.

**Description**: Buttons are used as triggers for actions. Depending on the use case, buttons contain a label and/or an icon. There are a variety of styles, sizes, and variations that can be used for different situations.

All button labels are sentence case. They should be as short as possible while clearly explaining what will happen when the button is clicked.

## Accessibility
### Accessibility specification

Accessible buttons specification is defined in WAI-ARIA Authoring Practices 1.1.
* [See: 2.6 Button. ](https://www.w3.org/TR/wai-aria-practices-1.1/#button)
* [See also about rolu button](https://www.w3.org/TR/wai-aria-1.1/#button)

### Screen look, behavior
_The content for this section is not yet available, please check back again for updates._

### Keyboard interaction

* **Space** or **Enter**: executes the action for that button.
* **Tab** or **Shift+Tab**: if button has focus, should move to the next or previous focusable page element respectively

**Behavior**

* If the button activation closes the containing entity or launches another entity, then focus moves to the newly opened entity.
* If the button activation does not close or dismiss the containing entity, then focus remains on the button.

### Screen reader interaction

* If virtual cursor is on button, it must be invokable by virtual cursor (e.g. VO+SPACE in VoiceOver).
* Role of 'button' must be announced.
* Label must be announced.
* Any state must be announced (e.g. expanded, haspopup).
* Any description must be announced (i.e. via aria-describedby).

### Pointer interaction
* Clicking on the button executes the action for the button.
* If focus is on another element when a button is clicked with a mouse, the focus moves to the clicked button.
* If focus is on another element and the mouse is moved over a button, a visual indicator is provided to show that the button may be clicked, but focus does not yet move.
* If focus is on another element and the mouse is moved over a button then moved away, the visual indicator goes away and focus is unchanged.

## ARIA markup
This section lists all relevant ARIA roles, states and properties for a button.

* **aria-haspopup**: Informs AT that the button opens a menu when clicked.
* **aria-controls**: Informs AT that the button controls another element.
* **aria-expanded**: Informs AT of the expanded state of any controlled element. Used in conjunction with aria- controls.
* **aria-label**: Creates a label for the button.
Warning! This label will override any inner text that may be present. This property is most commonly used for critical icon buttons (i.e. buttons with icon and no text).
* **aria-describedby**: Informs AT of any extended description or context related to the button. Note that this property has no effect on the accessible label of the button.

## Why is it important?
_The content for this section is not yet available, please check back again for updates._

## Utilities
### When to use
* Use buttons for the most important actions you want users to take on your site, such as "download," "sign up," or "log out."

### When to consider something else
* If you want to lead users between pages of a website. Use links instead.
* Less popular or less important actions may be visually styled as links.

### Use in Joomla
 - _The content for this section is not yet available, please check back again for updates._

## Best practices
* Use the &lt;a> tag if the button is a link to another page, or a link to an anchor within a page.
* Use the &lt;button> tag if the button performs an action that changes something on the current page.
* Generally, use primary buttons for actions that go to the next step and use secondary buttons for actions that happen on the current page.
* Style the button most users should click in a way that distinguishes from other buttons on the page. Try using the "large button" or the most visually distinct fill color.
* Make sure buttons should look clickable - use color variations to distinguish static, hover and active states.
* Avoid using too many buttons on a page.
* Use sentence case for button labels.
* Button labels should be as short as possible with "trigger words" that your users will recognize to clearly explain what will happen when the button is clicked (for example, "download," "view" or "sign up").
* Make the first word of the button's label a verb. For example, instead of "Complaint Filing" label the button "File a complaint."
* At times, consider adding an icon to signal specific actions ("download", "open in a new window", etc).
* Make sure that the text of the button is descriptive. If for some reason, your button contains no readable text (for example, just a symbol or icon), add screen reader-only text to the button to clarify its purpose. The symbol or icon should be wrapped in an element with the attribute aria-hidden="true", to prevent screen readers from trying to pronounce the symbol.

## Code patterns for Joomla and Joomla extension
### Current

_The content for this section is not yet available, please check back again for updates._

### Improved

_The content for this section is not yet available, please check back again for updates._

## Resources
### WCAG Reference
* **[1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-programmatic)** - Level A
* **[1.3.3 Sensory Characteristics](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-understanding)** - Level A 
* **[2.1.1 Keyboard](https://www.w3.org/WAI/WCAG20/quickref/#keyboard-operation-keyboard-operable)** - Level A
* **[4.1.2 Name, Role, Value](https://www.w3.org/WAI/WCAG20/quickref/#ensure-compat-rsv)** - Level A

### Design Patterns
* [WAI ARIA practices - Button Examples ](https://www.w3.org/TR/wai-aria-practices-1.1/examples/button/button.html)
* [WAI ARIA practices - Actions Menu Button Example Using element.focus()](https://www.w3.org/TR/wai-aria-practices-1.1/examples/menu-button/menu-button-actions.html)
* [WAI ARIA practices - Actions Menu Button Example Using aria-activedescendant](https://www.w3.org/TR/wai-aria-practices-1.1/examples/menu-button/menu-button-actions-active-descendant.html)
* [Accessible jQuery-ui Components - Buttons](http://hanshillen.github.io/jqtest/?tabid=tooltip#goto_button)
* [U.S. Web Design Standards - Buttons](https://standards.usa.gov/components/buttons/)
* [Bootstrap 4.0](https://getbootstrap.com/docs/4.0/components/buttons/)
* [Open Ajax Accessibility ex. 3 - Button role example using text-only buttons  ](http://oaa-accessibility.org/example/3/)
* [Open Ajax Accessibility ex. 4 - Button role example using image buttons ](http://oaa-accessibility.org/example/4/)
* [EBay MIND patterns](http://ianmcburnie.github.io/mindpatterns/input/button/)

### Articles
* [Using the button role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_button_role)
* [WebAIM: Creating Accessible Forms](http://webaim.org/techniques/forms/controls)
* [Paul J. Adam: Building Accessible Buttons with ARIA: A11y Support Series](https://www.deque.com/blog/accessible-aria-buttons/)
* [Nicholas C. Zakas: Making accessible icon buttons](https://www.nczonline.net/blog/2013/04/01/making-accessible-icon-buttons/)
* [The ARIA Role Matrices](http://whatsock.com/training/matrices/)
