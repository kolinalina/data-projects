# next word prediction

desc: to predict the next word, like using AI models like chat gpt. in this case using neural network

dataset: text from book.txt


# steps:
1. read dataset and split data to individuals word
2. filter rare words
3. freqg and bigram analys
4. sequence - seq-5
5. one-hot encoding
6. train/val/test
7. train 2layer lstm
8. training visualization
9. predict next word



The charts look clean! Here's my read:
- Loss chart (left)

Train loss keeps dropping nicely ✅
Val loss dropped then flattened around epoch 5-6 and started creeping back up ⚠️
That gap between train and val loss = overfitting starting around epoch 6

- Accuracy chart (right)

Train accuracy steadily climbing to ~19% ✅
Val accuracy plateaued around 14-15% from epoch 6 onwards ⚠️
Same story — model is memorizing training data but not generalizing well

# result

"Model shows signs of overfitting after epoch 6, indicated by diverging train/val loss. This is likely due to limited sample size (20K sequences). Increasing training data would improve generalization."