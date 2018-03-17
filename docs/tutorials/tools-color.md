# Color tools &#8211; generators, simulators, checkers

Appropriate choice of colors is a very important aspect of web accessibility.

If there is not enough contrast between the text and the background, people will have problems. People with blindness or other visual impairments, as well as persons browsing the Web in less than ideal conditions (bad monitor, window reflections, sunlight striking the screen),  may not be able to read the text, at least not without difficulty.

[Read more about visual impairments](tutorials/understanding-disability.md).

## Color schemes vs. accessibility standards

[Web Content Accessibility Guidlines 2.0](http://www.w3.org/TR/WCAG20/#visual-audio-contrast-contrast) require that text (and images of text) provide adequate contrast for people who have visual impairments. Contrast is measured using [a formula](http://www.w3.org/TR/WCAG20/#contrast-ratiodef) that gives a ratio ranging from 1:1 (no contrast, e.g., black text on a black background) to 21:1 (maximum contrast, e.g., black text on a white background).

WCAG 2.0 requires that there is sufficient luminance contrast between text and background color: 

* **Success criteria 1.4.3 Contrast (Minimum)** (Level AA): The visual presentation of text and images of text has a contrast ratio of at least 4.5:1, except for the following: 
  - Large Text: Large-scale text and images of large-scale text have a contrast ratio of at least 3:1; […]

* **Success criteria 1.4.6 Contrast (Enhanced)** (Level AAA): The visual presentation of text and images of text has a contrast ratio of at least 7:1, except for the following: 
  - Large Text: Large-scale text and images of large-scale text have a contrast ratio of at least 4.5:1; […]"

## Color tools list

On the web, we have tools that can be used to check whether the colors used on the website are in compliance with the relevant WCAG 2.0 accessibility levels. They can also make it easier for web developers to design an accessible website.

It is worth knowing that there are are different algorithms used to calculate contrast ratios. Some tools use the luminosity contrast ratio algorithm mentioned by the WCAG (Web Content Accessibility Guidelines) 2.0 working draft, while others use the colour brightness and colour difference algorithms that are mentioned in a companion document to WCAG 1.0. Some even use both.

Note that neither of these algorithms are W3C recommendations (at least not yet), but they are still useful for determining if a combination of text and background colours is likely to cause problems for people with colour blindness or other visual impairments.

Choosing the right tools from such an extensive list can be difficult, especially for beginners. We encourage you to get acquainted with them. Short quotes will help you find out about their functions. 

Below you will find a list of tools that help you choose the right color for your pages. 

## Color finder tools

- [A11y Color Palette &#8211; by Matt Long](http://a11yrocks.com/colorPalette/)

  "This tool should help you visualize an entire palette of colors with accessibility in mind. An indicator will be placed next to each foreground color to show if its contrast with the background color is WCAG 2.0 AA and/or AAA compliant for normal and large text. No indicator next to a foreground color means its contrast ratio with the background color is not at all compliant." 

* [Accessibility Color Wheel &#8211; Giacomo Mazzocato](http://gmazzocato.altervista.org/colorwheel/wheel.php)

  "Choose a foreground color by pointing the mouse over the wheel or the vertical grey gradation strip and click or, if you have a touch screen, just touch them. Then click the 'Background' button and choose a background color the same way. If a checkmark becomes visible the color pair is good for accessibility. Otherwise change one color or both by selecting foreground or background with the buttons." 

* [Accessible color palette builder &#8211; by &#8220;toolness&#8221;](https://toolness.github.io/accessible-color-matrix/)

  "This is a tool to help designers build color palettes with combinations that conform with accessibility standards."
  
* [Color Contrast Checker &#8211; by SSB Bart Group](http://www.ssbbartgroup.com/reference/color-contrast-checker/)

  "Enter a RGB foreground and background color in #hex or integer format to check contrast for accessibility."

* [Color Contrast iOS app &#8211; UserLight Ltd](https://itunes.apple.com/na/app/color-contrast/id1095478187)

  "Color Contrast is a tool to measure the contrast between two colors in a screenshot or mobile website, helping ensure your app meets the internationally recognized recommendations in the Web Content Accessibility Guidelines (WCAG) 2.0."  
   
* [Colour Contrast Determinator &#8211; Vision Australia](http://www.visionaustralia.org/business-and-professionals/digital-access-consulting/resources/tools-to-download/colour-contrast-determinator)
 
   "This tool is a colour contrast analyser that makes it easy to find colours with sufficient contrast. Simply type in colour values or copy and paste a value form a style sheet, then use the sliders to adjust the colour - full height on the slider means the colour has sufficient contrast."

* [Color Conversion Calculator &#8211; Autopedia.com](http://autopedia.com/html/ColorCalculator.html)

  "You may select a color name, enter RGB values or the Hexidecimal values and then push the "compute" button next to your entry and you will see the results. Your selection will automatically be translated to all the appropriate coresponding values."
  
* [Color Safe &#8211; Donielle Berg and Adrian Rapp](http://colorsafe.co/).

  "Empowering designers with beautiful and accessible color palettes based on WCAG Guidelines of text and background contrast ratios..."
  
* [Color Theory &#8211; Tiffany B. Brown](https://colors.webinista.com/) 

  "Ever want to pick a start color and then click a button to create a color scheme? Me too. So I built it." 

* [Colorable &#8211; interactive web tool by Brent Jackson](http://jxnblk.com/colorable/demos/text/)

  "Takes a set color palette and shows contrast values for every possible combination. This is useful for finding safe color combinations with predefined colors and includes pass/fail scores for the WCAG accessibility guidelines..."

* [ColorZilla &#8211; color picker for Firefox and Chrome](http://www.colorzilla.com/chrome/)

   ColorZilla for Google Chrome and for Mozilla Firefox "is an extension that assists web developers and graphic designers with color related tasks - both basic and advanced."
  
   "ColorZilla includes a Color Picker, Eye Dropper, Gradient Generator and many additional advanced color tools. With ColorZilla you can get a color reading from any point in your browser, quickly adjust this color and paste it into another program. You can analyze the page and inspect a palette of its colors. You can create advanced multi-stop CSS gradients."
  
* [Contrast-A &#8211; by Annika Hamann](http://dasplankton.de/ContrastA/)

  "The application allows users to experiment with color combinations, examine them under the aspect of accessibility guidelines and to create custom color palettes. Contrast-A checks color combinations for sufficient contrast and displays the results according to WCAG 2.0 (Luminance Ratio) as well as the results according to older accessibility guidelines, WCAG 1.0 (Difference in Brightness and Color)."  

* [Hex Naw - The Scenery](https://hexnaw.com/)

  "Hex Naw is a tool that helps designers and developers test entire color systems for contrast and accessibility. Plug in your palette or color system and let Hex Naw do the rest."  
  
* [HTML Color Codes &#8211; by Alex Dixon](http://htmlcolorcodes.com/)

  "Get HTML color codes, Hex color codes, RGB and HSL values with our color picker, color chart and HTML color names..."

* [Tanaguru Contrast-Finder](http://contrast-finder.tanaguru.com/)

  "Tanaguru Contrast-Finder finds correct color contrasts for web accessibility..."  
  
* [Text on background image a11y check &#8211; great for text over images](http://www.brandwood.com/a11y/)

  "This is a guide to foreground colour accessibility on a background image. It is intended as guide for designers and developers to test if their design solution is accessible. Change the text size, colour and position. It will check the dimensions of the textarea against the background image."  
  
* [The Color Palette Creator &#8211; by S.G. Chipman](http://slayeroffice.com/tools/color_palette/)

  "It will create 10 shades of the base color, located top-left, at varying degrees of opacity. The top row emulates opacity over a white background, the bottom over black (or colors of your choosing as of v1.4). The opacity values are 100% opaque, 75%, 50%, 25% and 10% on the top row. The bottom row begins at 85% rather than 100% and continues on as the first."
 

### Color Simulators
* [ChromeLens &#8211; Chrome extension by ngzhian](https://chrome.google.com/webstore/detail/chromelens/idikgljglpfilbhaboonnpnnincjhjkd?utm_source=chrome-app-launcher-info-dialog) 
  
  "Visual impairment simulation and auditing tools to develop for accessibility. ChromeLens is a Google Chrome extension that provides a suite of tools to help with web accessibility development."

* [Color Oracle &#8211; by Bernhard Jenny](http://colororacle.org/)

   "Color Oracle is a colorblindness simulator for Window, Mac and Linux. It takes the guesswork out of designing for color blindness by showing you in real time what people with common color vision impairments will see..."

 * [Colorblind Web Page Filter](https://www.toptal.com/designers/colorfilter)

   "Use the Colorblind Colorlab to select safe colors earlier in the design process. This tool is still in development, but feedback is welcome while we work on it. If you only use one filter, use the greyscale filter which will not only point out potential problem areas, but will also let you see more clearly which areas the filter is unable to process." 

* [Eye Dropper &#8211; Chrome extension](https://chrome.google.com/webstore/detail/eye-dropper/hmdcmlfkchdmnmnmheododdhjedfccka?hl=en)

   "Eye Dropper is open source extension which allows you to pick colors from web pages, color picker and your personal color history. Eye Dropper is extension for Google Chrome and Chromium. It allows you to pick color from any webpage or from advanced color picker. It is great tool for web developers." 
   
* [NoCoffee Vision Simulator &#8211; Chrome extension by Aaron Leventhal](https://chrome.google.com/webstore/detail/nocoffee/jjeeggmbnhckmgdhmgdckeigabjfbddl)

  "NoCoffee can be helpful for understanding the problems faced by people with slight to extreme vision problems, such as": Low Acuity, Low Contrast Sensitivity, Colorblindness        
* [Sim Daltonism &#8211; by Michel Fortin](https://michelf.ca/projects/sim-daltonism/)

  "Sim Daltonism lets you visualize colors as they are perceived with various types of color blindness. Use the camera on your iOS device, or use the Mac app to filter a region of the screen."
  
* [Vischeck](http://www.vischeck.com/vischeck/vischeckURL.php)

  Vischeck is a way of showing you what things look like to someone who is color blind. You can use it on a single image or on a web page. You can also download programs to let you run it on your own computer.

  
### Contrast Checker

* [Accessible Colors &#8211; by Misha Moroshko and Vedran Arnautovic](http://accessible-colors.com/)

  "We evaluate your color combination using the WCAG 2.0 guidelines for contrast accessibility. If your combination does not meet the guidelines, we find the closest accessible combination by modifying the color lightness. We modify the lightness value only, in order to stay as true to the original color as possible."
  
* [CheckMyColours &#8211; by Giovanni Scala](http://www.checkmycolours.com)

  "It is a tool for checking foreground and background color combinations of all DOM elements and determining if they provide sufficient contrast when viewed by someone having color deficits. All the tests are based on the algorithms suggested by the World Wide Web Consortium (W3C)."
  
* [Color Contrast Analyzer for Chrome &#8211; by by NCSU/Greg Kraus](https://chrome.google.com/webstore/detail/color-contrast-analyzer/dagdlcijhfbmgkjokkjicnnfimlebcll?hl=en)

  "This extension allows you to analyze text color contrast problems on a webpage according to the WCAG 2 text color contrast requirements. It evaluates the page as it appears in the browser, so it is able to handle text over gradients and advanced CSS attributes. You can choose to analyze a portion of a web page, the entire visible contents of a tab, or an entire web page."

* [Color Contrast Checker for Chrome](https://chrome.google.com/webstore/detail/color-contrast-checker/jibccbkkepidahndjomdfbmbnfappopf)

  "Test your web content to make sure the luminosity ratio meets WCAG 2.0 level AA and AAA."
  
* [ColorA11y Chrome extension](https://chrome.google.com/webstore/detail/colora11y/icfneoldcbdmgaiocnnobpbbjncdfbfb?hl=en)

  "ColorA11y allows you to easily select a foreground color and a background color, and determine whether or not the contrast ratio between the 2 colors is WCAG 2.0 compliant. ColorA11y can help validate the existence of web accessibility issues you think you already have with color contrast. This Developer Tools extension can also help verify you're technically adhering to the WCAG 2.0 color contrast guidelines." 
  
* [Color Contrast Checker &#8211; by Jared Smith, WebAIM](http://webaim.org/resources/contrastchecker/)

  "Simply select or enter a foreground and background color in RGB hexadecimal format (e.g., #fd3 or #f7da39). Select the lighten and darken options to modify the colors slightly. You can use the color picker to change colors or change luminosity..."
  
* [Color Contrast Comparison &#8211; by Joe Dolson](http://www.joedolson.com/color-contrast-compare.php)

  "I’ve created a basic tool which compares two colors, as well. Evaluate contrast between two colors."
  
* [Color Contrast Spectrum &#8211; by Joe Dolson](http://www.joedolson.com/color-contrast-tester.php)
   
  "This test allows you to see a spectrum of color combinations with a color of your choice. The spectrum is sorted into groups which pass or fail the color contrast tests specified in the Web Content Accessibility Guidelines (WCAG) versions 1 and 2."

* [Colour Contrast Check Tool &#8211; by Jonathan Snook.](https://snook.ca/technical/colour_contrast/colour.html)

  "The Colour Contrast Check Tool allows to specify a foreground and a background colour and determine if they provide enough of a contrast 'when viewed by someone having color deficits or when viewed on a black and white screen.'[W3C] The tool will indicate that the colours pass the test if both the colour difference and the brightness difference exceed their threshold. It will indicate that it sort of passes if only one of the two values exceed their threshold. And finally, it'll fail to pass if neither value exceeds its threshold. The tool will also indicate if the colours pass the newer WCAG 2.0 contrast ratio formula. The WCAG 2.0 formula differentiates between text smaller than 18pt text larger than 18pt (or text that is bold and larger than 14pt). For AA compliance, text should have a ratio of at least 4.5:1 (larger text, at least 3:1). For AAA compliance, text should have a ratio of at least 7:1 (larger text, at least 4.5:1)."
  

* [Colour Contrast Analyser app &#8211; by Paciello Group](https://www.paciellogroup.com/resources/contrastanalyser/)

  "The Colour Contrast Analyser (CCA) helps you determine the legibility of text and the contrast of visual elements, such as graphical controls and visual indicators. This tool provides two useful core functionalities: <br />- a pass/fail assessment against WCAG 2.0 color contrast success criteria<br />- a simulation of certain visual conditions, including dichromatic color-blindness and cataracts, to demonstrate how your web content appears to people with less than 20/20 vision."
  
* [Contrast Checker &#8211; by Acart Communications](http://contrastchecker.com/)
  
  "This tool is built for designers and developers to test color contrast compliance with the Web Content Accessibility Guidelines (WCAG) as set forth by the World Wide Web Consortium (W3C). These calculations are based on the formulas specified by the W3C."

* [Contrast-Finder &#8211; by Asqatasun](https://app.contrast-finder.org/result.html)

  "Contrast-Finder finds correct color contrasts for web accessibility. "

* [Contrast Ratio &#8211; by Lea Verou](http://leaverou.github.io/contrast-ratio/)

  "As you type, the contrast ratio indicated will update. Hover over the circle to get more detailed information. When semi-transparent colors are involved as backgrounds, the contrast ratio will have an error margin, to account for the different colors they may be over."
  
* [Juicy Studio Accessibility Firefox add-on](https://addons.mozilla.org/en-US/firefox/addon/juicy-studio-accessibility-too/)  

  "The Colour Contrast Analyser Firefox extension lists colour combinations used in the document in a table that summarises the foreground colour, background colour, luminosity contrast ratio, and the colour difference and brightness difference used in the algorithm suggested in the 26th of April 2000 working draft for Accessibility Evaluation and Repair Tools (AERT). Each element is also listed with its parent elements, and class and id attribute values when specified to make it easier to locate the elements." See: [Colour Contrast Analyser - Gez Lemon](http://juicystudio.com/article/colour-contrast-analyser-firefox-extension.php)

* [WCAG Contrast Checker &#8211; FireFox Extension by Jorge Rumoroso](https://addons.mozilla.org/en-us/firefox/addon/wcag-contrast-checker/)

  "Checks for compliance with the contrast levels, brightness and shine in the color combination of foreground and background of textual content based on the requirements of WCAG 1 and WCAG 2..."
