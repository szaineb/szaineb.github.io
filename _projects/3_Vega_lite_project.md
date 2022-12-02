---
name: Take 2 - Vega Lite plots in Jekyll, Multiple Ways
tools: [Python, HTML, vega-lite, Jekyll]
image: assets/pngs/cars.png
description: Ways to get vega-lite plots in our webpages, day 2.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


## Example including vega-lite Specs, Multiple ways to include

## Directly from the Vega editor

The following plots are coming directly from the [vega-lite editor](https://vega.github.io/editor).

Example comes from this [great blog post right here](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).

We can use a vegachart HTML tag like so:

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/cars.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/cars.json" style="width: 100%"></vegachart>

<vegachart schema-url="{{ site.baseurl }}/assets/json/interactive2vegaeditor.json" style="width: 100%"></vegachart>

In theory, you can also use [Jekyll hooks](https://jekyllrb.com/docs/plugins/hooks/) to do it, but I haven't figured out a way that looks nice yet.

## Copy specifications directly from online sources (Starboard) through Altair

Here is an example of a plot from a starboard notebook. It uses the Altair 'from_dict' function.

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart1.json" style="width: 100%"></vegachart>

I can start building up a dashboard in ALtair using severa; 'from_dict' calls and 'hconcat' in Altair:

<vegachart schema-url="{{ site.baseurl }}/assets/json/sidebyside.json" style="width: 100%"></vegachart>

I now have added a brush selector using Altair 'add_selection' to the heatmap on the left and also a 'transform_filter' to the histogram on the right.

<vegachart schema-url="{{ site.baseurl }}/assets/json/dashboard_mobility.json" style="width: 100%"></vegachart>

Quick scatterplot of the mobility dataset
<vegachart schema-url="{{ site.baseurl }}/assets/json/mobility_scatter.json" style="width: 100%"></vegachart>

Dashboard in Altair python
<vegachart schema-url="{{ site.baseurl }}/assets/json/dashboard_alt_with_url.json" style="width: 100%"></vegachart>
## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

```
<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html" text="The Analysis" %}
</div>
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

