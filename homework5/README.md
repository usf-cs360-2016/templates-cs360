# Homework 5

For this homework assignment, you will build an interactive geographic visualization of 311 Tree Maintenance requests from 2015. You can create either a choropleth, proportional symbol map, or a non-proportional symbol map. You can choose to group the data by district, neighborhood, or not at all.

**:octocat: This is your last homework assignment.**

## Data Source

The dataset can be downloaded at:

<https://data.sfgov.org/City-Infrastructure/Tree-Maintenance-2015/jzte-ntie>

However, please use the CSV file provided here directly:

[Tree_Maintenance_2015.csv](Tree_Maintenance_2015.csv)

Requests marked as transfered, canceled, duplicated, or invalid were removed. Requests without valid GPS coordinates, district, or neighborhood information were also removed. And, some basic preprocessing has been done to make certain columns more readable.

## Boundaries

You should show some district or neighborhood boundaries (or both) no matter which visualization technique you choose. However, some techniques will work better with different underlying boundaries.

### District Boundaries

The supervisor district boundaries can be downloaded at:

<https://data.sfgov.org/Geographic-Locations-and-Boundaries/Supervisor-Districts-as-of-April-2012/xz9b-wyfc>

These *should* match the supervisor districts listed in the data file.

### Neighborhood Boundaries

The SF neighborhood boundaries are more tricky, as there are multiple conflicting definitions of a "neighborhood" available. It looks like the following set of boundaries are the closest match to the ones used by 311:

- [SF Find Neighborhoods](https://data.sfgov.org/Geographic-Locations-and-Boundaries/SF-Find-Neighborhoods/pty2-tcw4): Created by the Office of Neighborhood Services for use with the SF Find tool.

If you use the above file, keep in mind that there are no boundaries defined for the "Fisherman's Wharf" and "St. Mary's Park" neighborhoods. Everything else should match one of the boundaries exactly.

If you are not trying to match the neighborhood names to the data file, then you can use any of the neighborhood boundaries available. Other options include:

- [Neighborhood Groups](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Neighborhood-Groups-Map/iacs-ws63): Created by the Department of City Planning.

- [Analysis Neighborhoods](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Analysis-Neighborhoods/p5b7-5n3h): Created by the Department of Public Health and the Office of Housing and Community Development by grouping 2010 Census tracts.

- [Realtor Neighborhoods](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Realtor-Neighborhoods/5gzd-g9ns): Created by the San Francisco Association of Realtors (SFAR).

You may use the same projection provided in lecture for the San Francisco region.

### Bonus: Streets

You can earn extra credit if you also show streets. You will need to [parse shapefiles](https://data.sfgov.org/data?search=streets&dept=&category=Geographic+Locations+and+Boundaries&type=) from <https://data.sfgov.org> into GeoJSON/TopoJSON files for this option.

## Visualization Techniques

You can create either a choropleth, proportional symbol map, or a non-proportional symbol map. All are worth the same amount of points.

### Non-Proportional Symbol Map

This option should show the location of every individual request made. You will need to properly parse the "Point" column in the CSV file, and can use any underlying boundary map.

You should encode an additional piece of information using color, and show a color legend. You may decide what information you encode by color. For example, you can color by the "Source", "Request Type", "Opened", or "Status" columns.

Also, consider how to use shape, stroke, and opacity of the symbols effectively.

### Choropleth Map

You will need to nest and rollup the data by either district or neighborhood. You should choose the appropriate underlying boundary map based on your choice.

You should also provide a color legend. You may also want to consider using a threshold scale instead of a linear scale. For example:

- [Kentucky Population Density](http://bl.ocks.org/mbostock/5144735)
- [California Population Density](http://bl.ocks.org/mbostock/5562380)
- [Threshold Key](http://bl.ocks.org/mbostock/4573883)

Consider what color scales make the most sense for your data, and how to use color (or lack thereof) for the other map components (such as boundaries between regions).

### Proportional Symbol Map

You will need to nest and rollup the data by either district or neighborhood. You should choose the appropriate underlying boundary map based on your choice.

You should also provide a size legend. For example:

- [County Bubbles](http://bl.ocks.org/mbostock/9943478)

You will also need to calculate the "center" of that region to place each the symbol. You should be able to use [`d3.geo.path.centroid()`](https://github.com/mbostock/d3/wiki/Geo-Paths#path_centroid), but it might be easier to just [find the bounding box](http://stackoverflow.com/questions/12062561/calculate-svg-path-centroid-with-d3-js) for a region and calculate the center pixel location.

# Interaction

You should have a details-on-demand interaction **and** either brushing, filtering, or zooming implemented. Details are below.

:bulb: I recommend you create a working version of your homework without this brush/filter/zoom interactivity first, and save it as a branch or release on Github. Then, attempt to implement this interactivity and revert to the previous version if you are unable to get it working. *It is possible to pass this assignment without brush/filter/zoom interactivity.*

## Details on Demand

You should have a details-on-demand interaction. For example, show details when the mouse hovers over a region and/or symbol. You should implement this in base D3---please do not use a tooltip library.

Your details should be readable and informative. Think about which details will be useful, and adjust the formatting of the text as appropriate. 

## Zooming/Panning

Here are some examples specific for maps for zooming/panning:

- [Zoomable Geography](http://bl.ocks.org/mbostock/2374239)
- [Zoom to Bounding Box II](http://bl.ocks.org/mbostock/9656675)
- [Zoom to Bounding Box](http://bl.ocks.org/mbostock/4699541)

This type of interactivity will work with any visualization type, but can be tricky to properly scale the size of symbols.

## Brushing/Filtering

For brushing or filtering, you will need to be creative. You should choose a column in the dataset with semi-categorical information (or a date/time column), and then how you want to control which information is brushed/filtered. 

You could add a linked visualization to control what information is brushed or filtered, or add HTML form controls to your page to control this. See the following blocks for examples:

- [SVG Controls](https://github.com/mbostock/d3/wiki/SVG-Controls)
- [Sortable Bar Chart](http://bl.ocks.org/mbostock/3885705)
- [Dispatching Events](http://bl.ocks.org/mbostock/5872848)

Alternatively, if you use a non-proportional symbol map, you could brush/filter other points based on a characteristic of a clicked symbol. For example, if you clicked on a symbol that was opened in April, you could brush all other symbols that occurred in April. 

# Findings

**Use your visualization to learn something about the data.** Include your findings on your submission page. This should be 1 paragraph with 3 to 5 sentences. 

Look for simple conclusions (which district has the most reports) *and* more complex conclusions (which street or general region seems to be most problematic). If you do not learn something, rethink your visualization!

# Evaluation

There will be peer reviews for this homework. Specifically, you will be asked to evaluate 2 to 3 other submissions. You must evaluate the data-ink ratio, data density, lie factor, context, interactivity, and overall design of the visualization on a 5 point scale:

| #   | Description |
|:---:|:-----------|
|   0 | Missing Submission, Not Applicable |
|   1 | Poor, Significant Improvement Needed |
|   2 | Okay, Major Improvement Needed |
|   3 | Good, Some Improvement Possible |
|   4 | Great, Little Improvement Possible |
|   5 | Excellent, No Improvement Possible |

You must provide significant feedback to justify your rating. Ratings will be factored into the final grade.

# Grade Breakdown

The grade will be calculated as follows:

| Points | Description |
|-------:|-------------|
|     40 | Visualization - Overall |
|     10 | Visualization - Legend |
|     20 | Interactivity - Brush/Filter/Zoom |
|     10 | Interactivity - Details on Demand |
|     10 | Findings |
|     10 | Evaluation |

## Extra Credit

You can earn up to 10 points extra credit by completing **one** of the following:

- Use Voronoi tesselation for the details-on-demand interactivity. See for example:

  <https://mbostock.github.io/d3/talk/20111116/airports.html>

- Show street boundaries in your visualization. You will need to [parse shapefiles](https://data.sfgov.org/data?search=streets&dept=&category=Geographic+Locations+and+Boundaries&type=) from <https://data.sfgov.org> for this option.

There is a cap on the number of points you can earn, so choose one or the other to implement.

# Submission

You must submit a single webpage for your homework submission. Place your homework submission in a subdirectory of your submission repository named `homework5` without spaces in all lowercase. Your entire homework submission should be accessible via the link:

```
http://usf-cs360-2016.github.io/templates-cs360/homework5/
```

Replace `templates` with your MyUSF username, double-check the link works, and then submit it in Canvas by the deadline.

**:warning: Late submissions are not accepted. You must have your link submitted on Canvas on time to receive a grade for this homework and the associated peer review exercise.**
