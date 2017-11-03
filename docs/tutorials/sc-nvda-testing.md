# NVDA testing

NVDA is a Windows-based screen reader and is best used with Firefox.

NVDA has two different viewing modes:

* **Browse mode** presents the textual information on web pages to the user and allows the user to navigate the page.
* **Focus mode** allows the user to interact with forms and ARIA-enabled DHTML elements.

The system focus, also known simply as the focus, is the object which receives keys, typed on the keyboard. For example, if you are typing into an editable text field, the editable text field has the focus.

The most common way of navigating around Windows with NVDA is to simply move the system focus using standard Windows keyboard commands, such as pressing **Tab** and **Shift** + **Tab** to move forward and back between controls, pressing **Alt** to get to the menu bar and then using the arrows to navigate menus, and using **Alt** + **Tab** to move between running applications. As you do this, NVDA will report information about the object with focus, such as its name, type, value, state, description, keyboard shortcut and positional information.

When an object that allows navigation and/or editing of text is focused, you can move through the text using the system caret, also known as the edit cursor.

When the focus is on an object that has the system caret, you can use the arrow keys( **↓** and **↑** ), **PageUp**, **PageDown**, **Home**, **End**, etc. to move through the text. You can also change the text if the control supports editing. NVDA will announce as you move by character, word and line, and will also announce as you select and unselect text.

Keep the following in mind as you interact with the web page:

* NVDA intercepts the arrow keys and some other keys (noted in brackets next to each instruction) to offer additional navigation operations for the user. View a list of [NVDA keyboard shortcuts](http://webaim.org/resources/shortcuts/nvda). * NVDA's "browse" cursor may not always follow the visible cursor, so do not trust your eyes--trust your ears! Better yet, turn off or cover up your monitor.
* NVDA will try to switch between "browse" and "focus" modes automatically when the user navigates with a tab key and encounters a form element or leaves a form and encounters a link. The change between modes will be indicated by two distinct sounds.
* If NVDA does not change the modes automatically, press the **space** bar on an edit control or an ARIA-enabled widget to force the switch in modes.

For more information on testing web pages with NVDA, see the WebAIM article [Using NVDA to Evaluate Web Accessibility.](http://webaim.org/articles/nvda/)

## The testing procedure

The following is a sample testing sequence using NVDA that you can use as a starting point for your evaluation.

 1. Open NVDA.
 1. Open your web browser and type in the address you want to check.

| Step&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| Test | Yes | No | Note |
| --- | --- | --- | --- | --- |
| **Test 1** | **Listen to the page from top to bottom**.<br />- Is all of the content read? <br />The page should read top-to-bottom automatically. Use the **Ctrl** key if you wish to pause, and then use the **↓** to proceed through the document, line by line. Is all of the content read? Return to the top of the page ( **Ctrl**+ **Home**) | - | - | - |
| **Test 2** | **Listen to the page title** ( **NVDA** + **t**).<br />- Does it uniquely describe the page content? | - | - | - |
| **Test 3** | **Tab through links and form inputs** ( **Tab**).<br />- Are they read in an order that makes sense?<br /> Does any content receive focus besides links and inputs? | - | - | - |
| **Test 4** | Check the page structure ( **NVDA** + **F7** -> Landmarks). - Are the main areas of the page marked (banner, navigation, main content, contentinfo, complementary)?<br />- Is the site structure simple and understandable? | - | - | - |
| **Test 5** | **Scan the headings** ( **h** and **Shift**+ **h**).<br />- Does the page have headings?<br />- Do the individual headings make sense?<br />- Are the heading levels read?<br />- Does the hierarchy of headings make sense? | - | - | - |
| **Test 6** | **Scan the link phrases** ( **k** and **Shift**+ **k**).<br />- Do the individual phrases make sense?<br />- Are there redundant entries? | - | - | - |
| **Test 7** | **Tab through the links** :<br />- Does each link work? (press **Enter** to check)<br />- Does each link phrase match the destination page title?<br />- Is the link text uniquely descriptive? | - | - | - |
| **Test 8** | **Examine the graphics** ( **g** and **Shift**+ **g**).<br />- Does each graphic have proper alt text or is merely the image name announced (an error)?<br />- If the image is a link is the link destination the alt text or is it an image description (an error)? | - | - | - |
| **Test 9** | **Test any web forms** : - Scan the form fields ( **f** and **Shift**+ **f**)<br />- Are form labels announced with input boxes or operations?<br />- Do the forms work? (switching to forms mode should be automatic; press **NVDA** + **Space** to force a change in mode)<br />- Can data be entered and the form submitted? ( **Enter**) | - | - | - |
| **Test 10** | **Test any tables** : - Scan the tables ( **t** and **Shift**+ **t**).<br />- Are table captions or summaries read?<br />- Does the table information make sense navigating between cells? ( **↓** and **↑**) | - | - | - |
| **Test 11** | **Test any widgets** (as tabs, accordion, tooltip):<br />- Is the type of widget announced, when it receives focus? <br />- Can the widget be manipulated using the keyboard? <br />- Is it clear how to use it?<br />- If it is not clear how to use the widget, is an explanation provided? | - | - | - |
| - | Quit NVDA ( **NVDA** + **q**) | - | - | - |

## Resources
* [Evaluating accessibility with NVDA](http://webaccess.hr.umich.edu/eval/nvda.html) (source)
* [Using NVDA to Evaluate Web Accessibility](https://webaim.org/articles/nvda/)
* [Evaluating web accessibility with NVDA](http://bd.ub.edu/adaptabit/en/content/Evaluating-web-accessibility-NVDA)
* [Using NVDA to Evaluate Web Accessibility - Cal OES](http://www.caloes.ca.gov/AccessFunctionalNeedsSite/Documents/NVDA%20to%20Evaluate%20Web%20Accessibility.docx)
* [Basic screen reader commands for accessibility testing by Léonie Watson](https://developer.paciellogroup.com/blog/2015/01/basic-screen-reader-commands-for-accessibility-testing/)
