# Training BERT-based models for text classification using Pytorch and Hugging Face Transformers library

This notebook is a demo for training a BERT-based model for text classification using Pytorch the Hugging Face Transformers library.


## Data

The data are 699 self posts (text submissions) from the r/cancer subreddit stripped of punctuation and truncated at 200 words. The posts are labeled for patient, gender, and age. The classes for each label are shown in the tables below.

Patient label | Meaning
------------ | -------------
0 | None
1 | Self
2 | Non-self, single
3 | Non-self, multiple

'Self' means that the patient is the creator of the post.

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

The data were labeled by two annotators, 'Z' and 'N' (me). For this demo, we will be training the model to predict the gender of the patient based on Z's labels since the two annotators were in 99% agreement for gender.

## Model and Training

In this demo, we will train a RoBERTa model for text classification. The parameters are shown below. The transformers library makes it very easy to adapt the model for a different task or to use a different model (e.g. BERT, DistilBERT, ALBERT) all together.

![](/img/model_params.PNG)

Remember to choose the appropriate tokenizer for the model you are using.

![](/img/tokenizer.PNG)

The data were split 80:20 training to testing.

## Results

We can see the model performs quite well even after just 4 epochs of training.

![](/img/test_res.PNG)
