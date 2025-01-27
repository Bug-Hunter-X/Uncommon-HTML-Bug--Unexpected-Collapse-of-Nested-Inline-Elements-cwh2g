# Uncommon HTML Bug: Unexpected Collapse of Nested Inline Elements

This repository demonstrates an uncommon HTML bug related to the unexpected collapse of nested inline elements. The inner `inline` element's specified width is ignored by the outer `inline-block` element, causing unexpected layout behavior.  The issue arises due to the complexities of how browsers handle inline and inline-block element interactions.

## Bug Description

The bug occurs when an `inline` element is nested within an `inline-block` element.  The inner `inline` element's width declaration is unexpectedly ignored, leading to layout problems. The outer `inline-block` element doesn't occupy the expected width, but rather collapses to the content size of the inner `inline` element.  This behavior is not immediately intuitive and can be challenging to diagnose.

## Solution

The solution involves changing the `display` property of the inner element to `inline-block`. This ensures that the inner element is treated as a block-level element within the context of the outer `inline-block` container, allowing its width to be respected.   Alternatively, using explicit widths or different layout mechanisms (like flexbox or grid) provides more robust and predictable solutions.