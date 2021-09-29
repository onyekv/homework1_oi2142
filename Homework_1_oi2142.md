oi2142\_Homework1
================

## Attaching packages

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.1 ──

    ## ✓ ggplot2 3.3.5     ✓ purrr   0.3.4
    ## ✓ tibble  3.1.4     ✓ dplyr   1.0.7
    ## ✓ tidyr   1.1.3     ✓ stringr 1.4.0
    ## ✓ readr   2.0.1     ✓ forcats 0.5.1

    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

## Problem 1:

Creating a data frame using Tibble

    ## # A tibble: 10 × 4
    ##    vec_numeric vec_char vec_logical vec_factor
    ##          <dbl> <chr>    <chr>       <fct>     
    ##  1       0.331 Wendy    TRUE        work      
    ##  2      -0.560 Kevin    TRUE        home      
    ##  3       0.680 Fred     TRUE        mobile    
    ##  4       0.246 Jeff     FALSE       work      
    ##  5      -0.708 Leslie   TRUE        home      
    ##  6      -0.165 Jen      TRUE        mobile    
    ##  7       1.39  Michelle TRUE        work      
    ##  8       0.345 Emily    FALSE       home      
    ##  9      -0.667 Jake     TRUE        mobile    
    ## 10       1.24  Sam      TRUE        home

## Taking the mean using the pull function

``` r
mean(pull (homework1_df, var = vec_numeric))
```

    ## [1] 0.2127609

``` r
mean(pull(homework1_df, var = vec_char))
```

    ## Warning in mean.default(pull(homework1_df, var = vec_char)): argument is not
    ## numeric or logical: returning NA

    ## [1] NA

``` r
mean(pull(homework1_df, var = vec_logical))
```

    ## Warning in mean.default(pull(homework1_df, var = vec_logical)): argument is not
    ## numeric or logical: returning NA

    ## [1] NA

``` r
mean(pull(homework1_df, var = vec_factor))
```

    ## Warning in mean.default(pull(homework1_df, var = vec_factor)): argument is not
    ## numeric or logical: returning NA

    ## [1] NA

## 

Taking the mean for the numeric variable in the data fram worked, but
taking the mean for the logical, character, and factor did not work.

# Using the as.numeric function to convert variable

I believe that the as.numeric function worked for vec\_factor because
this variable has a has 3 different “levels”. The numbers assigned are
now coded as 1,2, or 3.

When trying to convert vec\_char and vec\_logistical, I get a warning
message that says “NAs introduced by coercion”. \#

``` r
x <- as.numeric(pull(homework1_df, vec_factor))
mean(x)

y <- as.numeric(pull(homework1_df, vec_char))
mean(y)

z <- as.numeric(pull(homework1_df, vec_logical))
mean(z)
```

# Problem 2

The dataset ‘penguins’ has 344 observations and 8 variables. Using ncol
= 8 and nrow = 344. The variables include:

(3)Species: Adele, Chinstrap, Gentoo

(3)Islands: Biscoe, Dream, Torgersen

Bill length- mm

Bill depth - mm

Flipper length - mm

body mass - g

Sex - M/F

year - 2007 -2009

The mean flipper length is 201 mm.

``` r
data("penguins", package = "palmerpenguins")
```

## 

Plots

    ## Warning: Removed 2 rows containing missing values (geom_point).

![](Homework_1_oi2142_files/figure-gfm/Scatterplot-1.png)<!-- -->
