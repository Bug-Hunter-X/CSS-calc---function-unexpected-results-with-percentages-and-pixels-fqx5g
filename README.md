# CSS calc() function unexpected results with percentages and pixels

This repository demonstrates an uncommon issue with the CSS `calc()` function when combining percentages and pixel units.  The issue results in unexpected layout behavior, particularly noticeable in different browsers.

## Bug Description
The `calc()` function, while powerful, can produce inconsistent results if units are not handled carefully.  For example, `width: calc(50% - 10px);` aims to set the width to 50% of the container minus 10 pixels. However, this can lead to incorrect calculations depending on the context and browser.

## Reproduction
1. Clone this repository.
2. Open `bug.css` and `bugSolution.css` to see the buggy code and the solution.
3. Run the HTML files with the corresponding CSS files. Observe the difference in layout behaviors. 

## Solution
The solution involves a more robust approach ensuring consistent calculations.  Using viewport units (`vw`) for percentage-based calculations can provide a more reliable outcome across different browsers.