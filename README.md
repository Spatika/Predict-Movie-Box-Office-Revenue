# Predicting Box Office Revenue

## Data
- YouTube trailer metadata (view count, like count, dislike count, # of comments)
- IMDb movie data (average rating, # of reviews/ratings, # of critic ratings, motion picture rating - e.g. PG13, language, genres (one-hot encoded), production house (top few), country)
- TMDb: Popularity scores for headlining cast of each movie
- AFINN score of IMDb reviews pre-relase (but after promotional activities have started) and post release
  - This can be simulated when trying to predict revenue bucket before production has started

## Prediction
- Movie box office revenue prediction converted to a classification problem from a regression problem
- Each movie in the test set is classified into one of 5 revenue buckets: very low, low, medium, high, very high
- Bucket ranges are defined by quintiles of the entire range of revenues (on the full dataset, before train-test split)


## Models
- Comparison of well-known ML models: k-NN, multilayer perceptron, random forest, logistic regression
- Hyperparameters tuned and best of each found using RandomizedSearchCV

## Metrics
Precision, Recall (TPR/Sensitivity) and F1 Score 
