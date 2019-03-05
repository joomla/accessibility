# All functionality is accessible from the keyboard

## Why?
Some users navigate the Internet without a mouse, just using the keyboard or keyboard interfaces. 

Such people include people with physical disabilities, blind people who do not see the mouse pointer, people with chronic conditions such as multiple sclerosis, Parkinson’s disease or repetitive stress injuries. These are also people with temporary limitations, e.g. a broken arm or a damaged mouse.

## How?
* **Provide event handling independent of the device**
  - When possible, use device independent event handlers. 
  - When you are using device dependent event handlers, use both mouse dependent and keyboard dependent event handlers (`onMouseOver`, `onMouseOut` and `onFocus`, `onBlur`).
  - When using the `onClick` event for custom elements (not links, buttons, etc.), ensure that Enter and Space keystrokes are detected.
  - Do not use the `onDblClick` event - there is no device independent handling or keyboard equivalent of this event.
  - Make sure that `onChange` and `onSelect` events do not cause unexpected results and accessibility problems.
* **Use recommended keyboard support patterns in custom user interface elements** 
  - If you program custom user interface elements, e.g. accordion, carousel, dropdown menu, tabs, implement keyboard support as recommended in the [WAI-ARIA Authoring Practices 1.1](https://www.w3.org/TR/wai-aria-practices)
  - If you are building a website make sure that controls can be operated using the keyboard and avoid using components, modules, plugins, widgets, or JavaScript techniques which cannot be operated via the keyboard.
* **Keep the focus visible**
  - Provide visibility of the focus. 
  - If you are attaching the events to a different type of element, like a `<div>` or `<span>`, you need to enable the element to receive keyboard focus. 
* **Ensure logical focus order of interactive elements**
  - Ensure that tabbing order through active elements is logical and matches visual layout.
  - If you program complex user interface components, use appropriate focus management techniques ([using a roving tabindex](https://www.w3.org/TR/wai-aria-practices/#kbd_roving_tabindex) or [using aria-activedescendant](https://www.w3.org/TR/wai-aria-practices/#kbd_focus_activedescendant)).
  - Avoid changing focus unexpectedly.

## WCAG reference
* [2.1 - Keyboard accessible](http://www.w3.org/WAI/WCAG20/quickref/#keyboard-operation)
  - [2.1.1 Keyboard (Level A)](https://www.w3.org/WAI/WCAG21/quickref/?versions=2.0#keyboard)
  - [2.1.2 No Keyboard Trap (Level A)](https://www.w3.org/WAI/WCAG21/quickref/?versions=2.0#no-keyboard-trap)
  - [2.1.3 Keyboard (No Exception) (Level AAA)](https://www.w3.org/WAI/WCAG21/quickref/?versions=2.0#keyboard-no-exception)
* [2.4.1 Bypass Blocks (Level A)](https://www.w3.org/WAI/WCAG21/quickref/?versions=2.0#bypass-blocks)
* [2.4.3 Focus Order (Level A)](https://www.w3.org/WAI/WCAG21/quickref/?versions=2.0#focus-order)
* [2.4.7 Focus Visible (Level AA)](https://www.w3.org/WAI/WCAG21/quickref/?versions=2.0#focus-visible)

## ATAG reference
* [Principle A.1: Authoring tool user interfaces follow applicable accessibility guidelines](https://www.w3.org/TR/ATAG20/#principle_a1)
* [Guideline A.3.1: Provide keyboard access to authoring features](https://www.w3.org/TR/ATAG20/#gl_a31)
* [Part B. Support the production of accessible content](https://www.w3.org/TR/ATAG20/#part_b)

## Further reading 

* [Keyboard Compatibility by W3C WAI](https://www.w3.org/WAI/perspective-videos/keyboard/)
* [Difficulty Typing and Using Your Keyboard? by W3C WAI](https://www.w3.org/WAI/users/browsing#keyboard)
* [Support keyboard interaction by Harvard University](https://accessibility.huit.harvard.edu/support-keyboard-interaction)
* [Designing for Keyboard Accessibility by University of Washington](https://www.washington.edu/accessibility/checklist/keyboard/)
* [Using Keyboard-only Navigation, for Web Accessibility by Joseph C. Dolson](https://www.practicalecommerce.com/Using-Keyboard-only-Navigation-for-Web-Accessibility)
* [Keyboard-Only Navigation for Improved Accessibility by Nielsen Norman Group](https://www.nngroup.com/articles/keyboard-accessibility/)
* [Keyboard access by 18F Accessibility Guide](https://accessibility.18f.gov/keyboard/)
* [The Enter Key should Submit Forms, Stop Suppressing it](https://www.tjvantoll.com/2013/01/01/enter-should-submit-forms-stop-messing-with-that/)
* [Implicit Submission of Form When Pressing Enter Key](http://stonefishy.github.io/blog/2015/06/30/implicit-submission-of-form-when-pressing-enter-key/)
* [Enter by Computer Hope](https://www.computerhope.com/jargon/e/enterkey.htm)
* [Create a logical tabbing order through links, form controls and objects by A11y Tips](http://dboudreau.tumblr.com/post/80948821036/create-a-logical-tabbing-order-through-links-form)
* [Why Keyboard Usability Is More Important Than You Think by David Sloan & Sarah Horton](https://blog.usertesting.com/blog/why-keyboard-usability-is-more-important-than-you-think/)
* [Designing Better Keyboard Experiences. By David Sloan & Sarah Horton](https://blog.usertesting.com/blog/designing-better-keyboard-experiences/)
* [Keyboard Navigation in Mac Browsers](http://www.weba11y.com/blog/2014/07/07/keyboard-navigation-in-mac-browsers/)
* [Keyboard accessibility (again). By Rogera Johansson](https://www.456bereastreet.com/archive/201104/keyboard_accessibility_again/)
* [Keyboard Accessibility with the Space Bar](http://www.last-child.com/keyboard-accessibility-with-the-space-bar/)
* [3 Simple Tips to Improve Keyboard Accessibility](https://www.a11ywithlindsey.com/blog/3-simple-tips-improve-keyboard-accessibility/)
* [Keyboard accessibility quick tip. By Emily Coward](https://www.nomensa.com/blog/2011/keyboard-accessibility-quick-tip/)
* [Accessible Javascript. Overview of Accessible Javascript. By WebAIM](https://webaim.org/techniques/javascript/)
* [Accessible Javascript. JavaScript Event Handlers. By WebAIM](https://webaim.org/techniques/javascript/eventhandlers)
* [Accessible Javascript. Other Issues. By WebAIM](https://webaim.org/techniques/javascript/other)
* [Accessible Javascript. JavaScript Alternatives. By WebAIM](https://webaim.org/techniques/javascript/alternatives)
