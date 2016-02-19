# Midterm Project

For your midterm project, you will work as a group to produce 3 to 4 visualizations using [D3](https://d3js.org/) for one of the datasets below. You can use any of the basic, time series, or multivariate visualization techniques discussed in class. These visualizations must be placed on a professional-quality project website, and your group must present your visualizations in class.

## Group Requirements

Each group must have 3 to 4 students, up to a maximum of 8 groups total. Each group must decide on a group name, and will have a dedicated Github repository for this project. 

:busts_in_silhouette: *See the related assignment on Canvas for instructions on how to form and finalize midterm groups.*
    
## Data Requirements

Each group must select a dataset from the list below, and use this dataset for all their visualizations.

- Pending

You are welcome to filter and preprocess these datasets to focus only on what you are interested in and to reduce the size of the dataset if necessary. You can do this preprocessing outside of JavaScript to generate a clean, compact CSV or JSON file that will be loaded by your visualizations. You can use Python, R, Excel, or the free [Trifacta Wrangler](https://www.trifacta.com/products/wrangler/) for this preprocessing stage.

:page_facing_up: *You will have to submit a proposal with the dataset and visualization techniques you plan to use in Canvas roughly 2 weeks before your midterm project is due.*

## Visualization Requirements

Each group must produce **one visualization per person** in the group (i.e. 1 svg per person in the group). All visualization must be of the same dataset, but **must provide a unique perspective** of that dataset. 

:bar_chart: *You can be fairly confident you are meeting this requirement if you have with unique encodings of the data that support different actions and tasks. Try first to identify different questions you have about the data and design visualizations to answer those questions.*

You can use any of the basic, time series, or multivariate visualization techniques discussed in class. Possible visualization techniques include:

- **Area Charts:** Includes area charts, stacked area charts, 100% stacked area charts, small multiple area charts, [streamgraphs](https://bl.ocks.org/mbostock/4060954), and area charts on Cartesian or polar coordinate systems.
- **Bar Charts:**: Includes vertical and horizontal bar charts, stacked bar charts, 100% stacked bar charts, grouped bar charts, small multiple bar charts, histograms, and bar charts on Cartesian or polar coordinate systems.
- **Box Plots:** Includes all variants of [box plots](https://bl.ocks.org/mbostock/4061502).
- **Bullet Charts:** Includes [bullet charts](https://bl.ocks.org/mbostock/4061961) and small multiple bullet charts.
- **Heatmaps:** Includes heatmaps using Cartesian or polar coordinate systems.
- **Horizon Charts:** Includes both offset and mirrored horizon charts, and small multiple horizon charts. *You may use the [d3.horizon](http://bl.ocks.org/mbostock/1483226) plugin or [Cubism.js](https://square.github.io/cubism/) library for these.*
- **Line Charts:** Includes single line charts, multiseries line charts, and small multiple line charts.
- **Parallel Coordinates:** Includes parallel coordinates using Cartesian coordinates. Also includes radar or star charts using [polar](http://bl.ocks.org/mbostock/4583749) coordinates, *but why would you want to do this*?
- **Pie Charts:** Includes pie charts and donut charts. *But, why would you want to do this?*
- **Scatter and Bubble Plots:** Includes scatterplots, scatterplot matricies, bubble charts, and small multiple bubble charts.

You are welcome to inquire about other techniques on Piazza.

:computer: *Keep in mind you will have to present your project in class. Try to keep the maximum required dimensions of your website and visualizations to a reasonable size!*

## Website Requirements
  
Each group must create a professional-quality project website to showcase their visualizations. This website should use Github Pages and the dedicated Github repository created for this project. The website should include the following content:
  
  - A list of group members, ideally with profile photos, USF email addresses, and a brief biography for each member. Please also indicate who worked on what. This includes which member(s) in the group put together the website, processed the data, and produced each visualization.
  
  :octocat: *Your first Github Pages assignment for this class will be useful for this part!*
  
  - A description of the original dataset, a description of any preprocessing done to this dataset, and a link to the original and processed data. In your descriptions, indicate the size of your dataset (number of columns and rows), the descriptions of key columns that gives the type of data and range of values for that column.   
    
  - A clear way to navigate to each of the visualizations. These can be spread across multiple pages or placed on a single page, as long as it is clear how to find each visualization. *Keep in mind you can only submit 1 link in Canvas!*
  
  - A brief note or caption stating at least one interesting finding about the dataset for each visualization.
  
The end goal is to have (a) a website that satisfies these project requirements and (b) a website that you want to show off to friends, family, and future employers. 
  
:link: *You must submit a single link to your project website by the deadline in Canvas. Make sure all of the required content is accessible from this link!*
    
## Presentation Requirements

Each group must give a brief 10 minute project presentation in class. Each person in the group should speak for a roughly equal time. During the presentation, please make sure to cover the following:

- Briefly discuss the dataset you selected and any preprocessing you performed. Try to keep this to under a minute.
 
- For each visualization, describe how you encoded the data and at least one insight about the dataset revealed by the visualization. This should take the majority of your presentation time.

- Leave 1 or 2 minutes for questions. If you do not get any questions, you can fill the time by discussing the challenges you faced.

You should not need to produce any slides. Instead, take advantage of your project website and show off your visualizations live! 

We will use the following schedule for presentations. Groups will be *randomly* assigned to time slots.

| Time Slot           | Monday Group    | Wednesday Group |
|--------------------:|:----------------|:----------------|
|  *2:15pm – 2:20pm*  | *Setup*         | *Setup*         |
| **2:20pm – 2:30pm** | **Group A**     | **Group E**     |
|  *2:30pm – 2:35pm*  | *Setup/Voting*  | *Setup/Voting*  |
| **2:35pm – 2:45pm** | **Group B**     | **Group F**     |
|  *2:45pm – 2:50pm*  | *Setup/Voting*  | *Setup/Voting*  |
| **2:50pm – 3:00pm** | **Group C**     | **Group G**     |
|  *3:00pm – 3:05pm*  | *Setup/Voting*  | *Setup/Voting*  |
| **3:05pm – 3:15pm** | **Group D**     | **Group H**     |
|  *3:15pm – 3:20pm*  | *Voting*        | *Voting*        |

:hourglass: *Presentations will be timed and your group will be docked points if you run too short or too long. To keep the schedule on track, I will eventually cut you off if you run long!*

## Useful References

You can find examples at:

- <https://github.com/mbostock/d3/wiki/Gallery>
- <http://bl.ocks.org/mbostock>
- <http://christopheviau.com/d3list/gallery.html>

You may use existing examples as inspiration, but the final product must be your own. Remember to cite all your sources and inspirations in your code and website to avoid any issues with academic honesty.

