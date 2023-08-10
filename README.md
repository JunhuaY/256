Sarcasm is a linguistic phenomenon in which the speaker or author states the opposite or a variation of the desired meaning. The detection of sarcasm is a difficult task, as it's rather dependent on subjective understadings. But it's also a critical NLP application, especially in correctly handling texts expressing opinions. One of the most typical scenario is titles of news articles, where sarcasm is popularly used and limited context poses great challenge for accurate detection. 

For the data source, a Kaggle dataset consisting of news headlines and their corresponding labels is chosen.  It has a total number of 28,619 records, with 13,634 sarcastic and 14,985 not sarcastic.

An ensemble model is implemeted, integrating vanilla LSTM with GloVE, encoder transformer and BERT. The vanilla transformer consists of tokenized embedded input that is processed into two sequential encoder blocks, each consisting of multihead attention layers, and a feedforward layer to generate the output. A voting system is employed to select between
outputs of these different transformer architectures and best capture sarcasm by taking advantage of any specific class prediction strengths.For both vanilla LSTM and encoder transformer, a strict probability threshold was chosen (0.90-0.95) to maximize the precision of positive class predictions, with the intention of improving the
performance of BERT.


