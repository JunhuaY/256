# CSE 256: Sarcasm Detection In News Titles With Combined Language Models
This project aims to detect sarcasm through a large language model combined with simpler, more traditional models.

Sarcasm is a linguistic phenomenon in which the speaker or author states the opposite or a variation of the desired meaning. The detection of sarcasm is a difficult task, as it's rather dependent on subjective understandings. However, it's also a critical NLP application, especially in correctly handling texts expressing opinions. One of the most typical scenarios involves titles of news articles, where sarcasm is frequently used and limited context poses a significant challenge for accurate detection.

For the data source, we chose a dataset consisting of news headlines and their corresponding labels. It has a total of 28,619 records, with 13,634 labeled as sarcastic and 14,985 labeled as not sarcastic.

An ensemble model was implemented, integrating vanilla LSTM with GloVE, encoder transformer, and BERT. The vanilla transformer consists of tokenized embedded input processed through two sequential encoder blocks, each containing multihead attention layers, and a feedforward layer to generate the output. A voting system is employed to select between outputs of these different transformer architectures and best capture sarcasm by leveraging the specific class prediction strengths of each model. For both the vanilla LSTM and encoder transformer, a strict probability threshold was chosen (0.90-0.95) to maximize the precision of positive class predictions, aiming to boost the performance of BERT. The ensemble model achieved 91.9% accuracy, outperforming individual existing generalized models.


