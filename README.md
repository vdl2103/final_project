# Hot Humid Baseball

Welcome to our Hot Humid Baseball project github!

### Project Overview

In order to review our project, please use the following documents:

Website: 

Report: report_draft_original.md

### Data

Data is Stored in the following Google Drive locations:  

The raw data files from Earth Engine and the stadium index from Fusion Table are available at the links below:  

"tdmean_ballpark.PRISM.csv": https://drive.google.com/open?id=11Wptk3Eaul1rJEmXB2Xb9T7G_B82i3MK  
"tmin_ballpark.PRISM.csv"  : https://drive.google.com/open?id=1gtjdciCF4zJmrcyjXnUrj-JNDs437MCa  
"tmax_ballpark.PRISM.csv"  : https://drive.google.com/open?id=1AYqLA1Qp3tOOG7hltIN9-aXuYUkF3SSq  
"stadium_index.csv"        : https://drive.google.com/open?id=13mteZpqRSzkeUObmaL6VwYT9s3QNlDOo  
 
The geocoded stadium index source is: https://fusiontables.google.com/DataSource?docid=1EXApOoxEgJUFlbMjUodfxBSWlRvgQNpABeddHqiN#rows:id=1

The joined and cleaned weather dataframe, `weather.csv`, is available at:

"weather.csv" : https://drive.google.com/open?id=1jr1_sSAzSn8SVKralTHWGdQWH0BEX08W

The baseball data used for this project can be accessed here: https://drive.google.com/drive/u/0/search?q=sqlite

### Needed Packages

If you intend to knit the R Markdown document to replicate this project, be sure the following packages are installed:  

`install.packages("tidyverse")`  
`install.packages("lubridate")`
`install.packages("pitchRx")`  
`install.packages("knitr")`
`install.packages("kableExtra")` 
`install.packages("weathermetrics")` 
`install.packages("patchwork")`
