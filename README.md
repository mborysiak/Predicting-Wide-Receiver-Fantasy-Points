# Predicting Wide Receiver Scores for Fantasy Football
### Overview
This project aims to predict the fantasy football scores of NFL wide receivers. It scrapes individual player receiving and team passing data from pro-football-reference.com, as well as average draft position (ADP) data from myfantasyleague.com for the 1998–2016 seasons. The data is cleaned and merged prior to feature engineering. The final dataset is used to make machine learning predictions with an ensemble of 5 algorithms.

### Key Questions Explored
- What is the model accuracy for predicting NFL wide receiver fantasy scores in the upcoming season?
- Which features correlate strongly with next season's fantasy points?
- Does the model improve upon conventional wisdom, i.e. the average draft position of players.

### Key Findings
- The final ensemble model following has an average root-mean-squared-error (RMSE) of ~2.8 fantasy points for out-of-sample data using 10-fold cross-validation. 


- For context of the RMSE, the top 10% of wide-receivers score ~15 fantasy points per game (FP/g), while the bottom 10% score ~8 FP/g, resulting in coefficient of variance around 15% and 33% respectively. Considering the small sample sizes for each season (16 games) and volatility of fantasy football performances, these predictions are relatively accurate.


- When comparing the projected rankings of the model (ordinal values) to the average draft position ranking from ~6000 drafts, the model has 30% higher accuracy in predicting the correct ranking for holdout data.

### Techniques used
- pandas and numpy for data scraping, exploration, and cleaning
- Pipeline and GridSearchCV for modeling and optimization
- Ridge / Lasso Regression, RandomForestRegressor, XGBoost, and KNearestNeighbors for modeling
- Principal Component Analysis (PCA) for dimensionality reduction
- seaborn and matplotlib for visualization
