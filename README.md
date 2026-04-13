# Laundry Web App - Mobile Hamburger Menu (Task)

## Overview
This task implements a responsive navigation bar for a Laundry Web App. On desktop screens, standard navigation links are displayed. On mobile screens (under 768px), the links are hidden and replaced with a hamburger menu icon.

Per the assignment instructions, this layout is built entirely with **CSS and HTML**—no JavaScript or Bootstrap was used.

## How to Run
1. Make sure `index.html` and `style.css` are in the same folder.
2. Open `index.html` in any web browser.
3. Open Developer Tools (F12 or Right Click -> Inspect) and resize the screen below 768px, or view it on a mobile device simulator to see the hamburger menu appear.
4. Click the hamburger icon to see the menu drop down.

## What I Learned
The most interesting part of this assignment was creating a functional click-to-open menu without using JavaScript. 

To achieve this, I used the **`:focus` pseudo-class** combined with the **adjacent sibling combinator (`+`)**. 
1. I wrapped the hamburger icon in a `<button>` tag so it can naturally receive focus when clicked.
2. I placed the dropdown `.mobile-menu` div immediately after the button in the HTML structure (making them siblings).
3. In the CSS, I wrote `.hamburger-btn:focus + .mobile-menu { display: block; }`. 

This tells the browser: "Whenever the button is currently being focused (clicked), find its next sibling and change its display from `none` to `block`." It's a clever CSS trick that mimics JavaScript toggle functionality!
