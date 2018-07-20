
# Introduction

Oh no, yesterday I backed another Kickstarter [campaign](https://www.kickstarter.com/projects/eaglegryphon/escape-plan-by-vital-lacerda-with-artwork-by-ian-o?ref=nav_search&result=project&term=escape%20plan). The game looks fantastic, and is coming from [Vital Lacerda](http://www.vitallacerda.com/), one of my favourite designers, how am I supposed to resist to that?

[Kickstarter](https://www.kickstarter.com/), aka KS, is the most popular crowfunding platform on the planet and it has changed completely some industries, specifically, **Tabletop Gaming**. 

The steps to start a Kickstarter project are: start a campaign, set the minimum funding goal, set reward levels and choose a deadline. The most important aspect to know about launching a Kickstarter project is that if the project falls short of meeting its minimum funding goal, the project will not receive any fund and turn out failed.

For the purpose of this project, we are going to use four datasets coming from different sources:

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

After reviewing the data, I determined to create 7 Explores in my model:

- **kickstarter** 

   All the data from KS, including every category.

- **bgg** 

   BGG-only game info.

- **collection** 

   Explore all the games from my collection.

- **boardgames_all** 

   The three tables above joined together by `name`.

- **kickstarter_boardgames** 

   Kickstarter explore with the followin sql_always_where clause:

   ```sql_always_where: ${category} IN ("Tabletop Games") and ${state} IN ("successful","failed") and ${launched_month} NOT IN   ("2018-01","2017-12");;```

  Filtering from the results all categories but Tabletop Games, removing `suspended`,`canceled` and `live` status (not very 
  trustworthy and a minority) and the last month in the dataset, as it wasn't complete (we will be focusing on months in our
  date fields).

- **kickstarter_prediction** 

  Same than `kickstarter_boardgames` but joined with `mr_dates` for a prediction analysis purpose.

- **kickstarter_facts** 

  Derived table (no persistance added) with some interesting info.

A data warehouse plan is accessible from [here](https://docs.google.com/document/d/1ruow7fZZsb8bLO0r0rU3tGHZlfpi5vxq4wo4PIE-ikc/edit?usp=sharing) with all the fields and some explanations.

---

Move to [Kickstarter page](https://diegocamlooker.github.io/Kickstarter/ks)


