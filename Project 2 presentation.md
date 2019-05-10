
Project 2 presentation
===
author: Joseph Audras & Devin Romines
date: May 13, 2019
autosize: true


Introduction
===

## Description
[summarize]
The Google Play Store Data Set is a data set containing data on over 10,000 apps in the Google Play Store for Android products. The data set looks at things such as rating, number of installations, and genre to produce a plethora of information on each app. For this project, we would like to see if the rating of the app can be accurately predicted by the variables provided in the data set.

[summarize]
The data set was gathered from https://www.kaggle.com/lava18/google-play-store-apps which was last updated 2 months ago, giving us Version 6, with which we are working.  The data was posted by Lavanya Gupta, a software engineer at HSBC Software Development in India.  More information on her can be found here https://www.kaggle.com/lava18.  The information in the data set was scraped from the Google Play Store by Lavanya Gupta, in an effort to provide similar information on its apps as is publically available from the Apple App Store so that developers may be more inclined to work in the Android market.




Data Dictionary
===

* App - The name of the app.
* Category: Factor - The general type of app, such as Dating, Cooking, or Art and Design
* Rating: Numerical - The rating of the app on a scale from 0-5.
* Reviews: Numerical - The number of reviews that the app received.
* Installs: Numerical - The number of installations an app received.
* Price: Numerical - The Price of the app.
* Content.Rating: Factor - The rating for the app, Everyone, Everyone 10+, Mature 17+, and Teen.
* Genres: Factor - The genre of the app, Action, Action and Adventure, etc.
* Last.Updated: Factor - The date on which the app was last updated


Data Cleaning
===



Because we intend on making a predictive model, here we split the data into a testing and training data set.



Exploratory Data Analysis
===


To begin the exploratory data analysis, let's look at the data set as a whole.


```
                                                App      
 CBS Sports App - Scores, News, Stats & Watch Live:   6  
 Nick                                             :   6  
 ROBLOX                                           :   5  
 Subway Surfers                                   :   5  
 8 Ball Pool                                      :   4  
 AliExpress - Smarter Shopping, Better Living     :   4  
 (Other)                                          :5590  
            Category        Rating         Reviews        
 FAMILY         :1062   Min.   :1.000   Min.   :       1  
 GAME           : 638   1st Qu.:4.000   1st Qu.:     192  
 TOOLS          : 440   Median :4.300   Median :    6078  
 MEDICAL        : 215   Mean   :4.191   Mean   :  471539  
 PERSONALIZATION: 208   3rd Qu.:4.500   3rd Qu.:   80327  
 PRODUCTIVITY   : 206   Max.   :5.000   Max.   :66509917  
 (Other)        :2851                                     
                 Size        Type          Price        
 Varies with device: 965   0   :   0   Min.   :  0.000  
 14M               : 107   Free:5242   1st Qu.:  0.000  
 15M               : 101   NaN :   0   Median :  0.000  
 13M               :  99   Paid: 378   Mean   :  1.084  
 11M               :  93               3rd Qu.:  0.000  
 12M               :  89               Max.   :400.000  
 (Other)           :4166                                
         Content.Rating             Genres                 Android.Ver  
                :   0   Tools          : 440   4.1 and up        :1197  
 Adults only 18+:   2   Entertainment  : 325   Varies with device: 775  
 Everyone       :4490   Education      : 293   4.0.3 and up      : 756  
 Everyone 10+   : 225   Medical        : 215   4.0 and up        : 709  
 Mature 17+     : 254   Action         : 211   4.4 and up        : 532  
 Teen           : 648   Personalization: 208   2.3 and up        : 342  
 Unrated        :   1   (Other)        :3928   (Other)           :1309  
```

![plot of chunk unnamed-chunk-4](Project 2 presentation-figure/unnamed-chunk-4-1.png)


Exploratory Data Analysis part 2
===

Now, let's look at the individual variables.








```
Warning message:
package 'knitr' was built under R version 3.5.3 


processing file: Project 2 presentation.Rpres
-- Attaching packages -------------------------------------------- tidyverse 1.2.1 --
v ggplot2 3.1.1       v purrr   0.3.2  
v tibble  2.1.1       v dplyr   0.8.0.1
v tidyr   0.8.3       v stringr 1.4.0  
v readr   1.3.1       v forcats 0.4.0  
-- Conflicts ----------------------------------------------- tidyverse_conflicts() --
x dplyr::filter() masks stats::filter()
x dplyr::lag()    masks stats::lag()

Attaching package: 'lubridate'

The following object is masked from 'package:base':

    date
```
