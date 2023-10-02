# NewsHub Advanced News Intelligence:
![News_Application_Architecture_-1](https://github.com/DriveMyScream/News_Application/assets/93398864/b13f2e2d-a060-47fa-ab78-2aceff5d53e9)
1) Fake News Detection: To distinguish real from fake news, we try different model like bidirectional RNN, LSTM, GRU, and Conv1D. We trained custom word embeddings with Gensim and used pre-trained Google News embeddings (Google-news-300). The best performer was bidirectional LSTM, which beat baseline from 86.33% to 93.36% accuracy. To track our experiments, we employed TensorBoard.
2) Sentiment Analyzer: To identify the news sentiment, we started by labeling unlabeled news data as either positive or negative using snorkel. We tried various models bidirectional RNN, LSTM, GRU & Conv1D, with universal sentence encoder embeddings. The good performing model was a simple & compact bidirectional  LSTM, which beats the baseline model from 88.72% to 99.14% accuracy. We used TensorBoard to keep track of our experiments.
3) News Category Classifier: To classify news into 15 categories, we use a transformer encoder-based model, achieving a top-5 accuracy of 85%.
4) News Subcategory Classifier: To classify news into 256 subcategories, we fine-tune a pretrained BERT model, achieving an accuracy of 84%.
5) Entity Recognizer: For NER task, we try a bidirectional LSTM model & fine-tuned a RoBERTa model. LSTM model excelled with a recall of 99%.
7) News Similarity Analysis: For news similarity analysis, we try shared & combined LSTM multiple input single output models and a siamese neural network based Sentence Transformer model. A shared model gives a good 0.71% F1 score on an imbalanced dataset.
8) English 2 Hindi Translator: To convert news into Hindi for Hindi-preference users, we experimented with a transformer-based model, fine-tuning a T5-Small model, and a pre-trained model. The pre-trained model has a BLEU score of 6.9.
9) News Summarizer: For news summarization, we try a transformer model and fine-tuned T5-Small model, achieving a BLEU score of 0.70.
10) Grammar Optimizer: For grammatical error correction, we fine-tuned a T5-Small model, resulting in a BLEU Score of 0.34.
11) Search Engine: To enhance performance, we added a search engine with 120,000 news headlines. We experimented with both a Siamese network-based transformer encoder and a Sentence Transformer model, ultimately opting for the Sentence Transformer model.
12) ChatVoice AI: For voice assistant feature, we use a speech recognition DeepSpeech model achieving a 0.14 CTC loss, and for a chatbot, we try a seq2seq, bahdanau attention & blenderBot model and ultimately selecting the BlenderBot model.
13) Personalized News Recommendations: We start by calculating a news popularity score based on engagement factors. An LSTM model outperforms XGBoost with an MSE of 2.48. We then use a content-based recommendation system to suggest news to users.
