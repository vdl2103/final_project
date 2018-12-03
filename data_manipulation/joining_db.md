Joining pitching and weather databases
================

``` r
my_db <- src_sqlite("./data/GamedayDB.sqlite3", create = TRUE)
pitch = tbl(my_db$con, "pitch")
atbat = tbl(my_db$con, "atbat")
test2 <- collect(inner_join(pitch, atbat, by = c("num", "url")))
```

``` r
#Import and clean pitching data 
pitch_tidy_db = test2 %>% #test2 comes from pitch_data.rmd, but I included a few more variables 
  separate(gameday_link.x, into = c("remove", "away_home"), sep = ".............._") %>%
  separate(away_home, into = c("away", "home"), sep = "mlb_") %>% 
  select(start_speed, end_speed, home, away, pitcher_name, stand, pitch_type, date, inning.x, pitcher, type,
         num, event, score) %>% 
  mutate(date = ymd(date)) %>% 
  rename(inning = inning.x)
```

    ## Warning: Expected 2 pieces. Additional pieces discarded in 2744247 rows [1,
    ## 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, ...].

``` r
#Add team names to pitching data 
team_names = read_csv("./data/team_abbrv.csv")
pitch_tidy_db = left_join(pitch_tidy_db, team_names)  
```

``` r
#Import weather data 
weather_db = read_csv("./data/weather.csv") 

#Join databases and remove: 1) teams with roofs, 2) spring training games, 3) AS games 
complete_db = left_join(pitch_tidy_db, weather_db) %>% 
  filter(!home %in% c("aas", "nas", "tor", "ari", "sea", "hou", "tba", "mia", "1", "2")) %>%  
  separate(date, c("y", "m", "d")) 
```

``` r
#Examining missing data
missing_data = complete_db %>% 
  filter(is.na(start_speed)) %>% #we are missing pitch speed for 62,971 pitches 
  group_by(team_name) %>% 
  count() #see if the missing data are (roughly) evenly distributed among the teams 
```
