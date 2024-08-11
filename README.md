## Multiclass-Noisy-Text-Classification
An advanced machine learning project focused on classifying noisy text data in real-time using a Bidirectional LSTM model.
This project involves developing a multiclass classifier for predicting the most probable hashtags for given tweets. The classifier is designed to handle social media text's noisy and imbalanced nature, aiming to achieve highly balanced accuracy in hashtag prediction.

## Project Structure
- **Data Files:**
  - `hashtags.txt`: List of possible hashtags.
  - `train.txt`: Training tweets with de-identified IDs, followed by their hashtags and content.
  - `val.txt`: Validation data formatted like `train.txt`.
  - `test.txt`: Test data similar to `train.txt` but without hashtag IDs.

- **Classifier Script:** 
  - `classifier.py`: The main script containing the multiclass classifier's implementation.

- **Predictions:**
  - `predictions.txt`: The output file with the predicted hashtag IDs for each test tweet.

## How to Run the Project
1. **Ensure Python is Installed:**
   - This project requires Python 3. Make sure it is installed on your system.

2. **Prepare the Data:**
   - Place the `train.txt`, `val.txt`, and `test.txt` files in the same directory as the `classifier.py` script.

3. **Run the Classifier:**
   - Use the following command to generate predictions:
   ```bash
   python3 classifier.py -d train.txt -v val.txt -t test.txt

# Results
The project's report, Multiclass Noisy Text Classification-Output.pdf, provides detailed insights into the model's performance, including precision, recall, and F1 scores for different classes.

