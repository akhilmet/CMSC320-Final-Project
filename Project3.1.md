### Primary Analysis: Predicting Player Position from Game Statistics

In this section, we treat player position prediction as a supervised learning problem.  
Each row in our dataset corresponds to a single NBA player-season with many numerical
features (points, assists, rebounds, shooting percentages, etc.). Our goal is to predict
a player’s on-court position (Guard, Forward, or Center) based only on these statistics.

- **Inputs (features X):** box-score and efficiency stats such as points per game (PTS),
  assists (AST), rebounds (TRB), blocks (BLK), steals (STL), turnovers (TOV), and shooting
  percentages (FG%, 3P%, FT%).
- **Output (target y):** a simplified position label with three classes:
  - `G` for Guards (PG/SG)
  - `F` for Forwards (SF/PF)
  - `C` for Centers

We train and evaluate two models:
1. Logistic Regression – a linear baseline classifier.
2. Random Forest – a non-linear ensemble model that can capture more complex patterns.

We evaluate both models using a held-out test set, accuracy, and a confusion matrix.
This tells us how well statistical patterns alone can recover traditional NBA positions.


