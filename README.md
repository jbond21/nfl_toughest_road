# NFL's Toughest Road

## Project Description
Apply machine learning model to determine which NFL team had the toughest and easiest opponents driven by statistical performance only. 
The model takes in individual team statistics per game for over 20 years and produces results based on predicting wins and losses measured by the optimal stat threshold


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
#### Game Type Descriptions

#### Toughest Games
- Games that opponent were predicted to win regardless of actual outcome

#### Easy Games
- Games that opponent were predicted to lose regardless of actual outcome

#### Game Type Categories

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
## Teams that Played the Most Difficult Games in the past 20 years. Outcome: Win or Lose
### Top 10 Teams
- Jaguars: 201 games.
- Browns: 198 games.
- Raiders: 197 games.
- Lions: 193 games.
- Jets: 187 games.
- Colts: 185 games.
- Texans: 182 games.
- Rams: 182 games.
- Bengals: 178 games.
- Giants: 178 games.


## Teams that Played the Most Difficult Games in the past 20 years. Outcome: Win
### Top 10 Teams
- Colts: 64 games.
- Patriots: 56 games.
- Cowboys: 38 games.
- Chiefs: 36 games.
- Eagles: 34 games.
- Saints: 34 games.
- Packers: 33 games.
- Seahawks: 33 games.
- Broncos: 33 games.
- Chargers: 32 games.


## Teams that Played the Most Difficult Games in the past 20 years. Outcome: Loss
### Top 10 Teams
- Browns: 181 games.
- Jaguars: 180 games.
- Raiders: 172 games.
- Lions: 169 games.
- Texans: 164 games. 
- Washington: 164 games. 
- Jets: 163 games.
- Rams: 157 games.
- 49ers: 150 games. 
- Tied
- Giants: 150 games.
- Bengals: 150 games. 
- Dolphins: 150 games. 


## Teams that Played the Easiest Games in the past 20 years. Outcome: Win or Lose
### Top 10 Teams
- Patriots: 223 games.
- Steelers: 222 games.
- Ravens: 206 games.
- Packers: 205 games.
- Seahawks: 187 games.
- Eagles: 182 games.
- Vikings: 181 games.
- Chiefs: 181 games.
- Panthers: 180 games.
- Saints: 180 games.


## Teams that Played the Easiest Games in the past 20 years. Outcome: Win
### Top 10 Teams
- Patriots: 209 games.
- Steelers: 191 games.
- Packers: 182 games.
- Seahawks: 167 games.
- Ravens: 167 games.
- Saints: 162 games.
- Eagles: 158 games.
- Chiefs: 152 games.
- Colts: 150 games.
- Broncos: 149 games.



## Teams that Played the Easiest Games in the past 20 years. Outcome: Loss
### Top 10 Teams
- Lions: 42 games.
- Ravens: 39 games.
- Vikings: 38 games.
- Bears: 37 games.
- Chargers: 34 games. 
- Browns: 33 games. 
- Panthers: 33 games.
- Cowboys: 33 games.
- Titans: 32 games. 
- Tied
- Washington: 31 games.
- Steelers: 31 games. 
- Buccaneers: 31 games. 


