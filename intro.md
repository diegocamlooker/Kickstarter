
# Introduction and Preliminary Analysis

Oh no, yesterday I backed another Kickstarter [campaign](https://www.kickstarter.com/projects/eaglegryphon/escape-plan-by-vital-lacerda-with-artwork-by-ian-o?ref=nav_search&result=project&term=escape%20plan). The game looks fantastic, and is coming from [Vital Lacerda](http://www.vitallacerda.com/), one of my favourite designers, how am I supposed to resist to that?

[Kickstarter](https://www.kickstarter.com/), aka KS, is the most popular crowfunding platform on the planet and it has changed completely some industries, specifically, **Tabletop Gaming**. 

The steps to start a Kickstarter project are: start a campaign, set the minimum funding goal, set reward levels and choose a deadline. The most important aspect to know about launching a Kickstarter project is that if the project falls short of meeting its minimum funding goal, the project will not receive any fund and turn out failed.

For the purpose of this project, we are going to use three datasets coming from different sources:

- **ks-projects-201801**
  
  This table contains all the details from every project in the platform since 2009.
  
  ```SELECT COUNT(*) FROM `lookerdata.diegocam_thesis.kickstarter``` : 378661
  
  Source: [Kaggle](https://www.kaggle.com/kemical/kickstarter-projects).

- **bgg**

  It has all the information in BoardGameGeek, aka BGG, from every game in the Top 5000.
  
  Source: BGG using [this](https://boardgamegeek.com/wiki/page/BGG_XML_API2) XML API.

- **collection**
  
  Everything I have at home but in csv form. Information about my owned games ~ 155.

  Source: BGG (direct Download).

- **mr_dates**
  
  Future dates to feed Explores in order to do some estimations.
  
  Source: Manually.

# Preliminary Analysis
