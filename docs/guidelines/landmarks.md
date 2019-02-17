# Place all content within landmarks regions
The **landmark role** delineates the segments of the page that contains content of significance so that they are easy to find and navigate.

## Why?
* communicate visual structural information to users of assistive technologies
* provide an easy way for users of assistive technologies to skip content blocks that are repeated on multiple pages
* facilitate sighted keyboard-only users navigate to different sections of a page using a browser add-on
* programmatically identify sections of a page
* convey the basic semantic meaning of the various areas of the page
* clearly identifies the relationships and meaning of elements on the page

## How
* Use the new HTML5 semantic tags and role atribute to identify the most important segments of the layout and structure of the page: 
  - `header` tag and `banner` role for the segment at the top of each page that identifies website - logo, site name, search tool 
  - `nav` tag and `navigation` role for a collection of links for navigation
  - `main` tag and `main` role for the main content of a page
  - `aside` tag and `complementary` role for content that supports the main but remains autonomous
  - `footer` tag and `contentinfo` role for a metadata applies to the site, such as copyrights, links to privacy statements, or disclaimers.
  - `search` role for the search tool of a website
  - `region` role for a significant element of the page that cannot be described by the role listed above.
* Use the `aria-label` or `aria-labelledby` attribute to identify multiple landmarks of the same type on the page
* Use the `aria-label` or `aria-labelledby` attribute to treat the section with roles="region" as a landmark.
* Element with `role="region"` (usually `section`) must have label.  Use the `aria-label` or `aria-labelledby` attribute to label it.
* Ensure that no content is orphaned, outside of landmarks.

## Pattern
### Example page structure

```html
<body>
   <header role="banner">
      // header content here
      <div role="search">
         // Search here
      </div>
   </header>   
   <nav role="navigation">
      // Navigation links here
   </nav>
   <main role="main">
      // Main content here
   </main>
   <aside role="complementary">
      // Complementary content here
   </aside>
   <section role="region" aria-label="Section name">
      // Significant content here
   </section>
   <footer role="contentinfo">
      // Footer content here
   </footer>
</body>
```

**Note**: New HTML5 tags have an implicit role, e.g tag `nav` have `navigation` role, tag `footer` have `contentinfo` role.  Using the `role` attribute is therefore redundant. But because Joomla supports Internet Explorer 11, which does not support new HTML5 tags, we also use the role attribute.   

### Labelling regions using `aria-labelledby`
```html
<nav role="navigation" aria-labelledby="landmark_heading_id">
   <h3 id="landmark_heading_id">Secondary menu</h3>
   <ul>
      <li><a href="url1">Page1</a></li>
      <li><a href="url2">Page2</a></li>
   </ul>	  
</nav>
```

### Labelling regions using `aria-label`
```html
<nav role="navigation" aria-label="Secondary menu">
   <ul>
      <li><a href="url1">Page1</a></li>
      <li><a href="url2">Page2</a></li>
   </ul>	
</nav>
```

## Reference
* [1.3.1 Info and Relationships. (Level A)](https://www.w3.org/WAI/WCAG20/quickref/#qr-content-structure-separation-programmatic).  
* [2.4.1 Bypass Blocks. (Level A)](https://www.w3.org/WAI/WCAG20/quickref/#qr-navigation-mechanisms-skip)
* [2.4.6 Headings and Labels. (Level AA)](https://www.w3.org/WAI/WCAG20/quickref/#qr-navigation-mechanisms-descriptive)
* [2.4.10 Section Headings (Level AAA)](http://www.w3.org/TR/WCAG20/#navigation-mechanisms-headings)

## Further reading
* [Web Accessibility Tutorials: Page regions](https://www.w3.org/WAI/tutorials/page-structure/regions/)
* [Web Accessibility Tutorials: Labeling Regions](https://www.w3.org/WAI/tutorials/page-structure/labels/)
* [ARIA Landmarks Example](https://www.w3.org/TR/wai-aria-practices/examples/landmarks/index.html)
* [Using navigation landmarks by Léonie Watson](https://accessibility.blog.gov.uk/2016/05/27/using-navigation-landmarks/)
* [Accessible Landmarks by Scott O'Hara](https://www.scottohara.me/blog/2018/03/03/landmarks.html)
* [HTML5 Sectioning and Landmark Elements by Keith J. Grant](https://keithjgrant.com/posts/2018/03/html5-sectioning-and-landmark-elements/)
* [Creating Accessible HTML: A Crash Course in ARIA Landmark Regions](https://medium.com/c2-group/creating-accessible-html-a-crash-course-in-aria-landmark-regions-40513850298b)

