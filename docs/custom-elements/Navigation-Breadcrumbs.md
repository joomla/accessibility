# Breadcrumbs (draft)
**Purpose**: Users need to understand their current location and navigate within a hierarchical navigation scheme.

**Description**: Breadcrumbs display the current path to a particular page relative to the starting point. Breadcrumbs let the user know their current position in the site hierarchy and the ability to navigate up the structure easily.
The term 'breadcrumbs' comes from the trail of breadcrumbs left by Hansel and Gretel in the popular fairytale.

### Keyboard interaction
* **Tab** key moves from breadcrumb to breadcrumb. The last breadcrumb is not a link and therefore must not be in the tab order.

### Screenreader internaction
* The screen reader will recognize the breadcrumbs as a navigation landmark.
* Each breadcrumb will be announced as 'link', followed by the link text.
* The screen reader will announce each separator symbol as 'greater than'. This is the typically convention for separating breadcrumbs.

## Best Practices
* Breadcrumbs are typically used as secondary navigation on sites that are organized in a hierarchical manner.
* The breadcrumb pattern has two conventions that set it apart from a typical list of ordered links.
* The navigation root is the first element, the current location is the last element.
* The 'greater than' symbol > is used to separate each link.
* The last breadcrumb is not clickable.
* Breadcrumbs must have a heading of 'You are here', or words to those effect. This heading can be hidden offscreen using the **.?????** class.
* Depending on the complexity of the navigational hierarchy and the type of page or application, it may make sense for the breadcrumb to represent only part of the hierarchy while sub tabs/trees/navigation represent the remaining hierarchy. In that case, you may want to make the far right element clickable.


## Resources
### Articles
* [Accessible breadcrumbs using ARIA](https://www.uvd.co.uk/blog/accessible-breadcrumbs-using-aria/)
* [Chris Coyier: Exploring Markup for Breadcrumbs](https://css-tricks.com/markup-for-breadcrumbs/)
* [Jacob Nielsen: Breadcrumb Navigation Increasingly Useful](https://www.nngroup.com/articles/breadcrumb-navigation-useful/)
* [Michel Vloon: Mission Impossible? Making Drupal 7 more accessible(https://www.nomensa.com/blog/2015/mission-impossible-making-drupal-7-more-accessible)
* [Brandon Leibowitz: Breadcrumb Navigation: Good for Website Usability or Not?](http://blog.usabilla.com/breadcrumb-navigation-good-website-usability-not/)

### Design patterns
* [WAI-ARIA Authoring Practices 1.1 - Breadcrumb Example](https://www.w3.org/TR/wai-aria-practices/examples/breadcrumb/index.html)
* [Techniques for WCAG 2.0 - G65: Providing a breadcrumb trail](https://www.w3.org/TR/WCAG20-TECHS/G65.html)
* [Jonathan Neal: Accessible breadcrumbs markup](https://codepen.io/jonneal/pen/ianKu)
* [Karl Adams: Schema & Accessible Breadcrumbs](https://codepen.io/Five50/pen/reQREV)
* [ZURB Foundation: Breadcrumbs](http://foundation.zurb.com/sites/docs/v/5.5.3/components/breadcrumbs.html)
* [Microformats: breadcrumbs-formats](http://microformats.org/wiki/breadcrumbs-formats)
