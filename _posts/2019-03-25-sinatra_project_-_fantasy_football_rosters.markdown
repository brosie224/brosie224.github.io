---
layout: post
title:      "Sinatra Project - Fantasy Football Rosters"
date:       2019-03-25 21:32:40 +0000
permalink:  sinatra_project_-_fantasy_football_rosters
---


Continuing with my football-themed projects, I decided to build a fantasy football roster tracker for my Sinatra project. 

Many people who play fantasy football have multiple teams across multiple leagues. This can get difficult to track. The idea for this app (for now) is to be able to track all of your players in one location. I say “for now” because the plan is for it to have many more functions down the road, such as tracking stats, news, etc.

For this app, I created three models: User, Team, and Player. The User model was used for login information, such as email and password, while the Team and Player models were used to store various attributes for each. The one unique thing about the Team modeal was that it “belongs_to” user and “has_many” players. This was the first time I was using both relationships for one class, and I wasn’t even 100% sure it would work… but it did!

Some of the functions for this app include creating teams, creating players, assigning players to teams, viewing teams or players created by all users, as well as editing/deleting teams and players that only you created.

Thinking down the road…

When users create a player, they are required to enter that player’s ESPN ID. For now, this is only used to link to that player’s ESPN page. Eventually, this ID can be used to populate things mentioned previously, such as stats and news. 

