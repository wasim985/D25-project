# Title: Is specializing better for posters in social media?

Original paper: "Generalists and Specialists: Using Community Embeddings to Quantify Activity Diversity in Online Platforms"

## Abstract: 

The backbone of social media websites is creation / posting of information. A post allows others to comment / engage within a community, both quality and quantity of posts determine a platform's success.
However, with numerous communities in social media, how does community-wise specialization influence success and type of content being posted. The goal of this paper is to utilize community embeddings to judge how specialization affects posts / creations on a platform. In particular we will be looking into Reddit, which is driven by post submissions and is seperated into distinct communities. The methods to categorize success of posts, and finding user specialization can be generalized to more complicated platforms. This project builds on top of the idea of GS-scores to categorize creators' specialization and sentiment analysis to quantify enthusiasm.
## Link to Data Story on this project
[Click here for Data Story](https://bit.ly/4853pUM) \
Also stored as a pdf in repo

## Code of analysis

Stored in analysis\analysis.ipynb \
must download text_comments.csv and text_submissions.csv seperately.

Pre-processed csv files are stored at: \
[Google drive link](https://drive.google.com/drive/folders/1vroB8FpjWzmyMb6Cf81svC3M5AOByg3h?usp=sharing)
## Research Questions:

How does specialization correspond to key metrics in post creation? \
Are the top creators in a certain community more or less specialized? \
Specialists tend to be more enthusiasic? Does this hold up online? \
Are more specialized communities subject to certain social conditions? 


## Proposed additional datasets:

https://github.com/CSSLab/social-dimensions
Utilize the community-embeddings of "Quantifying social organization and political polarization in online platforms" rather than finding hyper parameters and training it ourselves.
Saves us alot of processing power and time.

https://github.com/ptuls/movielens-diversity-metric
Take a lot of inspiration from their implementation of GS-score calculation within pandas.

## Methods:
Data filtering:
The original paper uses data from 2017 and top 10k subreddits, we shall only use data from January 2019–June 2021 and top 5k subreddits for the sake of processing time (tentative). Additionally, we filter all removed users when necessary.


GS-scores:
For calculating the gs-scores I'm utilizing the pre-existing word embeddings of reddit communities from https://github.com/CSSLab/social-dimensions. We shall take the average cosine distance of a user and the subreddits they have interacted with.

Visualizing embeddings or user diversity:
We can utilize PCA or t-SNE to visualize a subset of embeddings in 2D or 3D. Plotly can be used to generate an interactive display.

Clustering:
Use k-means and elbow method to optimally cluster communities along social dimensions and investigate specialization.

Social-dimensions:
https://github.com/CSSLab/social-dimensions, we use their research on word embeddings and social dimensions.
A social dimension is based on similar subreddit differences upon whose unit vector other embedding vectors are projected upon to get the "social-dimension" value.

## Sentiment Analysis:
For the sentiment analysis, for now I'm planning to use Vader sentiment analysis which categorizes text into 3 major categories : neutral, positive, and negative.
And compound for the overall sentiment.

## Visualization:
Utilize line graphs and box plots (like original paper) to show how community GS-scores vary with elite posters GS-scores.

Scatter / line plots will be used to plot the sentiment against the gs-scores. Similar to the original paper, we can break this down into quartiles to get a better picture.

Histograms to view distributions of GS-scores and other metrics.
## Conclusion:
How does specialization correspond to key metrics in post creation? \
There seems to be no clear correlation with factors such as scores, posting frequency, number of posts \
However as number of posts increase the avg score per post decreases \
Are the top creators in a certain community more or less specialized? \
Yes, the top active creators are more specialized \
Specialists tend to be more enthusiasic? Does this hold up online? \
More specialized communitites have more positive conversations \
Are more specialized communities subject to certain social conditions? \
specialization of posters in a community correlates with "sociality" of a community i.e communities centered around a social activity are more specialized \
Team members:
MD Wasim Zaman

