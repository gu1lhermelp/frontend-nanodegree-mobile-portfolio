## Image optimizations
All images were made smaller. (I used ImageMagick)

## CSS and JS minification
The CSS and JS files for the index page were minified
(Got the minified files from PageSpeed Insights).

## index.html optimizations
* added the media attribute to _print.css_ so to unblock DOM creation;
* set the google-analytics js file as **async** as it does not tweak the DOM.

## Pizza main.js optimizations
Two optimizations were made to the main.js file, both related with
**forced reflow**:
* the first change was made to the _changePizzaSizes_ function.
The loop was made simpler by removing the line that queried the _offsetWidth_,
forcing the layout to be painted just to be repainted in the next line when the
_width_ was set;
* the second optimization was made to the _updatePositions_ function. The loop
in it was also forcing the layout to be repainted every iteration. In order to
solve this, one loop was made to calculate the new position of each pizza and
another loop to set the position.

# Instructions to run
Open **index.html** on your browser.
