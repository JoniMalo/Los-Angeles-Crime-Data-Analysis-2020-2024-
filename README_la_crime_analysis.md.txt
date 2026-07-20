# Los Angeles Crime Data Analysis (2020–2024)

## Overview
Exploring crime patterns across a major metropolis requires digging into the granular details of daily incidents. 
This project dives into a comprehensive dataset of over one million (**1,004,894**, to be exact) recorded incidents in Los Angeles, 
spanning a five-year window from **January 1, 2020, to December 30, 2024**. The data provides a rich context for each event, d
etailing exact dates and times, specific neighborhoods, crime types, victim demographics, and geographic coordinates.

## Unlocking Temporal Insights
Raw data rarely comes ready for analysis. Initially, temporal columns are often read as standard strings, which locks away potential time-based insights. 
By converting the occurrence dates into proper datetime objects early on using pandas, 
it became possible to organically break down the timeline and extract days of the week, monthly fluctuations, 
and broader yearly trends without relying on overly complex filtering.

**Key Temporal Finding:**
This temporal breakdown quickly revealed the rhythm of the city. As the week progresses towards the weekend, there is a noticeable spike in activity. 
* **Highest Activity:** Fridays emerged as the most active days, recording **153,663** incidents, closely followed by Saturdays with **147,457**. 
* **Lowest Activity:** Tuesdays saw the lowest volume at **138,125**. 

While the gap isn't drastically wide, the shift towards the weekend paints a clear picture of how daily human routines influence incident rates.

## Understanding Incident Complexity
A single criminal event isn't always straightforward. The dataset structure accounts for this complexity by utilizing multiple crime code columns. 
* **Primary Offense:** Captured in the main crime code column.
* **Secondary/Tertiary Offenses:** Subsequent columns exist to log additional offenses that occurred during the exact same event—for instance, 
a vehicle break-in coupled with identity theft. 

Naturally, most of these secondary columns contain null values because the majority of incidents involve a single reported offense, 
but having this structure available allows for a much deeper look into compounded crimes.

## Visualizing the Patterns
Numbers tell a story, but visuals make it accessible. Moving away from standard defaults 
the visual framework for this project relies on tailored styles using **Matplotlib** and **Seaborn** to build clean, intuitive layouts. 

The analytical narrative is driven by:
* **Horizontal bar charts** highlighting the most frequent offenses.
* **Weekly timelines** tracking crime rate trends over the years.
* **Geographic mapping** based on area names to pinpoint districts with the highest concentrations of specific activities. 

The goal is to provide a clear, visual exploration that allows anyone looking at the data to imagine the spatial and temporal landscape of the city and draw their own conclusions.

Click the link below to access the dataset

https://catalog.data.gov/dataset/crime-data-from-2020-to-present?from_hint=eyJxIjoiQ3JpbWUgZGF0YSBmcm9tIDIwMjAgdG8gMjAyNCJ9

*Built with Python, Pandas, Matplotlib, and Seaborn.*
