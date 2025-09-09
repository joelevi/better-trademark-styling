# Joez Better Trademark Styling for the Registered and Trademark Symbols
This makes (TM) and (R) marks look more like they're supposed to: superscripted and smaller than the neighboring text.

## CSS:
The `.reg-trademark` and `.trademark` classes use `font-size: 0.6em` and `vertical-align: super` to mimic the superscript appearance of <pre><sup>&reg;</sup></pre> and <pre><sup>&trade;</sup></pre>.
      
## JavaScript:
Uses a `TreeWalker` to select text nodes, explicitly excluding those within <pre><sup></pre> or <pre><script></pre> tags via the `acceptNode` filter.

Applies a regular expression <pre>(®|&reg;|™|&trade;)</pre> to match standalone symbols.

Wraps matched symbols in <pre><span class="symbol-sup"></pre> tags.

## Behavior:
Standalone ®, &reg;, ™, and &trade; are styled to appear superscripted.

This solution ensures that only standalone ®, &reg;, ™, and &trade; symbols are styled, leaving <pre><sup>&reg;</sup></pre> and <pre><sup>&trade;</sup></pre> untouched.
