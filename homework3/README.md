# Homework 3 Multivariate Data

For this homework assignment, you must visualize the [Zillow Market Health Index](http://www.zillow.com/research/data/) dataset for cities using one of three multi-variate visualization techniques. You will first prototype the technique in Tableau, and then implement the technique in D3. See below for details.

## Eligibility

All of the following requirements must be satisfied for your submission to earn a grade for this homework assignment:

- You must use [Tableau Desktop](http://www.tableau.com/products/desktop), [Tableau Public](https://public.tableau.com/), and/or [D3](https://d3js.org/) to generate your visualizations. You may also use the [ColorBrewer](https://github.com/mbostock/d3/wiki/Ordinal-Scales#colorbrewer) D3 library for this assignment. You may not use any other JavaScript libraries unless explicitly approved by the instructor.

- You must use [`d3.csv()`](https://github.com/mbostock/d3/wiki/CSV) to load the exact CSV provided for this assignment. Any preprocessing of this data must be done in JavaScript, ideally using [`d3.nest()`](https://github.com/mbostock/d3/wiki/Arrays#nest) or [`d3.map()`](https://github.com/mbostock/d3/wiki/Arrays#maps) to process your data.

- You must follow the submission instructions for this assignment, including committing your files on-time to your Github Pages repository and submitting your homework link on-time in Canvas.

- The width of each visualization must not exceed 960 pixels, but may be any (reasonable) height.

:warning: **Failure to meet the above requirements will at worst make your submission ineligible for grading, and at best result in severe point deductions.**

## Requirements

You must choose **exactly one** of the following multivariate visualization techniques to implement in both Tableau and D3. The technique you choose will determine your the possible score:

| Description | Bubble Plot | Heatmap | Scatterplot Matrix | Parallel Coordinates |
|:------------|:-----------:|:-------:|:------------------:|:--------------------:|
| Tableau Prototype | 30pts | 30pts | 40pts | 40pts | 
| Tableau Customization | 10pts | 10pts | 10pts | 10pts |
| D3 Implementation | 30pts | 30pts | 40pts | 40pts | 
| D3 Customization | 10pts | 10pts | 10pts | 10pts |
| **Total Possible** | **80pts** | **80pts** | **100pts** | **100pts** |

You must complete the Tableau prototype **BEFORE** the D3 implementation. No matter which technique you choose, your visualizations should encode *at least* 4 columns and include *at least* 50 rows from the dataset. You are encouraged to visualize more of the dataset if possible.

To earn customization credit, you must make at least 5 modifications to the visualization defaults. Example changes include changing the color scale, adding text annotations, adjusting legends, adjusting the tick marks, and changing the formatting of axis lines. *You must list the changes you made on your website to earn credit.*

:thumbsup: You may earn up to 20 points extra credit if you implement 2 extra techniques in Tableau (10 points per extra technique). You may receive these points regardless of whether you completed any D3 implementations.

## Data Source

You must use the [Zillow Market Health Index](http://www.zillow.com/research/data/) dataset for cities. The original CSV file contains 10,790 rows, but many of those rows contain 1 or more null values. 

Instead, please use the pre-filtered [MarketHealthIndex_City_Filtered.csv](MarketHealthIndex_City_Filtered.csv) file, which contains only 1,380 rows after filtering out all of the null values.

## Submission

You must still submit a single webpage for your homework submission. Place your homework submission in a subdirectory of your submission repository named `homework3` without spaces in all lowercase. Your entire homework submission should be accessible via the link:

```
http://usf-cs360-2016.github.io/templates-cs360/homework3/
```

Replace `templates` with your MyUSF username, double-check the link works, and then submit it in Canvas by the deadline.

For your Tableau visualizations, [save your workbook to Tableau Public](http://onlinehelp.tableau.com/current/pro/online/windows/en-us/help.html#publish_workbooks_tableaupublic.html). Once your workbook is published, there is a "Share" button with embed code you can copy/paste onto your website. If you are having trouble, it is also acceptable to export your prototype as an image and place that on your website instead.

For your customizations, please include a numbered list of the changes you made for both your Tableau prototype and your D3 implementation on your homework website. You may not receive credit for your customizations if you forget to list them!

:warning: **You must submit your link on-time to participate in peer feedback. Please submit your link early to avoid any issues!**

## References

The following blocks may be useful for this assignment:

- [Bubble Plot](https://bl.ocks.org/sjengle/ff5c5d2ca23389739f05)
- [Scatterplot Matrix](https://bl.ocks.org/mbostock/3213173)
- [Scatterplot Matrix in Tableau](https://www.interworks.com/blog/mtreadwell/2013/08/29/statistical-insights-using-tableau)
- [Parallel Coordinates](http://bl.ocks.org/mbostock/1341021)
- [Parallel Coordinates in Tableau](http://www.bzst.com/2014/04/parallel-coordinate-plot-in-tableau.html)

You may use existing examples as inspiration, but the final product must be your own. Remember to cite all your sources and inspirations in your code and README to avoid any issues with academic honesty.
