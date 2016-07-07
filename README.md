# Website Performance Optimization portfolio project

The project consists of two parts: make this page render as quickly as possible by optimizing the critical rendering path and optimize frames per second in pizza.html.

##  Tools used:

* Google DevTools
* Grunt task-runner and the following plugins: [imageoptim](https://github.com/JamieMason/grunt-imageoptim), [uglify](https://github.com/gruntjs/grunt-contrib-uglify), [uncss](https://github.com/addyosmani/grunt-uncss), [cssmin](https://github.com/gruntjs/grunt-contrib-cssmin), [htmlmin](https://github.com/gruntjs/grunt-contrib-htmlmin)
* Google PageSpeed Insights to measure the metrics
* Kraken.io for better compression of the images

##  PageSpeed Insights score after the optimization

* Desktop: 94/100
* Mobile: 95/100

The optimized version of the site: [Performance Optimization project](https://tragetraje.github.io/fend-optimization/)

### The steps taken to optimize performance:

1. Compress the images
2. CSS: get rid of unused code, apply media-type `media="print"`, inline CSS and minify the files
3. Minify HTML-files
4. JS: add `async`-attribute to the scripts where possible, move the scripts to the bottom of the page for faster rendering, minify the files
5. `Main.js`: recorded a timeline to find out what functions cause performance bottlenecks and made changes to `updatePositions()` and `changePizzaSizes()`. Replace `querySelector` and `querySelectorAll` with more effective `getElementById` and `getElementsByClassName`. Refactor the `for`-loops.
