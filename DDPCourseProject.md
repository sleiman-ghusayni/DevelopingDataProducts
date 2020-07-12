Developing Data Products - Week 4 Course Project
========================================================
author: Sleiman Ghusayni
date: July 12, 2020
autosize: true
width: 1600
height: 900

Introduction
========================================================
This project is the  final course project for Developing Data products course.

-  UI and server part of Shiny included in this project
- Documentation is created using Rstudio presenter

Analysis of Miles per Gallon for various cars
mtcars data set used for analysis

Documentation
========================================================
mtcars dataset information 


```r
summary(mtcars)
```

```
      mpg             cyl             disp             hp       
 Min.   :10.40   Min.   :4.000   Min.   : 71.1   Min.   : 52.0  
 1st Qu.:15.43   1st Qu.:4.000   1st Qu.:120.8   1st Qu.: 96.5  
 Median :19.20   Median :6.000   Median :196.3   Median :123.0  
 Mean   :20.09   Mean   :6.188   Mean   :230.7   Mean   :146.7  
 3rd Qu.:22.80   3rd Qu.:8.000   3rd Qu.:326.0   3rd Qu.:180.0  
 Max.   :33.90   Max.   :8.000   Max.   :472.0   Max.   :335.0  
      drat             wt             qsec             vs        
 Min.   :2.760   Min.   :1.513   Min.   :14.50   Min.   :0.0000  
 1st Qu.:3.080   1st Qu.:2.581   1st Qu.:16.89   1st Qu.:0.0000  
 Median :3.695   Median :3.325   Median :17.71   Median :0.0000  
 Mean   :3.597   Mean   :3.217   Mean   :17.85   Mean   :0.4375  
 3rd Qu.:3.920   3rd Qu.:3.610   3rd Qu.:18.90   3rd Qu.:1.0000  
 Max.   :4.930   Max.   :5.424   Max.   :22.90   Max.   :1.0000  
       am              gear            carb      
 Min.   :0.0000   Min.   :3.000   Min.   :1.000  
 1st Qu.:0.0000   1st Qu.:3.000   1st Qu.:2.000  
 Median :0.0000   Median :4.000   Median :2.000  
 Mean   :0.4062   Mean   :3.688   Mean   :2.812  
 3rd Qu.:1.0000   3rd Qu.:4.000   3rd Qu.:4.000  
 Max.   :1.0000   Max.   :5.000   Max.   :8.000  
```

Summary plot of the mtcars data 
========================================================

```r
library(ggplot2)
data("mtcars")
qplot(mtcars$hp, mtcars$mpg, color = mtcars$cyl,geom =c("point","smooth"),method = "lm", data = mtcars)
```

![plot of chunk unnamed-chunk-1](DDPCourseProject-figure/unnamed-chunk-1-1.png)

Links
========================================================
Instruction for shiny app
- Use the check box to select model type 1 or 2 or both
- Use the slider to select mpg of car
- Press Submit button to see predicted Horsepower from either or both Models.

- shiny app: https://sleiman-ghusayni.shinyapps.io/developingdataproducts/
- source code: https://github.com/leiman-ghusayni/
