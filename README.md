# Title: Difference specialists and generalists engagement in online communities

Original paper: "Generalists and Specialists: Using Community Embeddings to Quantify Activity Diversity in Online Platforms"

## Abstract: 
In the original paper on how generalists and specialists engage with their communities the idea of a GS-score was establisted and user commenting meta-data was used to investigate how user engagement varies in online communities.
The goal of this paper is to build upon this question of user engagement with other data (from Reddit) not utilized in the original paper, such as: User submissions and raw text data. We shall be utilizing the same idea of GS-score to categorize the users into generalists and specialists. Reddit is driven by post submissions , thus making posts is more benefitial for online communities, and analysis of text data allows us to examine the raw details of what users are saying. Hopefully adding in a new dimension of data helps us further differentiate behavior between generalists and specialists.

## Link to Data Story on this project
[Click here for Data Story](https://docs.google.com/document/d/15C_A4wTtUgRlxh6HuQqQUfhtFGW75HyBkHM7qvRwb4A/edit?usp=sharing)

## Research Questions:

User GS-Score's relation Post Submission Rate and Avg Rating
User GS-Score and Sentiment of their comments
Community GS-Score's and Top Post submitters [Elite Posters]

## Proposed additional datasets:

https://github.com/CSSLab/social-dimensions
Utilize the community-embeddings of "Quantifying social organization and political polarization in online platforms" rather than finding hyper parameters and training it ourselves.
Saves us alot of processing power and time.

## Methods:
Data filtering:
The original paper uses data from 2017 and top 10k subreddits, we shall only use data from January 2019–June 2021 and top 5k subreddits for the sake of processing time (tentative). Additionally, we filter all removed users when necessary.

GS-scores:
For calculating the gs-scores I'm utilizing the pre-existing word embeddings of reddit communities from https://github.com/CSSLab/social-dimensions. We shall take the average cosine distance of a user and the subreddits they have interacted with. We shall be utilizing the word2vec package.

Visualizing embeddings or user diversity:
We can utilize PCA or t-SNE to visualize a subset of embeddings in 2D or 3D. Plotly can be used to generate an interactive display.

## Sentiment Analysis (tentative):
For the sentiment analysis, for now I'm planning to use Vader sentiment analysis which categorizes text into 3 major categories : neutral, positive, and negative.
NTLK also gives us tools to remove punctuation, stopwords, lowercase all text, sentence compression, etc.
All text will be preprocessed in order to make sentiment analysis faster.

## Visualization:
Utilize line graphs and box plots (like original paper) to show how community GS-scores vary with elite posters GS-scores.

Scatter / line plots will be used to plot the sentiment against the gs-scores. Similar to the original paper, we can break this down into quartiles to get a better picture.



Team members:
MD Wasim Zaman

