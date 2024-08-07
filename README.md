# NLP-Project
Teknofest Natural Language Processing Competition Project

# NLP-Project

# Emotion Classification NLP Project

This project focuses on classifying emotions from text data using various machine learning models. The dataset used includes text data labeled with different emotions.

## Dataset

The dataset consists of three files:
- `train.txt`: Training data with 16,000 entries.
- `test.txt`: Test data with 2,000 entries.
- `val.txt`: Validation data with 2,000 entries.

Each file has two columns:
- `Text`: The text data.
- `Emotion`: The emotion label for the corresponding text.

## Data Preprocessing

1. **Exploratory Data Analysis (EDA)**
   - Load the datasets and display basic information.
   - Count and display the occurrences of each emotion in the datasets.
   - Remove emotions with low representation ('love' and 'surprise') to improve model performance.

2. **Text Processing**
   - Define a custom `TextProcessor` class for text preprocessing.
   - Convert text to lowercase and remove stopwords.
   - Optionally perform stemming on the text.

3. **Text Vectorization**
   - Use `CountVectorizer` to convert text data into numerical vectors.

## Models

Several models were trained and evaluated on the preprocessed data:

1. **Random Forest Classifier**
   - Achieved 99.94% accuracy on the training set.
   - Achieved 89.77% accuracy on the validation set.
   - Achieved 91.10% accuracy on the test set.

2. **Support Vector Machine (SVM)**
   - Achieved 98.05% accuracy on the training set.
   - Achieved 92.88% accuracy on the validation set.
   - Achieved 93.75% accuracy on the test set.

3. **Logistic Regression**
   - Achieved 99.21% accuracy on the training set.
   - Achieved 93.16% accuracy on the validation set.
   - Achieved 93.92% accuracy on the test set.

4. **Multinomial Naive Bayes**
   - Achieved 93.46% accuracy on the training set.
   - Achieved 86.56% accuracy on the validation set.
   - Achieved 84.90% accuracy on the test set.

5. **Gradient Boosting Classifier**
   - Achieved 89.90% accuracy on the training set.
   - Achieved 87.71% accuracy on the validation set.
   - Achieved 87.72% accuracy on the test set.

## Model Evaluation

- Confusion matrices were plotted for each model to visualize their performance.
- The best performing model was found to be Logistic Regression with the highest test set accuracy of 93.92%.

## Implementation

### Dependencies

Install the required dependencies using:

```bash
pip install -r requirements.txt

