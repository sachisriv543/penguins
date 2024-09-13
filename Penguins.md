Penguins
================
Sachi Srivastava
2024-09-13

## Data

The Palmer Penguins dataset was made available by Dr. Kristen Gorman and
the Palmer Station, Antarctica LTER (Long Term Ecological Research)
Network. The package includes 2 datasets, one raw, and one modified, to
aid in data visualization. More information is available at this link:
<https://allisonhorst.github.io/palmerpenguins/>

<br>

<figure>
<img
src="https://allisonhorst.github.io/palmerpenguins/reference/figures/lter_penguins.png"
alt="These are the three types of penguins observed at Palmer Station." />
<figcaption aria-hidden="true">These are the three types of penguins
observed at Palmer Station.</figcaption>
</figure>

<br>

Let’s install and load the Palmer Penguins package.

``` r
library(palmerpenguins)
library(tidyverse)
```

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.4     ✔ readr     2.1.5
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.1
    ## ✔ ggplot2   3.5.1     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.3     ✔ tidyr     1.3.1
    ## ✔ purrr     1.0.2     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

``` r
view(penguins)
```

<br>

## Single trait distribution

Now we are ready to visualize the distribution of a single trait. Let’s
look at the density distribution of bill sizes among the three species
surveyed at Palmer Station.

``` r
ggplot(penguins) +
  geom_density(mapping = aes(bill_length_mm, fill = species), alpha = 0.5) + 
    facet_wrap(~species, nrow=3)
```

    ## Warning: Removed 2 rows containing non-finite outside the scale range
    ## (`stat_density()`).

![](Penguins_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

Let’s also see how these traits overlap.

``` r
ggplot(penguins) +
  geom_density(mapping = aes(bill_length_mm, fill = species), alpha = 0.5)
```

    ## Warning: Removed 2 rows containing non-finite outside the scale range
    ## (`stat_density()`).

![](Penguins_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

## Relationship between multiple traits

## Sexual dimorphism
