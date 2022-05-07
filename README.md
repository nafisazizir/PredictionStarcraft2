# Analysis and Prediction of the Matchup of Starcraft II Matches
Starcraft II is a science fiction real-time strategy video game developed and published by Blizzard Entertainment. For the last decade, it has been the premier 1v1 competitive esports title and is widely played around the globe. While it is well past its golden years, Starcraft II remains an interesting game for machine learning and deep learning research due to its strategical depth and real-time engine. For example, the DeepMind team created an AI to play Starcraft II called AlphaStar.

## Description
Starcraft II is a science fiction real-time strategy video game developed and published by Blizzard Entertainment. For the last decade, it has been the premier 1v1 competitive esports title and is widely played around the globe. While it is well past its golden years, Starcraft II remains an interesting game for machine learning and deep learning research due to its strategical depth and real-time engine. For example, the DeepMind team created an AI to play Starcraft II called AlphaStar.

In this instance, the problem is not in making an AI to play Starcraft II, nor is it making a predictive model for a match outcome. The problem is to predict the racial matchup of a match given match summary statistics.

To give more context, in 1v1 competitive Starcraft II, each player can choose to play as 1 out of three races: Terran (T), Protoss (P), and Zerg (Z). Therefore, there are 6 possible matchups (including 3 mirror matchups): TvT, TvP, TvZ, PvP, PvZ, and ZvZ. What is interesting is that each matchup is usually played differently. For example, TvT is often described as a chess game, while TvZ is a game of momentum. Each race is also often regarded as having its own unique characteristics. For example, Zerg players are often considered as having higher APM (Actions per Minute) in general.

Given the background above, it is of interest to build a predictive model for the matchup. This model is not intended to actually be used to predict the matchup (since it is already apparent after all). Still, it is interesting to see whether we can analyze the different characteristics of each matchup using our predictive model. Therefore, the challenge here is not just building a good predictive model, but a good and interpretable model.

## Dataset
The dataset is sourced from the replays of professional Starcraft II matches in the last three premier tournaments (IEM Katowice 2022, DH Masters Last Chance, DH Masters Winter) and parsed through a SC2 replay parser. 

Dataset source: https://www.kaggle.com/competitions/oprec-ristek-ds-2022/data

To understand about the dataset, here is the data dictionary for this dataset:
1. ```game_length```: length of match in seconds.
2. ```winner```: winner of the match (1 for player 1 and 2 for player 2).
3. ```matchup```: target variable; 6 possible values.
4. ```p{i}_apm```: actions per minute for player ```i```.
5. ```p{i}_spm```: screens per minute for player ```i```.
6. ```p{i}_avg_pac_per_min```: average number of Perception-Action Cycle per minute for player ```i```.
7. ```p{i}_sq```: Spending Quotient for player ```i```.
8. ```p{i}_race```: race for player ```i```

## Dependencies
| Pandas | Numpy | Matplotlib | Seaborn | warnings | Scikit-learn | CatBoost |
| ------ | ----- | ---------- | ------- | -------- | ------------ | -------- |

Install the required packages by executing the following command.

```$ pip install -r requirements.txt```

### Files
- ```noetbook.ipynb``` : notebook of the anaklysis and the prediction model of the dataset
- ```train.csv``` : dataset of the training data
- ```requirements.txt``` : text file contains the dependencies
