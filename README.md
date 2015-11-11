# Website Performance Optimization
The purpose of this project was two fold. This first goal was to take a portfolio website and optimize the critical rendering path of its home page (index.html) in order to improve its pagespeed insight's score from 30% to 90%. The second goal was to optimize the pizza.html which boasts a scrolling pizza background to eliminate jank and run at 60 frames per second (FPS). Outlined below are the steps I took to achieve these goals.

### Optimizing the Critical Rendering Path (CRP) of index.html
* Compressed images
* Removed render blocking css by using media tag
* Inlined CSS
* Made non essential scripts (google analytics) async to to prevent render blocking on page laod
* Loaded google fonts asynchronously

To check the pagespeed insights score paste the url below into the analyze box at [PageSpeed Insights] (https://developers.google.com/speed/pagespeed/insights/)

Live index.html : http://monsuratolaosebikan.github.io/portfolio-optimization/

### 60FPS on page scroll of pizza.html
* Optimized for loops to complete calculations that didn't need to be repeated or didn't change outside the loop
* Changed expensive querySelectorAll to getElementbyClassName
* Created an array of repeating values to be used and reused by the function instead of recalculating the same values repeatedly
*Reduced the amount of pizzas animated in the background from 200 to 30 since only a few can be seen at any given time

Live pizza.html : http://monsuratolaosebikan.github.io/portfolio-optimization/views/pizza.html
