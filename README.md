# Geospatial-Analysis-of-Sentiment

## Table of Contents
- [Compiled Yelp Review Data for Chicago](https://github.com/alabellehahn/Geospatial-Analysis-of-Sentiment/blob/main/review_data_Chicago.csv)
- [Compiled Yelp Review Data for DC](https://github.com/alabellehahn/Geospatial-Analysis-of-Sentiment/blob/main/review_data_DC.csv)
- [Compiled Yelp Review Data for Los Angeles](https://github.com/alabellehahn/Geospatial-Analysis-of-Sentiment/blob/main/review_data_Los_Angeles.csv)
- [Data Wrangling and Regression Code for Chicago](https://github.com/alabellehahn/Geospatial-Analysis-of-Sentiment/blob/main/Data%20Wrangling%20Chicago.Rmd)
- [Geospatial data for regression analysis](https://github.com/alabellehahn/Geospatial-Analysis-of-Sentiment/blob/main/CHICAGO_wide_FIXED.gpkg)
- [Data for Colocation Analysis](https://github.com/alabellehahn/Geospatial-Analysis-of-Sentiment/blob/main/Coloc_DATA.csv)

## Purpose of this repository
This repository contains the R code and data required to reproduce the findings in my Masters Thesis "The Impact of Pandemic-Induced Anti-Asian Sentiment on Asian Restaurants: Analyzing User Engagement with Yelp Reviews." The report utilized data specific to Chicago area restaurants, but web scraping was performed for both DC and Los Angeles as well. Please refer to a separate repository entitled [Yelp Restaurant Data Collection in Python](https://github.com/alabellehahn/Yelp-Restaurant-Data-Collection-in-Python) for the code used to retrieve data. Users are free to tweak the code and perform the same geospatial analyses for these cities as well. 

## Required Libraries
- library(sf)
- library(tidyverse)
- library(tmap)
- library(leaflet)
- library(data.table)
- library(raster) 
- library(adehabitatHR)
- library(tidycensus)
- library(RColorBrewer)
- library(dplyr)
- library(corrr)
- library(spdep)
- library(rgdal)
- library(car)
- library(spatialreg)
- library(stargazer)

## Steps used to tidy the data

1) Removed rows with superfluous/non-user text as well as unnecessary columns
2) Created averages of polarity and subjectivity scores for each restaurant and standardized measurement
3) Added geometry to the resulting dataframe 
4) Retrieved and wrangled demographic data from the American Community Survey
5) Combined demographic data, vaccine data, and review data 
6) Checked for correlations between the variables
7) Created a spatial weights matrix
8) Set up various regression models, ran through them for each dependent variable, and exported tables 
