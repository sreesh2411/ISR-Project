# [Code-Maroon-Global-Edition](https://yash8005.github.io/code-maroon-report/)

Information retrieval is a critical component of crisis response, but it's not always easy to find reliable sources in the midst of chaos. Rumors, gossip, and wild speculation run rampant, leaving authorities scrambling to sort fact from fiction. In this scenario, there is a need for a global, reliable and user friendly application to provide quick and accurate facts to the general masses.
This task is from 2022 TREC CrisisFACTs Track: https://crisisfacts.github.io/

## Features
Utilizes state-of-the-art machine learning models (T5, Roberta, OpenAI) to provide accurate and reliable information.
Extracts important information from news articles and stores them in a vector database for fast searching.
Supports multiple sources such as Twitter, Reddit, Facebook, and news websites.
Provides answers to user queries in real-time.
User-friendly web-based interface.

## Contents

This repository contains the following directories:

* Test_Data: contains smaller chunk of data used for inital testing
* data: contains the datasets used for training and testing the models. TREC 2022 dataset

## Approach

* Collect and preprocess data by gathering from various sources and removing irrelevant text.
* Extract relevant context text called "Headlines" and embed chunks using Sentence-Transformer model "paraphrase-MiniLM-L6-v2".
* Use cosine similarity to extract relevant headline chunks from embedded headline data based on query.
* Perform fact extraction using large language models (LLMs) pre-trained on QA datasets like SQuAD dataset.
* Three successful LLMs used: "deepset/roberta-base-squad2," "Google Flan T5 Model," and "Open AI text-davinci-002 - GPT 3.5 series model".
* Input embeddings of query and relevant documents to LLMs using Roberta model tokenizer for "deepset/roberta-base-squad2" model.
* Output of models is extracted facts in answers form.

## Observations

We conducted experiments on T5, Open AI, and Roberta models for general and fact-based queries. On average, T5 outperformed the other models in terms of exact match, F1 score, recall, and precision for general queries, achieving an exact match rate of 14.38%, F1 score of 0.204, recall of 25.74%, and precision of 34.87%. However, for fact-based queries, T5 performed significantly better with an exact match rate of 60.00%, F1 score of 0.6, recall of 60.00%, and precision of 60.00%. Open AI and Roberta followed with 20.00% and 33% exact match rate respectively for fact-based queries.

These results highlight the potential of T5 as the preferred model for general queries, while Open AI and Roberta can be used as alternative models. However, for fact-based queries, T5 proved to be the most effective model, followed by Open AI and Roberta. These results were obtained from our experimentation repository, which includes all the code, data, and results. For more details, please refer to our report website. To experience our demo version, please visit our demo website and demo repository.

## Team Members

Abhishek Maurya<br>
Bhavya Shah<br>
Yash Patel<br>
K. Sreesh Reddy


