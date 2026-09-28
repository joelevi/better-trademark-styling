# Joez Better Trademark Styling for the Registered and Trademark Symbols
This makes (TM) and (R) marks in HTML look more like they're supposed to: superscripted and smaller than the neighboring text.

## CSS:
 - ~~The `.reg-trademark` and `.trademark` classes use `font-size: 0.6em` and `vertical-align: super` to mimic the superscript appearance of `<sup>&reg;</sup>` and `<sup>&trade;</sup>`.~~ No more proprietary CSS is needed.
 - Add the new CSS rules to your CSS file
 - Add `var(--regmark-font), ` to the start of your `font-family` tags to use the new font.
      
## JavaScript:
 - ~~Applies a regular expression to match standalone symbols.~~
 - ~~Wraps matched symbols in `<span class="symbol-sup">` tags.~~
 - No javascript is needed.

## Files:
 - Place the `regmark.woff2` file into your fonts folder; this document presumes that to be `url("regmark.woff2") format("woff2");`

## Behavior:
 - Standalone ®, &reg;, ™, and &trade; are styled to appear superscripted.
 - ~~This solution ensures that only standalone ®, &reg;, ™, and &trade; symbols are styled, leaving `<sup>&reg;</sup>` and `<sup>&trade;</sup>` untouched.~~
