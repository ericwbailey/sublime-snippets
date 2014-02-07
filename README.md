sublime-snippets
================

*This repo is by no means a finished work. Snippets will be added, removed, and updated periodically*

A comprehensive snippet library for [Sublime Text](http://www.sublimetext.com/), built with thoroughness and accessibility in mind. This collection tries to capture sensible presets for web design/development, in the order of what I would personally consider most useful for my day-to-day work.

As opposed to something like [Emmet](http://emmet.io/) (which is an absolutely wonderful plugin), this library strives to be a little slower, more verbose, and more *opinionated*. The cleverness of, and gains with in-the-moment speed with Emmet-style expansion are oftentimes at the expense of a sloppier, more inaccessible greater whole. 


## Approach

### Modular
Because I am ~~bad at coding~~ a fan of modular-based approaches, each snippet is a self-contained file so the project can be a little more adaptable and portable for future efforts. This project's origin was a [TextMate](http://macromates.com/) snippet library, after all

### Commenting and legibility
Verbosity is nice. Major HTML sectioning elements and complicated embeds/forms/etc. have start of/end of commenting to help when wayfinding when coding or inspecting. Remove to shave size off for larger-scale sites. 

Indentation is generous. Space is cheap and code written with legibility in mind makes for easier understanding and interpretation.

### Snippet ordering and naming
Sublime lists snippets with a common Tab Trigger in alphabetical order. Each snippet's filename has an `xx-name-attribute` convention, to allow for manual ordering of snippets. Commonly used code patterns are put first, but alternatives are always available.

### Paths
Suggested file paths (ex: `url('../img/')`) are baked in where they're commonly needed.

### Placeholders
Plain language placeholders help remember what is being modified, and if accidentally left in will usually trigger an error when a preprocessor fires, helping to eliminate difficult to find errors resulting from unintended iterpretation. 

### Exit Points
Snippet exit points (`$0`) are explicitly declared. This is helpful for longer, more complicated snippets where it might not be more advantageous for the exit point to be at the end of the snippet, instead placing the cursor where further work is commonly needed.

### Accessibility
Basic accessibility considerations and practices are baked-in where applicable. An example would be [ARIA landmark roles](http://blog.paciellogroup.com/2013/02/using-wai-aria-landmarks-2013/) for HTML section tags. Little cost, great gains. 


## Languages

### [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) / [Slim](http://slim-lang.com/)
Ordering inspired by via [HTML5 Doctor's Element Index](http://html5doctor.com/). Also contains [WAI-ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA) attributes for creating accessible sites and applications. Slim tag attributes are wrapped with brackets for easier visual parsing.

#### Tab Triggers
Tab triggers are three characters long. 

**Ex:** `<meta>` is triggered by `met`.

Attributes can only be triggered within a tag. 

### [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) / [SASS](http://sass-lang.com/)
Ordering inspired by [HTML Dog](http://htmldog.com/guides/css/)'s CSS Properties.

#### Tab Triggers
Tab triggers are four characters long. If a tag is one word long, the trigger is its first four letters:

**Ex:** `quotes` is triggered by `quot`.

If the tag's name is hyphenated, the trigger is the first three letters of the first word, followed by the first letter of the second word:

**Ex:** `align-items` is triggered by `alii`.

Less commonly used tags are five characters long, allowing (relatively) quick expansion, but keeping the namespace free for more commonly-used properties:

**Ex:** `border-bottom-width` is triggered by `borbw`.

##### Measurements and Colors
Measurement units and color declarations can be triggered via `m` or `#`, respectively.