# topic-modeling
The objective is to investigate different topic modeling techniques for unsupervised topic extraction from the corpus. For this task, yahoo answer dataset has been chosen. The dataset has ~1.5 M question-answer pairs. For the model training, only 60,000 samples has been randomly chosen from the data. Only the answers are used to train the models. The models are trained using [LDA](https://www.jmlr.org/papers/volume3/blei03a/blei03a.pdf?TB_iframe=true&width=370.8&height=658.8) and [Top2Vec](https://arxiv.org/abs/2008.09470). The main dataset can be found in the following link:
https://www.kaggle.com/soumikrakshit/yahoo-answers-dataset!

## Model 1: Topic Model - LDA: 
• Different preprocessing strategies (e.g., lemmatization, stop word removal) are followed to process the input text.
• Topic Coherence metric is used to select the number of topics to generate.
• The topics are further analyzed to give them a semantic name. (e.g., naming "topic 1" to "science").
• The inference model is used to test with unknown data from different websites. 

## Model 2: Topic Model - Top2Vec:
• This model does not need any pre-processing so the raw text (only removed hyperlinks) is used for the model training.
• For generating the document vectors, bert embeddings have been used.
• Hierarchical topic reduction has been used to reduce the generated topic space to 20 dimensions.
• Topic labeling is performed to generate a semantic name for all the 20 topics.


# Topic Labeling Process:
To genearate a semantic name for the generated topics the following steps are followed.

1. Find the top representative documents for each topic and qualitatively analyze them to get a common theme.
2. Investigate the word distributions for each topic.
3. Name the topic with a keyword which supports the words (i.e., from word distributions) as well the documents (i.e., representative documents).

# How to run:
Run the code in the following order to train a topic model: 

1. yahoo_answer_lda.ipynb: This file is used to train the lda model.
2. yahoo_answer_lda_result.ipynb: This file is used to analyze the lda model's results and give a name to each generated topic (e.g., topic-labeling).
3. yahoo_answer_lda_infer: This file is used to test the lda model with unknown data.
4. yahoo_answer_top2vec.ipynb: This file is used to train the top2vec model.
5. yahoo_answer_top2vec_result.ipynb: This file is used to analyze the top2vec model's results and give a name to each generated topic (e.g., topic-labeling).
6. yahoo_answer_top2vec_infer: This file is used to test the top2vec model with unknown data.
