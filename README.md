Archived: Jan 28 2018

By: Xon-Xoff


## Introduction

### Peer Assessment 1  

**"Reproducible Research"**   

Coursera, Aug 2015  

Date: 15 Aug, 2015   

By: Xon-Xoff     

**Assumptions:**   

1. The data set is at the link location provided, and the zip file contains the **activity.csv** file  

2. The Daylight Savings Time changeover was not taken into consideration when generating the original dataset  

3. In dealing with missing values, for all practical purposes, the replacement by the relevant mean value for the time interval over the two-month period is valid   

3. My audience has a good enough grasp of the **[R language]**(https://www.r-project.org/)  

--------

**Part 1: Loading and preprocessing the data**  

The dataset is downloaded and read-in from the web directly  

Then two variables, a `datetime` class vector and a `times` class vector, are added to allow calculations based on dates and times  

For downloading the dataset, we used the `utils` library functions  

For preprocessing the dataset, we used the `dplyr`, `lubridate`, and `chron` libraries functions  

We prefer the `dplyr` library functions because:  

* the syntax tends to make the code easily readable  

* the functions are reasonably fast  

* it will work with `data.frames` and `data.tables`   

--------

**Part 2: What is mean total number of steps taken per day?**  

As the R code shows, we made use of the `dplyr` syntax to calculate the numbers, and `ggvis` to plot the histogram  

We searched high and low, but we could not retrieve details on how to add a "main" title to a histogram when using `ggvis`  

--------

**Part 3: What is the average daily activity pattern?**  

For this section, we grouped by the intervals to calculate the needed values   

`ggvis` plotted the time-series plot  

--------

**Part 4: Imputing missing values**   

Here, firstly we calculated the number of missing values (NAs), and confirmed that they occur only within the **steps** variable of the dataset  

Once identified, we decided to replace these missing values with the mean values of the corresponding 5-minute intervals over the entire two-month period   

We then created an updated dataset with the imputed values, from which an updated histogram was produced, along with updated mean and median values  

Both the histogram and the updated mean/median values tend to show that the imputed values transformed the distribution to a more normal distribution   

We should note that even if this is the case that the imputed values "normalised" the distribution, we should need yet to validate our decision to use the corresponding mean interval values    

--------

**Part 5: Are there differences in activity patterns between weekdays and weekends?**   

In the last part, we see in the panel plot that there is a difference in activity between weekdays and weekends.  On average, it appears that there is greater activity during the weekends.   


--------

### Summary:

Hopefully all that we have done is reproducible by our audience.

To the best of our knowledge, none of the code detailed in the R markdown file submitted is malicious.  It is readable, and in plain text.
