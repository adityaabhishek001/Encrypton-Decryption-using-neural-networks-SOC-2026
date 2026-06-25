# Week 3

This week consisted of learning about RNNs (Recurrent Neural Networks).

Recurrent Neural Networks (RNNs) are a class of neural networks designed to process sequential data by retaining information from previous steps.
They are especially effective for tasks where context and order matter:

- Designed for sequential and temporal data
- Maintains memory of past inputs
- Widely used in NLP, forecasting and speech tasks

These networks have recurrent neurons which hold a hidden state that contains information about the previous state and finally an output is produced using an fully connected layer.

There are different types of RNNs:

### 1. One-to-One
- **Description:** A single input produces a single output.
- **Applications:** Image classification, regression tasks.

### 2. One-to-Many
- **Description:** A single input generates a sequence of outputs.
- **Applications:** Image captioning, music generation.

### 3. Many-to-One
- **Description:** A sequence of inputs produces a single output.
- **Applications:** Sentiment analysis, spam detection, document classification.

### 4. Many-to-Many
- **Description:** A sequence of inputs produces a sequence of outputs.
- **Applications:** Machine translation, speech recognition, text summarization, named entity recognition.

## Assignment

The assignment is to Create an RNN model which takes a sentence as an input and gives out the sentiment of the sentence.
The sentiment could be one of Positive, Negative and Neutral.

### HyperParameters

- Learning Rate: 0.0001
- Loss : Cross Entropy loss
- Optimizer: Adam
- Input size: 128
- Hidden state size: 128
- Output Size: 3 (3 types of sentiments)

After tokenizing the text for better results and training it for 5 epochs the final accuracy was 78.84 %.
