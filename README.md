# CSS Pseudo-element Issue within Media Query

This repository demonstrates a subtle bug related to using CSS pseudo-elements (::before, ::after) within media queries.  The expected behavior is for the pseudo-element styles to only apply when the media query conditions are met. However, due to the specificity and cascade of CSS, this behavior isn't always guaranteed.

## Bug Description
The provided CSS attempts to add a "Mobile" text using the `::before` pseudo-element for elements with class `container` only when the screen width is less than 768 pixels.  The expectation is that the text appears only on smaller screens.  In some circumstances this will not happen.

## Solution
The solution involves ensuring sufficient specificity to override existing styles and proper ordering to ensure the media query is correctly applied.