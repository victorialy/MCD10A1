# MCD10A1: a robust MODIS snow cover and snow phenology product

## Description

The Google Earth Engine (GEE) code within this project combines MODIS Aqua - Terra snow cover products and derives snow melt - accumulation (snow phenology) dates.

The original MODIS products (MOD10A1 & MYD10A1, for the Terra and Aqua platforms respectively) as processed by the National Snow and Ice Data Center (NSIDC) have the tendency to be biased low.

My code fuses the two data streams using a maximum value approach to account for this bias. More importantly, the script also generates a derived snow phenology product where I calculate snow melt in spring and and snow accumulation in autumn.

As an example the script runs a simple regression analysis to mark trends in snow melt dates, answering the question if snow melt occurs later or earlier over time.

## Using the code

You can clone the project, copy and paste the code into your current workspace / project or use the [GEE link](https://code.earthengine.google.com/bd06f9efa757b7fbf9d2ae282d319282).

## Example (as generated by the code)

Below you see a snow melt trend map of the US and Canada, with earlier snow melt marked in red and later snow melt marked in blue. 

Some clear trends can be seen in the mountain ranges in the West of the US with very pronounced earlier snow melt dates. High latitudes throughout Alaska and Canada also see a shorter snow season. Some later snow melt date trends can be noted as well, sweeping east from the middle of Alberta, Canada, to the great lakes.

Caution is needed in interpreting the trend analysis as generated by the code. The analysis relies on a simple linear regression which might be skewed by outliers. I suggest using a panel analysis or a robust regression analysis before making any scientific inference.

![](snowmelt_trends.png)

## Acknowledgements

Please acknowledge my code by citing the github release through it's DOI.
