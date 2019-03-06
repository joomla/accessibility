# Define the page language and its parts
## Why?
* Text-to-speech software can read content correctly.
* Spell-checking software can correctly identify errors.
* Browsers correctly format language-dependent text styles (e.g. they use the appropriate font).
## How?
* Use the `lang` attribute in the `html` tag, to define the page language. 
* Use the `lang` attribute in the `span`, `blockquote` and other tags, to define the language of text fragments other than the page language.
## Pattern
**How to define the language of the page?**
```php
<!DOCTYPE html>
<html lang="<?php echo $this->language; ?>" dir="<?php echo $this->direction; ?>">
```
**How to define the language of a text fragment?** 
```html
<p>
    In: English - <span lang="en-GB">Welcome</span>, Dutch <span="nl">Welkom</span>, 
    French <span="fr">Bienvenue</span>, German <span="de">Willkommen</span>, 
    Italian - <span="it">Benvenuti</span>, Spanish <span="es">Bienvenidos</span>, 
    Polish - <span="pl">Witamy</span>.
</p>
<blockquote lang="fr">
   La vérité vaut bien qu'on passe quelques années sans la trouver. Renard
</blockquote>
```
## WCAG Reference
* [WCAG 3.1.1 Language of page. (Level A)](https://www.w3.org/TR/WCAG21/#language-of-page)
* [WCAG 3.1.2 Language of Parts. (Level AA)](https://www.w3.org/TR/WCAG21/#language-of-parts)
## Further reading
* [Why use the language attribute?](https://www.w3.org/International/questions/qa-lang-why)
* [3.1.1 Language of Page](http://www.maxability.co.in/2014/11/3-1-1-language-page/)
* [3.1.2 Language of Parts](http://www.maxability.co.in/2015/02/3-1-2-language-parts/)
* [Accessible Language Pickers: a11y meets i18n/l10n](http://terrillthompson.com/blog/759)


