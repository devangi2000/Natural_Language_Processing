# Natural_Language_Processing

This is an implementation of LSTM (Long-short term memory) network, which is a special kind of RNN, capable of learning long-term dependencies. This model generates words like Shakespeare, after being trained on a sample. TensorFlow has been used with Keras as the backend.

Initially, a corpus of all the words is formed. Using a Tokenizer (which assigns a unique index to every unique word),  word indices are generated.
Every line is extracted and a sequence of the indices of every word is formed, n-gram-sequences generated and consequently padded for the sake of uniformity. 
of sentences' lengths.
The predictors and labels are subsequently separated and converted to a categorical  form where the total number of classes is the total word count.
This is fed to a Sequential model with Bidirectional LSTMs and Dense layers; I also chose to add a dropout layer of 0.2 to avert over-fitting and randomly turn off neurons.
Dense layers have 'ReLU' and 'softmax' activations.
This model is compiled using Adam optimizer, with loss as categorical crossentropy and the evaluation metric as accuracy.
The performance of the model is plotted and tested with a random input sequence of words as well.
During the project implementation, I learnt about LSTMs and their applications. They can not only process single data points (such as images), but also entire data sequences (like speech or video). For instance, LSTM is applicable to tasks such as unsegmented, connected handwriting recognition, speech recognition and anomaly detection in network traffic. An LSTM is a particular type of RNN with a mechanism to avoid the vanishing gradient problem and learn long term dependencies. It is still capable of learning short term dependencies, hence the name "Long-Short Term Memory". They are an unsupervised learning method, although technically, they are trained using supervised learning methods.
Given a sequence of "N" words, an N-gram model predicts the most probable word that might follow this sequence. It's a probabilistic model that's trained on a corpus of text.This is  an "N-gram sequence".
