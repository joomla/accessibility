# Messages

## What is this

**Purpose**: Users need to be aware of important information related to their current activity (contextual alerts) or related to the system (system notifications).

**Description**: An alert is an element that displays a brief, important message in a way that attracts the user's attention without interrupting the user's task.

Alerts are available for any length of text, as well as an optional dismiss button. Alerts can also contain additional HTML elements like headings and paragraphs.

**Types:**

There are four types of alerts in Joomla:

 - **message**: used when user action performed successfully (in Bootstrap - success alerts)
 - **notice**: used to give the user a hint or useful information (in Bootstrap - info alerts)
 - **warning**: used when an action is out of the ordinary or might not be desired (in Bootstrap - warning alerts)
 - **error**: used when the system has failed to perform an action, or when the user has made an error (in Bootstrap - danger alerts).

## Accessibility

### Accessibility specification

Accessible alert specification is defined in WAI-ARIA Authoring Practices 1.1.

See: [WAI ARIA Practices - 2.3 Alert](https://www.w3.org/TR/wai-aria-practices-1.1/).

### Keyboard Interaction

An alert (WAI-ARIA live region) does not require any keyboard interaction.

If the alert contains an element to dismiss and hide the notice, it should be a button. In this case:

* **Enter** - closes the message.

### Screenreader Interaction

Dynamically rendered alerts are automatically announced by most screen readers, and in some operating systems, they may trigger an alert sound.

**Note**: At this time screen readers do not inform users of alerts that are present on the page before page load completed.

## ARIA markup

**role="alert"**

* Identifies the element (typically div) as the container where alert content will be added or updated.

**aria-live="assertive"**

* **This does not have to be declared in the code** because it is implicit in the alert role.
* Tells assistive technologies to interrupt other processes to provide users with immediate notification of relevant alert container changes.

**aria-atomic="true"**

* **This does not have to be declared in the code** because it is implicit in the alert role.
* Tells assistive technologies to use the entire content of the alert element as the alert message even if only a portion of it has changed.

## Utilities

### When to use

* As a notification that keeps people informed of the status of the system and which may or may not require the user to respond. This includes errors, warnings, and general updates.
* As a validation message that alerts someone that they just did something that needs to be corrected or as confirmation that a task was completed successfully.

### When to consider something else

* On long forms, always include in-line validation in addition to any error messages that appear at the top of the form.
* If an action will result in destroying a user's work (for example, deleting an application) use a more intrusive pattern, such as a confirmation modal dialogue, to allow the user to confirm that this is what they want.

### Use in Joomla

Alerts are positioned at the very top of the main content area.

## Best practices

* Use the ARIA role="alert" to inform assistive technologies of a time-sensitive and important message that is not interactive. If the message is interactive, use the _alertdialog_ role instead.
* Do not visually hide alert messages on the page and then make them visible when they are needed. Users of older assistive technologies may still be able to perceive the alert messages even if they are not currently applicable.
* Ensure that information about type of alert denoted by the color is either obvious from the content itself (e.g. the visible text), or is included through alternative means, such as additional text hidden with the.sr-only class.

## Code patterns for Joomla and Joomla extension

### Current

**Source**: Joomla 3.7.4 / layouts/joomla/system/message.php

**Note**:

* No object role has been specified
* The closing element is a link, not a button
* The text of the link is the x character, which may be incomprehensible to screen readers

```php
$msgList = $displayData['msgList'];

?>
<div id="system-message-container">
	<?php if (is_array($msgList) && !empty($msgList)) : ?>
		<div id="system-message">
			<?php foreach ($msgList as $type => $msgs) : ?>
				<div class="alert alert-<?php echo $type; ?>">
					<?php // This requires JS so we should add it through JS. Progressive enhancement and stuff. ?>
					<a class="close" data-dismiss="alert">×</a>

					<?php if (!empty($msgs)) : ?>
						<h4 class="alert-heading"><?php echo JText::_($type); ?></h4>
						<div>
							<?php foreach ($msgs as $msg) : ?>
								<div class="alert-message"><?php echo $msg; ?></div>
							<?php endforeach; ?>
						</div>
					<?php endif; ?>
				</div>
			<?php endforeach; ?>
		</div>
	<?php endif; ?>
</div>
```

### Improved

**Note**:

* Attribute role="alert" has been added to div element.
* The element <button> was used as the closing element
* Attribute aria-label="Close" has been added to dismiss element
* The x (button label) was marked with the attribute aria-hidden="true"

```php
<?php
// ...
$msgList = $displayData['msgList'];

?>
<div id="system-message-container">
   <?php if (is_array($msgList) && !empty($msgList)) : ?>
      <div id="system-message">
         <?php foreach ($msgList as $type => $msgs) : ?>
         <div class="alert alert-<?php echo $type; ?>" role="alert">
            <?php // This requires JS so we should add it trough JS. Progressive enhancement and stuff. ?>
            <?php if (!empty($msgs)) : ?>
            <h4 class="alert-heading"><?php echo JText::_($type); ?></h4>
         <div>
            <?php foreach ($msgs as $msg) : ?>
               <div class="alert-message"><?php echo $msg; ?></div>
            <?php endforeach; ?>
         </div>
      <?php endif; ?>
            <button type="button" class="close" data-dismiss="alert" aria-label="<?php echo JText::_('JLIB_HTML_BEHAVIOR_CLOSE'); ?>">
               <span aria-hidden="true">&times;</span>
            </button>
      </div>
   <?php endforeach; ?>
   </div>
   <?php endif; ?>
</div>
```

**Call a message**

On the site and admin template, they are called by the statement:

The alert messages are displayed at the place marked in the template with a special jdoc:include statement.

```html
<jdoc:include type="message" />
```

Alerts can be displayed from any component, module, plugin or template using the methods outlined below.

```php
_// Get a handle to the Joomla! application object_
---
$application = JFactory::getApplication();
---
_// Add a message to the message queue_
---
$application->enqueueMessage(JText::\_('SOME\_ERROR\_OCCURRED'), 'error');
---
```

_/\*\* Alternatively you may use chaining \*/_

---

```php
JFactory::getApplication()->enqueueMessage(JText::\_('SOME\_ERROR\_OCCURRED'), 'error');
```
---

General syntax is:

```php
JFactory::getApplication()->enqueueMessage('Your Message', 'type');
```
---

The second argument to the enqueueMessage function is the type of the message. The default is ' _message_'.

Type can be one of:

* 'message' (or empty) - green
* 'notice' - blue
* 'warning' - yellow
* 'error' - red

**Note**: The alert type name is used in the code as the name of the message CSS class (more precisely: part of the class name). Bootstrap 3 and Bootstrap 4 use class names: 'success', 'info', ''warning', 'danger'. **You need to decide if your existing names will be retained in Joomla 4 or whether new names will be used in Bootstraps**. If so, look for all function calls and correct the type of alert.


## WCAG 2.0 Reference

* **[1.3.3 Sensory Characteristics](https://www.w3.org/WAI/WCAG20/quickref/#content-structure-separation-understanding)** (Level A): Instructions provided for understanding and operating content do not rely solely on sensory characteristics of components such as shape, size, visual location, orientation, or sound.
* **[1.4.1 Use of Color](https://www.w3.org/WAI/WCAG20/quickref/#visual-audio-contrast-without-color)** (Level A): Color is not used as the only visual means of conveying information, indicating an action, prompting a response, or distinguishing a visual element.
* **[2.2.3 No Timing](https://www.w3.org/WAI/WCAG20/quickref/#time-limits-no-exceptions)** (Level AAA). Timing is not an essential part of the event or activity presented by the content, except for non-interactive synchronized media and real-time events.
* **[2.2.4 Interruptions](https://www.w3.org/WAI/WCAG20/quickref/#time-limits-postponed)** (Level AAA). Interruptions can be postponed or suppressed by the user, except interruptions involving an emergency
* **[3.3.1 Error Identification](https://www.w3.org/WAI/WCAG20/quickref/#minimize-error-identified)** (Level A): If an input error is automatically detected, the item that is in error is identified and the error is described to the user in text.
* **[3.3.2 Labels or Instructions](https://www.w3.org/WAI/WCAG20/quickref/#minimize-error-cues)** (Level A): Labels or instructions are provided when content requires user input.
* **[3.3.3 Error Suggestion](https://www.w3.org/WAI/WCAG20/quickref/#minimize-error-suggestions)** (Level AA): If an input error is automatically detected and suggestions for correction are known, then the suggestions are provided to the user, unless it would jeopardize the security or purpose of the content.
* **[4.1.2 Name, Role, Value](https://www.w3.org/WAI/WCAG20/quickref/#ensure-compat-rsv)** (Level A): For all user interface components, the name and role can be programmatically determined; states, properties, and values that can be set by the user can be programmatically set; and notification of changes to these items is available to user agents, including assistive technologies.

## Resources
### Articles
* [The ARIA Role Matrices](http://whatsock.com/training/matrices/)
* [JDOCS - Display error messages and notices](https://docs.joomla.org/Display_error_messages_and_notices)

### Design Patterns

* [WAI ARIA practices](https://www.w3.org/TR/wai-aria-practices-1.1/examples/alert/index.html)
* [U.S. Web Design Standards ](https://standards.usa.gov/components/alerts/)
* [Bootstrap 4 - Alerts ](https://v4-alpha.getbootstrap.com/components/alerts/)
* [Open Ajax Accessibility ex. 1 - Alert role example using an ARIA alert box  ](http://oaa-accessibility.org/example/1/)
* [Open Ajax Accessibility ex. 2 - Alert example using a modal ARIA dialog box ](http://oaa-accessibility.org/example/2/)
* [UPSTO Design ](http://uspto.github.io/designpatterns/1.x/docs/components/alerts.html)
* [EBay MIND Patterns - Messages](https://ebay.gitbooks.io/mindpatterns/content/messaging/readme.html)
* [Deque Code Library – Inline Alert](https://dequeuniversity.com/library/aria/content-feedback/sf-inline-alert)
