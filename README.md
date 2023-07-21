# deep-learning-challenge
deep-learning-challenge files go here
Data Preprocessing

The model aims to predict the success of applicants in receiving funding, indicated by the IS_SUCCESSFUL column in the dataset. Relevant feature variables include every column except the target variable (IS_SUCCESSFUL) and non-relevant variables such as EIN and names. These non-relevant variables were dropped from the dataset to avoid potential noise that might confuse the model.

During preprocessing, binning or bucketing was applied to handle rare occurrences in the APPLICATION_TYPE and CLASSIFICATION columns. Specifically, a cutoff value was selected to create additional bins for rare occurrences. Categorical data were transformed into numeric data to facilitate the model's understanding of the information. The data was then split into separate sets for features and targets and further divided into training and testing sets. Finally, the data was scaled to ensure uniformity in the data distribution, which helps in training the model effectively.

Compiling, Training, and Evaluating the Model

The initial model was constructed with three layers: an input layer with 80 neurons, a second layer with 30 neurons, and an output layer with 1 neuron for binary classification. The activation function used for the first and second layers was ReLU, and for the output layer, the sigmoid activation function was applied.

Optimization Attempts

    The first optimization attempt involved increasing the number of neurons in each hidden layer. This modification aimed to allow the model to learn more complex patterns. The number of neurons in the first hidden layer was increased to 128, and in the second hidden layer, it was increased to 64.

    The second optimization attempt involved changing the activation function for all hidden layers to tanh. This activation function introduces non-linearity to the model, allowing it to capture more intricate relationships in the data.

    The third optimization attempt involved reducing the cutoff value for the APPLICATION_TYPE column during preprocessing to create additional bins for rare occurrences. By increasing the number of bins, the model could better capture the nuances of rare application types. After training the model for 100 epochs, this optimization attempt yielded the best accuracy score, but still bellow the 75% goal.

Summary

Despite multiple optimization attempts, the model's accuracy did not reach the target of 75%. While the third attempt with reduced cutoff value for APPLICATION_TYPE showed the best results, it was still below the desired threshold. Additional exploration of alternative approaches, such as trying different architectures, optimizers, and regularization techniques, may be necessary to achieve the desired accuracy goal. The model could also benefit from further hyperparameter tuning and additional data preprocessing techniques to improve its predictive performance.
