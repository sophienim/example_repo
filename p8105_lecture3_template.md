Simple document
================

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
    ## ✔ ggplot2 3.3.5     ✔ purrr   0.3.4
    ## ✔ tibble  3.1.6     ✔ dplyr   1.0.7
    ## ✔ tidyr   1.2.0     ✔ stringr 1.4.0
    ## ✔ readr   2.1.2     ✔ forcats 0.5.1
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

I’m an R Markdown document!

# Section 1

Here’s a **code chunk** that samples from a *normal distribution*:

``` r
samp = rnorm(100)
length(samp)
```

    ## [1] 100

# Section 2

I can take the mean of the sample, too! The mean is 0.05.

# Section 3

### Plot from last time

This is going to make a plot! First I generate a dataframe, then use
`ggplot` to make a scatterplot.

<!--eval=FALSE, message=FALSE, echo=FALSE-->

``` r
plot_df=
  tibble(
    x=rnorm(n=1000),
    y=1+2*x^2+rnorm(n=1000)
  )
ggplot(plot_df,aes(x=x,y=y))+geom_point()
```

![](p8105_lecture3_template_files/figure-gfm/chunk_scatterplot-1.png)<!-- -->

``` r
ggplot(plot_df,aes(x=x))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](p8105_lecture3_template_files/figure-gfm/chunk_histogram-1.png)<!-- -->

### Plot for learning assessment

This is a quick kind of solution to the LA!

``` r
la_df=
  tibble(
    norm=rnorm(n=500,mean=1),
    logical=norm>0,
    abs_norm=abs(norm)
  )
  ggplot(la_df,aes(x=abs_norm))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](p8105_lecture3_template_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

Here’s a list:

-   list item 1
-   list item 2
