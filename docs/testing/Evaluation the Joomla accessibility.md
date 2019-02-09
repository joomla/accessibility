## What is accessibility evaluation
An accessibility evaluation shall verify that all relevant parts of a website are accessible to everyone whatever their hardware, software, language, location, or ability. This means that all relevant elements of the website should be perceivable, operable, understandable and robust.

The evaluation shall verify compliance with the success criteria defined, in the WCAG and ATAG. But the purpose is not to declare compliance with the guidelines. The goal is real, functional accessibility of the website for different users.

You do not need to be a specialist to evaluate the web accessibility. Anyone who wants to can carry out simple accessibility tests. Do not be afraid that you will make mistakes. Don't be afraid that your evaluation will be imperfect. Don't be afraid that it will be incomplete.

If your evaluation helps to fix even a few accessibility issues, it will be a great success. Simple accessibility testing detects up to 80% of accessibility issues. That is a very big amount. If all the pages had been accessible only 80%, the Internet would already have been great.

Do not wait until you have enough knowledge and skills. Apply a gradual approach. Start with simple tests to get more and more complete assessment, as you gain experience.

## Where to start?
If you're just starting your accessibility evaluation adventure, use the great W3C WAI guide: [Easy Checks - A First Review of Web Accessibility](https://www.w3.org/WAI/test-evaluate/preliminary/). 

It is a very good idea to practice with:
* [Assessment: Accessibility troubleshooting](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/Accessibility_troubleshooting)
* [The Before and After Demonstration (BAD)](https://www.w3.org/WAI/demos/bad/).

Explore and evaluate any website, such as your own. You will gain first good experiences and basic knowledge about accessibility. You will get to know some helpful tools. 
 
## Site accessibility evaluation vs. Joomla! CMS evaluation
Joomla CMS is an authoring tool. The accessibility requirements for authoring tools are defined by [Authoring Tool Accessibility Guidelines (ATAG)](https://www.w3.org/TR/ATAG/). 

Evaluating the accessibility of authoring tools is more complex than evaluating the web accessibility. However, this does not mean that the evaluation of Joomla! CMS accessibility is much different from the evaluation of websites accessibility. On the contrary, it is similar because ATAG in Part A defines the guidelines for the accessibility of user interfaces for authoring tools. In short, the user interfaces should meet the success criteria of WCAG 2.1. 

However, part B of ATAG, on the other hand, provides guidance on how authoring tools should support the production of accessible content. However, this will be the subject of another guide.

To summarize, gaining some experience in assessing web accessibility is a necessary step in acquiring the competence to evaluate the accessibility of authoring tools and the evaluation, of the accessibility of the authoring tools interface, requires the same actions as the evaluation, of the web accessibility.

## Evaluation the Joomla accessibility as an authoring tool
Over time, as you gain experience, each evaluator develops his own evaluation methodology. You will also discover the best tools and procedures for you.

### Step 1. Overview of the page
Always start with a review of the page you are going to evaluate. Explore a number of key issues in this review:
* **Purpose.** Can you tell what the page is for? 
* **Structure.** What is the interface layout? What key areas can you distinguish on the page? Which of these areas are repeated on other pages of this type? Which elements are unique?
* **Presentation.** Are all the elements on the page perceivable? Visible? Is there hidden content and can you see it?
* **Navigation.** How can you navigate the page? Can you get to everything on the page?
* **Interaction.** What can you do on this page? What task or tasks can you perform?

### Step 2. Specify the scope of the evaluation
Based on the review of the page structure, decide whether you want to evaluate all or only selected elements of the page. If you decide to evaluate only selected elements of a page, decide which elements will be evaluated. We usually evaluate the accessibility of the key areas of the website and the directly related elements. 

Elements that appear as standard on all or many pages, such as header, footer, admin menu, are evaluated separately. Of course, all other accessibility issues that are detected can be reported in the report but you should focus on the specific features of the tested page or the evaluation, of a selected element of the user interface.

### Step 3. Perform automatic tests
Do not waste your valuable time searching for errors that can be detected by automatic tests. Automatic testing ensures that around 25% of best accessibility practices can be thoroughly tested. In addition, automated tests may indicate a further 35% of the problems that need to be confirmed by a human being. That is why it is best to start with automatic tests.

There are many very good tools for automatic testing and new ones are coming into being. These tools help to organize an evaluation and may provide insight into issues that are not easily recognizable. No tool does everything. That's why it's a good idea to get become familiar with a various tools available and using a few selected ones. Here are some suggestions to consider:

* [WAVE](http://wave.webaim.org/extension/): a browser extensions offered by WebAIM that allows you to evaluate the accessibility of web pages directly in Chrome and Firefox. It can also check pages, to which access is password protected, such as Joomla Backend pages.
* [aXe](https://axe-core.org/): small, portable, lightweight JavaScript library offered by Deque University that executes automated accessibility testing inside your browser (Chrome, Firefox) or testing framework. Because it works in your browser, you can also use it to check for password-protected pages. 
* [Lighthouse](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk): an automated tool for Chrome to improve the performance, quality and correctness, including the accessibility, of web applications.
* [tota11y - an accessibility visualization toolkit](http://khan.github.io/tota11y/): a Javascript that you can add to your site or use as a bookmarklet in any desktop browser. Indicates accessibility errors and suggests ways to fix them.
* [HTML_CodeSniffer](http://squizlabs.github.io/HTML_CodeSniffer/): bookmarklet that run on all popular browsers. It can also be called at the source of the page. HTML_CodeSniffer checks a HTML document or source code, and detects violations of a defined presentation or accessibility standard. All these tools not only detect and indicate accessibility issues, but also explain what these issues are and suggest how to solve them.

All these tools not only detect and indicate accessibility issues, but also explain what these issues are and suggest how to solve them.

Note that some of these tools allow you to select a target level of compliance with WCAG or Section 508 standards.

For more information, see the following articles: 
* [The problem with automated accessibility testing tools](https://www.webcredible.com/blog/problem-automated-accessibility-testing-tools/)
* [What we found when we tested tools on the world’s least-accessible webpage](https://accessibility.blog.gov.uk/2017/02/24/what-we-found-when-we-tested-tools-on-the-worlds-least-accessible-webpage/)
* [Automated Web Accessibility Testing Tools Are Not Judges](http://www.karlgroves.com/2017/03/24/automated-web-accessibility-testing-tools-are-not-judges/)

### Step 4. Perform automatic manual tests
The purpose of the manual tests is to evaluate the properties of a page, which cannot be checked automatically. Almost all of the tools, above, indicate which features require manual testing. To test the accessibility of these elements, you can:
* perform a code inspection
* manipulate the browser and hardware (mouse, keyboard).

For manual testing, our tests kit can be helpful: [A single page accessibility test](https://github.com/joomla/accessibility/blob/master/docs/testing/testing-single-page.md)

### Step 5. Explore the feasibility of all tasks under special conditions 
When we examine the accessibility of administrative interfaces, it is fundamental that we are able to effectively perform all the tasks that the page serves. However, our task is not to carry out basic usability tests, but to examine whether all tasks are feasible, for those with accessibility difficulties. For example, can all tasks be performed by people who use only the keyboard and cannot use the mouse.

Typical ways to assess the feasibility of tasks under special conditions are by testing:
* testing with keyboard only
* checking with assistive technology.

#### Keyboard testing
Keyboard testing is an essential part of any accessibility evaluation. A page can only be successfully evaluated if two conditions are met:
* each action on the page can only be performed using the keyboard
* all interactions with the keyboard are predictable.

Testing a page with keyboard requires no special tools or skills. Necessarily, unplug the mouse and cover the touchpad. Then navigate the page using the keyboard and perform administration tasks.
* Do you always see where you are?
* Do you have access to all functions?
* Can you run all the controls? 
* Isn't there a keyboard trap somewhere?

Here is a list of common keys used in keyboard operation:
* **Tab**: move to the next interactive elements (ink, form element or button)
* **Shift+Tab**: move to the previous interactive elements
* **Arrow keys**: move between radio buttons, menu links, tab panels, list options, sliders, tree menus, etc.
* **Enter**: activate the current link or button, expand the menu, select a menu option 
* **Space**: check or uncheck a checkbox form element, activate the current button, expand the option list
* **Escape**: close the current modal dialog or dropdown menu and return focus to the element that spawned it.

**Note**: To toggle Mac keyboard accessibility press Control + F7. To activate the Tab key in Safari, go to Preferences > Advanced > Accessibility and check the Press Tab. 

For more information, see the following articles:
* [Keyboard Accessibility](https://webaim.org/techniques/keyboard/)
* [Quick Reference](https://webaim.org/resources/evalquickref/)
* [Using Keyboard-only Navigation, for Web Accessibility](https://www.practicalecommerce.com/Using-Keyboard-only-Navigation-for-Web-Accessibility)
* [Designing for Keyboard Accessibility](https://www.washington.edu/accessibility/checklist/keyboard/)
* [18F Accessibility Guide. Keyboard access](https://accessibility.18f.gov/keyboard/)

#### Screen reader testing
Checking a website with a screen reader is an invaluable way to make sure that a website is functionally accessible.
* **Windows users** can use the free [NVDA screen reader](https://www.nvaccess.org/).
* **Mac users** can use the native [Voiceover screen reader](https://help.apple.com/voiceover/info/guide/10.12/?lang=en) utility. 
* **Linux users** can use the [screen reader Orca](https://help.gnome.org/users/orca/stable/). 

All are free and have a low learning curve. 

Instead of a screen reader, you can use [ChromoVox for Chrome](https://chrome.google.com/webstore/detail/chromevox/kgejglhpjiefppelpmljglcjbhoiplfn). It is a highly effective tool for developers when testing Web content.

For more information, see the following articles:
* [Using NVDA to Evaluate Web Accessibility](https://webaim.org/articles/nvda/)
* [Using VoiceOver to Evaluate Web Accessibility](https://webaim.org/articles/voiceover/)
* [Using JAWS to Evaluate Web Accessibility](https://webaim.org/articles/jaws/)
* [Basic screen reader commands for accessibility testing](https://developer.paciellogroup.com/blog/2015/01/basic-screen-reader-commands-for-accessibility-testing/)

### Step 6. Reporting the results of accessibility evaluation
The accessibility evaluation should end with a factual report so that designers, programmers and webmasters can solve the problems detected.

It is a good idea to save the report in one document and use a simple template:
* **Report title** 
* **Review process**:
  * **Scope of review**. Name of site/page/UI component
  * **Date of review**. Range of dates on which review conducted
  * **Reviewers**. Name of reviewer or review team
  * **Evaluation environment**. Briefly inform about the operating system, browser and versions thereof
  * **Method and tools**. Describe method and tools used, their versions
* **Result and recommended action**
  * **Summary of results**. Specify if it meets/does not meet/is close to meeting WCAG 2.1 AA / ATAG 2.0
  * **Strengths**. Indicate features in which this site/page/UI component is strong
  * **Failures and recommendations**
    * **Problem**. Name each problem identified
    * **Explanation**. Explain why this is a problem, how it can make accessibility more difficult for users. Describe the difficulty of accessing the object and its contents or functionality.
    * **References to standards**: If possible, indicate references to WCAG and/or ATAG references.
    * **Suggested remedies**. Propose practical techniques to achieve compliance or improve accessibility. You can indicate the appropriate solutions from the document [Techniques for WCAG](https://www.w3.org/TR/WCAG20-TECHS/) (It is best to look for tips [How to Meet WCAG 2](https://www.w3.org/WAI/WCAG21/quickref/)

### Step 7. Reporting the problems in the Joomla! Issue Tracker
Reporting issues is essential to the development of Joomla. By reporting issues, anyone can contribute to the development of Joomla. Everyone can report detected bugs and faults, suggestions for code improvements and ideas for new features. 

If you want to be sure that the problems you detected will be considered and solved by the Project Team, report them in the system [Joomla! Issue Tracker](https://issues.joomla.org/).
To report problems, you must have a Github account. The Joomla! Issue Tracker uses GitHub accounts for authentication.

Each problem must be reported separately. 

When you reporting problems in the Joomla! Issue Tracker, simply use the descriptions you provided in the previous step to report them.

