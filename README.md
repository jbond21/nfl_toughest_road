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
- Jaguars: 205 games.
- Browns: 201 games.
- Raiders: 197 games.
- Jets: 187 games.
- Colts: 186 games.
- Lions: 185 games.
- Rams: 183 games.
- Texans: 181 games.
- Dolphins: 180 games.
- Washington: 176 games.


## Teams that Played the Most Difficult Games in the past 20 years. Outcome: Win
### Top 10 Teams
- Colts: 65 games.
- Patriots: 55 games.
- Cowboys: 37 games.
- Chiefs: 34 games.
- Seahawks: 33 games.
- Saints: 32 games.
- Packers: 31 games.
- Eagles: 31 games.
- Chargers: 31 games.
- Broncos: 30 games.


## Teams that Played the Most Difficult Games in the past 20 years. Outcome: Loss
### Top 10 Teams
- Jaguars: 184 games.
- Browns: 181 games.
- Raiders: 172 games.
- Jets: 163 games.
- Texans: 163 games. 
- Lions: 163 games.
- Washington: 163 games. 
- Rams: 160 games.
- Buccaneers: 152 games.
- Dolphins: 152 games.  


## Teams that Played the Easiest Games in the past 20 years. Outcome: Win or Lose
### Top 10 Teams
- Patriots: 225 games.
- Steelers: 223 games.
- Ravens: 209 games.
- Packers: 209 games.
- Seahawks: 186 games.
- Eagles: 185 games.
- Chiefs: 184 games.
- Vikings: 183 games.
- Chargers: 183 games.
- Tied
- Panthers: 179 games.
- Saints: 179 games.


## Teams that Played the Easiest Games in the past 20 years. Outcome: Win
### Top 10 Teams
- Patriots: 210 games.
- Steelers: 196 games.
- Packers: 184 games.
- Ravens: 170 games.
- Seahawks: 167 games.
- Saints: 164 games.
- Eagles: 161 games.
- Chiefs: 154 games.
- Broncos: 152 games.
- Colts: 149 games.



## Teams that Played the Easiest Games in the past 20 years. Outcome: Loss
### Top 10 Teams
- Lions: 48 games.
- Ravens: 39 games.
- Vikings: 38 games.
- Chargers: 37 games. 
- Bears: 34 games.
- Browns: 33 games. 
- Cowboys: 33 games.
- Washington: 32 games. 
- Panthers: 32 games.
- Tied
- Giants: 31 games.
- Raiders: 31 games


