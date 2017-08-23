# Pagination
## What is this
**Purpose**: Users need to navigate through pages of items.

**Description**: Collections of data are often split into multiple pages for performance reasons. Either the size of the data is too much to download at once, or the size of the data would take too long to render all at once. Pagination controls allow for the user to retrieve or view pages of data in a performant matter.

### Terminology
We use the following terminology when discussing this pattern.

* **Pagination**: The composite patterns as a whole, containing the items defined below
* **Previous**: Link that navigates to previous page of results
* **Next**: Link that navigates to next page of results
* **Items**: Links that navigate to exact page of results
* **Bookends**: Collective name for the previous and next links, as they 'bookend' the navigation items
* **Current Page**: The current resultset index, as reflected in the pagination UI

## Accessibility
### Accessibility specification
* See: [Accessible pagination by Accessibility Matters](http://www.a11ymatters.com/pattern/pagination/).

### Keyboard Interaction
* **Tab** or **Shift+Tab**: move focus to next or previous link
* **Entter** or **Space:** open link

#### Behavior
* The bookend and item links must be keyboard focusable at all times (even when visually disabled).
* If the Previous bookend has keyboard focus, pressing TAB key must move focus to first pagination link.
* If pagination item has keyboard focus, pressing TAB key must move focus to next pagination item.
* If last pagination item has keyboard focus, pressing TAB key must move focus to Next bookend link.
* For client-side pagination, keyboard focus must remain on the previous, next or item link after activation.

### Screenreader Interaction

* Bookend link text must be announced (i.e. "Previous page" and "Next page").
* If bookend links are visually disabled, they must also be announced as disabled.
* If a pagination item is visually displayed as the current page, it must also be announced as the current page.
* For client-side pagination, the new page index must be announced after previous, next or item link activation.

### Mouse Interaction

* [Describe the expected behavior ]

### Touch Interaction

* [Describe the expected behavior ]

## ARIA markup

* **role=navigation**: Creates a navigation landmark for assistive technology.
* **role=img**: Applied to bookend SVG tags to reinforce image semantics.
* **aria-labelledby**: Use this property to label the navigation landmark with the text of the heading tag. Use this property to label the SVG element with the text of the title tag.
* **aria-current**: Refers to the current item in the pagination (i.e. the current dataset index).
* **aria-live**: Creates a polite live-region around the heading. Meaning the heading state will be announced by assistive technology when it changes.
* **role=status**: Creates a polite live-region around the heading. Meaning the heading state will be announced by assistive technology when it changes.

### Why is it important?

[...].

## Utilities
### When to use
* [...]

### Use in Joomla
* **backend**: On page types like: Article Manager, Category Manager, etc
* **frontend**: On page types like: category blog, category list item

## Best practices
* Do not use buttons for URL based pagination. Because the URL is updated, and the browser history stack updated, a link is the correct tag to use.
* Pagination must have a heading element. For example "Results Pagination". This heading can be hidden offscreen for sighted users.
* Items must be marked up as a list of links (not buttons). Bookends must be marked up as links (not buttons).
* Bookend icons should be created using SVG or Font Awesome (Glipicons)

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

## Resources
### Design Patterns
* [Pagination by Upsto design](http://uspto.github.io/designpatterns/1.x/docs/components/pagination.html)
* [Accessible pagination by Accessibility Matters](http://www.a11ymatters.com/pattern/pagination/)
* [Pagination by Bootstrap](http://getbootstrap.com/components/)
* [Pagination by ZURB Foundation](http://foundation.zurb.com/sites/docs/pagination.html)

### Articles
* [Accessible pagination by Accessibility Matters](http://www.a11ymatters.com/pattern/pagination/).
* [Pagination – Examples And Good Practices](https://www.smashingmagazine.com/2007/11/pagination-gallery-examples-and-good-practices/)
* [MIke West: An Accessible Pagination Pattern](https://mikewest.org/2010/02/an-accessible-pagination-pattern) 
* [Joe Watkins: Accessible Pagination Test](https://codepen.io/joe-watkins/pen/EgXGZo)
* [Hanny Elemary: Accessible pagination with ARIA](http://hanyelemary.com/?p=889)
* [Pagination by ZURB Foundation](http://foundation.zurb.com/sites/docs/v/5.5.3/components/pagination.html)
* [The ARIA Role Matrices](http://whatsock.com/training/matrices/)
