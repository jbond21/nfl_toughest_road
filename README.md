# NFL's Toughest Road

## Project Description
Apply machine learning model to determine which NFL team had the toughest and easiest games played driven by statistical performance only. 
The model takes in individual team statistics per game for over 20 years and produces results based on predicting wins and losses measured by the optimal stat threshold. My Motivation is to test my abilites to analysis a sport I grew up watching and produce interesting findings that might go unnoticed by the NFL and fans.


### Installations
- import pandas as pd
- import numpy as np
- import matplotlib.pyplot as plt
- import seaborn as sns
- %matplotlib inline
- from sklearn.model_selection import train_test_split, cross_val_score
- from sklearn.svm import SVC
- from sklearn.tree import DecisionTreeClassifier
- from sklearn.neighbors import KNeighborsClassifier 
- from sklearn.ensemble import RandomForestClassifier
- from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

### Files
#### nfl_team_stats_2002-2021.csv
The nfl_team_stats_2002-2021.csv file is the only file used. It consist of date of games, name of both home and aways teams, stats from both teams in the game
and the score to determine the winner and loser.

### Definitions
#### Game Type Category

#### Toughest Games
- Games that opponent were predicted to win regardless of actual outcome

#### Easy Games
- Games that opponent were predicted to lose regardless of actual outcome

#### Game Type Descriptions

#### Hard Fought Loss
- team has optimal stats to win game but still lost because opponent also had optimal stats to win game.
- positive for toughest games

#### Tough Loss
- team has optimal stats to win game but still lost while the opponent did not have optimal stats.
- negative for toughest games

#### Loss Bad Game
- both teams have sub optimal stast and opponent wins
- negative for toughest games

#### Expected Loss
- team has sub optimal stats to win the game and opponent has optimal stat, so opponent expected to win.
- positive for toughest games

#### Hard Fought Win
- team has optimal stats to win game and actually win the game even when their opponent has optimal stats to win the game as well.
- positive for toughest games

#### Lucky Win
- team has below optimal stats to win the game and still wins when their opponent did have optimal stats to win. 
- positive for toughest games

#### Win Bad Game
- team has below optimal stats to win and still wins while their opponent also had sub optimal stats
- negative for toughest games

#### Expected Win
- team has optimal stats to win the game and opponent has below optimal stats, so expected outcome
- negative for toughest games


### Instructions
The last line of code is a the function called team_report that requires the team name as an input to run successfully.


### Results
## Difficulty Score Rank
1. Jaguars         83
2. Browns          79
3. Raiders         68
4. Lions           48
5. Jets            42
6. Dolphins        37
7. Rams            33
8. Texans          31
9. Washington      27
10. Colts           25
11. Bengals         22
12. Bills           16
13. Buccaneers      15
14. 49ers           12
15. Giants           8
16. Cardinals        7
17. Falcons         -3
18. Bears           -7
19. Titans          -8
20. Broncos        -17
21. Cowboys        -19
22. Saints         -20
23. Panthers       -24
24. Seahawks       -25
25. Chiefs         -28
26. Eagles         -29
27. Chargers       -33
28. Vikings        -36
29. Packers        -72
30. Ravens         -76
31. Patriots       -90
32. Steelers      -104


## Teams that Played the Most Difficult Games in the past 20 years. Outcome: Win or Lose
### Top 10 Teams
1. Jaguars tough_games count: 205
2. Browns tough_games count: 201
3. Raiders tough_games count: 197
4. Jets tough_games count: 187
5. Colts tough_games count: 186
6. Lions tough_games count: 185
7. Rams tough_games count: 183
8. Texans tough_games count: 181
9. Dolphins tough_games count: 180
10. Washington tough_games count: 176


## Teams that Played the Most Difficult Games in the past 20 years. Outcome: Win
### Top 10 Teams
1. Colts won_tough_game count: 65
2. Patriots won_tough_game count: 55
3. Cowboys won_tough_game count: 37
4. Chiefs won_tough_game count: 34
5. Seahawks won_tough_game count: 33
6. Saints won_tough_game count: 32
7. Packers won_tough_game count: 31
7. Eagles won_tough_game count: 31
7. Chargers won_tough_game count: 31
8. Broncos won_tough_game count: 30
9. Dolphins won_tough_game count: 28
9. Ravens won_tough_game count: 28
10. Titans won_tough_game count: 27
10. Falcons won_tough_game count: 27


## Teams that Played the Most Difficult Games in the past 20 years. Outcome: Loss
### Top 10 Teams
1. Jaguars loss_tough_game count: 184
2. Browns loss_tough_game count: 181
3. Raiders loss_tough_game count: 172
4. Jets loss_tough_game count: 163
4. Texans loss_tough_game count: 163
4. Lions loss_tough_game count: 163
4. Washington loss_tough_game count: 163
5. Rams loss_tough_game count: 160
6. Buccaneers loss_tough_game count: 152
6. Dolphins loss_tough_game count: 152
7. Bengals loss_tough_game count: 151
8. 49ers loss_tough_game count: 150
9. Bills loss_tough_game count: 148
9. Cardinals loss_tough_game count: 148
10. Giants loss_tough_game count: 146


## Teams that Played the Easiest Games in the past 20 years. Outcome: Win or Lose
### Top 10 Teams
1. Patriots easy_games count: 225
2. Steelers easy_games count: 223
3. Ravens easy_games count: 209
3. Packers easy_games count: 209
4. Seahawks easy_games count: 186
5. Eagles easy_games count: 185
6. Chiefs easy_games count: 184
7. Vikings easy_games count: 183
7. Chargers easy_games count: 183
8. Panthers easy_games count: 179
8. Saints easy_games count: 179
9. Broncos easy_games count: 176
10. Cowboys easy_games count: 175



## Teams that Played the Easiest Games in the past 20 years. Outcome: Win
### Top 10 Teams
1. Patriots won_easy_game count: 210
2. Steelers won_easy_game count: 196
3. Packers won_easy_game count: 184
4. Ravens won_easy_game count: 170
5. Seahawks won_easy_game count: 167
6. Saints won_easy_game count: 164
7. Eagles won_easy_game count: 161
8. Chiefs won_easy_game count: 154
9. Broncos won_easy_game count: 152
10. Colts won_easy_game count: 149



## Teams that Played the Easiest Games in the past 20 years. Outcome: Loss
### Top 10 Teams
1. Lions loss_easy_game count: 48
2. Ravens loss_easy_game count: 39
3. Vikings loss_easy_game count: 38
4. Chargers loss_easy_game count: 37
5. Bears loss_easy_game count: 34
6. Browns loss_easy_game count: 33
6. Cowboys loss_easy_game count: 33
7. Washington loss_easy_game count: 32
7. Panthers loss_easy_game count: 32
8. Giants loss_easy_game count: 31
8. Raiders loss_easy_game count: 31
9. Titans loss_easy_game count: 30
9. 49ers loss_easy_game count: 30
9. Chiefs loss_easy_game count: 30
9. Cardinals loss_easy_game count: 30
10. Buccaneers loss_easy_game count: 28
10. Jets loss_easy_game count: 28


