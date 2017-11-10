# A single page accessibility test
The following is an example of a single page accessibility test sequence that can be used as a starting point for evaluation.

## Test 1. HTML Code validation

**Use the Nu Html Checker Validator (experimental).**

Does the validator report errors and warnings? [(4.1.1 Parsing - Level A)][1]

If the validator reports errors, write them down in the report.

If you recognize important comments, please report them in the report.

[Read the article on html validation.][2]

## Test 2. Automatic

**Execute one of the automated tests**. 

You can use browser add-ons, such as WAVE, AXE, OpenWAX, Accessibility Developer Toolbar or the selected web service.

[Read the article about automated tests.][3]

## Test 3. Navigation

### A. Website navigation

**Disconnect the mouse. If you use notebook cover the touch panel laptop. Move between links, buttons, and form controls using the TAB key.**

* Can all links, buttons, and form controls be handled from the keyboard? [(2.1.1 Keyboard -  Level A)][4]
* Can you see the content of all page elements, including dynamic elements such as tabs, accordions, drop-down panels, menus, sliders?
* Is the navigation order understandable - logical and intuitive (makes sense)? [(1.3.2 Meaningful Sequence - Level A)][5]
* Is there any focus on item selected? Are there any areas where focus disappears? [(2.4.7 Focus Visible - Level AA)][6]
* Does any content besides links, buttons and form controls, get focus?
* Can the focus always be moved, from the place where it is, using the TAB key? [(2.1.2 No Keyboard Trap - Level A)][7]

### B. Menu and other navigation elements

* Do the main menu items point to index pages?
* Can you access all menu items?
* Are the number of links in the menu and on the whole page too big and troublesome?
* Can you skip navigation and get straight to the main content? [(2.4.1  Bypass Blocks - Level A)][8]
* Are there any other ways to reach the subpages of your site (search engine, sitemap, etc.) [(2.4.5  Multiple Ways - Level AA)][9]
* Are the elements of the navigation in the same order, on subpages? [(3.2.3 Consistent Navigation - Level AA)][10]
* Are elements of the same functionality (such as page section titles, modules) designed consistently? [(3.2.4  Consistent Identification - Level AA)][11]
* Is the location of the current page/sequence in the site structure indicated [(2.4.8  Location - Level AAA)][12]

### C. Page title [(2.4.2 Page Titled - Level A)][13]
* Does the page have a unique title (different from other page titles)?
* Is the page title concise and descriptive?
* Does the page title signal its main content?
* Does the title include the name of the site?
* Are there only necessary and meaningful punctuation marks in the title?

## Test 4. Page structure
### A. Main areas
**Review the source code paying special attention to content areas**.
* Are the main areas of the page marked with appropriate tags or attributes roles (tag header or banner role, tag nav or navigation role, tag main or role main, tag footer or contentinfo role, aside tag or complementary role, search role)?
* Are all contents within the areas marked with landmarks?
* Is the site structure simple and understandable?

### B. Headings
**Examine the headlines. Use WAVE or OpenWAX.**
* Does the page have h1-h6 headers?
* Are headers used only for content headings?
* Does h1 heading start the main content of the page?
* Are page sections tagged with headings? [(2.4.10 Section Headings - Level AAA)][14]
* Do headlines properly describe the content they follow?
* Are there headline levels skipped with no reason?
* Are constant section headings consistent? 
  [(2.4.6  Headings and Labels - Level AA)][15]

### C. Paragraphs, lists and other text blocks
**Explore the main content organisation on the site**.
* Has the text been subdivided into sections with subheadings?
* Have suitable forms (paragraphs, lists, block quotes, tables) been used for content presentation? [(1.3.1 Info and Relationships - Level A)][16]
* Are content blocks (paragraphs, lists...) marked with the appropriate tags?
* Are there short paragraphs (2-5 lines)?
* Are the ordered and unordered lists used according to their purpose?

### D. Dynamic widgets (tabs, accordions, slides, panels, etc.)
* Do all interface elements have a specific name and role?
* Is the value of their attributes available for Assistive Technology? [(4.1.2  Name, Role, Value - Level A)][17]

## Test 5. Appearance - color - movement - time - sound
### A. Site layout
* Does the layout adapt to the viewing area? (responsive)
* Does the change of viewing area width causes the situation that order of the content elements becomes incomprehensible, illogical?

### B. Fonts size and enlargement
* Is the font size sufficiently large?
* Can you enlarge the font at least twice without special software?
* Is the content still readable?
* Do parts of text overlap?
* Does the content disappear outside the screen area?

### C. Color and contrast
* Is important information conveyed differently, than in a way that is not based solely on the senses, eg only by color? [(1.3.3 Sensory Characteristics - Level A][18], [1.4.1 Use of Color - Level A)][19]
* Is the contrast between text and background at least 4.5: 1 and for large fonts at least 3: 1?

### D. Time, movement, disturbance
* Can you stop, pause or hide moving, flicking, or auto-refreshing elements? [(2.2.2 Pause, Stop, Hide - Level A)][20]
* Are there any elements flashing with frequency more than 3 times per second or does the flash exceed the threshold values? (Three flashes or values below the threshold)
* Can you turn off, pause, or extend the time limit to read content or use site features? [(2.2.1 Timing Adjustable -Level A)][21]
* Can you skip or disable distracting elements (alarms, messages, information)? [(2.2.4 Interruptions - Level AAA)][22]

## Test 6. Links
**Scan the text of the links**.
* Does the place they go to follow their or their immediate surroundings context? [(2.4.4 Link Purpose (In Context) - Level A)][23]
* Are the names of links clear and understandable without context? [(2.4.9 Link Purpose (Link Only) – Level AAA)][24]
* Does each expression make sense (indicate the purpose of the link, match the title of the target page)?
* Do links on the site lead to unique places (are there repeated links to the same places)?
* Does every link work?
* Are the links highlighted (eg underlined, marked with an icon)?
* Are there "click here", "read more", "link to..." links?
* Do graphic links have alternate text?
* Are there uppercase URL addresses or emotion icons used in links?
* Is there a warning before opening new windows?
* Do download links provide helpful information?
* Are the pagination links (paging) understandable?

## Test 7. Graphics and Multimedia

### A. Graphics (text alternative) ([1.1.1 Non-text Content  – Level A][25])
* Do all graphics have the alt attribute (with or without value)?
* Does every meaningful graphic have an alternate text describing its content with up to 140 characters?
* Do alternative texts convey the same meaning as images?
* Do decorative graphics have an empty alt attribute? (`alt=""`)
* Do informative graphics (graphs, infographics) have a proper description in the text near the image?

### B. Multimedia (time-varying media)
* Are all audio recordings provided with an alternative text? 
* Are all recordings containing only moving pictures annotated with an alternative text or recording? [(1.2.1 Audio-only and Video-only (Prerecorded) – Level A)][26]
* Are all audiovideo recordings (movies) annotated by subtitles for deaf people? [(1.2.2 Captions (Prerecorded) – Level A)][27]
* Are all audiovideo recordings (movies) annotated by an audio description or alternative for media? [(1.2.3 Audio Description or Media Alternative (Prerecorded) – Level A)][28]
* Can you turn off automatic playback lasting longer than 3 seconds? [(1.4.2 Audio Control – Level A)][29]
* Are all audiovideo recordings (movies) recorded with audio description? [(1.2.5 Audio Description (Prerecorded) – Level AA)][30]
* Do live audiovisual broadcasts contain subtitles for the deaf? (1.2.4 Captions (Live) – Level AA)][31]

## Test 8. Forms
### A. Formal actions
**Fill out and submit the form by testing all controls and filling in all fields.**
* Do the forms work? Can any form element be selected and filled in?
* Does the selected form element receive focus?
* Does the cursor appear in the selected form element?
* Do all input fields have understandable labels or instructions? [(3.3.2 Labels or Instructions – Level A)][32]
* Can you send a correctly completed form?
* Does indicating form control with focus cause an unexpected change of its context? [(3.2.1 On Focus– Level A)][33]
* Does, while filling the form, unexpected change of the context appear? [(3.2.2 On Input – Level A)][34]

### B. Reaction to errors
**Investigate form responses to errors - fill incorrect data in different fields.**
* Can you send a form with an error?
* Is the incorrectly filled field marked (do the error areas have an indicator)?
* Is there any sensible suggestion next to the field, marked as incorrectly filled? [(3.3.1 Error Identification – Level A)][35]
* Does it detect any errors in the user input data that prompts them? [(3.3.3 Error Suggestion – Level AA)][36]
* Does the service provide adequate protection against errors involving legal, financial or other implications for entering and modifying data? [(3.3.4 Error Prevention (Legal, Financial, Data) – Level AA)][37]

## Test 9. Tables
**Scan the tables**.
* Are tables used to present data?
* Are tables simple or complex?
* Can you read tables descriptions or summaries? Do tables have a title in the `caption` tag and a summary in the `summary` tag?
* Are cells with headings marked with a `th` tag?
* Is the scope of each header specified with `scope="col"` or `scope="row"`?
* Are header cells' IDs, in complex tables, identified with `headers` attributes for each cell? [In the complex tables for each cell, have `headers` attributes been marked with header cell identifiers?] [(1.3.1 Info and Relationships – Level A)][38]

## Test 10. Understanding
* Is the language in which the content of the page is written properly declared? [(3.1.1 Language of Page – Level A)][39]
* Are text excerpts written in the other than basic language of the page correctly declared? [(3.1.2 Language of Parts – Level AA)][40]
* Does the content of the page require reading ability at a level higher than junior high school? [(3.1.5 Reading Level – Level AAA)][41]
* Do hallmarks help you to understand the content?
* Are the hallmarks, used, thrifty and justified?
* Are unusual words, expressions, abbreviations explained? [(3.1.3 Unusual Words – Level AAA][42], [3.1.4 Abbreviations – Level AAA)][43]

  [1]: https://www.w3.org/WAI/WCAG20/quickref/#qr-ensure-compat-parses
  [2]: https://github.com/joomla/accessibility/blob/master/docs/tutorials/testing-validation.md
  [3]: https://github.com/joomla/accessibility/blob/master/docs/tutorials/testing-automatic.md
  [4]: https://www.w3.org/WAI/WCAG20/quickref/#keyboard-operation-keyboard-operable
  [5]: https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-sequence
  [6]: https://www.w3.org/WAI/WCAG20/quickref/#navigation-mechanisms-focus-visible
  [7]: https://www.w3.org/WAI/WCAG20/quickref/#keyboard-operation-trapping
  [8]: https://www.w3.org/WAI/WCAG20/quickref/#navigation-mechanisms-skip
  [9]: https://www.w3.org/WAI/WCAG20/quickref/#navigation-mechanisms-mult-loc
  [10]: https://www.w3.org/WAI/WCAG20/quickref/#consistent-behavior-consistent-locations
  [11]: https://www.w3.org/WAI/WCAG20/quickref/#consistent-behavior-consistent-functionality
  [12]: https://www.w3.org/WAI/WCAG20/quickref/#navigation-mechanisms-location
  [13]: https://www.w3.org/WAI/WCAG20/quickref/#navigation-mechanisms-title
  [14]: https://www.w3.org/WAI/WCAG20/quickref/#navigation-mechanisms-headings
  [15]: https://www.w3.org/WAI/WCAG20/quickref/#navigation-mechanisms-descriptive
  [16]: https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-programmatic
  [17]: https://www.w3.org/WAI/WCAG20/quickref/#ensure-compat-rsv
  [18]: https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-understanding
  [19]: https://www.w3.org/WAI/WCAG20/quickref/#visual-audio-contrast-without-color
  [20]: https://www.w3.org/WAI/WCAG20/quickref/#time-limits-pause
  [21]: https://www.w3.org/WAI/WCAG20/quickref/#time-limits-required-behaviors
  [22]: https://www.w3.org/WAI/WCAG20/quickref/#time-limits-postponed
  [23]: https://www.w3.org/WAI/WCAG20/quickref/#navigation-mechanisms-refs
  [24]: https://www.w3.org/WAI/WCAG20/quickref/#navigation-mechanisms-link
  [25]: https://www.w3.org/WAI/WCAG20/quickref/#text-equiv-all
  [26]: https://www.w3.org/WAI/WCAG20/quickref/#media-equiv-av-only-alt
  [27]: https://www.w3.org/WAI/WCAG20/quickref/#media-equiv-captions
  [28]: https://www.w3.org/WAI/WCAG20/quickref/#media-equiv-audio-desc
  [29]: https://www.w3.org/WAI/WCAG20/quickref/#visual-audio-contrast-dis-audio
  [30]: https://www.w3.org/WAI/WCAG20/quickref/#media-equiv-audio-desc-only
  [31]: https://www.w3.org/WAI/WCAG20/quickref/#media-equiv-real-time-captions
  [32]: https://www.w3.org/WAI/WCAG20/quickref/#minimize-error-cues
  [33]: https://www.w3.org/WAI/WCAG20/quickref/#consistent-behavior-receive-focus
  [34]: https://www.w3.org/WAI/WCAG20/quickref/#consistent-behavior-unpredictable-change
  [35]: https://www.w3.org/WAI/WCAG20/quickref/#minimize-error-identified
  [36]: https://www.w3.org/WAI/WCAG20/quickref/#minimize-error-suggestions
  [37]: https://www.w3.org/WAI/WCAG20/quickref/#minimize-error-reversible
  [38]: https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-programmatic
  [39]: https://www.w3.org/WAI/WCAG20/quickref/#meaning-doc-lang-id
  [40]: https://www.w3.org/WAI/WCAG20/quickref/#meaning-other-lang-id
  [41]: https://www.w3.org/WAI/WCAG20/quickref/#meaning-supplements
  [42]: https://www.w3.org/WAI/WCAG20/quickref/#meaning-idioms
  [43]: https://www.w3.org/WAI/WCAG20/quickref/#meaning-located
