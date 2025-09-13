# QB MVP Predictor

**Goal:** Predict NFL MVP award outcomes based on quarterback passing statistics.  
**Focus:** Sports analytics, feature engineering, and predictive modeling.

## Approach
- Data: QB passing stats (source: .pro-football-reference.com)  
- Features: Games played, completions, passing attempts, completion percentage, passing yards, passing touchdowns, touchdown percentage, interceptions,interception percentage, first downs passing, passing success rate, yards per attempt, adjusted yards per attempt, yards per completion, yards per game, passer rating, quarterback rating, sacks, yards given up to sacks, sacked percentage, net yards gained per pass attempt, adjusted net yards gained per pass attempt, comebacks led by quarterback
- Models: Random Forest Classifier, XGBoost  
- Evaluation: Accuracy, AUC

## Results
  1.Random Forest Classifier
      cross-validation scores on training data: 0.9759463087248322
      Accuracy on test data : 0.9574468085106383
  2.Xgboost
      cross-validation scores on training data: 0.9772796420581656
      Accuracy on test data : 0.9521276595744681
