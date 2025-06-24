# EPL-match-prediction
Predicting EPL (English Premier League) Match Results

This group project, completed during my undergraduate degree, focused on predicting the outcomes of English Premier League (EPL) matches from Matchday 22 of the 2021-22 season using Machine Learning (ML) techniques.

To tackle this challenge, we developed a pipeline that incorporated both the provided historical match data and a range of additional sources, such as per-player match-time statistics and seasonal player market values. These datasets were merged and cleaned, with feature engineering applied to create informative inputs like shots-on-target ratios and interceptions per opponent pass. Missing data was handled using multivariate imputation with Scikit-Learn's IterativeImputer, and all features were standardized for model training. We then trained regression models to estimate four key performance metrics - expected goals won (xG-won), expected goals conceded (xG-con), defensive pressure (xDef), and offensive effectiveness (xOff). These predictions were used to compute Elo-like scores for each team that evolve over time based on match performance.

Finally, these Elo-like scores served as input to a match outcome classification model predicting whether the result would be a home win (H), draw (D), or away win (A). The final model, a K-Nearest Neighbours classifier, achieved a macro-averaged F1 score of 43.07% using stratified 5-fold cross-validation, comparable to the ~53% accuracy reportedly achieved by bookmakers.

This repository contains both the full report and the code implementation in a Jupyter notebook.

Check out the summary documented here: https://www.asalabdullatif.com/projects/predicting-epl-match-results
