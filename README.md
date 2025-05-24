Alphabet Soup Charity: Deep Learning Model Report
The goal of this project was to build a neural network that could help Alphabet Soup predict which organizations they fund are likely to be successful. Using historical data, I cleaned and prepared the dataset, built a binary classification model, and then worked on improving its accuracy through model tuning and data adjustments.

Results
Data Preprocessing
Target variable:
The target for the model is IS_SUCCESSFUL — it tells us whether an organization succeeded (1) or not (0).

Feature variables:
Everything else in the dataset after cleaning — like APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, INCOME_AMT, etc.

Dropped columns:
I removed columns like EIN, NAME, STATUS, and SPECIAL_CONSIDERATIONS since they weren’t useful for prediction and just added noise.

Model Structure and Training
Neurons, layers, activations:
I used two hidden layers:

First layer: 80 neurons, ReLU

Second layer: 30 neurons, ReLU

Output layer: 1 neuron, Sigmoid
I picked ReLU for the hidden layers since it’s efficient, and Sigmoid for the output to handle binary classification.

Performance:
The final model reached about 72% accuracy, which is decent but just shy of the 75% target.

What I tried to improve it:

Grouped rare categories into “Other” for cleaner inputs

Used StandardScaler to normalize the data

Tweaked the number of neurons and added an extra hidden layer

Trained for 50 epochs and used a callback to save the best model

Overall Takeaway
The model did a solid job — not perfect, but definitely useful. Even though it didn’t hit the 75% accuracy goal, the results show that there’s predictive value in the data, especially with better tuning or different model approaches.



