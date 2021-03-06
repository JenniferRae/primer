---
layout: post
title: "Mobile First &amp; Responsive Design"
modified: 2015-02-22 22:09:03 -0800
category: assignments
tags: [JavaScript, jQuery]
description: Use Mobile-first and responsive design to create a simple magazine site.
---


Objectives
==========
0. Create an HTML-only web site ("So Retro!")
0. Add styling to make a mobile-first design
0. Use media queries to extend this styling to larger screen formats
0. Use Scalable Vector Graphhics (SVG) to create responsive logos
0. Use responsive image techniques to reduce bandwidth and improve usability
0. Publish the site using github pages
0. Work on a small team


Overview
========
The site is a single page with a set of at least three articles. Articles can have any number of paragraphs. Your design should work with at least 20 or more articles.

The logo should be SVG and 75x75px without any styling. In the "small" mobile version, it should be 100x100. In the "medium" mobile, it should be 200x200.

The page title is used differently in all three layouts. See the wireframes for details.

The articles should scroll, but no scroll bar should appear. They are too small a target for mobile use. On a device, you should be able to flick them up and down easily and use the nav menu to jump to any article.

Each article will have one image. They should be very small in the HTML-only version, very small in the mobile version, and larger with a click-through to full size on the large version.

Test your work using Chrome Developer Tools in "device mode."  [device-mode](https://developer.chrome.com/devtools/docs/device-mode)

Feel free to use real devices to test your site when it is live on the web.

Resources
=========
* You can get a bunch of easy placeholder images at [placehold.it](http://placehold.it/) (conveniently shows image size) or [lorempixel](http://lorempixel.com/)
* You can get a bunch of fun SVG icons at [The Noun Project](http://thenounproject.com/).
* Here's a list of [lorem ipsum generators.](http://mashable.com/2013/07/11/lorem-ipsum/)

Things to do
=====

Part 0 - set up the assignment
----------------------------------

### Steps

0. Make a repository and establish a remote on github.com. This should be review
0. Create a gh-pages branch both locally and on github.com to set up web hosting
0. Work on the master branch unless you are deploying via the gh-pages branch
0. Create a simple HTML file with minimal content
0. Add, commit, and push your file to github.com on master
0. Merge from master to gh-pages and push to publish your file to the web
0. Verify that your file is available

Part 1 - Create a no-CSS, no-JavaScript site that works on a smart phone in portrait mode.
----------------------------------

Wireframe:
![HTML-only wireframe](/primer/images/responsive-homework-step-1.png "HTML-only wireframe")

### Steps

0. Create HTML for
  * a heading
  * a logo
  * a <kbd>nav</kbd> panel
  * a contents panel with a bunch of articles.
  * Each article should have a title, an image, and a couple paragraphs of text.
0. Be sure to put the various elements in the proper order.
0. Do not use any JavaScript or CSS
0. Test, add, commit, and push your code on master
0. Merge your code to gh-pages and push to deploy your site.
0. View your site on your phone to observe how it behaves.

Part 2 - Progressively enhance the site to use mobile-first conventions
----------------------------------

Wireframe:
![Mobile wireframe](/primer/images/responsive-homework-step-2.png "Mobile wireframe")

Use CSS and JavaScript to style the site using mobile user interface patterns:

* Non-scrolling title bar at top
* Non-scrolling menu bar at bottom
* Content should appear to scroll beneath the title and menu bars
* Navigation menu that is revealed either by swipe or menu icon
* Navigation menu should appear to be behind all other page elements.
* This should use fluid layout so that it works in either portrait or landscape mode on a "small" smartphone. Do not use media queries to handle orientation in this step.

### Steps
0. Add a menu <kbd>div</kbd> in a place that does not impact your HTML-only version (HINT: this div may need to be set aside or perhaps even off of the main canvas of your html page)
0. Add a stylesheet to implement the mobile user interface elements
0. Link to the [jQuery](http://jquery.com/) and [jQuery UI](http://jqueryui.com/) libraries using a [content delivery network](https://developers.google.com/speed/libraries/devguide)
  * ````<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>````
  * ````<link rel="stylesheet" href="https://ajax.googleapis.com/ajax/libs/jqueryui/1.11.3/themes/smoothness/jquery-ui.css" />````
  * ````<script src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.11.3/jquery-ui.min.js"></script>````
0. Add a JavaScript event listener to move the main content <kbd>div</kbd> to the right and reveal the <kbd>nav</kbd> panel. You can use jQuery-UI to add smooth animation to your <kbd>.addClass() method</kbd>. Example:
````
$( this ).addClass( "displaced",200 );
````
0. Make sure the content panel moves back to cover the nav panel when an article is selected or when the menu icon is clicked again.
0. (Optional - figure out how to reveal nav panel if JavaScript is turned off)
0. Test, add, commit, and push your code on master
0. Merge your code to gh-pages and push to deploy your site.
0. Test on your phone.

Part 3 - Use Responsive Design techniques to Progressively enhance the site for larger screens
----------------------------------

Wireframe:
![Tablet wireframe](/primer/images/responsive-homework-step-3.png "Tablet wireframe")


Use media queries to adapt layout to a "medium" mobile device - a tablet - in landscape orientation. It is up to your discretion to handle "medium" portrait orientation either by fluid layout or media query. You must have at least one media query.

Add responsive images to all articles.
* Use small, cropped images for html-only and mobile versions
* Use larger images for larger layouts
* Use media queries to manage the two layouts
* Use fluid image layout to deal with device variations within different devices
Example: http://codepen.io/Auraelius/pen/sClka?editors=110


Steps

0. Use one media query to detect when the layout is larger than a landscape phone
0. Use CSS to in the media query to
    * adjust the logo to be 200x200
    * Slightly overlay the page title on top of the logo
    * Keep the nav panel visible at all times, but, if there are enough article titles, scroll the nav panel independant of the content panel
    * use larger images for this layout and smaller images for the mobile layout
    * Float the images within the articles using alternating left and right positions
0. Test, add, commit, and push your code on master
0. Merge your code to gh-pages and push to deploy your site.
0. Test on your phone.
