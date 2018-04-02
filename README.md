Load external data from a .csv file into a data frame
================

-   This page: <http://bit.ly/2018-04-03-dataframes>.
-   DataCarpentry [lesson](http://bit.ly/2GQue5W).

------------------------------------------------------------------------

Presentation of the Survey Data
-------------------------------

`surveys`: Species repartition and weight of animals caught in plots in a study area ([via](http://bit.ly/2GOdpIV)).

![](https://i.imgur.com/SGqtN09.png)

### Setup

``` r
# Install software
# If you haven't yet -- once for good
# install.packages("tidyverse")

# "Open" software
# Every time you re-run this document (Ctrl + Alt + R)
library(tidyverse)
#> ── Attaching packages ────────────────────────────────────────────────────────── tidyverse 1.2.1 ──
#> ✔ ggplot2 2.2.1     ✔ purrr   0.2.4
#> ✔ tibble  1.4.2     ✔ dplyr   0.7.4
#> ✔ tidyr   0.8.0     ✔ stringr 1.3.0
#> ✔ readr   1.1.1     ✔ forcats 0.3.0
#> ── Conflicts ───────────────────────────────────────────────────────────── tidyverse_conflicts() ──
#> ✖ dplyr::filter() masks stats::filter()
#> ✖ dplyr::lag()    masks stats::lag()
```

### Get data from the web: <http://bit.ly/carpentry-start-with-data-surveys>

![](https://i.imgur.com/B103PIO.png)

### Import dataset from text (**readr** lives in the **tidyverse**)

![](https://i.imgur.com/Sn3lNv2.png)

Provide url, update, copy the code, and cancel
----------------------------------------------

![](https://i.imgur.com/XxxcJAn.png)

### Paste, rename?

``` r
library(readr)
surveys <- read_csv("http://bit.ly/carpentry-start-with-data-surveys")
#> Parsed with column specification:
#> cols(
#>   record_id = col_integer(),
#>   month = col_integer(),
#>   day = col_integer(),
#>   year = col_integer(),
#>   plot_id = col_integer(),
#>   species_id = col_character(),
#>   sex = col_character(),
#>   hindfoot_length = col_integer(),
#>   weight = col_integer(),
#>   genus = col_character(),
#>   species = col_character(),
#>   taxa = col_character(),
#>   plot_type = col_character()
#> )
```

### View data

    View(surveys)

![](https://i.imgur.com/5viRubE.png)

### Visualize contents in alternative ways

``` r
head(surveys)
#> # A tibble: 6 x 13
#>   record_id month   day  year plot_id species_id sex   hindfoot_length
#>       <int> <int> <int> <int>   <int> <chr>      <chr>           <int>
#> 1         1     7    16  1977       2 NL         M                  32
#> 2        72     8    19  1977       2 NL         M                  31
#> 3       224     9    13  1977       2 NL         <NA>               NA
#> 4       266    10    16  1977       2 NL         <NA>               NA
#> 5       349    11    12  1977       2 NL         <NA>               NA
#> 6       363    11    12  1977       2 NL         <NA>               NA
#> # ... with 5 more variables: weight <int>, genus <chr>, species <chr>,
#> #   taxa <chr>, plot_type <chr>
```

**You just met a data frame. What do you think data frames are?**

-   Continue [lesson](http://bit.ly/2GQue5W).

------------------------------------------------------------------------

-   [Contact Mauro](https://github.com/maurolepore).

<iframe src="https://todaysmeet.com/room/3261852/embed?type=live&amp;hide_ui=0" height="400" width="100%">
</iframe>
