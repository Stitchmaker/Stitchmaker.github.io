--- 
layout: post 
title: Metis Bootcamp first project 
--- 

My cohort just finished our first week at Metis Bootcamp in Seattle.  We come from various backgrounds, all wanting to learn more about data science.  Excited to be working with this great group of people.

Our first project was done in teams of four.  What a great way to get to know each other.  As with most teams, we each brought different strengths to the project.  It was fast paced work but very rewarding.

Let’s now move into the imaginary world of a data science team from the company Toucan Analysis, Inc. which has been presented a problem to solve by the New York organization, WomenTechWomenYes.
 

```
It was great to meet with you and chat at the event where we 
recently met and had a nice chat. We’d love to take some next 
steps to see if working together is something that would make 
sense for both parties.   

As we mentioned, we are interested in harnessing the power of 
data and analytics to optimize the effectiveness of our street 
team work, which is a significant portion of our fundraising 
efforts.   

WomenTechWomenYes (WTWY) has an annual gala at the beginning 
of the summer each year. As we are new and inclusive  
organization, we try to do double duty with the gala both to 
fill our event space with individuals passionate about 
increasing the participation of women in technology, and to 
concurrently build awareness and reach.   

To this end we place street teams at entrances to subway 
stations. The street teams collect email addresses and those 
who sign up are sent free tickets to our gala.   

Where we’d like to solicit your engagement is to use MTA subway 
data, which as I’m sure you know is available freely from the 
city, to help us optimize the placement of our street teams, 
such that we can gather the most signatures, ideally from those 
who will attend the gala and contribute to our cause.   

The ball is in your court now—do you think this is something 
that would be feasible for your group? From there we can 
explore what kind of an engagement would make sense for all 
of us.   

Best,

Karrine and Dahlia

WTWY International
```

## Optimization of MTA Stations to Target WomenTechWomenYes Gala

Karrine & Dahlia, thank you for allowing Toucan Analysis, Inc. to assist WTWY with their yearly gala.  We believe the analysis we have done will assist you in placing your volunteer teams at the best MTA stations in New York City to reach the right people for your gala.   

Let’s start by summarizing the problem and the goal.   

Problem:   
* WomenTechWomenYes has an annual gala held each year at the beginning of summer
* WTWY would like to fill the event with individuals passionate about increasing the participation of women in technology AND to build awareness and reach.
* WTWY will place street teams at entrances to subway stations to collect names of individuals who will receive free tickets to the gala.

The Goal:   Optimize the placement of teams so as to   
* Reach the desired people outlined above   
* Utilize limited volunteer resources most effectively   

### Toucan Analysis' Solution

To solve your problem we will be using several sets of data   
1. The MTA provides turnstile data for each of their stations in New York City.  We can harness this data to understand the patterns of people you want to reach at the stations.   
2. The Grace Hopper Convention has a similar mission to WYTY.  To this end, we will focus on people working at the companies who are strong supporters of the Grace Hopper Convention.  
3. Geographic locations of both the MTA stations and these companies.   

### Methodology:  

1. Determine the locations of the companies supporting the Grace Hopper Convention in NYC.  On the map below we see that all of these companies are in lower Manhattan so we will focus our analysis on this part of New York City.  We will catch people as they commute to and from these companies.   

![an image alt text]({{ site.baseurl }}/images/image13.png "an image title")

2. Determine the locations of the MTA Stations in NYC.  As you can see on the map below the subway stations have been superimposed on a map with the companies.  We continue the analysis to determine the stations on which WTWY should focus.   

![an image alt text]({{ site.baseurl }}/images/image4.png "an image title")

3. We turned our focus to the stations near the companies with people we wish to target.  We will catch them as the enter or leave the MTA stations so focus on stations within ½ mile (approximately a 10 minute walk) from the companies.  On the map below you can see this more limited set of stations.  To help in our analysis, the red dots were scaled so the stations with the higher volumes have larger dots.   

![an image alt text]({{ site.baseurl }}/images/image1.png "an image title")

4.  This data helped to show us which stations on which to focus but we did some more analysis to provide a concise list of stations for you to focus on.  

We gave each station a score.   

Score = (volume at the station) * (sum of companies within ½ mile of that station)   

This gave us a final list of 6 stations to target represented by red stars on the map.  The larger the star, the higher our suggestion that you target this station.   

![an image alt text]({{ site.baseurl }}/images/image10_copy.png "an image title")

1.  34th Street - Herald Square
2.  42nd Street - Times Square
3.  42nd Street - Bryant Park
4.  34th Street - Penn Station
5.  47-50th Streets - Rockefeller
6.  14th Street - Union Square

The first station is obvious, Harold Square has a lot of volume and is surrounded by our target companies.  But Bryant Square is not so obvious.  It ranked third on our list even though it has only ⅓ the volume of Harold Square.  What makes this a good station to target is it has twice as many target companies within ½ mile as any other station.  This is in the middle of the tech companies you want to target.  Union Square is the most southern of our stations.  It has almost as big a volume as Harold Square but due to the lack of companies in the area it is the last station on our list.   

### When Should You Target The Stations

Next we looked at the best time to target these six stations.  We analyzed the turnstile data looking at the entries and exits to the station in the Morning, Noon and Evening times.  Here is an example for the Harold Square Station.   

![an image alt text]({{ site.baseurl }}/images/image9.png "an image title")

The darker the cell the higher the volume of traffic.  From the above chart we see that Tuesday, Wednesday and Thursday in the evening is the best time to target Harold Square as people commute home.   

Based on similar analysis for all six of the identified stations we recommend the following schedule for your volunteers to target the stations.  This results in 18 shifts total, a significant decrease from the number of stations you targeted last year.  We believe that with these 18 shifts you will hit a high volume of the type of people you want to attract to your WTWY gala.   

![an image alt text]({{ site.baseurl }}/images/image11.png "an image title")

### Future Work   

If you find this analysis to be useful we would like to work with you further to refine the model and increase the effectiveness of your volunteers and improve the target audience for your gala.   
 
Some improvements to the algorithm which we recommend are   
1. Account for the size of the targeted companies.  In particular it would be useful to know how many women worked in tech in these companies.  This information would be used to add a company size weight to the analysis similar to how the station traffic was accounted for in the model.
2. Expand the list of companies in the study.   By increasing the list of companies you wish to target our analysis will focus on the people you wish to attract to WTWY and your gala.

### Appendix

Grace Hopper Convention Diamond Supporters with offices in NYC.   
Accenture   
Thoughtworks   
Amazon   
Bank of America   
Facebook   
HP   
Microsoft   
Two Sigma   
Workday   
Capital One   
Ebay   
Google   
PWC   

Station Traffic for each of the 6 identified stations

![an image alt text]({{ site.baseurl }}/images/image5.png "an image title")
![an image alt text]({{ site.baseurl }}/images/image6.png "an image title")
![an image alt text]({{ site.baseurl }}/images/image3.png "an image title")
![an image alt text]({{ site.baseurl }}/images/image8.png "an image title")
![an image alt text]({{ site.baseurl }}/images/image2.png "an image title")
![an image alt text]({{ site.baseurl }}/images/image7.png "an image title")

