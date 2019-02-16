## Joomla Accessibility Guidelines
### Define the language of the document and its parts
#### Why?
* Text-to-speech software can read content correctly
* Spell-checking software can correctly identify errors
* Browsers correctly format language-dependent text styles (e.g. they use the appropriate font)
#### How?
* Use the `lang` attribute in the `html` tag
* Use the `lang` attribute in the `span` tag to define the language of text fragments other than the language of the document.
#### Pattern
**How to define the language of the page?**
```php
<!DOCTYPE html>
<html lang="<?php echo $this->language; ?>" dir="<?php echo $this->direction; ?>">
```
**How to define the language of a text fragment?** 
```html
<p>
    In English - <span lang="en-GB">Welcome</span>, Dutch <span="nl">Welkom</span>, 
    French <span="fr">Bienvenue</span>, German <span="de">Willkommen</span>, 
    Italian - <span="it">Benvenuti</span>, Spanish <span="es">Bienvenidos</span>, 
    Polish - <span="pl">Witamy</span>.
</p>
```
#### Ref.:
* [WCAG 3.1.1 Language of page](https://www.w3.org/TR/WCAG21/#language-of-page)
* [WCAG 3.1.2 Language of Parts](https://www.w3.org/TR/WCAG21/#language-of-parts)
