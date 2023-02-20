# Restaurant Reviews NLP

## 1. Introduction
&nbsp;&nbsp;&nbsp;&nbsp; Herein this dataset, we have 1000 reviews of a certain restaurant each with an indicator of whether it is a good or bad review. My goal in this project was to create a model that would be able to decipher between a good and bad review based on the content of the comment. 

## 2. Data Analysis
&nbsp;&nbsp;&nbsp;&nbsp; Here, my first step was to remove all of the 'stop words' ('and', 'the', 'is', etc) from the review. Without those words distracting my model, it's potential accuracy would greatly improve. Additionally, I wrote a function that would 'clean' the reivew: making each word lower case, removing punctuation, and finding the stem version of each word. We were able to begin modeling with a simplified version of each review that would be easier for the model to learn.

## 3. Modeling
&nbsp;&nbsp;&nbsp;&nbsp; I first used sklearn's CountVectorizer to count the amount of times a word is said in each review and make each of those words into a feature. I wanted to try out a few different classifiers as well as a neural network to see which would work the best with this data. I decided to use the Gaussian Naive Bayes Classifier, the SGD Classifier, and the Multinomial Naive Bayes Classifier in addition to creating a neural network.

### 3.1 Gaussian Naive Bayes
&nbsp;&nbsp;&nbsp;&nbsp; The Gaussian Naive Bayes Classifier assumed that each of the events (in this case, review) are independent from one another. It will use each of the different words in a review and make a normal distribution model of the frequency of each word used and the probability of whether or not a person liked or disliked the restaurant. A Gaussian Naive Bayes model would likely be more helpful with data that does not have so many different variables, and is not a good pick for natural language processing in this instance. The Gaussian Naive Bayes model was 67% accurate when predicting the testing data.

### 3.2 Stochastic Gradient Descent
&nbsp;&nbsp;&nbsp;&nbsp; The SGD Classifier has a starting point for each of our features, and with each iteration will adapt to what a good review and bad review is likely to contain. With 1000 iterations and 1000 randomly chosen reviews, we are likely to see good representation of most of our unique reviews. While this classifier seems promising, we just simply have too many features for it's true value to be realized. The SGD model was 79% accurate when predicting the testing data.

### 3.3 Multinomial Naive Bayes
&nbsp;&nbsp;&nbsp;&nbsp; Very similarly to the aforementioned Gaussian Naive Bayes, Multinomial Naive Bayes is more fit for natural language processing. It can very simply see how frequently a word appears in a good or bad review, and determine whether the review is good or bad based on the likelyhood that each word is used in a good or bad review. We were able to see our most accurate model yet as the Multinomial Naive Bayes Classifier was 80.33% accurate when predicting the testing data.

### 3.4 Deep Neural Network
&nbsp;&nbsp;&nbsp;&nbsp; I decided that I would finally try training a neural network on the training data to see whether or not it would be as accurate as the Multinomial Naive Bayes Classifier. After 20 iterations through the training data, the model was over 98% accurate when predicting that data, and as a result was able to show very accurate predictions. The Deep Neural Network was 81% accurate when predicting the testing data.

## 4. Conclusion
&nbsp;&nbsp;&nbsp;&nbsp; With only 1000 reviews to work with, our models displayed a very strong showing. I'd be curious to see how the Multinomial Naive Bayes model and the Deep Neural Network would perform with more reviews, perhaps closer to 10000. Regardless, I am happy with what I was able to produce.
