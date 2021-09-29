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
    ##  1      0.147  Wendy    TRUE        work      
    ##  2      0.280  Kevin    TRUE        home      
    ##  3     -0.0355 Fred     TRUE        mobile    
    ##  4     -1.10   Jeff     FALSE       work      
    ##  5     -0.869  Leslie   TRUE        home      
    ##  6      1.15   Jen      TRUE        mobile    
    ##  7      1.99   Michelle TRUE        work      
    ##  8      1.14   Emily    FALSE       home      
    ##  9      0.179  Jake     TRUE        mobile    
    ## 10      0.374  Sam      TRUE        home

## Pull function - taking the mean

Taking the mean for var = vec\_numeric

``` r
mean(pull (homework1_df, var = vec_numeric))
```

    ## [1] 0.3254653

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
