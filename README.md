# Predicting Wide Receiver Scores for Fantasy Football
### Overview
This project aims to predict the fantasy football scores of NFL wide receivers. It scrapes individual player receiving and team passing data from pro-football-reference.com for the 2000–2016 seasons (n=~2200). The data is cleaned and merged prior to feature engineering. The final dataset is transformed using principal component analysis (PCA) and then modeled using linear regression.
### Key Questions Explored
- Can the model accurately predict NFL wide receiver fantasy scores?
- Which features correlate strongly with next season's fantasy points?
### Key Findings
The final regression model following dimensionality reduction has a root-mean-squared-error (RMSE) of 2.67 and an R^2 value of 0.692. For understanding the MSE, the top wide-receiver prediction is ~16 fantasy points per game (FP/g), while the 30th ranked wide-receiver is predicted to score ~10 FP/g. Considering the small sample sizes and volatility of fantasy football performances, these predictions are relatively accurate.
### Techniques used
- pandas and numpy for data scraping, exploration, and cleaning
- sklearn for principal component dimensionality reduction and regression modeling
- seaborn and matplotlib for visualization
