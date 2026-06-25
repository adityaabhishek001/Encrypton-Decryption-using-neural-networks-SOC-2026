# Week 2 

This week's assignment is to create a model that can decrypt the caeser cipher using a fully connected neural network.

To create the data I copied a chapter of a book innto data.txt and cleaned it up using the default string functions in python. The only characters it contained after cleaning were lowercase a-z and !,#,$,%.
Each sample had a length of 50 characters and the total length of the dataset is 90000 chars divided in 8:2 ratio.

## Model Architecture

The model is of architecture : 
16*50 -> 1024 -> 256 -> 128 -> 30 (30 since there could be 30 different types of shifts)

The hyperparameters of the model are listed below

- Learning Rate:0.001
- Epochs:20
- Optimiser:Adam
- Loss:Cross Entropy Loss
- Input size:16*50 (50 chars on a sample and got embedded to with 16)
- Output classes: 30 (30 diff kinds of shifts)

The model was not  using embedded initially and got like 4% accuracy since when encoding alphabets using ASCII values or indexes the models considers 
A is inferior compared to Z since 1<26. To overcome this we use one hot encoding or embedding.

This significantly improved the models performance but was still around 70%. Then I checked the train accuracy which was a bit too high and suspected overfitting so added a dropout
and also put batch normalisation. And finally I also increased the size of the dataset bringing th final accuracy to **92.22%**.

