---
title: "Statistical Analysis"
description: |
        Result of Iris dataset after performing Statistical Analysis
output:
  html_document:
    css: 
      - styles.css
      - |
        #my-header {
          width: 100%;
          position: fixed;
          top: 0;
    pandoc_args: ["--mathjax"]
    fig_width: 12
    fig_height: 8
    keep_md: true
    number_sections: true
    toc: true
    toc_depth: 2
    toc_float: true
    width: 100%   

---





```r
library(ggplot2)
data(iris)

# Summary statistics for the dataset
summary(iris)
```

```
##   Sepal.Length    Sepal.Width     Petal.Length    Petal.Width   
##  Min.   :4.300   Min.   :2.000   Min.   :1.000   Min.   :0.100  
##  1st Qu.:5.100   1st Qu.:2.800   1st Qu.:1.600   1st Qu.:0.300  
##  Median :5.800   Median :3.000   Median :4.350   Median :1.300  
##  Mean   :5.843   Mean   :3.057   Mean   :3.758   Mean   :1.199  
##  3rd Qu.:6.400   3rd Qu.:3.300   3rd Qu.:5.100   3rd Qu.:1.800  
##  Max.   :7.900   Max.   :4.400   Max.   :6.900   Max.   :2.500  
##        Species  
##  setosa    :50  
##  versicolor:50  
##  virginica :50  
##                 
##                 
## 
```

```r
# Boxplot of the four features by species
boxplot(iris[,1:4], col = iris$Species, main = "Iris Dataset")
```

![](about_files/figure-html/unnamed-chunk-1-1.png)<!-- -->

```r
# Scatterplot of sepal length vs. sepal width, colored by species
plot(iris$Sepal.Length, iris$Sepal.Width, col = iris$Species, main = "Iris Dataset")
```

![](about_files/figure-html/unnamed-chunk-1-2.png)<!-- -->

```r
# Histogram of petal length, colored by species
hist(iris$Petal.Length, col = iris$Species, main = "Iris Dataset")
```

![](about_files/figure-html/unnamed-chunk-1-3.png)<!-- -->

```r
# Correlation matrix of the four features
cor(iris[,1:4])
```

```
##              Sepal.Length Sepal.Width Petal.Length Petal.Width
## Sepal.Length    1.0000000  -0.1175698    0.8717538   0.8179411
## Sepal.Width    -0.1175698   1.0000000   -0.4284401  -0.3661259
## Petal.Length    0.8717538  -0.4284401    1.0000000   0.9628654
## Petal.Width     0.8179411  -0.3661259    0.9628654   1.0000000
```


