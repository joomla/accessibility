# Accordion

## What is this

**Purpose**: Users need to see only relevant content.

**Description**: Accordions is a set of drop-down sections. Collapsible panels provide users with the ability to expand and collapse content as needed. They can simplify the interface by hiding content until it is needed. Expanding the selected section automatically collapses the rest.

## Accessibility specification

Accessible accordions specification is defined in WAI-ARIA Authoring Practices 1.1. [See: 2.2 Accordion.](https://www.w3.org/TR/wai-aria-practices-1.1)

## Terms:

* **Accordion header**: Label for or thumbnail representing a section of content that also serves as a control for showing, and in some implementations, hiding the section of content.
* **Accordion panel**: Section of content associated with an accordion header.

##  Design Patterns

* [WAI ARIA practices](https://www.w3.org/TR/2017/WD-wai-aria-practices-1.1-20170628/examples/accordion/accordion.html)
* [Accessible jQuery-ui Components](http://hanshillen.github.io/jqtest/?tabid=accordion)
* [U.S. Web Design Standards ](https://standards.usa.gov/components/accordions/)
* [Tabbed Accordion by Deque](https://dequeuniversity.com/library/aria/tabpanels-accordions/tabbed-accordion)
* [Multiselect accordion by Deque](https://dequeuniversity.com/library/aria/tabpanels-accordions/sf-tabless-multiselect-accordion)
* [Responsive Tabs to Accordion by Deque](https://dequeuniversity.com/library/aria/tabpanels-accordions/sf-responsive-tabs-to-accordion)
* [Bootstrap](http://getbootstrap.com/components/)
* [Open Ajax Accessibility ex. 35](http://oaa-accessibility.org/example/35/)
* [Open Ajax Accessibility ex. 37](http://oaa-accessibility.org/example/37/)
* [jQuery UI - accordion](http://api.jqueryui.com/accordion/)
* [frend.co A collection....](https://frend.co/components/accordion/)

## Accessibility

### Keyboard Interaction

The accordion takes up one **tab** stop in the tab order. It can be navigated with the following shortcuts:

* **Space and Enter key**: Expand the currently focused accordion header
* **Up or Left Arrow** (optional): Move focus to the previous accordion header
* **Down or Right Arrow** (optional): Move focus to the next accordion header
* **Home** (optional): Move focus to the first accordion header
* **End** (optional): Move focus to the last accordion header
* **Control + Page Up** (optional): Move focus to the previous accordion header or move focus to the last accordion header
* **Control + Page Down** (optional): Move focus to the next accordion header or move focus to the first accordion header.

### Screenreader Interaction

[... ]

### Mouse Interaction

[... ]

### Touch Interaction

[... ]

## ARIA markup

* **role**: The accordion is marked up as tablist, the header panel is marked up as tab and the content panel is marked up as tabpanel.
**Alternatively**: header panel is marked up as heading and button, content panel is marked up as region.
* **aria-expanded**: Set to true when the accordion panel is expanded, otherwise set to false.
* **aria-controls**: Points to the ID of the panel which the header controls (Each button has a unique name aria-controls="id" that associates the control to the appropriate region by referencing the controlled element's id).
* **aria-hidden**: Each content area will have its aria-hidden attribute set to either true or false by the component, depending on its corresponding button's aria-expanded attribute.
* **aria-disabled**: If the accordion panel is expanded and is not allowed to be collapsed, then set to true.
* **aria-labelledby**: Points to the accordion header; labels the landmark region with the accordion header.

| **Role** | **States, and&nbsp;Properties**&nbsp;&nbsp; | **HTML tag** | - |
| --- | --- | --- | --- |
| **tablist** | - | - | - |
| **tab** | - | - | - |
| **tabpanel** | - | - | - |
| - | **aria- expanded** | - | Set to _true_ when the accordion panel is expanded, otherwise set to _false_. |
| - | **aria-controls** | - | Points to the ID of the panel which the header controls (Each button has a unique name aria-controls="id" that associates the control to the appropriate region by referencing the controlled element's id). |
| - | **aria- hidden** | - | Each content area will have its aria-hidden attribute set to either _true_ or _false_ by the component, depending on its corresponding buttons aria-expanded attribute. |
| - | **aria- disabled** | - | If the accordion panel is expanded and is not allowed to be collapsed, then set to _true_. |
| - | **aria- labelledby** | - | Points to the accordion header; labels the landmark region with the accordion header. |

### Why is it important?

In HTML there is no accordion or attribute tag that indicates the state of the accordion panels. Panels change their status dynamically, depending on user actions. Screen readers must be notified that the content panel has been expanded.

## Usability

### When to use

Accordions are commonly used to reduce the need to scroll when presenting multiple sections of content on a single page.

* Users only need a few specific pieces of content within a page.
* Information needs to be displayed in a small space.

### When to consider something else

* If visitors need to see most or all of the information on a page. Use well-formatted text instead.
* If there is not enough content to warrant condensing. Accordions increase cognitive load and interaction cost, as users have to make decisions about what headers to click on.

### Use in Joomla

* Contact component - single contact view
* Content component - single article view (with plugin Pagebreak)

## Code patterns for Joomla and Joomla extension

### Current

[...]

### Improved

[...]

## Guidance

* Allow users to click anywhere in the header area to expand or collapse the content; a larger target is easier to manipulate.
* Make sure interactive elements within the collapsible region are far enough from the headers that users don't accidentally trigger a collapse. (The exact distance depends on the device.)

## WCAG Reference

* **[1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-programmatic)** (Level A): Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text.
* **[1.3.3 Sensory Characteristics](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-understanding)** (Level A): Instructions provided for understanding and operating content do not rely solely on sensory characteristics of components such as shape, size, visual location, orientation, or sound.
* **[2.1.1 Keyboard](https://www.w3.org/WAI/WCAG20/quickref/#keyboard-operation-keyboard-operable)** (Level A): All functionality of the content is operable through a keyboard interface without requiring specific timings for individual keystrokes, except where the underlying function requires input that depends on the path of the user's movement and not just the endpoints.
* **[4.1.2 Name, Role, Value](https://www.w3.org/WAI/WCAG20/quickref/?showtechniques=412#qr-ensure-compat-rsv)** (Level A): For all user interface components (including but not limited to: form elements, links and components generated by scripts), the name and role can be programmatically determined; states, properties, and values that can be set by the user can be programmatically set; and notification of changes to these items is available to user agents, including assistive technologies.
