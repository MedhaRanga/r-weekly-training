
<!-- Please edit README.Rmd - not README.md -->

# Week 02: Introduction to R

Welcome to the DfE R Community’s weekly R training! This programme
should get you up-to-speed with the basics of R, ready to use it
effectively in your day-to-day work and continue to independently
develop your R skills moving forward.

# Prerequisites

- **R and RStudio**: If you don’t have these installed already, you can
  find out how to get them set up by referring to week 00.
- **Git and GitHub**: You’ll need to know how to use these to submit
  solutions. Read exercises 3-10 of [Week
  1](../week-01-version-control#03-check-the-state-of-the-repo) for a
  recap of how to do this.
- **Reading**: Read through chapters 1 - 5 of [R for Data
  Science](https://r4ds.had.co.nz/introduction.html) and try the
  examples as you go along - this will require you to install some
  packages too. (Note: It’s worth bookmarking R4DS as it will be one of
  the main resources we use in this training :))

# Exercises

1.  Create a new R script and name it after your AD username (the same
    one you use to log in on your laptop)

2.  Load the packages `dplyr`, `tidyr` and `ggplot2` at the top of your
    script

3.  Run `mtcars` in the console and look at the output. You’ll see the
    first column doesn’t have a header - this is because it gives *row
    names* for the dataset. Create a new version of the dataset,
    `mtcars2`, which gives the car names in a new column named `car`.
    This should be a `tibble`.

    ``` r
    # The mtcars dataset:
    head(mtcars, 10)
    #>                     mpg cyl  disp  hp drat    wt  qsec vs am gear carb
    #>  Mazda RX4         21.0   6 160.0 110 3.90 2.620 16.46  0  1    4    4
    #>  Mazda RX4 Wag     21.0   6 160.0 110 3.90 2.875 17.02  0  1    4    4
    #>  Datsun 710        22.8   4 108.0  93 3.85 2.320 18.61  1  1    4    1
    #>  Hornet 4 Drive    21.4   6 258.0 110 3.08 3.215 19.44  1  0    3    1
    #>  Hornet Sportabout 18.7   8 360.0 175 3.15 3.440 17.02  0  0    3    2
    #>  Valiant           18.1   6 225.0 105 2.76 3.460 20.22  1  0    3    1
    #>  Duster 360        14.3   8 360.0 245 3.21 3.570 15.84  0  0    3    4
    #>  Merc 240D         24.4   4 146.7  62 3.69 3.190 20.00  1  0    4    2
    #>  Merc 230          22.8   4 140.8  95 3.92 3.150 22.90  1  0    4    2
    #>  Merc 280          19.2   6 167.6 123 3.92 3.440 18.30  1  0    4    4
    ```

4.  1)  Add a new column which gives `TRUE`/`FALSE` depending on whether
        a car does more then 20 miles/gallon
    2)  Use `group_by()` and `summarise()` to create a new dataset
        giving the average miles/gallon for each combination of `cyl`
        and `gear`
    3)  `summarise()` is a function from `dplyr` which can be used to
        combine rows in a dataset. Run `?summarise` in the console to
        view the function’s documentation, and read through to discover
        what the `.groups` argument does. Using this information, review
        your answer to part b) and ensure the output is not ‘grouped’.
    4)  Bonus: Do the same, but include each *make* of car in the
        output. (Hint: look at the examples in the documentation for
        `tidyr`’s `separate()` function).

5.  1)  Create a scatter-plot of miles/gallon against weight (R4DS
        chapter 3, section 3 may be helpful here)
    2)  Colour the points to indicate the number of cylinders
    3)  Give the points a different shape if the car does more than 20
        miles/gallon
    4)  Give your plot a descriptive title and optional subtitle
        describing a key finding
    5)  Bonus: Fit a smooth line between the different points. (Hint:
        type `geom_` in the console and see what the autocomplete
        options are).

6.  Make sure your script is nicely commented. You might also want to
    try dividing it into [different
    sections](https://support.rstudio.com/hc/en-us/articles/200484568-Code-Folding-and-Sections-in-the-RStudio-IDE)

7.  Submit your solutions by making a pull request on GitHub. If someone
    has agreed to review your solutions, add them as a required reviewer
    and GitHub will send them an email asking them to check your code.

Good luck!
