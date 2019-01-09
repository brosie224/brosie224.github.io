---
layout: post
title:      "CLI Project - NFL Player News"
date:       2019-01-09 05:43:38 +0000
permalink:  cli_project_-_nfl_player_news
---


When I have a choice of topic for a project, I will almost always choose something I'm passionate about. After all, I decided to pursue a career in programming because it became a passion of mine. As a huge sports fan, especially NFL, I decided to create a Ruby Gem which provides a command line interface to view recent NFL player news, per Rotoworld.com.

I have experience creating programs with Visual Basic for Applications, so I am somewhat used to visualizing how I want my code to operate. However, this is the first time I am writing a program from scratch with Ruby. After reading and watching the provided materials, I got started. This project had its obvious benefits, such as helping me improve my programming skills, but one of the greatest benefits was utilizing the git commads, which I had no previous experience doing.

The greatest challenge for me while programming was iterating over an array to iterate over multiple hashes, but only displaying values with specific keys... and all on the same line (not beneath each other):

```
@players.each.with_index(1) do |player, i|
	player.each do |key, value|
		puts "#{i}. #{value} - #{player[:team]}" if key == :name
	end
end
```

I am not certain the technique I used is the most efficient, but it only uses a few lines and works well, so I am happy with it.
