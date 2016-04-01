# Mini Homework: Interactive Line Chart

It is your favorite block again! Add some interactivity to the [Multi-Series Line Chart](http://bl.ocks.org/mbostock/3884955) example for this **mini-homework**. Go to the [underlying Gist](https://gist.github.com/mbostock/3884955) for the [Multi-Series Line Chart](http://bl.ocks.org/mbostock/3884955) block and download the code. Place it in your homework repository, and start adding some interactivity!

:bulb: This mini-homework will be included in the "Homework" category, but will be worth fewer points than a normal homework.

## Link Submission

Place your homework submission in a subdirectory of your submission repository named `homework4` without spaces in all lowercase. Your entire homework submission should be accessible via the link:

```
http://usf-cs360-2016.github.io/templates-cs360/homework4/
```

Replace `templates` with your MyUSF username, double-check the link works, and then submit it in Canvas by the deadline.

## Point Breakdown

This assignment is worth 40 points total. You may implement up to 60 points of functionality for extra credit (especially helpful for those that did poorly on previous homework assignments). The possible types of interaction are:

- Choose **one** of the following filter/brush interactions to implement:

  - `[10 pts]` Add the ability to click on the city text to filter the lines shown. Specifically, clicking on a city name should remove (or make invisible) the line for that city. Clicking the text again should add (or make visible) the line for that city.
  
  - `[20 pts]` Add the ability to click on the city text to brush that line. The other lines should turn light grey, and only the line selected should be colored. Clicking the text again should turn off the brush functionality. *(You do not have to worry about lines being drawn on top of each other for now.)*

- Choose **one** or more of the following hover interactions to implement:
  
  - `[10 pts]` Draw each individual point for the lines (you will have to change the line interpolation), and show a tooltip with the point value when you hover over that point. **This interaction should not be combined with the previous interaction (using Voronoi tessellation)!**
  
  - `[10 pts]` Draw each individual point for the lines (you will have to change the line interpolation), and show drop lines from the point to the appropriate locations on the x-axis and y-axis when you hover over that point.

  - `[20 pts]` Draw a tooltip with the point and value label of the point closest to the mouse. You will need to use a [Voronoi tessellation](http://bl.ocks.org/mbostock/8033015) for this interaction.

- Choose **one** of the following zoom interactions to implement:

  - `[10 pts]` Add the ability to zoom and pan using the mouse. You will need to use the zoom behavior [(demo 1)](http://bl.ocks.org/mbostock/4015254) [(demo 2)](http://bl.ocks.org/mbostock/3892919) in D3 for this interaction. You only need to zoom in the x-direction, and do not need to reposition the city names.

  - `[20 pts]` Add the ability to zoom on a single month when you click. You can add a click interaction to the x-axis labels using the `d3.selectAll(".x .tick text")` selection, and get the x location of the mouse according to the outer `g` element using `d3.mouse(this.parentNode.parentNode)[0]`, and converting that to the nearest date using [scale.invert()](https://github.com/mbostock/d3/wiki/Time-Scales#invert). You can make other date manipulations using  [time intervals](https://github.com/mbostock/d3/wiki/Time-Intervals) in D3.

Bonus: Check out the [brush](https://github.com/mbostock/d3/wiki/SVG-Controls) control in D3, and figure out a way to apply it!

## Hints

If will be easier to do certain operations if you give your lines an ID. However, IDs may not contain spaces and should be unique. One way to do this is to use the first three letters of the city name. Try the following in the JavaScript console:

```
"San Francisco".substring(0, 3).toUpperCase();
```

Whatever you do, make sure it is consistent so you can always figure out the appropriate ID from the city name.
