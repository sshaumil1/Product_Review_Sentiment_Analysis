# Title: Product Review (Sentiment Analysis)
## Problem Statement
To build a NLP methodology to determine whether a customer happy with the product.
## Data Gathering & Initial Preprocessing
First I read a csv file and store it in a data frame. Then, I took only relevant features for sentiment analysis. After that, I used the LangDetect library to find out the languages in which the reviews were written. After locating the reviews, I translated them with the help of googletrans library. Then I exported the translated reviews in a csv file for further use as translator takes high time for translation.
## EDA
First I checked whether the data is balanced or not by plotting a bar plot. In that way, I found that the data was highly imbalanced, which means I had to do balancing. Then, I checked Unigram, Bigram, Trigram. Following, I plot a wordcloud. Then, I extracted the most common keywords using Rake as well as the Yhack Keyword Extractor. Thus, most of the reviews I found were positive.
## Preprocessing
I wrote functions to clean the data, including to remove spaces, to expand words, to handle accented characters, to remove stop words, to find root words, etc. Then I applied all the functions one by one on the data. I used different libraries for preprocessing, which were:
- **wordNetLemmatizer:** for finding root word
- **autocorrect library:** for autocorrection
- **unidecode:** for handling accented characters
- **contractions:** for expanding text
- **wordtokenizer:** for making tokens
Then I used replace function to change target variable categories in numerical data and drop the unwanted features.
#### Countvectorizer
First I splitted the data for training as well as testing so that I can avoid the data leakage. Then, I utilised countvectorizer to extract vectors of the documents.
#### Data Balancing 
As I had seen that data was imbalance. So, I used SMOTE to balance the data so that I can avoid duplicacy.
## Model Selection and Training
