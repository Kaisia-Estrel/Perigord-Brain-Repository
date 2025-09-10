# Shorthand Rules
Shorthand rules are usually in clock-wise order

- Remove text decorations with `text-decoration: none`, useful for `<a>` tags.

# Position
# Sticky
Place `top: 0` or on any direction to make the element stick to the edge when scrolled.
## Margin/Padding

- When one value is specified, it applies the same to all four sides.
- When two values are specified, the first margin applies to the top and bottom, the second to the left and right.
- When three values are specified, the first margin applies to the top, the second to the left and right, the third to the bottom.
- When four values are specified, the margins apply to the top, right, bottom, and left in that order (clockwise).


# Make a single border invisible
```css
border-width: 1px 2em 5px 0; /* top right bottom left */
```

- Make text unselectable via:
```css
  -webkit-user-select: none; /* Safari */  
  -ms-user-select: none; /* IE 10 and IE 11 */  
  user-select: none; /* Standard syntax */
```
## `display: inline-block`

Compared to `display: inline`, the major difference is that `display: inline-block` allows to set a width and height on the element.

Also, with `display: inline-block`, the top and bottom margins/paddings are respected, but with `display: inline` they are not.

Compared to `display: block`, the major difference is that `display: inline-block` does not add a line-break after the element, so the element can sit next to other elements.


# Pseudoclasses
- `:placeholder-shown` styles any element that still has a visible pseudoclass