# NFL's Toughest Road

## Project Description
Apply machine learning model to determine which NFL team had the toughest and easiest opponents driven by statistical performance only. 
The model takes in individual team statistics per game for over 20 years and produces results based on predicting wins and losses.


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
