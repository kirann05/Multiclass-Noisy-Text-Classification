
Approach Explanation:

1. Data Cleaning:
   - Tweets are preprocessed to remove URLs, mentions, and optional symbols like '#' from hashtags.

2. Data Loading and Preprocessing:
   - The script loads data from separate files for training, validation, and testing.
   - Each tweet is cleaned using the data cleaning function.
   - Tweet texts are tokenized and padded to ensure uniform length for input to the LSTM model.
   - Hashtags are encoded as labels for training and evaluation.

3. Model Definition:
   - A Bidirectional LSTM neural network model is defined using the Keras Sequential API.
   - The model architecture consists of an Embedding layer, Bidirectional LSTM layer, Dropout layers for regularization, and Dense layers for classification.
   - The model is compiled with appropriate loss function, optimizer, and evaluation metrics.

4. Model Training:
   - The model is trained on the training data with early stopping and model checkpointing for efficient training.
   - Training progress is monitored using validation data.

5. Model Evaluation:
   - The trained model is evaluated on the validation set to assess its performance using metrics like F1-score, precision, recall, and balanced accuracy.
   - Balanced accuracy is calculated to ensure performance across all classes is considered.
   - Additional models, such as Logistic Regression, are evaluated using cross-validation to explore ensemble methods and improve overall performance.

6. Prediction on Test Data:
   - The trained model is used to predict hashtags for the test data.
   - Predictions are made and saved in a format specified in the command line interface.

Instructions to Run the Classifier:

1. Ensure you have Python installed on your system.

2. Download the provided script "classifier.py" and the data files "train.txt", "val.txt", and "test.txt".

3. Open a terminal or command prompt or the Google collab link provided in classifier.py.

4. Navigate to the directory containing the script and data files.

5. Run the following command:
   $ python3 classifier.py -d train.txt -v val.txt -t test.txt

6. After execution, the script will generate predictions.txt containing the predicted hashtags for the test data.

[Note: Make sure you change the train, test, and val.txt paths in the classifier.py and you have installed  Tweet-Preprocessor[using '!pip install tweet-preprocessor'] ]
