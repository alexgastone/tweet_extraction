# Tweet Sentiment Extraction as a Question Answering task

## The Problem

https://www.kaggle.com/c/tweet-sentiment-extraction

> "My ridiculous dog is amazing." `sentiment: positive`

With all of the tweets circulating every second it is hard to tell whether the sentiment behind a specific tweet will impact a company, or a person's, brand for being viral (positive), or devastate profit because it strikes a negative tone. Capturing sentiment in language is important in these times where decisions and reactions are created and updated in seconds. But, which words actually lead to the sentiment description? Pick out the part of the tweet (word or phrase) that reflects the sentiment.

> What words in tweets support a positive, negative, or neutral sentiment? 

## Data
In this competition Kaggle has extracted support phrases from Figure Eight's Data for Everyone platform. The dataset is titled Sentiment Analysis: Emotion in Text tweets with **existing sentiment labels**, used here under creative commons attribution 4.0. international licence. The objective in this competition is to construct a model that can do the same - look at the labeled sentiment for a given tweet and figure out what word or phrase best supports it.

*Disclaimer: The dataset for this competition contains text that may be considered profane, vulgar, or offensive.*

The supervised training data therefore consists of prelabelled (i.e. sentiment) tweets with their corresponding selected text that best supports that sentiment.

## Question Answering 
The goal of question answering is to `answer` a `question` given a `context`. We can phrase our problem as a question answering task in the following way:
> `question`: sentiment label

> `context`: tweet

> `answer`: selected text

This is one of the nine NLP tasks that transformer models, such as Google's pretrained BERT, have been able to solve. Currently, one of the top scoring BERT models for question answering tasks on the SQuAD dataset is ALBERT (lite BERT), an ensemble model published in Sept 2019.

We will therefore be implementing this model using the transformers library from [Hugging Face](https://huggingface.co/).

For more info on ALBERT, check out https://paperswithcode.com/paper/albert-a-lite-bert-for-self-supervised.
