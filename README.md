# MMM-RecentRainfall
MagicMirror module to get recent US Rainfall amounts.
version 1.01 changes by Kayakbabe aka Kelly Eberhard Allen
  adding more options from the rcc-acis.org api in order to zoom in on smaller areas
  such as county or that defined by gps coordinates as some states are very large
  and some users may only want to see their own county or a defined area.

  WARNING: THIS IS IN DEVELOPMENT_ THIS IS NOT RELEASED AS WORKING YET.
           this message will be removed when this module is working.

  requires ^MagicMirror 2.26

## API
Uses the open/free api https://data.rcc-acis.org/StnData   http://www.rcc-acis.org/docs_webservices.html

## Preview
![screenshot1](screenshot1.JPG)

## Using the module
run git clone https://github.com/vincep5/MMM-RecentRainfall from inside your MagicMirror/modules folder

Add `MMM-RecentRainfall` module to the `modules` array in the `config/config.js` file:
````javascript
modules: [
  {
    module: "MMM-RecentRainfall",
    position: "top_right",
    header: "Rainfall",
    config: {
        station_id: 'JFK', // id via http://www.rcc-acis.org/docs_metadata.html
        days_to_get: 7, // number greater than 1
        show_image: true, // show the departure from normal as an image
        state_id: 'ny', // if show_image is true, then this is required
        image_width: 150 // if show_image is true, then this is required
    }
  },
]
