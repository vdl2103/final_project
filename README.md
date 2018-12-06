# Hot Humid Baseball

Welcome to our Hot Humid Baseball project github, by Brennan Baker, Nicole Comfort, Stephen Lewandowski, Victoria Lynch, and Jenni Shearston. 

### Project Overview

In order to review our project, please use the following:

**Website Link:** Vdl2103.github.io/hot_humid_baseball.github.io/

**Report Name:** final_report_hhb.pdf

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

The baseball team abbreviation file can be accessed here: https://drive.google.com/file/d/1IUVXPXsG_vuuIRoMJxzHgMLBWV4D4Kx7/view?usp=sharing

To knit the report Rmarkdown and recreate this project, ensure the following files are downloaded and placed into a "data" folder:

* GamedayDB.sqlite3
* stadium_index.csv
* tdmean_ballpark_PRISM.csv
* team_abbrv.csv
* tmax_ballpark_PRISM.csv
* tmin_ballpark_PRISM.csv

### Needed Packages

If you intend to knit the report R Markdown document, be sure the following packages are installed:  
  
*Please note that it will take approximately 15 minutes to knit this report.* 

`install.packages("tidyverse")`  
`install.packages("lubridate")`  
`install.packages("pitchRx")`    
`install.packages("knitr")`  
`install.packages("kableExtra")`   
`install.packages("weathermetrics")`   
`install.packages("patchwork")`

