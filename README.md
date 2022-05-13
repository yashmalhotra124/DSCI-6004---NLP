# Detecting Cyberbullying through Tweets and Network Graph
Final Term Project for Natural Language Processing ( DSCI 6004 ) - Spring 2022 by Yamini Ranganathan, Rachel Porter, and Yashpreet Malhotra.


 ## Aim
To provide an effective method of detecting cyberbullying from Tweets. Analyzing social media posts for linguistic clues that signal cyberbullying can pave way for faster and accurate approach to stop the cyberbullying at its source.

## Objectives: 
1. Create a model that can automatically successfully detect instances of bullying tweet Especially during the pandemic based high social media usage. 
2. Create Network graphs to deduct the patterns of relationship between different cyberbullying categories.

## Data 
> Link to dataset: https://ieee-dataport.org/open-access/fine-grained-balanced-cyberbullying-dataset

2021 Fine-Grained Balanced Cyberbullying Dataset: The dataset used was balanced and separated into tweets that fall into categories of cyberbullying targeting a victim’s age, ethnicity, gender, religion, or other quality.



## Methods and Models implemented:

The proposed approach is divided into five phases: 

1. Data loading and preprocessing. Data was downloaded from the above link and loaded.  Preprocessing involves checking for duplicate tweets, checking class balance, cleaning the tweet text, checking for duplicate tweets and class balance after tweet cleaning. 

 
2) Keyword trend analysis - Plot tweets based on their counts and Find the top 20 most common words.

3) Word embeddings for feature extraction – Create a Word Embedding  matrix using a pretrained Word2Vec model

4. Classification Models

a.	Naïve Bayes Baseline model –  Using a bag of words  created from CountVectorizer and a term-frequency times inverse document frequency (TF-IDF) transformation was performed on both the training and test sets.

b.	Bidirectional LSTM for sentiment classification – Top 20 most common words from the vocabulary dictionary was created using the tokenizer. Create a word embedding matrix using the original text tweets and the pre-trained model Word2Vec. 

c. BERT Transformer: original BERT model from Hugging Face library with additional Dense layers to perform the desired classification task. Create a custom BERT classifier class by adding the Dense layers to original BERT. Use a Linear Warmup Learning rate scheduler to reduce the volatility in the early stages of training. 

## Network Graphs

Create Parallel Coordinates Plot (PCP to analyze the pattens and relation between the different categories of cyberbullying. Create network graph to display relationships between elements (nodes) and to visualize clusters .

## Model Evaluation

As a classification problem for Tweet Sentiment Analysis, we used the evaluation metrics of Precision, Recall, F-score, and Accuracy (confusion matrix)
 
## Results

Among the different models, Naive Bayes classifier achieved an overall accuracy score of 85%, Custom Bidirectional LSTM had an overall accuracy score of 93%, custom BERT had the highest accuracy of 94%. Both Parallel coordinates plot graph and Network graph indicates that cyberbullying is directed towards more than one criterion.

