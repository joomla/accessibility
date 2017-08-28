# Accessibility evaluation Joomla UI components

## RFC version 1.0 - This is a first draft and a request for comments.

This is a request for comments on this subject, in order to come to an agreement upon various guidelines to follow, when helping with the project.

Instigated by Stefan Wajda and begun 6 August 2017

### Introduction
The purpose of this document is to collect and develop a set of procedures for testing and evaluating Joomla UI components for their accessibility. It is supplied as an RFC.

Please, contribute to RFCs, speak up, if you think you may have anything to contribute, comment, improve, suggest your own ideas. Together we will do more, faster and better.

### Description policy
 **Each procedure should include**:
 * a brief definition of the Joomla UI component
 * list of accessibility requirements, if needed, grouped by topic
 * a test description with a set of helpful questions in the assessment
 * report design
 * useful tools


# Alert

An alert is an element that displays a brief, important message, in a way that attracts the user's attention without interrupting the user's task.

Note: See Alert dialog.

## Accesibility requirements

### General

 - An alert (WAI-ARIA live region) does not require any keyboard interaction.
 - Alerts can be closable and may have other action buttons or links.
 - If the alert contains an element, to dismiss and hide the notice, it should be a button. In this case **Enter** key - closes the message.
 - Do not include notifications that are not related to the user's current goal.
 - Alerts, with low importance (info or success), can close automatically after 5 seconds (if desired)
 - Alerts with high importance (warning or danger) should not close automatically, unless the situation has been resolved in some other way.

### Announced

 - If high-priority, a notice must be announced.
 - If high-priority, a notice must be listed as a region/landmark.
 - Screen reader does not need to announce low-priority server-side notices.
 - Screen reader must announce client-side content changes to the notice.
 - Screen reader should announce the element notice, when a related interactive element gains focus.
 - Information about the type of alarm must be announced by screen readers, e.g. by using texts or an additional text, hidden with the.sr-only class. Information, about the type of alert, cannot be denoted only by the color

### Type of alerts

 - Info alerts serve to provide a hint or useful information.
 - Success alerts should be used, when a user action is performed successfully.
 - Warning alerts should be used for unusual or unwanted events.
 - Danger alerts should be announced when the system has failed to perform an action, or when the user has made an error.

## Testing procedure

 - Place the message.php file in the templates directory: template/[your\_template]/html/layouts /joomla/system/. Note the file version (for Joomla 3.7 or for Joomla 4.0.
 - Start a Joomla site with sample data in your browser.
 - Do some actions that may cause an alarm:
 - Log in with the wrong and correct login information
 - Send contact form
 - Save the article
 - Examine alert presentation in your browser and on your mobile device, such as your smartphone:
 - Is the type of alert (Info, Success, Warning, Danger) announced?
 - Is the visual presentation of the alert type understandable (color, icon)?
 - Is the color choice legible for people with color vision disorders?
 - Is there a dismiss element and is it visible?
 - Does the message disappear when you press the dismiss button?
 - Examine HTML code validation
 - Has the alert container been identified as an alert using the role attribute?
 - Is the dismiss element a button?
 - Does the off switch have an understandable label? (The x character is not a sufficient label, in which case the concise label should be expressed in the aria-label attribute)
 - Examine the availability of the screen reader
 - Is the alert announced by the screen reader?
 - Can you navigate to an alert using landmarks?
 - Is the name (title) of the landmark with the alert announced?
 - Is the content of the message read correctly?
 - Is the shutoff button announced as a button if it exists?

## Report design

To do...

## Useful tools

* [aXe for Chrome and Firefox][1] - Screen reader, e.g. JAWS, NVDA, VoiceOver, Orca
* [Fangs – screen reader emulator for Firefox][2]
* [Color contrast analyzer ][3]
* [NoCoffee or ChromeLens][4]

  [1]: https://www.deque.com/products/axe/
  [2]: https://addons.mozilla.org/pl/firefox/addon/fangs-screen-reader-emulator/
  [3]: https://www.paciellogroup.com/resources/contrastanalyser/
  [4]: https://chrome.google.com/webstore/detail/nocoffee/jjeeggmbnhckmgdhmgdckeigabjfbddl