# Validation

Validation is a fundamental prerequisite for online accessibility. WCAG 2.0 recognizes this condition as one of the four basic principles:

> **Principle 4: Robust** - Content must be robust enough that it can be interpreted reliably by a wide variety of user agents, including assistive technologies.  

Although web browsers and assistive technologies are quite tolerant of various syntax faults, it may happen that syntactic errors can make it difficult for screen readers and other assistive devices to work. WCAG 2.0 therefore considers compliance with the W3C standards to be an essential criterion for success (Level A): 

> **4.1.1 Parsing**: In content implemented using markup languages, elements have complete start and end tags, elements are nested according to their specifications, elements do not contain duplicate attributes, and any IDs are unique, except where the specifications allow these features.

You can check your site's compliance with different standards using the W3C Validator. The Validator will return you a list of errors and remedies.
*	legacy Markup Validator for markup other than HTML5:  https://validator.w3.org/
*	Nu Html Checker newer, experimental version of the validator: https://validator.w3.org/nu/

**Note**: At address https://validator.w3.org/unicorn you can use the default validator in your language version (Unicorn - W3C's Unified Validator). The unified validator also displays a list of CSS errors.

If you have restrictions on using online tools, you can choose to install this service locally and test against that. The source for the validator is available on github at https://github.com/validator/validator.

The Validator will not only display a list of errors and warnings, but will also make some pretty good suggestions regarding various ARIA roles and such.
## Procedure
1. Go to the W3C Validator page.
2. Enter the URL of the page you want to check on the **By URI** tab, in the **Address** field.
3. Then press or click the **Check** button. After a while, a list of errors, comments and suggestions is displayed.
4. Scan the error list.

Each line contains the line number in the page code, a code snippet, and an error description.
Note important errors and remarks in the audit report.
