sublime-snippets
================

A snippet library for Sublime Text built with thoroughness and accessibility in mind. This collection of snippets tries to capture sensible presets for web design/development, in the order of what I would consider most useful. 

As opposed to something like [Emmet](http://emmet.io/) (which is an absolutely wonderful plugin), this strives to be a little slower, more verbose, and more opinionated. The cleverness of, and gains in speed with Emmet-style string expansion are oftentimes at the expense of a sloppier, more inaccessible greater whole. 


## Approach

### Commenting and legibility
Verbosity is nice. Major HTML sectioning elements and complicated embeds/forms/etc. have start of/end of commenting to help when wayfinding when coding or inspecting. Remove if you need to shave size for larger-scale sites. 

Indentation is generous. Code that is legible makes for easier, better understanding and interpretation.

### Ordering and naming
Sublime lists snippets in alphabetical order. Each snippet's filename has an `xx-name-attribute` convention, to allow for manual ordering of snippets. Commonly used code patterns are put first, but alternatives are always available.

### Paths
Suggested file paths (ex: `url('../img/')`) are baked in where they're commonly needed.

### Exit Points
Snippet exit points (`$0`) are explicitly declared. This is helpful for longer, more complicated snippets where it might not be more advantageous for the exit point to be at the end of the snippet, instead placing the cursor where further work is commonly needed.

### Accessibility
Basic accessibility considerations and practices are baked-in where applicable. An example would be [ARIA landmark roles](http://blog.paciellogroup.com/2013/02/using-wai-aria-landmarks-2013/) for HTML section tags. Little cost, great gains. 


## Languages

### [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) / [Slim](http://slim-lang.com/)
Ordering inspired by via [HTML5 Doctor's Element Index](http://html5doctor.com/). Also contains [WAI-ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA) attributes for creating accessible sites and applications. Slim tag attributes are wrapped with brackets for easier visual parsing.

#### Tab Triggers
Tab triggers are three characters long. 

Ex: `<meta>` is triggered by `met`.

### [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) / [SASS](http://sass-lang.com/)
Ordering inspired by [HTML Dog](http://htmldog.com/guides/css/)'s CSS Properties.

#### Tab Triggers
Tab triggers are four characters long. If a tag is one word long, the trigger is its first four letter.

Ex: `quotes:` is triggered by `quot`.

If the tag is hyphenated, the trigger is the first three letters of the first word, followed by the first letter of the second word.

Ex: `align-items:` is triggered by `alii`.

Less commonly used tags are five characters long, allowing (relatively) quick expansion, but keeping the namespace free for more commonly-used properties.

Ex: `border-bottom-width:` is triggered by `borbw`.