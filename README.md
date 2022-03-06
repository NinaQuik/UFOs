# UFOs
## Overview
This project uses JavaScript, HTML and CSS to build a dynamic page that displays a table of UFO sightings that were reported during the early weeks of 2010.  The UFO sighting data is retrieved from a JavaScript array, and then read into an HTML table.  JavaScript is utilized to allow users to filter the table based on attributes of the UFO sightings.

### Tools
- Bootstrap 4.0
- D3.js version 4.11

## Results

The page is initially loaded with a short blurb about UFO sightings and a table containing all 111 records that were found in the [data.js](/static/data.js) file.

![Default](/resources/Default.png)

### Filtering

On the left hand side of the page, users can search for UFO sightings by date, city, state, country, shape, or combinations of each.

Here's an example of filtering By Date:

![Date](/resources/filterByDate.png)

And an example of filtering combinations; Date and Shape:

![Combo](/resources/filterByDateShape.png)

### Number of Results

Note that the number of results are returned each time a new filter is applied or cleared.

### Lower vs. Upper Case

Because most people capitalize city names and state abbreviations, I made a small tweak to convert the filterValue to lowerCase.  ```let filterValue = changedElement.property("value").toLowerCase();```.  This should improve usability.

Here's an example of state search with capitalized state entered:

![Capital](/resources/CapitalSearch.png)

### Responsiveness

The webpage uses Bootstrap 4.0 grid system so that it is mobile-responsive.  Here's how the page would look on an iPad Mini:

![ipad](/resources/responsive.png)

## Summary

The UFO Finder html page was easily created using javaScript D3 and HTML.  There are a number of improvements that could be made to enhance the page, however.

- One drawback to the page, is that there is not an easy way to clear the filters.  A button could be created that resets the filters to the original state.
- The date format in the data.js file doesn't account for zeros.  If the user entered 01/01/2010 they would not find results for 1/1/2010.  I created a regex pattern ```pattern="^([1-9]|[1][1-2])(\/)([1-9]|([1-2][0-9])|(3)[0-1])(\/)\d{4}$"``` that checks for the date format used in the js file.  With additional time and coding, it could be possible to alert the user that they entered an invalid date format.
- The data in the comments sections includes html coded character set, ex ```&#44;``` for commas and ```&#33``` for exclamation marks.  To improve readability it may be possible to decode those characters.
