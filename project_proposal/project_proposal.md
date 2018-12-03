Project Proposal
================
November 7, 2018

Project Title: Effects of weather on baseball pitcher performance
-----------------------------------------------------------------

Group Members
-------------

Brennan Baker (bhb2128), Nicole Comfort (nc2710), Stephen Lewandowski (sal2222), Victoria Lynch (vdl2103), Jenni Shearston (js5431)

Project Motivation
------------------

To examine the association between weather and the speed and type of baseball pitches. We hypothesize that the speed and type of Major League Baseball (MLB) pitches may be negatively impacted by extreme weather.

Intended Final Products
-----------------------

**Website containing the following:**

-   Landing page describing the project

-   Link to Github repository with data

-   Screencast

-   Flexdashboard containing the following items:
    -   Linear model for the effect of temperature on pitch speed (fastball), adjusted for pitcher and other covariates to be determined.
    -   Graph of variation in proportion of fastball vs off-speed pitches and temperature
    -   Graph of speed of fastballs and temperature
    -   Graph of pitch speed (all pitch types) and humidity
    -   Graph of pitch speed (all pitch types) and heat index

**Github Repo including RMarkdown report**

Anticipated Data Sources
------------------------

### Baseball data

Data on pitches are located in XML format on the MLB website. There are 30 MLB stadiums. We will exclude the 6 stadiums that have retractable roofs. Potential covariates: pitcher name, pitch count, pitch type. `mlbgameday` is an R package that we will use to scrape the website and construct our initial baseball dataset.

### Weather data

We will use either nearby weather station or gridded climate model data. The `meteo_nearby_stations` function in `rnoaa` can identify weather monitors within a specified radius from the latitude and longitude coordinates of outdoor ballparks. Daily measurements can be extracted by station and time range using `meteo_pull_monitors`.

Alternatively, we can utilize a gridded climate model such as PRISM, which provides daily values for the United States. We can access this model at approximately 5 km resolution through Google Earth Engine. This dataset also provides a daily mean dew point temperature, which can be used to calculate relative humidity and a heat index.

Planned Analyses / Visualizations / Coding Challenges
-----------------------------------------------------

### Planned Analyses and visualizations

-   Creating a model to assess the effect of temperature on fastball pitch speed, accounting for potential confounding variables.

-   A series of graphs depicting hourly temperature, max and min temperatures, humidity, and heat index and baseball pitch speed and type.

### Anticipated Challenges

-   Tidying the pitch and rnoaa datasets so that they can be merged.

-   Downloading the weather data at hourly resolution

-   Visualizing the wide range of temperatures both geographically and by other variables.

Planned Project Timeline
------------------------

-   November 15 - Have complete and clean dataset compiled

-   November 21 - Complete first draft of all figures/graphs

-   December 2 - Finalized analyses and website content (minus screencast)

-   December 3-5 - Create screencast
