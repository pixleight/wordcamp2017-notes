# Performance Under Pressure

Mat Marquis  
Worked at Bocoup, Filament Group  

Volunteered to redo Bocoup's website

Passionate about building things to be proud of. The work is just a means to an end.

##  The Critical Path

Blocking requests - requests that keep website to render until file is fully loading.  
Stylesheets, javascripts in the header.

New browsers are prioritizing necessary styles to load before render, waiting on others

First step in critical path is round trip between server & browser  
Put CriticalCSS in that initial reuest, then defer loading until after page render.

github.com/filamentgroup/loadcss  
npmjs.com/package/grunt-criticalcss  
Also webpack module to do the same

bocoup.com/about/bocouper/tkellen  
Bocoup website automate build

PHP function checks for criticalcss file, checks if it's cached, if available it sets criticalcss in a <style> tag in header, then also injects other css load

## Asyncronous Webfonts

dev.w3.com/csswg/css-font-loading  
github.com/bramstein/fontfaceobserver  *polyfill*

zachleat.com/web/critical-webfonts  
Loads a subset of a font — letters, numbers — then defer loading rest of font.

github.com/filamentgroup/glyphhanger  
Generate subsetted fonts

## Responsive Images

smashingmagazine.com/2015/12/responsive-images-in-wordpress-core

## Performace Budgets

npmjs.com/package/grunt-perfbudget  
calibreapp.com
