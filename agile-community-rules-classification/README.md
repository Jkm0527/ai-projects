# Kaggle: Jigsaw Agile Community Rules Classification 

**Competition:** Predict whether a comment broke a rule in a subreddit 
**Focus:** Text preprocessing, feature engineering, ensembling and generalising to unseen rules

## Approach
-Embedding models: use pretrained text embedding models lke e5-base/large and BAAI/bge-m3 to encode the comment, rule and negative and positive examples
-Feature engineering: cosine similarity between comment and rule and also between comment and examples.Some extra features included are jaccard overlap, rule frequency, subreddit signals and averaging the positive/negative example embeddings.
-Cross-validation with  5-fold stratification to check generalization and accuracy checked with column averaged AUC
-Ensembling multiple fine-tuned embeddors to give an extra cv boost

Possible Improvements:
-use logistic regression on top of the engineered features
-use an llm to probe the hidden rules, then mass produce synthetic data to further improve the model

Results:
-best model ensemble achieved 0.8776 cv score
