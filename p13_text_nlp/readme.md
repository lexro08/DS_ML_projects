# Project for Wikishop

Wikishop online store launches a new service. Now users can edit and supplement product descriptions, as in wiki communities. That is, clients offer their edits and comment on the changes of others. The store needs a tool that will search for toxic comments and send them for moderation. 

We need to train the model to classify comments into positive and negative. We have at our disposal a data set with markup on the toxicity of edits.

It is necessary to build a model with the value of the quality metric *F1* at least 0.75.

# Results of the research

According to the results:

1) Lemmatization of text in 159000 lines using the SpaCy library. Lemmatization takes about 15 minutes, which is acceptable in time.

2) When training models, as well as subsequent testing on a test sample, Logistic regression with the following parameters showed itself best {'C': 3, 'class_weight': 'balanced', 'max_iter': 500, 'penalty': 'l2', 'solver': 'lbfgs'}

3) The F1 metric was reached on the test sample of more than 0.75.

**Libraries** - pandas, spacy, nltk, sklearn, LogisticRegression, CatBoostClassifier
