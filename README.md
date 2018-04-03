Load external data from a .csv file into a data frame
================

-   [See <https://bit.ly/carpentry-slides>](#see-httpsbit.lycarpentry-slides)
-   [Try by intuition](#try-by-intuition)
-   [Back to the lesson](#back-to-the-lesson)
-   [Resources](#resources)

------------------------------------------------------------------------

See <https://bit.ly/carpentry-slides>
-------------------------------------

Try by intuition
----------------

Document what you did.

``` r
# Some code goes here
```

Back to the lesson
==================

> To download the data into the data/ subdirectory, run the following:

You may want to try:

-   `download` and get help from auto-completion
-   `??download`
-   Google whatever in R
-   `?download.file`, or `help(download.file)`, or `download.file` + F1

WARNING: This fails. Why? (Run and read the error message)

``` r
# MISTERY-FUNCTION-GOES-HERE("data")

download.file(
  "https://ndownloader.figshare.com/files/2292169",
  "data/portal_data_joined.csv"
)
#> Warning in download.file("https://ndownloader.figshare.com/files/
#> 2292169", : URL https://ndownloader.figshare.com/files/2292169: cannot open
#> destfile 'data/portal_data_joined.csv', reason 'No such file or directory'
#> Warning in download.file("https://ndownloader.figshare.com/files/
#> 2292169", : download had nonzero exit status
```

> You are now ready to load the data:

``` r
surveys <- read.csv("data/portal_data_joined.csv")
```

> Print the variable's value: `surveys`

``` r
# WARNING: In the console, this prints looooong output
surveys
```

> Let's check the top (the first 6 lines) of this data frame using the function `head()`:

``` r
head(surveys)
#>   record_id month day year plot_id species_id sex hindfoot_length weight
#> 1         1     7  16 1977       2         NL   M              32     NA
#> 2        72     8  19 1977       2         NL   M              31     NA
#> 3       224     9  13 1977       2         NL                  NA     NA
#> 4       266    10  16 1977       2         NL                  NA     NA
#> 5       349    11  12 1977       2         NL                  NA     NA
#> 6       363    11  12 1977       2         NL                  NA     NA
#>     genus  species   taxa plot_type
#> 1 Neotoma albigula Rodent   Control
#> 2 Neotoma albigula Rodent   Control
#> 3 Neotoma albigula Rodent   Control
#> 4 Neotoma albigula Rodent   Control
#> 5 Neotoma albigula Rodent   Control
#> 6 Neotoma albigula Rodent   Control
```

**You just met a data frame. The next section will answer, What are data frames?**

-   Continue [lesson](http://bit.ly/2GQue5W).

Resources
=========

-   Style guide: <http://style.tidyverse.org/>
-   Read data into R
    -   [With only base R](https://goo.gl/99kJEX)
    -   [With **readr**](https://goo.gl/vUJiHX)

------------------------------------------------------------------------

<iframe src="https://todaysmeet.com/room/3261852/embed?type=live&amp;hide_ui=0" height="400" width="100%">
</iframe>
-   [Contact Mauro](https://github.com/maurolepore).
