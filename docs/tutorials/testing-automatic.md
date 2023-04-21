# Automatic accessibility testing
Wouldn't it be great to connect the website to a slot machine that would examine all aspects of its accessibility and prepare a report on detected violations of WCAG 2.0 rules? After all, success criteria are concrete, measurable indicators.

Unfortunately! That is not possible. In the wide range of automatic tools, there is no one that can perform a full accessibility audit.
This is not because existing tools are imperfect, but because many aspects of accessibility require human evaluation. For example, the machine checks, whether the images have alternative text. But it won't decide whether the alternative text describes the content of the image well. This can only be done by a person. 

Automated testing ensures that approximately 25% of the accessibility best practices can be thoroughly tested. Another 35% or so can be checked by machine testing but the results require human verification.

This means that over 70% of good accessibility practices can not be tested automatically.

Despite the fact that a large number of accessibility best practices cannot be tested for automatically, they can find and indicate many accessibility errors. 
Therefore, you should always carry out automatic tests first. Karl Groves was right to write a few years ago:

 1. You should never pay a human to find errors that can be found through automated testing.
 2. Manual testing will close the gaps on what automated testing couldn’t find.
 3. You should never uncover errors in use case or usability testing that couldn’t be found by automated and manual testing.

Automatic accessibility tests are tests performed by means of desktop or web-based application, web services, browser plug-in or IDE plug-in. 

The [list of automatic tools that leads the W3C WAI](https://www.w3.org/WAI/ER/tools/) currently counts more than 100 items. Among them are comprehensive tools and tools that test individual aspects of accessibility. Look at this list to find the right tools for your needs.

Below you will find some of the most popular and most effective - in our opinion - tools. Try them. Perhaps the cornerstone of your accessibility tester workshop.
* **Web services**
  - [CynthiaSays](http://www.cynthiasays.com/)
  - [Tenon](https://tenon.io/)
  - [FAE](https://fae.disability.illinois.edu/anonymous/?Anonymous%20Report=/)
  - [WAVE](http://wave.webaim.org/)
  - [AChecker](https://achecker.ca)
* **Browser plug-in**
  - [AXE Dev Tools for Chrome](http://bitly.com/aXe-Chrome), [AXE for Firefox](http://bit.ly/aXe-Firefox) by Deque University
  - WAVE Evaluation Tool [for Chrome](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh) and [for Firefox](https://addons.mozilla.org/en-US/firefox/addon/wave-toolbar/)
  - [Accessibility Developer Tools](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb) for Chrome
  - OpenWAX (Open Web Accessibility eXtension) [for Chrome](https://chrome.google.com/webstore/detail/openwax/bfahpbmaknaeohgdklfbobogpdngngoe) and [for Firefox](https://addons.mozilla.org/pl/firefox/addon/openwax/)
  - [Juicy Studio Accessibility Toolbar](https://addons.mozilla.org/pl/firefox/addon/juicy-studio-accessibility-too/) for Firefox
  - [OpenAjax Accessibility Extension](https://addons.mozilla.org/en-US/firefox/addon/openajax-accessibility-exte/) for Firefox by Jon Gunderson
  - [WCAG Contrast Checker](https://addons.mozilla.org/pl/firefox/addon/wcag-contrast-checker/) for Firefox by Rumoroso
  - [tota11y](http://khan.github.io/tota11y/)
* **IDE plug-in**
  - [AXE-core](https://www.axe-core.org/) by Deque University
* **Desktop application** 
  - [Accessibility Viewer by Pacciello Group](https://developer.paciellogroup.com/resources/aviewer/)
  - [AChecker](http://www.atutor.ca/achecker/download.php)
  - [Colour Contrast Analyser by Pacciello Group](https://developer.paciellogroup.com/resources/contrastanalyser/)
  
 ## Resources
 * [Efficiency in Accessibility Testing or, Why Usability Testing Should be Last by Karl Groves](http://www.karlgroves.com/2012/04/27/efficiency-in-accessibility-testing-or-why-usability-testing-should-be-last/)
