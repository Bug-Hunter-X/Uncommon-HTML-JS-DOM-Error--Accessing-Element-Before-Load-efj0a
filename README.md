# Uncommon HTML/JS DOM Error: Accessing Element Before Load

This repository demonstrates an uncommon error that can occur when working with HTML and JavaScript.  The error arises from attempting to access and manipulate a DOM element before it has been fully loaded by the browser.

## The Bug

The `bug.html` file contains HTML with a `<div>` element.  JavaScript code attempts to access and modify the `innerHTML` of this `div` immediately.  Because the script runs before the browser has fully parsed and rendered the HTML, the element might not yet exist, causing an error. 

## The Solution

The `bugSolution.html` demonstrates the corrected approach.  This version uses the `DOMContentLoaded` event listener to ensure that the script executes only after the entire HTML document has been parsed and the DOM is ready.

This is a subtle yet important concept in web development.  Properly handling DOM interaction timing is crucial for avoiding unexpected behavior and errors.