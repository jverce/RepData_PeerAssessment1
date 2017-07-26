# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data


```r
unzip("activity.zip")
data <- read.csv("activity.csv", header=T, sep=",")
data$date <- as.Date(data$date)
```


## What is mean total number of steps taken per day?

First let's look at the steps per date data through an histogram.

```r
steps.per.date <- with(data, tapply(steps, date, sum, na.rm=T))
hist(
    steps.per.date,
    xlab="Steps per Date", ylab="Count",
    main="Steps per Date Histogram",
    col="blue"
)
```

![](PA1_template_files/figure-html/unnamed-chunk-2-1.png)<!-- -->

As per the mean and median, we have the following:

```r
mean(steps.per.date)
```

```
## [1] 9354.23
```

```r
median(steps.per.date)
```

```
## [1] 10395
```

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
