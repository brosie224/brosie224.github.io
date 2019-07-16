---
layout: post
title:      "Rails and JavaScript Project - Fantasy Football League"
date:       2019-07-16 20:16:57 +0000
permalink:  rails_and_javascript_project_-_fantasy_football_league
---


For my JavaScript project, I continued with the app I created with Rails, Fantasy Football League.

Four main features were added via JavaScript: 

1. New Team form submission 
2. 'Previous' and 'Next' options for each Player page
3. Option to view a player or team on the Players page
4. A new Users page

The most difficult of these was definitely the 'previous' and 'next' buttons. At first, it seemed relatively straightforward, but I quickly realized a big issue. I had originally built it by passing in the current player's ID into "data-id" then adding a +1 or -1 to go to the next player or previous player, respectively. The issue with this is it only works if ALL of your player IDs are sequential. For example, if the player assigned to ID "3" has been deleted, when the user click 'next' from Player 2's page, it will break since there is no ID of 3.

In order to fix this, I built the following two methods in my Player model:

```
    def previous
        player = Player.where("id < ?", self.id).last

        player ? player : Player.last
    end

    def next
        player = Player.where("id > ?", self.id).first

        player ? player : Player.first
    end
```

Calling these methods on a player instance will render the player whose ID is immediately before/after the instance in the existing dataset. Additionaly, the last line in each method will allow the user to go back to the beginning when clicking 'next' on the last player or to the end when clicking 'previous' on the first player.
