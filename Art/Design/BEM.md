https://getbem.com/

- [OOCSS](http://oocss.org/) — Separating container and content with CSS “objects”
- [SMACSS](http://smacss.com/) — Style-guide to write your CSS with five categories for CSS rules
- [SUITCSS](https://suitcss.github.io/) — Structured class names and meaningful hyphens
- [Atomic](https://acss.io/) — Breaking down styles into atomic, or indivisible, pieces

- use `block--modifier-value` syntax
	- **GOOD**
```html
<div class="block block--mod">...</div>
<div class="block block--size-big block--shadow-yes">...</div>
```
	- **BAD**
```html
<div class="block--mod">...</div>
<div class="block--big block--shadow">...</div>
```