---
layout: post
image: /assets/images/chelsea-celebrating-champions-league.jfif
---
## Introduction.

I’m a totally blind guy, yet I’m interested in a sport where some people might think that you'd actually need sight in order for you to know what’s going on in the playing field.

Thanks to the commentators out there who come in and describe almost everything happening in the game, admittedly some of them do a better job of it better than others, but still, for me, and for many other people like me, they’re the ones who help us enjoy football matches.

Personally speaking, I don’t depend just on the commentators, I also like to keep an eye on the live stats for the match I’m currently watching.

I use google for that. If I’m watching a match between say Juventus and Inter Milan, I’d just type in “Juventus vs Inter Milan” or “Juventus match” or anything of that nature. It’ll then bring me the current live status for the match including lineups, the time line of the match, the score, who scored, possession rate, yellow cards, red cards and more.

With those combined, I always get a very good idea on what’s going on in the game I’m watching.

In this post though, we’ll take the stats thing even further. I had to do a project in a udacity course and found myself able to choose my own dataset for data analysis and the first thing that came to my mind is football, since I always wanted to do something about it in my journey through data science.

We will be taking a look at the champions league 2020-2021 results dataset, with the hope that you’ll gain some useful insights.

I used [this dataset from kaggle for this analysis](https://www.kaggle.com/mcarujo/uefa-champions-league-20202021/tasks)

Just a recap, Chelsea won that league after defeating Man City in the final 1 – 0 with a goal scored by none other than Kai Havertz in the 42nd minute.

That’s probably old news for most of the readers, however, the answers to the questions we’re about to ask, hopefully lead up to some new and interesting information about that season of the champions league.

---

## What was the largest score for home and away teams?

We’ll separate both categories here. A home team is the team who’s playing the match at their own stadium, while an away team is the team who’s playing the match in another stadium but their own.

That’s basically it, although there are times where both teams play at a totally different stadium but we’re not going to get into that.

| stage                     | date       | team_name_home      | team_name_away      |   team_home_score |   team_away_score | possession_home   | possession_away   |   total_shots_home |   total_shots_away |   shots_on_target_home |   shots_on_target_away | location                          | match_win_status   |
|:--------------------------|:-----------|:--------------------|:--------------------|------------------:|------------------:|:------------------|:------------------|-------------------:|-------------------:|-----------------------:|-----------------------:|:----------------------------------|:-------------------|
| Group stage: Matchday 2   | 28.10.2020 | Manchester United   | RB Leipzig          |                 5 |                 0 | 47%               | 53%               |                 15 |                  9 |                      8 |                      2 | Old Trafford                      | home               |
| Group stage: Matchday 6   | 09.12.2020 | PSG                 | İstanbul Başakşehir |                 5 |                 1 | 69%               | 31%               |                 20 |                 10 |                      9 |                      4 | Parc des Princes                  | home               |
| Group stage: Matchday 1   | 20.10.2020 | Barcelona           | Ferencváros         |                 5 |                 1 | 62%               | 38%               |                 22 |                  8 |                     11 |                      2 | Camp Nou                          | home               |
| Group stage: Matchday 4   | 25.11.2020 | B. M‘Gladbach       | Shakhtar Donetsk    |                 4 |                 0 | 46%               | 54%               |                 14 |                 13 |                      6 |                      3 | BORUSSIA-PARK                     | home               |
| Group stage: Matchday 4   | 24.11.2020 | Manchester United   | İstanbul Başakşehir |                 4 |                 1 | 52%               | 48%               |                 16 |                 13 |                      8 |                      4 | Old Trafford                      | home               |

As we can see, the largest score for home teams was 5 - 0 in the match that was between Manchester United and RB Leipzig in the Matchday 2 of the Group stage, the match was on 28.10.2020.

Lets check for the case of the largest score away teams scored.

| stage                     | date       | team_name_home      | team_name_away      |   team_home_score |   team_away_score | possession_home   | possession_away   |   total_shots_home |   total_shots_away |   shots_on_target_home |   shots_on_target_away | location                          | match_win_status   |
|:--------------------------|:-----------|:--------------------|:--------------------|------------------:|------------------:|:------------------|:------------------|-------------------:|-------------------:|-----------------------:|-----------------------:|:----------------------------------|:-------------------|
| Group stage: Matchday 3   | 03.11.2020 | Shakhtar Donetsk    | B. M‘Gladbach       |                 0 |                 6 | 55%               | 45%               |                  4 |                 20 |                      1 |                     10 | Kiev Olympic Stadium              | away               |
| Group stage: Matchday 3   | 03.11.2020 | Salzburg            | Bayern Munich       |                 2 |                 6 | 40%               | 60%               |                 18 |                 21 |                     10 |                     10 | Red Bull Arena Salzburg           | away               |
| Group stage: Matchday 3   | 03.11.2020 | Atalanta            | Liverpool           |                 0 |                 5 | 43%               | 57%               |                  9 |                 15 |                      6 |                     12 | Gewiss Stadium                    | away               |
| Group stage: Matchday 5   | 02.12.2020 | Sevilla             | Chelsea             |                 0 |                 4 | 56%               | 44%               |                 17 |                 14 |                      3 |                      7 | Ramón Sánchez-Pizjuán             | away               |
| Group stage: Matchday 2   | 28.10.2020 | Krasnodar           | Chelsea             |                 0 |                 4 | 29%               | 71%               |                 13 |                 16 |                      4 |                      7 | Krasnodar Stadium                 | away               |

Wow, the largest score for away teams was 6 - 0 in the match that was between Shakhtar Donetsk and B. M‘Gladbach in the Matchday 3 of the Group stage, the match was on 03.11.2020.

That wasn’t surprising to me at least. Early matches specially in the group stage have a large chance of big teams meeting small teams thus big teams getting to score a lot of goals overall.

---

## What was the highest possession rate for a home and away team?

The possession rate is an indicator of who’s the team who had the ball the most in the match. For example:
If x was playing Y, X has a possession rate of 70% and Y had a possession rate of 30%, then that means that X was in control of the ball for 70% of the time.

It’s usually counted with getting the percentage of the number of passes X has made from the total of both teams passes altogether.

Lets take a look at the highest possession rate for home teams

| stage                     | date       | team_name_home      | team_name_away      |   team_home_score |   team_away_score | possession_home   | possession_away   |   total_shots_home |   total_shots_away |   shots_on_target_home |   shots_on_target_away | location                          | match_win_status   |
|:--------------------------|:-----------|:--------------------|:--------------------|------------------:|------------------:|:------------------|:------------------|-------------------:|-------------------:|-----------------------:|-----------------------:|:----------------------------------|:-------------------|
| Group stage: Matchday 6   | 09.12.2020 | Bayern Munich       | Lokomotiv Moscow    |                 2 |                 0 | 70%               | 30%               |                 22 |                  7 |                      7 |                      3 | Allianz Arena                     | home               |
| Group stage: Matchday 2   | 28.10.2020 | Borussia Dortmund   | Zenit               |                 2 |                 0 | 70%               | 30%               |                 11 |                  4 |                      5 |                      0 | SIGNAL IDUNA PARK                 | home               |
| Group stage: Matchday 6   | 09.12.2020 | PSG                 | İstanbul Başakşehir |                 5 |                 1 | 69%               | 31%               |                 20 |                 10 |                      9 |                      4 | Parc des Princes                  | home               |
| Group stage: Matchday 1   | 21.10.2020 | Manchester City     | FC Porto            |                 3 |                 1 | 69%               | 31%               |                  9 |                  6 |                      6 |                      2 | Etihad Stadium                    | home               |
| Round of 16 second leg    | 09.03.2021 | Juventus            | FC Porto            |                 3 |                 2 | 69%               | 31%               |                 31 |                 14 |                     13 |                      7 | Allianz Stadium                   | home               |

The highest possession rate a home team had was in the match that was between Bayern Munich and Lokomotiv Moscow, with Bayern Munich Having a 70% possession of the ball.

| stage                     | date       | team_name_home      | team_name_away      |   team_home_score |   team_away_score | possession_home   | possession_away   |   total_shots_home |   total_shots_away |   shots_on_target_home |   shots_on_target_away | location                          | match_win_status   |
|:--------------------------|:-----------|:--------------------|:--------------------|------------------:|------------------:|:------------------|:------------------|-------------------:|-------------------:|-----------------------:|-----------------------:|:----------------------------------|:-------------------|
| Round of 16 second leg    | 10.03.2021 | PSG                 | Barcelona           |                 1 |                 1 | 27%               | 73%               |                  7 |                 21 |                      3 |                     10 | Parc des Princes                  | draw               |
| Group stage: Matchday 2   | 28.10.2020 | Krasnodar           | Chelsea             |                 0 |                 4 | 29%               | 71%               |                 13 |                 16 |                      4 |                      7 | Krasnodar Stadium                 | away               |
| Group stage: Matchday 4   | 24.11.2020 | Dynamo Kyiv         | Barcelona           |                 0 |                 4 | 30%               | 70%               |                  7 |                 16 |                      3 |                      7 | Kiev Olympic Stadium              | away               |
| Round of 16 second leg    | 09.03.2021 | Borussia Dortmund   | Sevilla             |                 2 |                 2 | 31%               | 69%               |                  9 |                 19 |                      5 |                      8 | SIGNAL IDUNA PARK                 | draw               |
| Round of 16 first leg     | 24.02.2021 | Atalanta            | Real Madrid         |                 0 |                 1 | 31%               | 69%               |                  2 |                 19 |                      0 |                      4 | Gewiss Stadium                    | away               |

As for the away team, as you can tell from the table above, the highest possession rate for an away team was in a match between PSG and Barcelona, with Barcelona having 73% control of the ball. Although, that high possession rate wasn’t enough for them to win, the match ended on a draw and that was the end of Barcelona in that season, and PSG advanced to the quarter finals.

---

## How many times did home and away teams actually win their matches?

So the normal thing is for home teams to win their matches most of the time, mostly for the fact that they’re in their own stadium and they have their supporters by the thousand’s supporting them in the match right? Well, lets see if that holds water.

![image](https://github.com/mohammad-aloufi/mohammad-aloufi.github.io/blob/master/assets/images/winning_graf.png?raw=true)

So that wasn't surprising to me, throughout the whole season of that champions league, home teams won 51 matches, away teams won 50 matches, and 24 matches ended on a draw.

Some people probably didn’t see this coming. Sure, home teams won the most matches, but the chance of a team who wasn’t playing at their own stadium was almost the same.

If you ask me, I think that’s probably because of the pandemic and how crowds weren’t allowed to attend some of the matches, so that made things a bit more equal between teams, as in, stadiums didn’t really make that much of a difference when crowds weren't there so the crowd effect wasn't there to help some of the teams specially the big ones.

---

## Conclusion

Throughout this post, we asked some questions about the 2020 – 2021 season of the champions league and got some interesting answers.

1. We took a look at the largest scores in that season with Shakhtar Donetsk taking the lead in their match against  B. M‘Gladbach 6 – 0.
2. Bayern Munich killed it in their match against Lokomotiv Moscow, having the highest possession rate for a home team, with Barcelona having the highest possession rate for an away team in their match against PSG.
3. Away teams won almost the same number of matches as home teams, with covid being the most likely reason for why this happened because that season was played in the middle of the pandemic.

For more information about the champions league, please visit  the [uefa website](https://www.uefa.com/uefachampionsleague/)
