--- 
layout: post 
title: Predicting High School Track Results
date:  2018-10-12 10:00:00
--- 

This was the second project of my Metis Bootcamp.  The goal of the project was to scrape data from the web and 
use linear regression to analyze the data.  As with all Metis projects, this was very open ended.

I remembered that the web site www.athletic.net contained a wealth of track and field data so decided to make this 
the source for this project.  Although the site has data from across the US, I chose to focus on my home state of 
Washington and the 400 meter and 1600 meter events for their popularity (and larger data set).  I wanted data on 
athletes for all four years in high school which the web site had available from 2006 to 2018.

From the lists of top athletes for each athletic district in Washington I was able to get IDs on athletes that 
then led me to the page with their individual statistics.  From these indivudual pages I was able to scrape thir
personal records (PR) for each year.  If they had not competed for four years I then removed them from the dataset.

In the end I had 
