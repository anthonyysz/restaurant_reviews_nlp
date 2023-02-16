# Restaurant Reviews NLP

## 1. Introduction
&nbsp;&nbsp;&nbsp;&nbsp; Herein this dataset, we have 1000 reviews of a certain restaurant each with an indicator of whether it is a good or bad review. My goal in this project was to create a model that would be able to decipher between a good and bad review based on the content of the comment. 

## 2. Data Analysis
&nbsp;&nbsp;&nbsp;&nbsp; Here, my first step was to remove all of the 'stop words' from the review. Some examples of stop words are 'and', 'the', and 'is'. Without those words distracting my model, it's potential accuracy would greatly improve. Additionally, I wrote a function that would 'clean' the reivew: making each word lower case, removing punctuation, and finding the stem version of each word.
