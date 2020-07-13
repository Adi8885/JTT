# JTT Assignment - Result Summary
- Case Study Chosen - 'Sentiment Analysis'
- This Repository contains various notebooks for 'Sentiment Analysis'<br />
- Different approaches have been tried for the same problem in order of increasing model complexities

Different approaches and summary of results is as below :- <br />
1. Bag of words + XGBoost Classifier
2. Doc2vec + Neural Network
3. Classifier using LSTM 
4. Transfer Learning Classifier using BERT


# Observations
1. This Problem has class imbalance with negative (63%) , neutral (21%) and positive (16%) <br />
2. Hence chosen metric for comparison is f1_score
3. Based on f1_score - (Bag of words + XGBoost Classifier) and (Classifier using LSTM) perform well
4. If add accuracy as well Bag of words + XGBoost Classifier is clear winner

# 1. Bag of words + XGBoost Classifier
              precision    recall  f1-score   support
           0       0.77      0.92      0.84      1834
           1       0.65      0.35      0.45       628
           2       0.69      0.60      0.64       466
    accuracy                           0.75      2928
    macro avg      0.70      0.62      0.64      2928
    weighted avg   0.73      0.75      0.73      2928

# 2. Doc2vec + Neural Network
              precision    recall  f1-score   support

           0       0.63      0.99      0.77       916
           1       0.22      0.01      0.01       312
           2       0.00      0.00      0.00       236

    accuracy                           0.62      1464
    macro avg      0.28      0.33      0.26      1464
    weighted avg   0.44      0.62      0.48      1464

# 3. Classifier using LSTM 
              precision    recall  f1-score   support

           0       0.82      0.85      0.83       916
           1       0.54      0.63      0.58       312
           2       0.67      0.44      0.54       236

    accuracy                           0.74      1464
    macro avg      0.68      0.64      0.65      1464
    weighted avg   0.74      0.74      0.73      1464
   

# 4. Transfer Learning Classifier using BERT
              precision    recall  f1-score   support

           0       0.63      0.68      0.65       916
           1       0.22      0.18      0.20       312
           2       0.15      0.14      0.15       236

    accuracy                           0.49      1464
    macro avg      0.33      0.33      0.33      1464
    weighted avg   0.47      0.49      0.48      1464
   
# Way Forward
1. SInce number of classes are less, we aacan also try "One Vs rest" Classificataion
2. Hyperparameter optimization for LSTM Model will Increase metrics
3. Adding more data will definately help improving metrics, especially for Deep Learning Models
4. BERT is trained on Wikipedia Corpus, Either it could be retrained on twitter corpus of fine tuned
5. For Doc2Vec , round trip accuracy can be used for better tuning and hence getting better quality embeddings
