
## Final thoughts


With this analysis powered by Looker, we had been able to figure out how sucessful TableTop gaming is in Kickstarter, the biggest crownfunding platform in the world. We also have wondered how sustainable is this in the future, and how that will impact the average gamer habits. Also, we tried to find out what makes a project succesful by taking a look on goal, overfunding, campaign days, etc. and discovered how more games, doesn't mean more quality, and also, more success doesn't mean a better game. 

With this read a game data analyst might have more tools to create a better campaign.

---

## Future work

* Choose a classification technique (k-NNs, SVC, Random Forest, etc) and create a real prediction model. 

* Create a website based on it that can determine if the project you have in your head would be succesful or not with a given % accuracy.

* SSO embed in GitHub Pages project.

* Javascript events with dynamic frames:

```
<p align="center">
<iframe
  id="looker"
   src="https://dcl.dev.looker.com/embed/looks/871?embed_domain=https://diegocamlooker.github.io/Kickstarter/"
  width="400"
  height="250"
   frameborder='0'>
  {
  "type": "look:filters:update",
  "filters": {
    "kickstarter.state": "failed",
  }
}
</iframe></p>
```

* Ammend the `Kickstarter` dataset with a new column containing the `bgg name` field related to that specific `project name`, in order to not to miss data when joining both tables in the ``explore{}``.

* Having more info to play with: number of pledges, backers country, number of updates in the campaign, comments in the page, video yes/no, etc...

> Tip 8: Stop buying more games, and play them!

---

## Interesting (or not) Facts

* The **longest campaign** ran for 91 days and was for 'Heroic Chess' A legendary new board game!"

* There have been 87 titles with **0$USD funding**. Among the names:"The Family Soup Bowl","You Ate My Pie!" and "SlenderMan: Board of Horrors" (!).

* The **most overfunded game** is [something](https://www.kickstarter.com/projects/1456271622/band-of-brothers-2nd-chance-0) that I haven't heard about. Ah OK, it had a $1 funding goal :/.

* The **most backed game** has been [Exploding Kittens](https://www.kickstarter.com/projects/elanlee/exploding-kittens) with nearly 220,000. The second is Bears vs Babies - A Card Game, and yeah it is from the same guys.

* The **most succesful board game project** ever in Kickstarter is the reprint [Kingdom Death Monster](https://www.kickstarter.com/projects/poots/kingdom-death-monster-15) with more than 12 millions dollars. People have to wait until late 2020 to get the game, 4 years after the campaign!

