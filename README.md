# Joez Better Trademark Styling for the Registered and Trademark Symbols
This makes (TM) and (R) marks look more like they're supposed to: superscripted and smaller than the neighboring text.

## CSS:
The `.reg-trademark` and `.trademark` classes use `font-size: 0.6em` and `vertical-align: super` to mimic the superscript appearance of `<sup>&reg;</sup>` and `<sup>&trade;</sup>`.
      
## JavaScript:
Uses a `TreeWalker` to select text nodes, explicitly excluding those within `<sup>` or `<script>` tags via the `acceptNode` filter.

Applies a regular expression `(®|&reg;|™|&trade;)` to match standalone symbols.

Wraps matched symbols in `<span class="symbol-sup">` tags.

## Behavior:
Standalone ®, &reg;, ™, and &trade; are styled to appear superscripted.

This solution ensures that only standalone ®, &reg;, ™, and &trade; symbols are styled, leaving `<sup>&reg;</sup>` and `<sup>&trade;</sup>` untouched.
