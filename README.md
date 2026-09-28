# Joez Better Trademark Styling for the Registered and Trademark Symbols

## CSS:
 - Add the new CSS rules to your CSS file
 - Add `var(--regmark-font), ` to the start of your `font-family` tags to use the new font:
   - ```
     @font-face {
       font-family: "Regmark";
       src: url("/assets/fonts/regmark.woff2") format("woff2");
       unicode-range: U+00AE, U+2122;
       font-weight: 100 900;
       font-style: normal;
       font-display: swap;
     }
     
     @font-face {
       font-family: "Regmark";
       src: url("/assets/fonts/regmark.woff2") format("woff2");
       unicode-range: U+00AE, U+2122;
       font-weight: 100 900;
       font-style: italic;
       font-display: swap;
     }
     
     body {
      font-family: var(--regmark-font), Roboto, sans-serif, sans, clean;
     }
     ```
      
## JavaScript:
 - None.

## Files:
 - Place the `regmark.woff2` file into your fonts folder.

## Behavior:
This makes (TM) and (R) marks in HTML look more like they're supposed to: superscripted and smaller than the neighboring text.
 - Standalone ®, &reg;, ™, and &trade; (etc.) use the `regmark.woff2` font to appear smaller and superscripted.
