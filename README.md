# Text-Classifier
Implementation of  Naive bayes algorithm to classify text into 20 different categories.
Splitted the data into training and testing and made a dataframe where the path of files and their corresponding class( category ) was stored.
All the files in the training data were traversed and some of the top frequency words, except the stop Words  were selected as features.
A dataframe was then made where for every file in training data the frequency of the words selected as features were stored and their corresponding class value. Similarly a dataframe for testing data is also formed.
For the fit function , a 2-level dictionary called as 'counts' was formed in which the key values were the classes( categories ). Within these , another dictionary was formed whose key values were the features selected.
Now all the files in the dataframe belonging to a particular dataframe were selected and sum of the frequencies for the features were stored in the dictionary 'counts'.
A total count of frequencies is also stored for each class.
For making predictions, each tuple from testing data is passed to the predict single fuction which calculates its probability for each class using naive bayes and predicts the class with maximum probability.
Naive Bayes is a classification technique based on Bayes’ Theorem with an assumption of independence among predictors. A Naive Bayes classifier assumes that the presence of a particular feature in a class is unrelated to the presence of any other feature 
![alt text](https://cdn-images-1.medium.com/max/1600/1*7lg_uLm8_1fYGjxPbTrQFQ.png)
 
 Here , P(A)= probability of class.
 
 P(B)=Probability of feature
 
 P(B|A)= Probability of the feature given that it belongs to the particular class.
 Laplace correction is also considered and the log probabilities were added.
 Class with maximum probability is predicted.
