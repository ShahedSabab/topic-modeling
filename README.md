# topic-modeling
The objective is to investigate different topic models for topic extraction task. For this task, yahoo answer dataset has been chosen. 

# Topic Labeling Process:
To genearate a semantic name for the generated topics the following steps are followed.

1. Find the top representative documents for each topic and qualitatively analyze them to get a common theme.
2. Investigate the word distributions for each topic.
3. Name the topic with a keyword which supports the words (i.e., from word distributions) as well the documents (i.e., representative documents).

# File Description
• yahoo_answer_lda.ipynb: This file is used to train the lda model.

• yahoo_answer_lda_result.ipynb: This file is used to analyze the lda model's results and naming each generated topic (e.g., topic-labeling).

• yahoo_answer_lda_infer: This file is used to test the lda model with unknown data.

• yahoo_answer_top2vec.ipynb: This file is used to train the top2vec model.

• yahoo_answer_top2vec_result.ipynb: This file is used to analyze the top2vec model's results and naming each generated topic (e.g., topic-labeling).

• yahoo_answer_top2vec_infer: This file is used to test the top2vec model with unknown data.
7
