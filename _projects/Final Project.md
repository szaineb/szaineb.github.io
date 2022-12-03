---
name: Final Project
tools: [Python, HTML, vega-lite]
image: assets/pngs/final-project.png
description: IS 445 Data Visualization Final Project
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Hate Crimes in New York City (2021)


In this article, we will look into the hate crimes or bias motivated incidents in the New York City (NYC) during 2021. 

According to data provided by New York Police Department (NYPD), a total of 572 hate crimes were reported across NYC police precincts. Around 37% of these incidents had anti-jewish bias motivations.

The chart below presents the top 5 bias motivations behind hate crimes in NYC in the year 2021.

<vegachart schema-url="{{ site.baseurl }}/assets/json/NYPD_Bias_Motives_Top5.json" style="width: 100%"></vegachart>

Majority of the hate crimes occurred in Manhattan South borough and Staten Island had the least number of hate crimes reported. 

<vegachart schema-url="{{ site.baseurl }}/assets/json/NYPD_Patrol_Boroughs.json" style="width: 100%"></vegachart>

The charts below presents an overview of the hate crime complaints filed in various New York City police precincts in the year 2021. The map is color coded by the number of hate crime complaints filed. Lighter yellow shades represent lower number of crimes while brightest orange red color depicts highest number of crime complaints. On the right, there is a bar chart that shows count of complaints by 'Bias Motiviations'. Hover over the map to get details about police precinct, patrol borough and number of complaints filed. The distribution of incidents occurred in different precincts across various bias motivations can be seen by selecting precincts on map. To select more than one precinct, use Shift+Click. Click any where around map to reset.

In addition to Jews, Asian, Gay and Black population have also been the target of hate crimes in NYC. 

<vegachart schema-url="{{ site.baseurl }}/assets/json/NYPD_hate_crime_dashboard.json" style="width: 100%"></vegachart>

Since NYC and Chicago are often compared for crime rates, let's have a look at hate crimes in Chicago as well. Based on open data from Chicago Police Department, Chicago had a lower hate crime rate as compared to New York City in 2021. Total 109 complaints were filed. Majority of these incidents had anti-Gay and anti-Black motivations. 

The chart below presents the Top 5 bias motivations behind hate crimes in Chicago. 

<vegachart schema-url="{{ site.baseurl }}/assets/json/Chicago_Top5_Motives.json" style="width: 100%"></vegachart>

Austin and Near North Side community areas had the most occurrences of these incidents.

<vegachart schema-url="{{ site.baseurl }}/assets/json/Chicago_Top5_Communities.json" style="width: 100%"></vegachart>

Although there is a difference in the total number and rates of hate crimes reported in New York City and Chicago, there are similarities in the victim groups being targeted in both the cities.

<div><br><b>Sources & References:</b></div>


[Police Precints](https://data.cityofnewyork.us/Public-Safety/Police-Precincts/78dh-3ptz)

[NYPD Hate Crimes](https://data.cityofnewyork.us/Public-Safety/NYPD-Hate-Crimes/bqiq-cu78)

[Chicago Hate Crimes](https://home.chicagopolice.org/statistics-data/data-dashboards/hate-crime-dashboard/)



<div class="left">
{% include elements/button.html link="https://github.com/szaineb/szaineb.github.io/tree/master/data" text="The Data" %}
<br>
</div>

<div class="right">
{% include elements/button.html link="https://github.com/szaineb/szaineb.github.io/blob/master/python_notebooks/zaineb-syedarija-final-project-part3.ipynb" text="The Analysis" %}
</div>





