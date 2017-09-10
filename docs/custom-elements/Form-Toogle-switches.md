# Toggle swichtes
## What is this

**Purpose**: Users need to toggle an option between on/off or yes/no.

**Description**: A switch provides approximately the same functionality as a checkbox and toggle button, but makes it possible for assistive technologies to present the widget in a fashion consistent with its on-screen appearance.

## Accessibility
### Accessibility specification
WAI-ARIA defines and describes only the switch attribute. Please read: [The ARIA 1.1 switch role specification . ][6]

### Screen interaction
* When the switch is selected, it receives focus. Focus is visible.
* The states "pressed" and "not pressed" should be signaled graphically and labeled.

### Keyboard Interaction
* **Tab** - navigate between switches or other controls
* **Space** - toggle the state of the selected switch.

### Screenreader Interaction
* When the switch gets focus, the screen reader announces a name, such as "toggle button"
* Announces the state of the switch:
  * When the switch is pressed, announces its status eg "pressed"
  * When the switch is not pressed, announce its status eg "not pressed"

### Mouse / Pointer / Touch Interaction
* User may click / touch a switch to toggle the state

## ARIA markup
* **role="switch" attribute**
   Indicates that the widget is a switch that represents on/off values, as opposed to checked/unchecked values.
*  **aria-pressed** attribute
   Indicates the current "pressed" state of toggle buttons. If the attribute is not present, the button is not a toggle button.
   
   Toggle buttons require a full press-and-release cycle to change their value. Activating it once changes the value to true, and activating it another time changes the value back to false.

   The aria-pressed attribute is similar but not identical to the aria-checked attribute. Operating systems support pressed on buttons and checked on checkboxes

### Why is it important?

## Utilities

### When to use
 - [...]

### Use in Joomla
 - [...]

## Best practices
* Use a toggle switch for a binary option where the change occurs immediately.
* Use a checkbox instead if the user has to perform other actions for the change to be effective (e.g., pressing Save or Submit).

## Code patterns for Joomla and Joomla extensions

### Current
[...]

### Improved
[...]

## Resources
## WCAG Reference
* **[1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-programmatic)** - Level A
* **[1.3.3 Sensory Characteristics](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-understanding)** - Level A 
* **[2.1.1 Keyboard](https://www.w3.org/WAI/WCAG20/quickref/#keyboard-operation-keyboard-operable)** - Level A
* **[4.1.2 Name, Role, Value](https://www.w3.org/WAI/WCAG20/quickref/#ensure-compat-rsv)** - Level A

### Design Patterns
* [Bootstrap Toogle -][1]
* [ARIA Switch button component][2] and [demo][14]
* [CSS toogle switch][3]
* [On/Off CSS Radio Switches by Nick Bottomley][15]
* [Switches by ZURB Fondation][4]
* [Gogle Design Materials][5]

### Articles
* [A sweet toggle switch][7]
* [Toggle Buttons][8]
* [Accssible component modules: Aria Toggles, Checkboxes and Switches][9]
* [CSS toggle switch][13]
* [Accessible on/off Toggle Switch][10]
* [The a11y: Story of a toggle][11]
* [The ARIA Role Matrices][12]

  [1]: http://www.bootstraptoggle.com/
  [2]: https://github.com/scottaohara/aria-switch-button
  [3]: https://ghinda.net/css-toggle-switch/
  [4]: http://foundation.zurb.com/sites/docs/v/5.5.3/components/switch.html
  [5]: https://material.io/guidelines/components/selection-controls.html
  [6]: https://www.w3.org/TR/wai-aria-1.1/
  [7]: https://www.paypal-engineering.com/2014/01/15/a-sweet-toggle-switch/
  [8]: https://inclusive-components.design/toggle-button/
  [9]: http://whatsock.com/tsg/
  [10]: https://codepen.io/LFeh/pen/DIdKj
  [11]: https://yoast.com/dev-blog/a11y-monthly-story-toggle/
  [12]: http://whatsock.com/training/matrices/
  [13]: https://ghinda.net/css-toggle-switch/
  [14]: https://scottaohara.github.io/aria-switch-button/
  [15]: https://codepen.io/nickbottomley/pen/uhfmn
