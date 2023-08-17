# McDonald's Sentiment Analysis
In Progress...

# Motivation
Sentiment analysis was a popular topic in the Data Science Fellowship and I wanted to learn about natural language processing.

# Objective
- To learn natural language processing
- To learn about VADER sentiment analysis and compare VADER to star ratings
- To improve my knowledge of pandas

# Methods
McDonald's Reviews  
https://www.kaggle.com/datasets/nelgiriyewithana/mcdonalds-store-reviews  

VADER Sentiment Scoring  
https://www.kaggle.com/code/robikscube/sentiment-analysis-python-youtube-tutorial/notebook  

VADER sentiment scoring was compared to review star ratings.  
Star ratings of 2, 3, and 4 were dropped to leave 5 star ratings (1), and 0 star ratings (0).  
Reviews were processed with VADER as cleaned and original reviews to compare the effects of cleaning reviews on VADER.  
Sentiment was simplified to positive (1) and negative (0) using the compound sentiment output from VADER.  
If compound sentiment <=0, negative (0), else positive (1).  
VADER sentiment was compared to star rating by measuring how many correct matches/total number of reviews in the data set.

# Results
Clean reviews accuracy 82.8%  
Original review accuracy 84.3%  

# Discussion & Future Work
Lower accuracy with VADER on the cleaned reviews is expected as VADER considers aspects of the text in the review when determining sentiment. For example, an original review may end a sentence with "good." vs "good!". The latter sentence likely has a more positive sentiment. In the cleaned reviews, these would both show as "good" vs "good" and contribute the same sentiment to total sentiment of the review.

For future work, I would like to evaluate the reviews with Natural Language Toolkit (nltk).


# References
Functions to clean reviews (Ex missing characters). Clean reviews are not needed for VADER, but are listed here for use in future work with nltk
https://medium.com/@priyaag0707/mcdonald-review-project-on-sentiment-analysis-4a5108c8eb53
https://www.kaggle.com/code/aniketkadam702030/mcdonalds-store-reviews-keras
