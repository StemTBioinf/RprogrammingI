Foundations of R programming I
================
Shamit Soneji
12/10/2018

Why use R?
----------

R is a programming environment with a focus on mathematics and statistics, but can be used for a variety of applications given the flexibility of the language. R is also free and available for all operating systems. Given the richness of the language and no cost to use it, bioinformaticians have adopted R as the platform for which which to develop packages to solve bioinformatics problems.

Getting R
---------

Point your browser to <http://cran.r-project.org/> to download and install the latest version of R. For these tutorials we are also going o use [RStudio](http://www.rstudio.com/) which is an advanced environment for R which includes a window for an editor, console, and plotting window. You will see what this means later.

With respect to bioinformatics, the central repository for bioinformatics tools is [Bioconductor](http://www.bioconductor.org) where packages are deposited for easy installation.

Before we go on to these, we need to get to grips with the basics of the R language first.

R- The basics
-------------

### 1- Vectors

The R language is relatively intuative. For example, making a string of numbers from 1 to 10:

``` r
x <- c(1,2,3,4,5,6,7,8,9,10)
```

The "c" in the code above means "combine", therefore all the comma separated numbers between the parentheses are put together to create a `vector`.

To view the contents of the object you have just created, just type "x" and hit return:

``` r
x
```

    ##  [1]  1  2  3  4  5  6  7  8  9 10

There is a much simpler way to create the same type of object:

``` r
x <- 1:10
x
```

    ##  [1]  1  2  3  4  5  6  7  8  9 10

Much better. Using a comma will always do increments of 1, but is also bidirectional:

``` r
y <- 5:-5
y
```

    ##  [1]  5  4  3  2  1  0 -1 -2 -3 -4 -5

Another way of ceating a sequence of numbers is to use the `seq` function. To learn how this function works, issue the command `help(seq)`. In R you can get a manual for any function using the `help()` command. To generate a vector of numbers from 1 to 100 in steps of 10 we need:

``` r
a <- seq(0,100,by=10)
a
```

    ##  [1]   0  10  20  30  40  50  60  70  80  90 100

***Exercise:*** Generate a vector called 'b' ranging from 3 to 987 where the length of the vector is 53 entries long. Done? Check the length of the vector you have just made by issuing `length(b)`.

Now that we can make vectors we can start playing with them. for example:

``` r
c <- 1:50
d <- 1/c
```

Lets plot the numbers contained in the object we called `d`:

``` r
plot(d)
```

![](index_files/figure-markdown_github/unnamed-chunk-7-1.png) Note the way the axes are labelled in the plot function.

***Exercise:*** Call `help(plot)` and read about the other options available. Produce the same plot as above, but this time as a line plot which is coloured red. Also, label the axes and give the plot a title.

We can also do basic calculations on vectors:

``` r
mean(d) # calculate the mean of the vector
```

    ## [1] 0.08998411

``` r
sd(d) # the standard deviation
```

    ## [1] 0.1578087
