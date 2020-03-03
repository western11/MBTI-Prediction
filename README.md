# MBTI-Prediction

Main goal:
Predict MBTI personality dimensions based on social media text data (Indonesian languange)

how to:

step 1a: 
Predict big 5 personality traits using package mlr (R). The training model are build in english 
use 7 multi-label classification method:

a. Problem Transformation Methods:
- Binary Relevance (BR)
- Classifier Chains (CC)
- Nested Stacking (NS)
- Dependant Binary Relevance (DBR)
- Stacking (STA)

b. Algorithm Adaptation Methods:
- Random ForestSRC (RSRC)
- Ferns (RFERN)

after build model using all aviliable methods, check every performance using this following performance measurement indicator:
- f1-index
- subset 0/1
- hamming loss
- accuracy

Model with the best performance will be used as the Learner in the prediction machine

Expected output in step 1:
Prediction output with its probability. the prob will be used as weight (scoring) for the next step

Alternative step 1:
make regression model to target variabel one by one using every availiable algorithm. the best performance algorithm will be used as the learner in the prediction machine

Alternative regression output in step 1:
Extraversion: regression value in the scale of 0-1
Openness: regression value in the scale of 0-1
Agreebleness: regression value in the scale of 0-1
Consciencetiousness: regression value in the scale of 0-1

step 2:
Convert big 5 personality traits to MBTI dimensions.

find a way to  convert personality traits to MBTI dimensions. 
- Scoring (harvey et al, 1995)
- classification (logistic regression)

because the traits actually has no label, might be use UL method to find 2 K for every traits > MBTI dimensions

step 3:
Step 3: Build R shinny apps that connected to Twitter API



