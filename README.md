# Breakpoints.js

Define breakpoints for your responsive/adaptive web and Breakpoints.js will be aware of browser resize event when entering or exiting a concrete size, adding a class named with the breakpoint you defined previously within the DOM element you want.

This is a fork from the original [Breakpoint.js created by XOXCO](https://github.com/xoxco/breakpoints)

## Changes

Instead of having an interval checking for browser size changes, this fork uses the resize event over $(window). In addition, the size will be checked at the very beginning of the page load so there's no need to fire a manual resize or wait for a first resize to know which is the active breakpoint.

Additionally, you can configure which is the prefix for the breakpoint class and also where it will be added in the DOM by selecting a target.

## Instructions

  $(window).setbreakpoints({
    // Only the largest breakpoint will be added if true
    // All the breakpoints classes will be added if false
    distinct: true,
    // The prefix that will preceed the breakpoint number and turned into a class
    // Final class structure: prefix-breakpoint
    prefix: 'breakpoints',
    // The DOM element where the formed class will be added
    target: 'body,'
  // Array of widths in pixels where breakpoints should be triggered
    breakpoints: [
      // Add '1' if you want to have a breakpoint class even with a lower size than the minor breakpoint
      1
      320,
      480,
      768,
      1024
    ]
  });
