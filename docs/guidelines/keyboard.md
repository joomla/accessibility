# All functionality is accessible from the keyboard

## Why?
Some users navigate the Internet without a mouse, just using the keyboard or keyboard interfaces.  

## How?
* When possible, use device independent event handlers. 
* When you are using device dependent event handlers, use both mouse dependent and keyboard dependent event handlers (onMouseOver, onMouseOut and onFocus, onBlur).
* When using the onClick event for custom elements(not links, buttons, etc.), ensure that Enter and Space keystrokes are detected.
* Do not use the onDblClick event - there is no device independent handling or keyboard equivalent of this event.
* Make sure that onChange and onSelect events do not cause accessibility problems
* Make sure that keyboard events do not cause unexpected results.
* If you create custom components, e.g. accordion, carousel (slide show or image rotator) dropdown menu, tabs, provide keyboard support according to the standards set out in the [WAI-ARIA Authoring Practices 1.1](https://www.w3.org/TR/wai-aria-practices)
* Avoid using components, modules, plugins, widgets, or JavaScript techniques which cannot be operated via the keyboard.
* Provide visibility of the focus. If you are attaching the events to a different type of element, like a <div> or <span>, you need to enable the element to receive keyboard focus. 
* Maintain the logical order of the tabulation 
* Avoid changing focus unexpectedly
* Ensure that reading order is logical

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
* [Enter by Computer Hope](https://www.computerhope.com/jargon/e/enterkey.htm)
* [Create a logical tabbing order through links, form controls and objects by A11y Tips](http://dboudreau.tumblr.com/post/80948821036/create-a-logical-tabbing-order-through-links-form)
* [Designing Better Keyboard Experiences by David Sloan & Sarah Horton](https://blog.usertesting.com/blog/designing-better-keyboard-experiences/)
* [Why Keyboard Usability Is More Important Than You Think by David Sloan & Sarah Horton](https://blog.usertesting.com/blog/why-keyboard-usability-is-more-important-than-you-think/)
* [Keyboard accessibility quick tip by Emily Coward](https://www.nomensa.com/blog/2011/keyboard-accessibility-quick-tip/)
* [Keyboard Navigation in Mac Browsers](http://www.weba11y.com/blog/2014/07/07/keyboard-navigation-in-mac-browsers/)
* [Keyboard accessibility (again)](https://www.456bereastreet.com/archive/201104/keyboard_accessibility_again/)
* [Keyboard Accessibility with the Space Bar](http://www.last-child.com/keyboard-accessibility-with-the-space-bar/)
* [3 Simple Tips to Improve Keyboard Accessibility](https://www.a11ywithlindsey.com/blog/3-simple-tips-improve-keyboard-accessibility/)
* [Accessible Javascript. Overview of Accessible Javascript. By WebAIM](https://webaim.org/techniques/javascript/)
* [Accessible Javascript. JavaScript Event Handlers. By WebAIM](https://webaim.org/techniques/javascript/eventhandlers)
* [Accessible Javascript. Other Issues. By WebAIM](https://webaim.org/techniques/javascript/other)
* [Accessible Javascript. JavaScript Alternatives. By WebAIM](https://webaim.org/techniques/javascript/alternatives)
