---
layout: post
title:      "Rails Project - Fantasy Football League"
date:       2019-06-26 22:57:40 -0400
permalink:  rails_project_-_fantasy_football_league
---


The Rails project was a little bit more of a challenge for me than the other projects. During the Rails section, I had to stop and start multiple times due to unforeseen personal circumstances. This presented an obstacle of remembering certain aspects of Rails I hadn’t seen in weeks. 

I decided to stick with my fantasy football theme of previous projects and created an application to track a fantasy football league. Users have the ability to create/edit a team as well as add/remove players from their team. The long-term goal would also give the users the ability to track their players’ stats in real time.

Surprisingly, one of the most difficult aspects of this project for me was a very minor feature of the website – sorting players by their position. I could have saved a lot of time by just sorting alphabetically by player name or position, but that is not aesthetically pleasing. After numerous Google searches and a lot of trial and error, I added the following class method in the Player model, which worked perfectly:

```
def self.sort_position
    preferred_order = ["QB", "RB", "WR", "TE", "K", "DT"]
    self.all.sort_by { |a| preferred_order.index(a[:position]) }
end
```

