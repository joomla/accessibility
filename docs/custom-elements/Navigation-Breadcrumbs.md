# Breadcrumbs
## What it this
**Purpose**: Users need to understand their current location and navigate, within a hierarchical navigation scheme.

**Description**: _Breadcrumbs_ or _Breadcrumb trail_ consists of a list of links to the parent pages of the current page, in hierarchical order.  Breadcrumbs let the user know their current position, in the site hierarchy and gives the ability to navigate up the structure, easily.

Breadcrumbs are often placed horizontally before a page's main content.

The term 'breadcrumbs' comes from the trail of breadcrumbs left by Hansel and Gretel in the popular fairytale.

## Accessibility
### Accessibility specification
Accessible Breadcrumbs specification is defined in WAI-ARIA Authoring Practices 1.1. See [2.5 Breadcrumb](https://www.w3.org/TR/wai-aria-practices/#breadcrumb)

### Keyboard interaction
* **Tab** key moves from breadcrumb to breadcrumb. The last breadcrumb is not a link and therefore must not be in the tab order.

### Screenreader interaction
* The screen reader will recognize the breadcrumbs as a navigation landmark.
* Each breadcrumb will be announced as 'link', followed by the link text.
* The screen reader can be announced each separator symbol as 'greater than'. 
  **Note**: To prevent screen reader announcement of the visual separators between links, they are added via CSS.


## ARIA markup
* `role="navigation"`: Defines the breadcrumb element as the navigation landmark region.
* `aria-label="Breadcrumb"` or `aria-labelledby="IDREF"`: Provides a label or item ID that describes the type of navigation provided in the breadcrumb.
* `aria-current="page"`: Applied to the last link, in the set, to indicate that it represents the current page. If the element representing the current page is not a link, `aria-current` is optional.

## Utilities
### When to use
* Use breadcrumb navigation for large websites and websites that have hierarchically arranged pages. 
### When to consider something else
* Breadcrumbs should not be used for single-level websites that have no logical hierarchy or grouping.
* Breadcrumb navigation should be regarded as an extra feature and shouldn’t replace effective primary navigation menus.


## Use in Joomla
* Module **Breadcrumbs**

## Best practices
* The set of links is structured using an ordered list.
* Used as secondary navigation.
* Never replace primary navigation. 
* Not be used, if all the pages are on the same level.
* Show the site hierarchy, not the user's history. 
* Be located in the top half of your web page. 
* Not be too large. 
* Progress from the highest level to the lowest, one step at a time.
* Start with the homepage and end with the current page.
* The last breadcrumb is not clickable. 
* Have a simple, one-character separator between each level (usually _greater than_ symbol `>`).
* Not be cluttered with unnecessary text such as "You are here" (this guideline is debatable).
* Include the full navigational path from the homepage to the current page.
* Include the full page title in the breadcrumb trail. 

## Mistakes in breadcrumbs implementation
* Using breadcrumbs when you don’t need to.
* Using breadcrumb trails as primary navigation.
* Using breadcrumbs when pages have multiple categories.

## Resources
### WCAG references
* [2.4.8 Location](https://www.w3.org/TR/2008/REC-WCAG20-20081211/#navigation-mechanisms-location) - Level AAA: Information about the user's location within a set of Web pages is available.
* [Techniques for WCAG 2.0. G65: Providing a breadcrumb trail](https://www.w3.org/TR/WCAG20-TECHS/G65.html)

### Design patterns
* [WAI-ARIA Authoring Practices 1.1 - Breadcrumb Example](https://www.w3.org/TR/wai-aria-practices/examples/breadcrumb/index.html)
* [Techniques for WCAG 2.0 - G65: Providing a breadcrumb trail](https://www.w3.org/TR/WCAG20-TECHS/G65.html)
* [Jonathan Neal: Accessible breadcrumbs markup](https://codepen.io/jonneal/pen/ianKu)
* [Karl Adams: Schema & Accessible Breadcrumbs](https://codepen.io/Five50/pen/reQREV)
* [ZURB Foundation: Breadcrumbs](http://foundation.zurb.com/sites/docs/v/5.5.3/components/breadcrumbs.html)
* [Microformats: breadcrumbs-formats](http://microformats.org/wiki/breadcrumbs-formats)

### Articles
* [Accessible breadcrumbs using ARIA](https://www.uvd.co.uk/blog/accessible-breadcrumbs-using-aria/)
* [Chris Coyier: Exploring Markup for Breadcrumbs](https://css-tricks.com/markup-for-breadcrumbs/)
* [Jacob Nielsen: Breadcrumb Navigation Increasingly Useful](https://www.nngroup.com/articles/breadcrumb-navigation-useful/)
* [Justin Mifsud: 12 Effective Guidelines For Breadcrumb Usability and SEO](http://usabilitygeek.com/12-effective-guidelines-for-breadcrumb-usability-and-seo/)
* [Jacob Gube: Breadcrumbs In Web Design: Examples And Best Practices](https://www.smashingmagazine.com/2009/03/breadcrumbs-in-web-design-examples-and-best-practices/)
* [Thomas Baekdal: Usable Breadcrumbs with Guidelines](https://www.baekdal.com/insights/breadcrumbguidelines)
* [Michel Vloon: Mission Impossible? Making Drupal 7 more accessible](https://www.nomensa.com/blog/2015/mission-impossible-making-drupal-7-more-accessible)
* [Brandon Leibowitz: Breadcrumb Navigation: Good for Website Usability or Not?](http://blog.usabilla.com/breadcrumb-navigation-good-website-usability-not/)
* [Garret Fick: Breadcrumbs and Web Accessibility](http://www.ficksworkshop.com/blog/post/breadcrumbs-and-web-accessibility)


