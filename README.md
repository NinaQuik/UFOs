# UFOs
## Overview
This project uses JavaScript, HTML and CSS to build a dynamic page that displays a table of UFO sightings that were reported during two weeks of 2010.  The UFO sighting data is stored in a JavaScript array, which is then read into an HTML table.  JavaScript is utilized to allow users to filter the table based on attributes of the UFO sightings.

### Tools
- Bootstrap 4.0
- D3.js version 4.11

## Results

The page is initially loaded with a blurb about UFO sightings and a table containing all 111 records that were found in the [data.js](/static/data.js) file.

![Default](/resources/Default.png)

### Filtering

On the left hand side of the page, users can filter by date, city, state, country, shape, or combinations of each.

Here's an example of filtering By Date:

![Date](/resources/filterByDate.png)

And an example of filtering combinations; Date and Shape:

![Combo](/resources/filterByDateShape.png)

Note that the number of results are returned each time a new filter is applied or cleared.

### Responsiveness

Because the webpage uses Bootstrap 4.0 grid system it is mobile-responsive.  Here's how the page would look on an iPad Mini:

![ipad](/resources/responsive.png)
