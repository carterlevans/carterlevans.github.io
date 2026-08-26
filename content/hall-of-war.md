+++
title = "The Hall of WAR"
description = "While WAR and Sabermetrics have revolutionized baseball, I beat a dead horse and argue that my favorite players should be ranked higher"
draft = true 
+++

Labelling this as a post about the Hall of Fame does it a bit of a diservice. Broadly, there are players that the game overrate and underrate because of how the media frames statistics. I think many of them are properly rated inside the game and by the better front offices, and I have no illusions that I have insight that will revolutionaize the game of baseball like Bill James or Jonah Hill, from *Moneyball*. 

But I have been thinking a lot about how Baseball players are judged, and creating metrics for how to rank players, and I have wanted to write these thoughts down. 

This first came about when I created my [baseball keeper project](/baseball-keeper). Broadly, my goal for the project was to plagurize other simmilar project with Claude, and to keep a list of the best players I've seen. Living close to the farm team of the Washington Nationals when Bryce Harper and Stephen Strausberg came up, I also wanted a to be able to track MiLB games in there as well. The issue became, that added a large number of numbers, where in a given AAA game I was maybe interested in one or two that actually played that day. I wanted a way to parse the signal from the noise at a glace, and pop the notable players to the top. 

For hitters, this became trivial enough. Taking their career WAR and multiplying it by the number of games I'd seen them in returns a respectable and interesting enough top ten.

| Ranking | Player | Games Seen |
|:--|:--|--:|
| 1  | José Ramírez | 6 |
| 2  | George Springer  | 4  |
| 3  | Shohei Ohtani  | 2  |
| 4  | Steven Kwan  | 5  |
| 5  | Albert Pujols  | 1  |
| 6  | Alex Bregman  | 2  |
| 7  | Adrian Beltré  | 1  |
| 8  | Mike Trout  | 1  |
| 9  | Vladmir Gurrero Jr.  | 3  |
| 10 | Carlos Beltrán  | 1  |

This does create some funny situations (Steven Kwan would have to play two goods halves in ths same season to even sniff a list like this generally, and I am loath to rank two players at the heart of the Astros cheating scandal that high) but created a simple enough list that put the Hall Of Famers in the top 10. There are some players that for personal reasons I'd like to see higher (I've seen Teoscar Hernadex at 16 three times for 3 teams, or Randy Arozarena at 25 seen twice for two different teams) but perhapse they should get good and pump their WAR numbers up. Or I should add a vibes weighting for certain players

Once you get down the list, there are some players that maybe should be higher, just in terms of noteriety, such as Prince Fielder at 69, former ROY winner Jonathan India at 150, and any number of top prospects who simply hand't had enough time to accumulate WAR smattered in the 90-200 range, but it worked crudly enough. At some point, an automated way to pull a players highest prospect ranking and adding it to the list would be useful, although that might overrate other players (thinking of Amed Rosario, a former number one overall prospect, currently at 79  in my ranking).

Pitching became more of a game, to the point where starters and relievers had to be seperated. To be clear, I am still not fully satisfied with either. 

For starters, the formula became 

`peak_WAR (3-year) × games_seen`

This solution proved to be more imperfect than for Batters, but was fine enough. I could pull 3 year peak WAR from Baseball Referece easily, and this wouldn't overrate veterans too much higher than younger pitchers. Again, I did want to highlight players I'd see multiple times, as this is not my establishment of the greatest players to ever grace the field. This left us with a top 10 as follows:

| Rank  | Player Name  | Games Seen  |
|:--|:--|--:|
| 1  | Stephen Strasburg  | 2  |
| 2  | Gerrit Cole  | 1  |
| 3  | Carlos Rodón  | 1  |
| 4  | Jose Quintana  | 1  |
| 5  | Erick Fedde  | 2  |
| 6  | Carlos Carrasco  | 1  |
| 7  | Patrick Corbin  | 1  |
| 8  | Lucas Giolito  | 1  |
| 9  | Shane Bieber  | 1  |
| 10 | Chris Bassitt  | 1  |

The list quickly becomes less impressive from it's high of Strasburg and Cole, but to the formula's credit there aren't any other pitchers on the list of 41 you'd argue should be in the top 10 besides Shane Mclanahan at 14. Jose Quintana feels out of place until you remember how good he was after he came up. 

| Year |   W-L |  ERA |    IP |  SO | WAR |
| ---- | ----: | ---: | ----: | --: | --: |
| 2012 |   6-6 | 3.76 | 136.1 |  81 | 2.3 |
| 2013 |   9-7 | 3.51 | 200.0 | 164 | 5.1 |
| 2014 |  9-11 | 3.32 | 200.1 | 178 | 3.2 |
| 2015 |  9-10 | 3.36 | 206.1 | 177 | 4.1 |
| 2016 | 13-12 | 3.20 | 208.0 | 181 | 5.3 |

A three year peak from 2014 - 2016, accumilating a WAR of 12.8, and keeping an ERA+ over 110 each of those years is pretty impressive compared to some of the other pitchers on the list. Getting to play in an era where you could regularly hit 200 innings pitched certainly helps. 

The biggest dilema became relief pitchers. It would be easy enough to rank them by the same metric as their starting counterparts, but the data there became so noisy that it was unusable. I am the most dissatisfied with the outcome of this list and spent the most time thinking about it. 

| Rank  | Player Name  | Games Seen  |
|:--|:--|:--|
| 1  | Aroldis Chapman  | 1  |
| 2  | Kenley Jansen  | 1  |
| 3  | Raisel Iglesias  | 1  |
| 4  | Tyler Clippard  | 2  |
| 5  | Garrett Whitlock*  | 1  |
| 6  | Ryan Helsley  | 1  |
| 7  | Jason Adam  | 1  |
| 8  | Tyler Rogers  | 2  |
| 9  | Daniel Hudsdon  | 1  |
| 10  | Andrés Muñoz  | 2  |

The list itself is fine enough, it gets the few of the top closers of the last 10 years in there with a couple odd firemen I'd see a few times. Carrett Whitlock sneaks in despite having started in the game I saw him, since the perponderance of his opther appearences for Boston have been out of the bullpen. There are some other issues though. 

Veteran, notable are places almost randomly throughout the list. Guys like Jose Alvarado, Paul Sewald, Giovanny Gallegos and Camilo Doval languash in the mid 30s while you see guys like Drew Storen enjoy being in the top 10. Maybe those guys should be better at pitching, but if I was looking at a list of "Players I've Seen," I'd rather see their names than Cory Gearrin (no offense to Cory Gearrin).
