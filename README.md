# Training BERT-based models for text classification using Pytorch and Hugging Face Transformers library

This notebook is a demo for training a BERT-based model for text classification using the Hugging Face Transformers library.


## Data

The data are 699 self posts (text submissions) from the r/cancer subreddit stripped of punctuation and truncated at 200 words. The posts are labeled for patient, gender, and age. For this demo, we will train the model to predict the gender of the patient.


## Model

In this demo, we will train a RoBERTa model for text classification.


## Results

We 


## Key

Patient label | Meaning
------------ | -------------
0 | None
1 | Self
2 | Non-self, single
3 | Non-self, multiple

Gender label | Meaning
------------ | -------------
0 | Unknown
1 | Female
2 | Male

Age label | Meaning
------------ | -------------
0 | Unknown
1 | <18
2 | >=18 & <40
3 | <40
4 | >=40 & <65
5 | >=18 & <65
6 | <65
7 | >=18
8 | >=40
9 | >=65
