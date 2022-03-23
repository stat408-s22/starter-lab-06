Lab 06 - University of Edinburgh Art Collection
================
Insert team name here:  
Insert team member 1 here  
Insert team member 2 here  
Insert team member 3 here  
Insert team member 4 here

Insert date here

### Load packages and data

``` r
library(tidyverse) 
library(skimr)
```

### R scripts

Fill in the blanks and required information to complete the code in the
three R script files:

-   Exercises 1–5: `01-scrape-page-one.R`
-   Exercise 6: `02-scrape-page-function.R`
-   Exercises 7–9: `03-scrape-page-many.R`

After completing the code and running these scripts, you should have a
csv file named “uoe-art.csv” that stores the scraped data in the “data”
folder. Load this csv file using the code below and answer the remaining
exercises in this .Rmd file.

``` r
# Remove eval = FALSE or set it to TRUE once data is ready to be loaded
uoe_art <- read_csv("data/uoe-art.csv")
```

### Exercise 10

``` r
uoe_art <- uoe_art %>%
  separate(title, into = c("title", "date"), sep = "\\(") %>%
  mutate(year = str_remove(date, "\\)") %>% as.numeric()) %>%
  select(title, artist, year, ___)
```

    ## Error: <text>:4:31: unexpected input
    ## 3:   mutate(year = str_remove(date, "\\)") %>% as.numeric()) %>%
    ## 4:   select(title, artist, year, _
    ##                                  ^

### Exercise 11

Remove this text, and add your answer for Exercise 10 here. Add code
chunks as needed. Don’t forget to label your code chunk. Do not use
spaces in code chunk labels.

### Exercise 12

…

Add exercise headings as needed.
