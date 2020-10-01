# Sentiment-Analysis-with-Product-Reviews
Sentiment analysis, also called 'opinion mining', uses natural language processing, text analysis and computational linguistics to identify and detect subjective information from the input text. Here we're classifying text as either positive, negative, or neutral. Machine learning techniques are used to evaluate a piece of text and determine the sentiment behind it.

## Dataset
The dataset used here is from the Kaggle name [Amazon Fine Food Reviews](https://www.kaggle.com/snap/amazon-fine-food-reviews?select=Reviews.csv), which is the reviews of the food products. Here, Text — This variable contains the complete product review information.
Summary — This is a summary of the entire review.
Score — The product rating provided by the customer.

## Requirements
- Pandas
- Numpy
- Scikit Learn
- Matplotlib
- Plotly
- Seaborn
- NLTK
- Wordcloud

## The Code Flow
First of all here I used the Google Colab which is free and powerful that provides free GPU power. That's why you're seeing these lines of codes</br>```from google.colab import drive```\
```drive.mount('/content/drive')```\
```path = "/content/drive/My Drive/Colab Notebooks/Reviews.csv"```\
Otherwise you can directly do this by importing and reading the dataframe by pandas if you're doing in local jupyter notebook.</br>
- Now in **Step 1** Read the dataframe and see what's inside the data by printing heads and tails of it.
- In **Step 2** we're analyzing the data so we can plot the reviews "Score" in histogram with the help of plotly.</br>
Here is the result we can see that most of the customer rating is positive. This leads us to believe that most reviews will be positive, which will be analyzed next.
![Step 2 Histogram](https://github.com/taneemishere/Sentiment-Analysis-with-Product-Reviews/blob/master/newplot.png)</br>
We can now make the wordcloud of the most frequent words which will demostrate the type of reviews people posted.</br>
- In **Step 3** we're classifying reviews into “positive” and “negative,” so we can use this as training data for our sentiment classification model. Positive reviews will be classified as +1, and negative reviews will be classified as -1. We will classify all reviews with ‘Score’ > 3 as +1, indicating that they are positive. All reviews with ‘Score’ < 3 will be classified as -1. Reviews with ‘Score’ = 3 will be dropped, because they are neutral. Our model will only classify positive and negative reviews.
- In **Step 4** doin some more data analysis by making the wordclouds of the positive and negative reviews which we classify in step 3.</br>
Now by ploting the nagative and positive histogram we can see that more of the reviews are positive.
- In **Step 5** building the model as this will take reviews in as input. It will then come up with a prediction on whether the review is positive or negative. This is a classification task, so we will train a simple logistic regression model to do it.
- In **Step 6** test the model as we get the overall accuracy of over the test data around 93%, which is great.
