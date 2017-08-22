# Tabs

## What is this

**Purpose**: Users need to flip between multiple focused panes/views of content.

**Description**: Tabs manage stacked panes of content, giving the users the ability to view only the content pane they are interested in. Each tab button has a corresponding content pane. Tabs build on a real world metaphor. The selected state is reinforced with the tab metaphor of a folder physically in front of the others in the set.

## Accessibility specification

Accessible tabs specification is defined in [WAI-ARIA Authoring Practices 1.1 -  See 2.21 Tabs](https://www.w3.org/TR/wai-aria-practices-1.1/)

## Terms:

* **tabs or tabbed Interface**: a set of tab elements and their associated tab panels.
* **tab list**: a set of tab elements contained in a tablist element.
* **tab**: an element in the tab list that serves as a label for one of the tab panels and can be activated to display that panel.
* **tabpanel**: section of content associated with a tab header.

## Design Patterns

* [WAI ARIA practices - Tabs With Automatic Activation](https://www.w3.org/TR/wai-aria-practices/examples/tabs/tabs-1/tabs.html)
* [WAI ARIA practices - Tabs With Manual Activation](https://www.w3.org/TR/wai-aria-practices/examples/tabs/tabs-2/tabs.html)
* [Accessible jQuery-ui Components](http://hanshillen.github.io/jqtest/?tabid=tabs)
* [Tabpanel widget by Deque](https://dequeuniversity.com/library/aria/tabpanels-accordions/tabpanel)
* [Responsive Tabs to Accordion by Deque](https://dequeuniversity.com/library/aria/tabpanels-accordions/sf-responsive-tabs-to-accordion)
* [Open Ajax Accessibility ex. 34 - Tab Panel: ARIA CSS Selectors](http://oaa-accessibility.org/example/34/)
* [Open Ajax Accessibility ex. 36 - Tab Panel: ARIA CSS Selectors](http://oaa-accessibility.org/example/36/)
* [jQuery documentation](http://api.jqueryui.com/tabs/)
* [Frend - A collection...](https://frend.co/components/tabs/)

## Accessibility

### Keyboard Interaction

The tablist takes up one tab stop in the tab order. It can be navigated with the following shortcuts:

* **Left or Up Arrow**: Show the previous tab
* **Right or Down Arrow**: Show the next tab
* **Home**: Show the first tab
* **End**: Show the last tab
* **Alt + Page Down** (from anywhere inside the tab panel): Select the previous tab and move focus to the tablist
* **Alt + Page Up** (from anywhere inside the tab panel): Select the next tab and move focus to the tablist

**For the tab list:**

* **Tab**: When the tab list is receiving focus, places focus on the active tab element. When the tab list contains the focus, moves focus to the next element in the page tab sequence outside the tablist, which is typically either the first focusable element inside the tab panel or the tab panel itself.

**When focus is on a tab element in a horizontal tab list:**

* **Left Arrow**: moves focus to the previous tab. If focus is on the first tab, moves focus to the last tab. Optionally, activates the newly focused tab (See note below).
* **Right Arrow**: Moves focus to the next tab. If focus is on the last tab element, moves focus to the first tab. Optionally, activates the newly focused tab (See note below).

**When focus is on a tab in a tablist with either horizontal or vertical orientation:**

* **Space or Enter**: Activates the tab if it was not activated automatically on focus.
* **Home** (Optional): Moves focus to the first tab
* **End** (Optional): Moves focus to the last tab.
* **Shift + F10**: If the tab has an associated pop-up menu, opens the menu.
* **Delete** (Optional): If deletion is allowed, deletes (closes) the current tab element and its associated tab panel. If any tabs remain, sets focus to the tab following the tab that was closed and activates the newly focused tab. Alternatively, or in addition, the delete function is available in a context menu.

### Screenreader Interaction

* Tab must be announce as "Tab".
* Tab label must be announced, for example "Select Shipping for me".
* Tab selected state must be announced.
* Virtual cursor navigation can move from tab to tab without changing the active tab selection. The invoke command (e.g. VO+SPACE on Voiceover) selects the tab under the virtual cursor.

### Mouse Interaction

**[ Describe the expected behavior ]**

### Touch Interaction

**[ Describe the expected behavior ]**

### ARIA markup

**Commentary:**

The aria-expanded state is used to distinguish between a Tab panel's expanded vs. collapsed state. An AT should be sensitive to aria-expanded, and relay it meaningfully to the user. Here are some role/state combinations and their meaning:

* (role=tablist + aria-multiselectable= **true**) is a Accordion ( **sic**!)
* (role=tablist + aria-multiselectable= **false**) is a Tab Panel
* (role=tablist + aria-multiselectable= **true**) and (focus on role=tab + aria-expanded=true) is a Accordion ( **sic!**) Header whose panel is expanded
* (role=tablist + aria-multiselectable= **false**) and (focus on role=tab + aria-expanded=true) is a Tab whose panel is expanded
* (role=tablist + aria-multiselectable= **true**) and (focus on role=tab + aria-expanded=false) is a Accordion ( **sic!**) Header whose panel is collapsed.

| **Role** | **States,&nbsp;and&nbsp;Properties** | **HTML tag** | **Description** |
| --- | --- | --- | --- |
| **tablist** | - | - | Serves as the container for the set of tabs. |
| **tab** | - | - | Contains title for tab panel, activates tab panel when activated. |
| **tabpanel** | - | - | Contains the tab's associated content. |
| - | **aria-selected** | - | The active tab element has state set to true and other tab elements have it set to false. |
| - | **aria-controls** | - | Each element with role=tab has a unique name aria-controls="id" that associates the control to the appropriate element tabpanel by referencing the controlled element's id. |
| - | **aria-labelledby** | - | Each element with role tabpanel has the property aria-labelledby referring to its associated tab element. |
| - | **aria-haspopup** | - | If a tab element has a pop-up menu, it has the property aria-haspopup set to true. |
| - | **aria-orientation** | - | If the tablist element is vertically oriented, it has the property aria-orientation set to vertical. The default value of aria-orientation for a tablist element is horizontal. |

### Why is it important?

In HTML there is no tabs or attribute tag that indicates the state and properties of the tabs panels. Panels change their status dynamically, depending on user actions. Screen readers must be notified that the content panel has been expanded.

## Usability

### When to use

Tabs are commonly used to reduce the need to scroll when presenting multiple sections of content on a single page.

* Users only need a few specific pieces of content within a page.
* Information needs to be displayed in a small space.

### When to consider something else

* If visitors need to see most or all of the information on a page. Use well-formatted text instead.
* If there is not enough content to warrant condensing. Tabs increase cognitive load and interaction cost, as users have to make decisions about what headers to click on.

### Use in Joomla

* Backend Joomla - multiple screens on which the configuration of an item is defined
* Contact component - single contact view
* Content component - single article view (with plugin Pagebreak)

## Code patterns for Joomla and Joomla extension

### Current

[...]

### Improved

[...]

## Guidance

* You have multiple categories, views, and panes of content, but there is the need to only show one pane at a time.
* Avoid overflowing tabs to new lines.
* Tab titles should be short and predictable.
* Tab buttons can contain icons, text, both, and even dropdowns.

## WCAG Reference

* **[1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-programmatic)** (Level A): Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text.
* **[1.3.3 Sensory Characteristics](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-understanding)** (Level A): Instructions provided for understanding and operating content do not rely solely on sensory characteristics of components such as shape, size, visual location, orientation, or sound.
* **[2.1.1 Keyboard](https://www.w3.org/WAI/WCAG20/quickref/#keyboard-operation-keyboard-operable)** (Level A): All functionality of the content is operable through a keyboard interface without requiring specific timings for individual keystrokes, except where the underlying function requires input that depends on the path of the user's movement and not just the endpoints.
* **[2.4.3 Focus Order](https://www.w3.org/WAI/WCAG20/quickref/#navigation-mechanisms-focus-order)** (Level A): If a Web page can be navigated sequentially and the navigation sequences affect meaning or operation, focusable components receive focus in an order that preserves meaning and operability.
* **[2.4.7 Focus Visible](https://www.w3.org/WAI/WCAG20/quickref/#navigation-mechanisms-focus-visible)** (Level AA): Any keyboard operable user interface has a mode of operation where the keyboard focus indicator is visible.
* **[4.1.2 Name, Role, Value](https://www.w3.org/WAI/WCAG20/quickref/#ensure-compat-rsv)** (Level A): For all user interface components (including but not limited to: form elements, links and components generated by scripts), the name and role can be programmatically determined; states, properties, and values that can be set by the user can be programmatically set; and notification of changes to these items is available to user agents, including assistive technologies.

## Reference

* [Danger! ARIA tabs](http://simplyaccessible.com/article/danger-aria-tabs/)
* [Danger! Testing Accessibility with real people](https://medium.theuxblog.com/danger-testing-accessibility-with-real-people-4515f72db648)
* [ARIA tabs, UI problems and standards](https://alastairc.ac/2016/05/aria-tabs-ui-problems-and-standards/)

