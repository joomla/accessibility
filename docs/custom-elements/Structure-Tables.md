# Tables
## What is this

**Purpose**: Users need to provide structured data

**Description**: Tables show tabular data in columns and rows.

## Accessibility

### Accessibility specification
Simple tables can have two levels of headers. Each header cell should have scope="col" or scope="row".
* Complex tables are tables with more than two levels of headers. Each header should be given a unique id and each data cell should have a headers attribute with each related header cell's id listed.
* When adding a title to a table, include it in a <caption> tag inside of the &lt;table> element.

## Design interaction
### Screen look, behavior

_The content for this section is not yet available, please check back again for updates._

### Keyboard interaction
The only special consideration for table is sortable columns. Typically this is achieved by adding a toggle button as the contents of the table header cell. The usual rules for button apply.

### Screen reader interaction
* Table must be visible in screen reader list of tables.
* Screen reader must be navigable with screen reader table command.
* Screen reader must announce caption of table.
* Screen reader must announce value of every cell.
* Screen reader must announce value of column header when instructed to do so.
* Sortable column must be announced by screen reader.
* Current sort state of sortable columns must be announce by screen reader.
* When moving from column to column, screen reader announces new column scope. Typically this scope is the value of the column header.
* When moving from row to row, screen reader announces new row scope. Typically this scope is the value of the row header.

### Mouse / Pointer / Touch interaction
The only special consideration for table is sortable columns. Typically this is achieved by adding a toggle button as the contents of the table header cell. The usual rules for button apply.

## ARIA markup
* **role=" presentation"**: If you need to use a layout formatting table, use this role

## Why is it important?
> **Why is this important?**

> Tables without structural markup to differentiate and properly link between header and data cells, create accessibility barriers. Relying on visual cues alone is not sufficient to create an accessible table. With structural markup, headers and data cells can be programmatically determined by software, which means that:

> - **People using screen readers** can have the row and column headers read aloud as they navigate through the table. Screen readers speak one cell at a time and reference the associated header cells, so the reader doesn't lose context.
> - **Some people use alternative ways to render the data**, for example by using custom stylesheets to display header cells more prominently. Techniques like this enable them to change text size and colors and display the information as lists rather than grids. The table code needs to be properly structured to allow alternative renderings.

> (source: [Web Accessibility Tutorials: Tables Concepts](https://www.w3.org/WAI/tutorials/tables/) )

## Usability

### When to use

When you need tabular information, such as statistical data.

### When to consider something else

Depending on the type of content, consider using other presentation formats such as definition lists or hierarchical lists.

### Use in Joomla

[List of back-end and front-end screens on which this UI element is used]

## Code patterns for Joomla and Joomla extensions

### Current

_The content for this section is not yet available, please check back again for updates._

### Improved

_The content for this section is not yet available, please check back again for updates._

## Best practics
* Tables are great at displaying tabular data. Minimal visual styling helps surface this information more easily.
* Every table requires a caption element. The summary attribute is deprecated in HTML5.
* Every table cell should have a logical column header or row header.
* Do not use tables for row/column layout of page or modules.

## Resources
### WCAG reference
* **[1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-programmatic)** - Level A:   Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text.

### Design Patterns
* [U.S. Web Design Standards - Tables][4]
* [Bootstrap 4.0 - Table - ][5][MIND EBay  ][6]

### Articles
* [WebAIM: Creating Accessible Tables][7]
* [WebAIM: Creating Accessible Tables. Layout Tables][8]
* [Web Accessibility Tutorials. Tables Concepts][9]
* [Jim Thatcher: Accessible Tables][10]
* [Ros Shannon: Tables Accessibility][11]
* [The A11y Project: How–to: Create accessible data tables][12]
* [Accessible Tables][13]

  [1]: http://access.aol.com/dhtml-style-guide-working-group/
  [2]: https://www.w3.org/TR/wai-aria-practices-1.1/
  [4]: https://standards.usa.gov/components/tables/
  [5]: https://getbootstrap.com/docs/4.0/content/tables/
  [6]: https://ebay.gitbooks.io/mindpatterns/content/structure/table.html
  [7]: http://webaim.org/techniques/tables/data
  [8]: http://webaim.org/techniques/tables/
  [9]: https://www.w3.org/WAI/tutorials/tables/
  [10]: https://jimthatcher.com/webcourse9.htm
  [11]: http://www.yourhtmlsource.com/tables/tablesaccessibility.html
  [12]: http://a11yproject.com/posts/accessible-data-tables/
  [13]: http://www.washington.edu/accessibility/web/tables/
