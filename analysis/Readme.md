## ANALYSIS DETAILS

This directory contains the R scripts used in the project as well as the intermediate files that these scripts generate. Please find below details about each file in this directory.

### paper.Rmd

This is the main R markdown file which encapsulates our entire replication analysis. This markdown file executes the R scripts within the analysis directory to generate the results. It uses bibliography.bib to cite the references.

### 001-tweet-cleaning.R

This is the first step in the process of detecting abusive language in tweets. This R script reads the original dataset (twitter-hate-speech-classifier-data.csv), cleans it, and transforms the data to generate the data file "prepared_tweet_dataset.csv", which is used as the input by "002-modeling.R" script to generate the results.

### 002-modeling.R

This R script reads "prepared_tweet_dataset.csv" data file as input, which was generated by the first script, and performs classification of the tweets using Logistic regression. The outputs from this script are saved back in the analysis directory and referenced in the paper.Rmd markdown file at different stages.

### 003-display-bargraph.R

This R script is used to generate a bar graph showing the distribution of the tweets in the three hateful categories.

### Sampled Dataset for Replication

For our replication project, we have selected a random subset of 3000 tweets from twitter-hate-speech-classifier-data.csv. This selection has been made after several attempts to process all of the data on a local machine with limited processing power. **'sampled_tweet_dataset.csv'** data file contains the subset of size 3000 tweets from the original data that we use for replicating this project.

### Prepared Dataset for Replication

**'prepared_tweet_dataset.csv'** data file is the processed file which is an input to the 002-modeling.R code in the Analysis folder. This data file contains one-hot encoded data for the selected 3000 tweets which serves as an input to run the machine learning models. This dataset should be used to produce the figures that we have claimed to replicate using this project.

### Other files

All the other files in this directory are intermediate files which are generated and/or used to replicate the results.